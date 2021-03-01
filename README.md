<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width,initial-scale=1,maximum-scale=1">
    <meta name="description" content="Remote assistance for your family and friends.">
    <meta name="keywords" content="remote assistance, remote desktop, desktop sharing, remote support, remote desktop view, remote desktop java, screen capture java">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <title>Dayon! - Remote assistance for your family and friends</title>
    <link rel="stylesheet" type="text/css" href="style.css">
    <link rel="shortcut icon" type="image/x-icon" href="favicon.ico">
</head>
<body>
<div id="container">
    <div id="top">
        <a href="de_quickstart.html"><img src="germany.png" alt="Deutsch"></a> <a href="fr_quickstart.html"><img src="france.png" alt="Français"></a>
    </div>
    <div id="menu">
        <a href="index.html">Home</a> <a href="quickstart.html">Quick Start</a> <a href="download.html">Download</a>
        <a href="support.html">Support</a> <a href="feedback.html">Feedback</a> <a href="https://github.com/retgal/dayon">GitHub</a>
    </div>
    <div id="content">
        <h2>Quick Start</h2>
        <p>
            Typically, the <i>assistant</i> is communicating with the <i>assisted</i> using Skype, the phone, their
            favorite IM, or whatever tool they like. Then starting Dayon! allows for watching live the <i>assisted</i>
            computer screen.
        <p>
            In this documentation, the screenshot show the English localisation of the app.
            The application itself is also completely localised in French, German, Spanish and Russian.
            It will fall back to English, if the configured user language is none of the above.
        <p>
            <img src="assisted.png" alt="Assisted"> &nbsp; <a name="assisted-setup" class="no"><b>Setup the Assisted Computer</b></a>
        <p>
            Dayon! Assisted is acting as a client application calling the outside world and as such there's no network
            configuration to setup.
        <p>
            Download and install the Dayon! application. Then start the <i>Dayon!</i>
            application (you should have a shortcut on the desktop) and click the "play" button.
        <p>
            <img src="assisted_ready.jpg" alt="Dayon! Assisted : Ready">
        <p>
            Enter both the IP address and the port number as communicated by the <i>assistant</i>:
            (both input fields can be cleared by double clicking them) confirm with OK.
        <p>
            <img src="assisted_start.jpg" alt="Dayon! Assisted : Starting">
        <p>
            You'll then be shortly connected to the <i>assistant</i> that is monitoring your screen. Enjoy!
        <p>
            <img src="assistant.png" alt="Assistant"> &nbsp; <a name="assistant-setup" class="no">
            <b>Setup the Assistant Computer</b></a>
        <p>
            Dayon! Assistant is acting as a typical server application (the <i>assisted</i> is going to connect to) and
            as such you've to configure your network to make it visible from the outside world. First thing to do is to
            decide the <b>listening port</b> as
            shown in the following picture. Then authorize that port number in your <b>firewall</b> and possibly setup
            accordingly your <b>NAT</b> services (typically on your DSL router).<br><br>
            Check out <a href="https://portforward.com/router.htm">portforward.com</a> for a step by step guide for the
            most common router models.
        <p>
            <img src="assistant_network_settings.jpg" alt="Dayon! Assistant: Network Settings">
        <p>
            Then you've to determine which <b>IP address</b> you want to give to the <i>assisted</i> to connect to the
            <i>assistant</i>; you should typically give your <b>public</b> IP address. But for testing within your local
            network you might want to use a
            different one. You can retrieve your <b>public IP address</b> with the following menu:
        <p>
            <img src="assistant_network_addresses.jpg" alt="Dayon! Assistant: Network IP Addresses">
        <p>
            As you can see on the following picture, the menu contains an item to copy to the clipboard the actual <b>IP
            Address & Port Number</b>. It is then easy to <b>paste it into a chat session</b> (e.g., Skype) or into an
            email.
        <p>
            <img src="assistant_network_addresses_ex.jpg" alt="Dayon! Assistant: Network IP Address Actions">
        <p>
            <i>Note that this IP address is not required by the assistant application as it is listening on all the
                available network interfaces; but you need to communicate it to the assisted. (more on this later).</i>
        <p>
            That's it regarding the network configuration;<br>
            <b>For the impatient:</b> <a href="#assistant-start">Here</a> you'll learn, how to make the <i>assistant</i>
            <a href="#assistant-start">listening for incoming connections</a>.
        <p>
            But let's first find out about the advanced configuration options.
        <p>
            <img src="assistant.png" alt="Assistant"> &nbsp; <a name="assistant-details" class="no"><b>More on the Assistant Setup</b></a>
        <p>
            Use that form to setup how the <i>assisted</i> screen is going to be <b>captured</b>; you can configure the
            time (in milliseconds) between two captures (aka. tick) as well as the number of gray levels.
        <p>
            <img src="assistant_capture_settings.jpg" alt="Dayon! Assistant: Capture Settings">
        <p>
            You can then setup the <b>compression</b> method; three methods are available: ZIP, BZIP2 and LZMA. BZIP2
            and LZMA should give a better compression ratio but requires more CPU as they're much more complicated than
            ZIP and are currently implemented in JAVA (ZIP is being implemented using some native code in the JDK).
        <p>
            In addition a <b>cache</b> is used that allows for not sending many times the same bitmap as for example
            when opening and navigating menus (i.e., what's under the menus are not sent more than once). The screen is
            divided into many tiles, each one being
            possibly cached. You've to define the maximum number of tiles in the cache. Note that a tile is currently
            32x32 pixels of 256 levels, that is 1K.
        <p>
            <img src="assistant_compression_settings.jpg" alt="Dayon! Assistant : Compression Settings">
        <p>
            <a name="assistant-start" class="no">That's about it. After a click on the play button (the first from left) the
            <i>assistant</i> is ready to accept incoming connections:</a>
        <p>
            <img src="assistant_start.jpg" alt="Dayon! Assistant : Start">
        <p>
            Now you can ask the <i>assisted</i> to connect. You'll be shortly prompted to accept the incoming
            connection:
        <p>
            <img src="assistant_incoming_connection.jpg" alt="Dayon! Assistant : Incoming Connection">
        <p>
            You're now connected and monitoring the remote computer.
        <p>
            <img src="assistant_connected.jpg" alt="Dayon! Assistant : Running">
        <p>
            If the desktop of the <i>assisted</i> doesn't fit into your window, it can be scaled down:
        <p>
            <img src="assistant_fit_screen.jpg" alt="Dayon! Assistent : Fit Screen Toggle">
        <p>
            By default, the remote <b>control mode</b> is off; you can switch it on and of using the following icon:
        <p>
            <img src="assistant_control.jpg" alt="Dayon! Assistant : Control Toggle">
        <p>
        <h2>Advanced functions</h2>
        <p>
            Prerequisites: The following functions require an established connection to the assisted.
        <p>
        <h3>Clipboard transfer</h3>
        <p>
            By clicking on the up- or down button, the clipboard of the assistant can either be transferred to the
            assisted (up) or the clipboard of the assisted to the assistant (down).
        <p>
            <img src="assistant_clipboard.jpg" alt="Dayon! Assistent : Clipboard transfer">
        <p>
            Currently supported are:
            <ul>
                <li>Text: Select text locally or in the assisted window, copy (<code>Ctl + c</code>), click up or down.
                    Subsequently, the transmitted text can be inserted in a local or remote application (<code>Ctrl + v</code>).
                <li>Files: Select one or more files locally or in the window of the <i>assisted</i> person (<code>Ctl + c</code>),
                    click up or down. Subsequently, the file(s) can be inserted at the destination.
            </ul>
        <p>
            <strong>Caution</strong>: Depending on the display/windows manager and JDK combination, the clipboard content
            does not get copied into the recipients clipboard. So pasting (<code>Ctrl + v</code>) does have no effect.<br>
            In most cases the content is nonetheless transferred - take a look at the <code>/tmp</code> directory and
            look for a uuid folder (something like <code>68abde33-dd0d-4527-ab5c-fe4bbbec4d42</code>). There you will find the
            transferred clipboard files.
        <p>
        <h3>Transmit a Windows key press</h3>
        <p>
            To transmit the press of the Windows key, click the Windows symbol in the <i>assistants</i> control panel:
        <p>
            <img src="assistant_windows_key.jpg" alt="Dayon! Assistent : Windows Key">
        <p>
            The key remains pressed until you click the symbol again. This allows you to send Windows key shortcuts.<br>
            If you need for example to minimize all windows on the <i>assisted</i> side, you would click the Windows symbol,
            press the <code>M</code> key and then click the Windows symbol again.
        <p>
            That's all folks! You can find more information on the <a href="support.html">support</a> page.
    </div>
    <div id="footer"></div>
</div>
</body>
</html>

