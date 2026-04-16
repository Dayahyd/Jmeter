### Jmeter


JMeter's command-line interface (CLI) mode—formerly known as Non-GUI mode—is the recommended way to run load tests because it consumes significantly fewer resources than the graphical interface. 
Apache JMeter
Apache JMeter
 +1
Basic Execution Command
The standard command to run a test from the /bin directory is:
bash
jmeter -n -t [test_file.jmx] -l [results_file.jtl]
Essential Command Flags
Flag 	Description
-n	Starts JMeter in CLI (Non-GUI) mode.
-t	Path to the source .jmx script containing your test plan.
-l	Path to the .jtl (or .csv) file where results will be recorded.
-e	Automatically generates an HTML Dashboard Report after the test.
-o	Output folder for the HTML report (must be empty or non-existent).
-f	Forces deletion of existing results files or report folders before starting.
Advanced Usage Examples
Generate Dashboard Report from Existing Result File:
jmeter -g [results.jtl] -o [output_folder]
Override Script Properties at Runtime:
Use -J to set local properties (e.g., changing thread count without opening the GUI):
jmeter -n -t script.jmx -Jthreads=50 -l log.jtl
Distributed Testing (Remote Execution):
Run the test on all remote servers defined in your properties file:
jmeter -n -t script.jmx -r 
Apache JMeter
Apache JMeter
 +2
How to Stop a Running CLI Test
Graceful Shutdown: Run shutdown.cmd (Windows) or shutdown.sh (Linux) from the JMeter /bin folder.
Immediate Stop: Run stoptest.cmd (Windows) or stoptest.sh (Linux) for an abrupt termination.
Manual Kill: Press Ctrl + C in the terminal window where the test is running






Q116: Why might the candidate choose Apache JMeter over Gatling for a project?
A116: JMeter has a GUI for building tests quickly, extensive protocol support, and a larger ecosystem of plugins.
Explanation: Industry knowledge; the resume lists JMeter first as the primary tool.

Q117: When would the candidate prefer Gatling over JMeter?
A117: When the team prefers code-based tests (Scala), requires better performance for massive scale, or wants built-in advanced reporting.
Explanation: Gatling's known strengths.

Q118: Is LoadRunner still relevant given open-source tools like JMeter?
A118: Yes, for large enterprises requiring certified support, extensive protocol coverage (SAP, Citrix, etc.), and integration with HP/Micro Focus ecosystems.
Explanation: The resume includes LoadRunner, indicating enterprise experience.

Q119: What is BlazeMeter's relationship to Apache JMeter?
A119: BlazeMeter is a cloud platform that can run JMeter scripts at scale without managing infrastructure.
Explanation: Industry knowledge; both are listed as tools.

Q120: How does the candidate use Groovy in JMeter scripting?
A120: In JSR223 Samplers to write custom logic, generate dynamic data, parse responses, and implement conditional flows faster than BeanShell.
Explanation: The resume specifies "Groovy (JMeter scripting)."
