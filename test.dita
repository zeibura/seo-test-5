<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "technicalContent/dtd/concept.dtd">
<concept id="_ea83e38a-600e-4c53-9308-b07e3b1ec8da">
  <title>Manage Dependencies</title>
  <shortdesc>Configure your VS Code workspace to enable navigation across copybooks, macros and other dependencies, and enable automatic retrieval of dependencies from the mainframe.</shortdesc>
  <conbody>
    <p><keyword keyref="pname"></keyword> can retrieve COBOL copybooks and HLASM macros from the mainframe and download them to your VS Code workspace. You can also specify folders that contain dependencies in your workspace to enable LSP features for copybooks and macros, and facilitate navigation between the main source code and dependencies.</p>
    <section id="EnableSupportForLocallyStoredCOBOLCopybooksAndSubroutines">
      <title>Enable Support for Locally Stored COBOL Copybooks and Subroutines</title>
      <p>To enable LSP features for locally stored COBOL copybooks and subroutines, specify paths to folders which contain these files in your VS Code workspace extension settings. You can use Glob wildcards such as * to substitute one whole level of the path. The folders are searched in the order that you list them, or in alphabetical order if multiple paths are indexed by a wildcard.</p>
      <p>We recommend that you specify relative paths from the workspace root. To obtain the relative path of a folder in your workspace, right-click the folder in the folder tree and select <uicontrol>Copy Relative Path</uicontrol>.</p>
      <p>To specify folders that contain dependencies, perform the following steps:</p>
      <ol>
        <li>In VS Code, open the <uicontrol>Extensions</uicontrol> tab.</li>
        <li>Locate <uicontrol>COBOL Language Support</uicontrol>, click the <uicontrol>Manage</uicontrol> icon, and select <uicontrol>Extension settings</uicontrol>. </li>
        <li>Switch from <uicontrol>User</uicontrol> to <uicontrol>Workspace</uicontrol>.</li>
        <li>Under <uicontrol>Cobol-lsp › Cpy-manager: Paths-local</uicontrol>, click <uicontrol>Add Item</uicontrol> and specify the path of a folder that contains copybooks. Repeat this step for each folder that you want to add. </li>
        <li>Under <uicontrol>Cobol-lsp › Subroutine-manager: Paths-local</uicontrol>, click <uicontrol>Add Item</uicontrol> and specify the path of a folder that contains subroutines. Repeat this step for each folder that you want to add. </li>
        <li>If your copybooks use extensions other than .copy and .cpy, peform the following steps:
          <ol>
            <li>Under <uicontrol>Cobol-lsp › Cpy-manager: Copybook-extensions</uicontrol>, click <uicontrol>Edit in settings.json</uicontrol>.
              <p>The settings.json file opens.</p>
            </li>
            <li>Add your copybook file extensions to the <codeph>cobol-lsp.cpy-manager.copybook-extensions</codeph> array.</li>
            <li>Save and close the file.</li>
          </ol>
        </li>
        <li>Open a program or project.</li>
      </ol>
      <p>You enabled copybook and subroutine support. For a comprehensive overview of COBOL dependency support features, see the <xref href="https://marketplace.visualstudio.com/items?itemName=broadcomMFD.cobol-language-support" scope="external">COBOL Language Support documentation</xref> on the VS Code Marketplace.</p>
    </section>
    <section id="RetrieveCOBOLCopybooksFromMainframeAndUSSDataSets">
      <title>Retrieve COBOL Copybooks from Mainframe and USS Data Sets </title>
      <p><keyword keyref="pname"></keyword> automatically retrieves COBOL copybooks that are stored in partitioned data sets and in USS files, and downloads the copybooks to a folder in your workspace. To retrieve copybooks from remote locations, specify mainframe DSNs and USS paths in your VS Code workspace extension settings. Paths are indexed in the order that you list them. Copybooks that are downloaded from remote locations are also converted to UTF-8 encoding if they use an encoding other than UTF-8.</p>
      <note>A Zowe profile that contains a server URL and mainframe credentials is required to use this feature. For more information, see <xref href="create-a-zowe-client-configuration-file.dita#_034dca66-e9e6-470d-a9c6-52be1cb05eba" scope="local">Create a Zowe Client Configuration File</xref>.</note>
      <p>Use the following procedure to enable automatic copybook retrieval: </p>
      <ol>
        <li>In VS Code, open the <uicontrol>Extensions</uicontrol> tab.</li>
        <li>Locate <uicontrol>COBOL Language Support</uicontrol>, click the <uicontrol>Manage</uicontrol> icon, and select <uicontrol>Extension settings</uicontrol>. </li>
        <li>Switch from <uicontrol>User</uicontrol> to <uicontrol>Workspace</uicontrol>.</li>
        <li>Under <uicontrol>Cpy-manager: Profiles</uicontrol>, enter the name of your Zowe Profile configuration. </li>
        <li>Under <uicontrol>Cpy-manager: Paths-dsn</uicontrol>, click <uicontrol>Add Item</uicontrol> and specify the full name of a partitioned data set on the mainframe to search for copybooks.
          <p><b>Example:</b> HLQ.EXAMPLE.CPY</p>
        </li>
        <li>Under <uicontrol>Cpy-manager: Paths-uss</uicontrol>, click <uicontrol>Add Item</uicontrol> and specify a USS path to search for copybooks. Specify absolute paths.
          <p><b>Example:</b> /u/user01/acct/COBCPY</p>
        </li>
        <li>If your copybooks use a file encoding other than UTF-8, specify it under <uicontrol>Cpy-manager: Copybook-file-encoding.</uicontrol></li>
        <li>If your copybooks use extensions other than .copy and .cpy, perform the following steps:
          <ol>
            <li>Under <uicontrol>Cobol-lsp › Cpy-manager: Copybook-extensions</uicontrol>, click <uicontrol>Edit in settings.json</uicontrol>.
              <p>The settings.json file opens.</p>
            </li>
            <li>Add your copybook file extensions to the <codeph>cobol-lsp.cpy-manager.copybook-extensions</codeph> array.</li>
            <li>Save and close the file.</li>
          </ol>
        </li>
        <li>Open a program or project.</li>
      </ol>
      <p>Copybooks are automatically downloaded from the locations that you specify to the <uicontrol>.c4z/.copybooks</uicontrol> folder in your workspace. Copybook support features are also automatically enabled. For an overview of COBOL dependency support features, see the <xref href="https://marketplace.visualstudio.com/items?itemName=broadcomMFD.cobol-language-support" scope="external">COBOL Language Support documentation</xref> on the VS Code Marketplace.</p>
    </section>
    <section id="HLASMMacrosAndCOPYMembers">
      <title>HLASM Macros and COPY Members</title>
      <p>To enable LSP support for HLASM macros and COPY members, specify the locations that contain these dependencies in a processor group. For an overview of the available <keyword keyref="pname"></keyword> processor group options, see <xref href="define-processor-groups.dita#_034dca66-e9e6-470d-a9c6-52be1cb05eba" scope="local">Define Processor Groups</xref>.</p>
      <p><keyword keyref="pname"></keyword> can also download HLASM dependencies from mainframe data sets. To use this feature, a Zowe profile that contains a server URL and mainframe credentials is recommended.</p>
      <p>To enable support for HLASM dependencies, perform the following steps:</p>
      <ol>
        <li>Open or create a <uicontrol>/.hlasmplugin</uicontrol> folder in your workspace root.</li>
        <li>Open or create the file <uicontrol>proc_grps.json</uicontrol>.</li>
        <li>In the <codeph>pgroups</codeph> array, add a JSON element that contains the following fields:
          <parml>
            <plentry>
              <pt>name</pt>
              <pd>Type: string</pd>
              <pd>Specifies a name for the processor group.</pd>
            </plentry>
            <plentry>
              <pt>libs</pt>
              <pd>Type: array</pd>
              <pd>Specify an array of strings. Specify local folders or a mainframe data sets. You can specify local folders as absolute paths or as relative paths to the workspace root.</pd>
            </plentry>
          </parml>
        </li>
        <li>Save the <uicontrol>proc_grps.json</uicontrol> file.</li>
        <li>Open or create the file <uicontrol>pgm_conf.json</uicontrol>.</li>
        <li>In the <codeph>pgms</codeph> array, add a JSON element that contains the following fields:
          <parml>
            <plentry>
              <pt>program</pt>
              <pd>Type: string</pd>
              <pd>Specifies the program name. <note>To enable support for all programs, specify the wildcard <codeph>“*”</codeph>.</note></pd>
            </plentry>
            <plentry>
              <pt>pgroup</pt>
              <pd>Type: string</pd>
              <pd>Specifies the processor group name from step 3.</pd>
            </plentry>
          </parml>
        </li>
        <li>Save the <uicontrol>pgm_conf.json</uicontrol> file.</li>
        <li>Open a program or project.
          <p>LSP support for HLASM dependencies is now enabled.</p>
        </li>
      </ol>
      </section>
    <section id="DownloadHLASMDependenciesFromMainframeDataSets"><title>Download HLASM Dependencies from Mainframe Data Sets</title>
      <p>If you specify mainframe data sets in a processor group, use the following procedure to download dependencies from the mainframe to a folder in your workspace:</p>
      <ol>
        <li>Press <uicontrol>F1</uicontrol> to open the Command Pallet. </li>
        <li>Run the command <uicontrol>HLASM: Download dependencies</uicontrol>.</li>
        <li>Specify the name of your Zowe Profile configuration in the format @profilename.</li>
        <li>Enter your job header.</li>
      </ol>
      <p>All dependencies are downloaded from the specified data sets to a folder in your workspace.</p>
    </section>
    <section id="VerifyDependencyConfiguration">
      <title>Verify Dependency Configuration</title>
      <p>To verify your dependency configuration, right click the name of a dependency in your source code and select <uicontrol>Go To Definition</uicontrol>. If the dependencies are configured correctly, the copybook or macro opens in a new tab.</p>
    </section>
  </conbody>
</concept>
