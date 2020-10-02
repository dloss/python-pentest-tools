Python tools for penetration testers
====================================

If you are involved in vulnerability research, reverse engineering or
pentesting, I suggest to try out the
[Python](http://www.python.org) programming language. It has a rich set
of useful libraries and programs. This page lists some of them.

Most of the listed tools are written in Python, others are just Python
bindings for existing C libraries, i.e. they make those libraries easily
usable from Python programs.

Some of the more aggressive tools (pentest frameworks, bluetooth
smashers, web application vulnerability scanners, war-dialers, etc.) are
left out, because the legal situation of these tools is still a bit
unclear in Germany -- even after the [decision of the highest
court](http://www.bundesverfassungsgericht.de/entscheidungen/rk20090518_2bvr223307.html).
This list is clearly meant to help whitehats, and for now I prefer to
err on the safe side.

### Network

-   [Scapy](http://secdev.org/projects/scapy): send, sniff and dissect
    and forge network packets. Usable interactively or as a library
-   [pypcap](http://code.google.com/p/pypcap/),
    [Pcapy](http://oss.coresecurity.com/projects/pcapy.html) and
    [pylibpcap](http://pylibpcap.sourceforge.net/): several different
    Python bindings for libpcap
-   [libdnet](http://code.google.com/p/libdnet/): low-level networking
    routines, including interface lookup and Ethernet frame transmission
-   [dpkt](https://github.com/kbandla/dpkt): fast, simple packet
    creation/parsing, with definitions for the basic TCP/IP protocols
-   [Impacket](http://oss.coresecurity.com/projects/impacket.html):
    craft and decode network packets. Includes support for higher-level
    protocols such as NMB and SMB
-   [pynids](http://jon.oberheide.org/pynids/): libnids wrapper offering
    sniffing, IP defragmentation, TCP stream reassembly and port scan
    detection
    [Dirtbags py-pcap](https://github.com/dirtbags/py-pcap): read pcap
    files without libpcap
-   [flowgrep](http://monkey.org/~jose/software/flowgrep/): grep through
    packet payloads using regular expressions
-   [Knock Subdomain Scan](https://github.com/guelfoweb/knock), enumerate
    subdomains on a target domain through a wordlist
-   [Spyse](https://spyse.com/) - all in one recon service for IP, domains, AS, ports, etc... [py wrapper](https://github.com/zeropwn/spyse.py)
-   [SubBrute](https://github.com/TheRook/subbrute), fast subdomain
    enumeration tool
-   [Mallory](https://bitbucket.org/IntrepidusGroup/mallory), extensible
    TCP/UDP man-in-the-middle proxy, supports modifying non-standard
    protocols on the fly
-   [Pytbull](http://pytbull.sourceforge.net/): flexible IDS/IPS testing
    framework (shipped with more than 300 tests)
-   [Spoodle](https://github.com/vjex/spoodle): A mass subdomain + poodle
    vulnerability scanner
-   [SMBMap](https://github.com/ShawnDEvans/smbmap): 
    enumerate Samba share drives across an entire domain
-   [Habu](https://github.com/portantier/habu): 
    python network hacking toolkit

### Debugging and reverse engineering

-   [Paimei](https://github.com/OpenRCE/paimei): reverse engineering
    framework, includes [PyDBG](https://github.com/OpenRCE/pydbg), PIDA,
    pGRAPH
-   [Immunity Debugger](http://debugger.immunityinc.com/):
    scriptable GUI and command line debugger
-   [mona.py](https://www.corelan.be/index.php/2011/07/14/mona-py-the-manual/):
    PyCommand for Immunity Debugger that replaces and improves on
    pvefindaddr
-   [IDAPython](https://github.com/idapython/src): IDA Pro plugin that
    integrates the Python programming language, allowing scripts to run
    in IDA Pro
-   [PyEMU](http://code.google.com/p/pyemu/): fully scriptable IA-32
    emulator, useful for malware analysis
-   [pefile](https://github.com/erocarrera/pefile): read and work with
    Portable Executable (aka PE) files
-   [pydasm](http://code.google.com/p/libdasm/source/browse/trunk/pydasm/pydasm.c):
    Python interface to the [libdasm](http://code.google.com/p/libdasm/)
    x86 disassembling library
-   [PyDbgEng](http://pydbgeng.sourceforge.net/): Python wrapper for the
    Microsoft Windows Debugging Engine
-   [uhooker](https://www.coresecurity.com/corelabs-research/open-source-tools/uhooker):
    intercept calls to API calls inside DLLs, and also arbitrary
    addresses within the executable file in memory
-   [diStorm](http://www.ragestorm.net/distorm/): disassembler library
    for AMD64, licensed under the BSD license
-   [Frida](http://www.frida.re/): A dynamic instrumentation framework which can
    inject scripts into running processes
-   [python-ptrace](http://python-ptrace.readthedocs.org/):
    debugger using ptrace (Linux, BSD and Darwin system call to trace
    processes) written in Python
-   [vdb / vtrace](http://code.google.com/p/vdebug/): vtrace is a
    cross-platform process debugging API implemented in python, and vdb
    is a debugger which uses it
-   [Androguard](https://github.com/androguard/androguard): reverse
    engineering and analysis of Android applications
-   [Capstone](http://www.capstone-engine.org/): lightweight
    multi-platform, multi-architecture disassembly framework with Python
    bindings
-   [Keystone](http://www.keystone-engine.org): lightweight multi-platform,
    multi-architecture assembler framework with Python bindings
-   [PyBFD](https://github.com/Groundworkstech/pybfd/): Python interface
    to the GNU Binary File Descriptor (BFD) library
-   [CHIPSEC](https://github.com/chipsec/chipsec): framework for analyzing the
    security of PC platforms including hardware, system firmware (BIOS/UEFI),
    and platform components.

### Fuzzing

-   [afl-python](http://jwilk.net/software/python-afl): enables American fuzzy
    lop fork server and instrumentation for pure-Python code
-   [Sulley](https://github.com/OpenRCE/sulley): fuzzer development and
    fuzz testing framework consisting of multiple extensible components
-   [Peach Fuzzing Platform](http://peachfuzz.sourceforge.net/):
    extensible fuzzing framework for generation and mutation based
    fuzzing (v2 was written in Python)
-   [antiparser](http://antiparser.sourceforge.net/): fuzz testing and
    fault injection API
-   [TAOF](http://sourceforge.net/projects/taof/), (The Art of Fuzzing)
    including ProxyFuzz, a man-in-the-middle non-deterministic network
    fuzzer
-   [untidy](http://untidy.sourceforge.net/): general purpose XML fuzzer
-   [Powerfuzzer](http://www.powerfuzzer.com/): highly automated and
    fully customizable web fuzzer (HTTP protocol based application
    fuzzer)
-   [SMUDGE](http://www.fuzzing.org/wp-content/SMUDGE.zip)
-   [Mistress](http://www.packetstormsecurity.org/fuzzer/mistress.rar):
    probe file formats on the fly and protocols with malformed data,
    based on pre-defined patterns
-   [Fuzzbox](https://isecpartners.com/tools/application-security/fuzzbox.aspx):
    multi-codec media fuzzer
-   [Forensic Fuzzing
    Tools](https://isecpartners.com/tools/application-security/forensic-fuzzing-tools.aspx):
    generate fuzzed files, fuzzed file systems, and file systems
    containing fuzzed files in order to test the robustness of forensics
    tools and examination systems
-   [Windows IPC Fuzzing
    Tools](https://isecpartners.com/tools/application-security/windows-ipc-fuzzing-tools.aspx):
    tools used to fuzz applications that use Windows Interprocess
    Communication mechanisms
-   [WSBang](https://www.isecpartners.com/tools/application-security/wsbang.aspx):
    perform automated security testing of SOAP based web services
-   [Construct](http://construct.readthedocs.org/): library for parsing
    and building of data structures (binary or textual). Define your
    data structures in a declarative manner
-   [fuzzer.py
    (feliam)](http://sites.google.com/site/felipeandresmanzano/fuzzer.py?attredirects=0):
    simple fuzzer by Felipe Andres Manzano
-   [Fusil](http://fusil.readthedocs.org/): Python library
    used to write fuzzing programs

### Web

-   [Requests](http://python-requests.org/): elegant and simple HTTP
    library, built for human beings
-   [lxml](http://lxml.de/index.html): easy-to-use library for processing XML and HTML; similar to Requests
-   [HTTPie](http://httpie.org): human-friendly cURL-like command line
    HTTP client
-   [ProxMon](https://www.isecpartners.com/tools/application-security/proxmon.aspx):
    processes proxy logs and reports discovered issues
-   [WSMap](https://www.isecpartners.com/tools/application-security/wsmap.aspx):
    find web service endpoints and discovery files
-   [Twill](http://twill.idyll.org/): browse the Web from a command-line
    interface. Supports automated Web testing
-   [Ghost.py](http://jeanphix.me/Ghost.py/): webkit web client written
    in Python
-   [Windmill](http://www.getwindmill.com/): web testing tool designed
    to let you painlessly automate and debug your web application
-   [FunkLoad](http://funkload.nuxeo.org/): functional and load web
    tester
-   [spynner](https://github.com/makinacorpus/spynner): Programmatic web
    browsing module for Python with Javascript/AJAX support
-   [python-spidermonkey](http://code.google.com/p/python-spidermonkey/):
    bridge to the Mozilla SpiderMonkey JavaScript engine; allows for the
    evaluation and calling of Javascript scripts and functions
-   [mitmproxy](http://mitmproxy.org/): SSL-capable, intercepting HTTP
    proxy. Console interface allows traffic flows to be inspected and
    edited on the fly
-   [pathod / pathoc](http://pathod.net/): pathological daemon/client
    for tormenting HTTP clients and servers
-   [spidy](https://github.com/rivermont/spidy/): simple command-line web crawler with page downloading and word scraping

### Forensics

-   [Volatility](http://www.volatilityfoundation.org/):
    extract digital artifacts from volatile memory (RAM) samples
-   [Rekall](http://www.rekall-forensic.com):
    memory analysis framework developed by Google
-   [LibForensics](http://code.google.com/p/libforensics/): library for
    developing digital forensics applications
-   [TrIDLib](http://mark0.net/code-tridlib-e.html), identify file types
    from their binary signatures. Now includes Python binding
-   [aft](http://code.google.com/p/aft/): Android forensic toolkit

### Malware analysis

-   [pyew](https://github.com/joxeankoret/pyew): command line hexadecimal
    editor and disassembler, mainly to analyze malware
-   [Exefilter](http://www.decalage.info/exefilter): filter file formats
    in e-mails, web pages or files. Detects many common file formats and
    can remove active content
-   [pyClamAV](http://xael.org/norman/python/pyclamav/index.html): add
    virus detection capabilities to your Python software
-   [jsunpack-n](https://github.com/urule99/jsunpack-n), generic
    JavaScript unpacker: emulates browser functionality to detect
    exploits that target browser and browser plug-in vulnerabilities
-   [yara-python](https://github.com/VirusTotal/yara-python):
    identify and classify malware samples
-   [phoneyc](https://github.com/honeynet/phoneyc): pure Python
    honeyclient implementation
-   [CapTipper](https://github.com/omriher/CapTipper): analyse, explore and
    revive HTTP malicious traffic from PCAP file

### PDF

-   [peepdf](http://eternal-todo.com/tools/peepdf-pdf-analysis-tool):
    Python tool to analyse and explore PDF files to find out if they can be harmful
-   [Didier Stevens' PDF
    tools](http://blog.didierstevens.com/programs/pdf-tools): analyse,
    identify and create PDF files (includes
    [PDFiD](http://blog.didierstevens.com/programs/pdf-tools/#pdfid),
    [pdf-parser](http://blog.didierstevens.com/programs/pdf-tools/#pdf-parser)
    and
    [make-pdf](http://blog.didierstevens.com/programs/pdf-tools/#make-pdf)
    and mPDF)
-   [Opaf](http://code.google.com/p/opaf/): Open PDF Analysis Framework.
    Converts PDF to an XML tree that can be analyzed and modified.
-   [Origapy](http://www.decalage.info/python/origapy): Python wrapper
    for the Origami Ruby module which sanitizes PDF files
-   [pyPDF2](http://mstamy2.github.io/PyPDF2/): pure Python PDF toolkit: extract
    info, spilt, merge, crop, encrypt, decrypt...
-   [PDFMiner](http://www.unixuser.org/~euske/python/pdfminer/index.html):
    extract text from PDF files
-   [python-poppler-qt4](https://github.com/wbsoft/python-poppler-qt4):
    Python binding for the Poppler PDF library, including Qt4 support

### Misc

-   [InlineEgg](http://oss.coresecurity.com/projects/inlineegg.html):
    toolbox of classes for writing small assembly programs in Python
-   [Exomind](http://corelabs.coresecurity.com/index.php?module=Wiki&action=view&type=tool&name=Exomind):
    framework for building decorated graphs and developing open-source
    intelligence modules and ideas, centered on social network services,
    search engines and instant messaging
-   [RevHosts](http://www.securityfocus.com/tools/3851): enumerate
    virtual hosts for a given IP address
-   [simplejson](https://github.com/simplejson/simplejson/): JSON
    encoder/decoder, e.g. to use [Google's AJAX
    API](http://dcortesi.com/2008/05/28/google-ajax-search-api-example-python-code/)
-   [PyMangle](http://code.google.com/p/pymangle/): command line tool
    and a python library used to create word lists for use with other
    penetration testing tools
-   [Hachoir](https://hachoir.readthedocs.io/en/latest/): view and
    edit a binary stream field by field 
-   [py-mangle](http://code.google.com/p/pymangle/): command line tool
    and a python library used to create word lists for use with other
    penetration testing tools
-   [wmiexec.py](https://github.com/CoreSecurity/impacket/blob/master/examples/wmiexec.py):
    execute Powershell commands quickly and easily via WMI
-   [Pentestly](https://github.com/praetorian-inc/pentestly):
    Python and Powershell internal penetration testing framework
-   [hacklib](https://github.com/leonli96/python-hacklib):
    Toolkit for hacking enthusiasts: word mangling, password guessing,
    reverse shell and other simple tools

### Other useful libraries and tools

-   [IPython](http://ipython.scipy.org/): enhanced interactive Python
    shell with many features for object introspection, system shell
    access, and its own special command system
-   [Beautiful Soup](http://www.crummy.com/software/BeautifulSoup/):
    HTML parser optimized for screen-scraping
-   [matplotlib](http://matplotlib.sourceforge.net/): make 2D plots of
    arrays
-   [Mayavi](http://code.enthought.com/projects/mayavi/): 3D scientific
    data visualization and plotting
-   [RTGraph3D](http://www.secdev.org/projects/rtgraph3d/): create
    dynamic graphs in 3D
-   [Twisted](http://twistedmatrix.com/): event-driven networking engine
-   [Suds](https://fedorahosted.org/suds/): lightweight SOAP client for
    consuming Web Services
-   [M2Crypto](http://chandlerproject.org/bin/view/Projects/MeTooCrypto):
    most complete OpenSSL wrapper
-   [NetworkX](http://networkx.lanl.gov/): graph library (edges, nodes)
-   [Pandas](http://pandas.pydata.org/): library providing
    high-performance, easy-to-use data structures and data analysis
    tools
-   [pyparsing](http://pyparsing.wikispaces.com/): general parsing
    module
-   [lxml](http://lxml.de/): most feature-rich and easy-to-use library
    for working with XML and HTML in the Python language
-   [Whoosh](https://bitbucket.org/mchaput/whoosh/): fast, featureful
    full-text indexing and searching library implemented in pure Python
-   [Pexpect](https://github.com/pexpect/pexpect): control and automate
    other programs, similar to Don Libes \`Expect\` system
-   [Sikuli](http://groups.csail.mit.edu/uid/sikuli/), visual technology
    to search and automate GUIs using screenshots. Scriptable in
    [Jython](http://www.jython.org/)
-   [PyQt](http://www.riverbankcomputing.co.uk/software/pyqt) and
    [PySide](http://www.pyside.org/): Python bindings for the Qt
    application framework and GUI library

### Books

-   [Violent Python](https://www.elsevier.com/books/violent-python/unknown/978-1-59749-957-6) by TJ O'Connor. A Cookbook for Hackers, Forensic Analysts, Penetration Testers and Security Engineers
-   [Grey Hat Python](http://www.nostarch.com/ghpython.htm) by Justin Seitz: 
    Python Programming for Hackers and Reverse Engineers.
-   [Black Hat Python](http://www.nostarch.com/blackhatpython) by Justin Seitz:
    Python Programming for Hackers and Pentesters
-   [Python Penetration Testing Essentials](https://www.packtpub.com/networking-and-servers/python-penetration-testing-essentials) by Mohit:
    Employ the power of Python to get the best out of pentesting
-   [Python for Secret Agents](https://www.packtpub.com/hardware-and-creative/python-secret-agents) by Steven F. Lott. Analyze, encrypt, and uncover intelligence data using Python
-   [Python Web Penetration Testing Cookbook](https://www.packtpub.com/networking-and-servers/python-web-penetration-testing-cookbook/) by Cameron Buchanan et al.: Over 60 Python recipes for web application testing
-   [Learning Penetration Testing with Python](https://www.packtpub.com/networking-and-servers/learning-penetration-testing-python) by Christopher Duffy: Utilize Python scripting to execute effective and efficient penetration tests
-   [Python Forensics](http://www.sciencedirect.com/science/book/9780124186767) by Chet Hosmer:
    A Workbench for Inventing and Sharing Digital Forensic Technology
-   [The Beginner's Guide to IDAPython](https://leanpub.com/IDAPython-Book) by Alexander Hanel
-   [Python for Offensive PenTest: A Practical Guide to Ethical Hacking and Penetration Testing Using Python](https://www.amazon.com/Python-Offensive-PenTest-practical-penetration/dp/1788838971) by Hussam Khrais

### Talks, slides and articles

-   [Python & Reverse Engineering Software](https://bitbucket.org/Alexander_Hanel/papers/raw/afa0228ffc53efc105a1fb632c4296f534a44429/Python%20&%20Reverse%20Engineering%20Software.pdf) by Alexander Hanel
-   [Python Arsenal for Reverse Engineering](http://dsec.ru/upload/medialibrary/7d5/7d5e8a49b25b285b37800480a41583f8.pdf) by Dmitriy Evdokimov at RUCTF 2016

### More stuff

-   [SecurityTube Python Scripting Expert (SPSE)](http://www.securitytube-training.com/online-courses/securitytube-python-scripting-expert/) is an online course and certification offered by Vivek Ramachandran.
-   SANS offers the course [SEC573: Python for Penetration Testers](http://www.sans.org/course/python-for-pen-testers).
-   The [Python Arsenal for Reverse Engineering](http://pythonarsenal.erpscan.com/)
    is a large collection of tools related to reverse engineering.
-   There is a SANS paper about Python libraries helpful for forensic analysis
    [(PDF)](http://www.sans.org/reading_room/whitepapers/incident/grow-forensic-tools-taxonomy-python-libraries-helpful-forensic-analysis_33453).
-   For more Python libaries, please have a look at
    [PyPI](http://pypi.python.org/pypi), the Python Package Index.

