# AkkaVisual
<h2>Actor model visualisation for Pedagogical Purposes</h2>
<p>AkkaVisual is a project intended for Actor model visualisation for Pedagogical Purposes. Project contains VCLogger library that collects information about actors in your Akka.NET project and sends those information on Web API to visualise project behavior.</p>

<h2>Code Introduction </h2>
<h3>zad6</h3>
<p>Project contains <b>VCLogger</b> library that collects Actor model behavior and sends it to API and an Akka.NET project <b>Zdk01</b> for testing purposes. Zdk01 uses Ask for actor comunication, which VCLogger has problems visualising. Should be primarily used with .Tell() actor communication.</p>
<h3>API</h3>
<p>Web Api collects information from VCLogger and should be runned at the same time as your project is executing. It is using Real time server client communication.</p>

<h2>Getting started</h2>
<p>Add VCLogger library to project you wish to visualise. Add this code to HOCON configuration in <b>App.config</b> file.</p>

      akka.actor.default-mailbox {
          mailbox-type = "VCLogger.VisualMailboxType, VCLogger"
      }
<p>Start your project and enjoy :)</p>

