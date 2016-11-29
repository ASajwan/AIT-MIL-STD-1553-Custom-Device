If upgrading to 2013 sp1 from previous version, you need to place the xml content at this link in a file alongside your lvproj or you will have problems with system definition dll linkages.

https://decibel.ni.com/content/docs/DOC-26812


Here is content from link


StephenB Apr 24, 2014 1:53 PM (in response to Dan A.)

Dan, you might need to force the assemblies that the library is linked to be the ones for NIVS 2013. You can do this by placing an XML file next to your labview 
project named <project name>.lvproj.config and/or by placing an XML file next to your LabVIEW.exe named LabVIEW.exe.config. 
I would attach the XML file here but you cannot do so in comments so I'm pasing the contents. 
I'm giving two, one for NIVS 2013 and one for NIVS 2013 SP1 (which is available for download now).



NIVS 2013 SP1:
<?xml version ="1.0"?>
<configuration>
    <runtime>
        <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
        <!-- ================================= GAC files ==================================== -->
          <dependentAssembly>
            <assemblyIdentity name="NationalInstruments.VeriStand.APIInterface" publicKeyToken="a6d690c380daa308" culture="Neutral" />
            <!-- Assembly versions can be redirected in application,
              publisher policy, or machine configuration files. -->
            <bindingRedirect oldVersion="0.0.0.0-2013.0.0.0" newVersion="2013.1.0.0" />
          </dependentAssembly>
          <dependentAssembly>
            <assemblyIdentity name="NationalInstruments.VeriStand.ClientAPI" publicKeyToken="a6d690c380daa308" culture="Neutral" />
            <!-- Assembly versions can be redirected in application,
              publisher policy, or machine configuration files. -->
            <bindingRedirect oldVersion="0.0.0.0-2013.0.0.0" newVersion="2013.1.0.0" />
          </dependentAssembly>
          <dependentAssembly>
            <assemblyIdentity name="NationalInstruments.VeriStand" publicKeyToken="a6d690c380daa308" culture="Neutral" />
            <!-- Assembly versions can be redirected in application,
              publisher policy, or machine configuration files. -->
            <bindingRedirect oldVersion="0.0.0.0-2013.0.0.0" newVersion="2013.1.0.0" />
          </dependentAssembly>
          <dependentAssembly>
            <assemblyIdentity name="NationalInstruments.VeriStand.Internal" publicKeyToken="a6d690c380daa308" culture="Neutral" />
            <!-- Assembly versions can be redirected in application,
              publisher policy, or machine configuration files. -->
            <bindingRedirect oldVersion="0.0.0.0-2013.0.0.0" newVersion="2013.1.0.0" />
          </dependentAssembly>
          <dependentAssembly>
            <assemblyIdentity name="NationalInstruments.VeriStand.SystemDefinitionAPI" publicKeyToken="a6d690c380daa308" culture="Neutral" />
            <!-- Assembly versions can be redirected in application,
              publisher policy, or machine configuration files. -->
            <bindingRedirect oldVersion="0.0.0.0-2013.0.0.0" newVersion="2013.1.0.0" />
          </dependentAssembly>
          <dependentAssembly>
            <assemblyIdentity name="NationalInstruments.VeriStand.SystemStorage" publicKeyToken="a6d690c380daa308" culture="Neutral" />
            <!-- Assembly versions can be redirected in application,
              publisher policy, or machine configuration files. -->
            <bindingRedirect oldVersion="0.0.0.0-2013.0.0.0" newVersion="2013.1.0.0" />
          </dependentAssembly>
          <dependentAssembly>
            <assemblyIdentity name="NationalInstruments.VeriStand.SystemStorageUI" publicKeyToken="a6d690c380daa308" culture="Neutral" />
            <!-- Assembly versions can be redirected in application,
              publisher policy, or machine configuration files. -->
            <bindingRedirect oldVersion="0.0.0.0-2013.0.0.0" newVersion="2013.1.0.0" />
          </dependentAssembly>
          <dependentAssembly>
            <assemblyIdentity name="NationalInstruments.VeriStand.WorkspaceMacro" publicKeyToken="a6d690c380daa308" culture="Neutral" />
            <!-- Assembly versions can be redirected in application,
              publisher policy, or machine configuration files. -->
            <bindingRedirect oldVersion="0.0.0.0-2013.0.0.0" newVersion="2013.1.0.0" />
          </dependentAssembly>
          <dependentAssembly>
          <assemblyIdentity name="NationalInstruments.VeriStand.XMLReader" publicKeyToken="a6d690c380daa308" culture="Neutral" />
            <!-- Assembly versions can be redirected in application,
              publisher policy, or machine configuration files. -->
            <bindingRedirect oldVersion="0.0.0.0-2013.0.0.0" newVersion="2013.1.0.0" />
          </dependentAssembly>
          <dependentAssembly>
          <assemblyIdentity name="NationalInstruments.VeriStand.DataTypes" publicKeyToken="a6d690c380daa308" culture="Neutral" />
            <!-- Assembly versions can be redirected in application,
              publisher policy, or machine configuration files. -->
            <bindingRedirect oldVersion="0.0.0.0-2013.0.0.0" newVersion="2013.1.0.0" />
          </dependentAssembly>
          <dependentAssembly>
          <assemblyIdentity name="NationalInstruments.VeriStand.ATMLTestResults" publicKeyToken="a6d690c380daa308" culture="Neutral" />
            <!-- Assembly versions can be redirected in application,
              publisher policy, or machine configuration files. -->
            <bindingRedirect oldVersion="0.0.0.0-2013.0.0.0" newVersion="2013.1.0.0" />
          </dependentAssembly>
          <dependentAssembly>
          <assemblyIdentity name="NationalInstruments.VeriStand.RealTimeSequenceDefinitionApi" publicKeyToken="a6d690c380daa308" culture="Neutral" />
            <!-- Assembly versions can be redirected in application,
              publisher policy, or machine configuration files. -->
            <bindingRedirect oldVersion="0.0.0.0-2013.0.1.0" newVersion="2013.1.0.0" />
          </dependentAssembly>
          <dependentAssembly>
          <assemblyIdentity name="NationalInstruments.VeriStand.UsiDotNetApi" publicKeyToken="a6d690c380daa308" culture="Neutral" />
            <!-- Assembly versions can be redirected in application,
              publisher policy, or machine configuration files. -->
            <bindingRedirect oldVersion="0.0.0.0-2013.0.0.0" newVersion="2013.1.0.0" />
          </dependentAssembly>
    <!-- ================================= Local files ==================================== -->
          <dependentAssembly>
          <assemblyIdentity name="NationalInstruments.VeriStand.CommonUI" publicKeyToken="a6d690c380daa308" culture="Neutral" />
            <!-- Assembly versions can be redirected in application,
              publisher policy, or machine configuration files. -->
            <bindingRedirect oldVersion="0.0.0.0-2013.0.0.0" newVersion="2013.1.0.0" />
          </dependentAssembly>
          <dependentAssembly>
          <assemblyIdentity name="NationalInstruments.VeriStand.Compiler" publicKeyToken="a6d690c380daa308" culture="Neutral" />
            <!-- Assembly versions can be redirected in application,
              publisher policy, or machine configuration files. -->
            <bindingRedirect oldVersion="0.0.0.0-2013.0.0.0" newVersion="2013.1.0.0" />
          </dependentAssembly>
          <dependentAssembly>
          <assemblyIdentity name="NationalInstruments.VeriStand.MacroPlayerRecorder" publicKeyToken="a6d690c380daa308" culture="Neutral" />
            <!-- Assembly versions can be redirected in application,
              publisher policy, or machine configuration files. -->
            <bindingRedirect oldVersion="0.0.0.0-2013.0.0.0" newVersion="2013.1.0.0" />
          </dependentAssembly>
          <dependentAssembly>
          <assemblyIdentity name="NationalInstruments.VeriStand.ResXResourceManager" publicKeyToken="a6d690c380daa308" culture="Neutral" />
            <!-- Assembly versions can be redirected in application,
              publisher policy, or machine configuration files. -->
            <bindingRedirect oldVersion="0.0.0.0-2013.0.0.0" newVersion="2013.1.0.0" />
          </dependentAssembly>
          <dependentAssembly>
          <assemblyIdentity name="NationalInstruments.VeriStand.ServerAPI" publicKeyToken="a6d690c380daa308" culture="Neutral" />
            <!-- Assembly versions can be redirected in application,
              publisher policy, or machine configuration files. -->
            <bindingRedirect oldVersion="0.0.0.0-2013.0.0.0" newVersion="2013.1.0.0" />
          </dependentAssembly>
          <dependentAssembly>
          <assemblyIdentity name="NationalInstruments.VeriStand.UIStyleManager" publicKeyToken="a6d690c380daa308" culture="Neutral" />
            <!-- Assembly versions can be redirected in application,
              publisher policy, or machine configuration files. -->
            <bindingRedirect oldVersion="0.0.0.0-2013.0.0.0" newVersion="2013.1.0.0" />
          </dependentAssembly> 
          <dependentAssembly>
          <assemblyIdentity name="NationalInstruments.VeriStand.DataTypes.Utilities.dll" publicKeyToken="a6d690c380daa308" culture="Neutral" />
            <!-- Assembly versions can be redirected in application,
              publisher policy, or machine configuration files. -->
            <bindingRedirect oldVersion="0.0.0.0-2013.0.0.0" newVersion="2013.1.0.0" />
          </dependentAssembly>
        </assemblyBinding>
    </runtime>
</configuration>
