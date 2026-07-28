# Awesome BPMN [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

> A curated list of BPMN 2.0 tools, libraries, and developer resources for building, executing, and understanding business processes.

Process knowledge is one of the most valuable and most neglected assets in software organizations. BPMN (Business Process Model and Notation) is the standard for capturing it. This list covers the developer tooling ecosystem around BPMN: rendering libraries, execution engines, parsers, linters, knowledge platforms, and learning resources.

Contributions welcome! Open a PR or create an issue.

**See also:** [awesome-bpm](https://github.com/ungerts/awesome-bpm) — companion list focused on enterprise BPM platforms and suites.

## Contents

- [Process Knowledge Platforms](#process-knowledge-platforms)
- [Diagramming Tools with BPMN Support](#diagramming-tools-with-bpmn-support)
- [JavaScript / TypeScript Libraries](#javascript--typescript-libraries)
  - [Rendering & Editing](#rendering--editing)
  - [Parsing & Serialization](#parsing--serialization)
  - [Validation & Linting](#validation--linting)
  - [Simulation](#simulation)
  - [Layout](#layout)
- [Process Execution Engines](#process-execution-engines)
  - [Node.js](#nodejs)
  - [Java](#java)
  - [Python](#python)
  - [.NET](#net)
  - [Go](#go)
- [AI + BPMN](#ai--bpmn)
- [Process Mining & Analytics](#process-mining--analytics)
- [Converters & Migration](#converters--migration)
- [Standards & Specifications](#standards--specifications)
- [Learning Resources](#learning-resources)
  - [BPMN Element References](#bpmn-element-references)
  - [Courses](#courses)
  - [Books](#books)
  - [Blogs & Articles](#blogs--articles)
- [Community](#community)

---

## Process Knowledge Platforms

Tools that treat processes as structured organizational knowledge, not just diagrams. They combine modeling with collaboration, governance, and discovery so process knowledge is captured, shared, and kept alive.

- [Crismo](https://www.crismo.io/) - AI-native process knowledge layer for teams. Collaborative BPMN modeling with AI-assisted process discovery, a [75+ element reference library](https://www.crismo.io/bpmn-elements), and free [format converters](https://www.crismo.io/convert/drawio-to-bpmn) to rescue process knowledge trapped in non-standard tools.
- [SAP Signavio](https://www.signavio.com/) - Enterprise process intelligence platform combining modeling, mining, and automation. Acquired by SAP in 2021.
- [ARIS](https://aris.com/business-process-analysis/) - Software AG's BPA platform. The original process repository, supporting BPMN alongside EPC, value chains, and organizational models.
- [Trisotech](https://www.trisotech.com/) - Enterprise BPMN, DMN, and CMMN platform with strong standards compliance and decision modeling.
- [Bizagi](https://www.bizagi.com/) - BPM suite with a free modeler, process automation engine, and cloud execution capabilities.

## Diagramming Tools with BPMN Support

General-purpose diagramming tools that offer BPMN shape libraries. Useful for quick sketches but typically don't produce standards-compliant BPMN 2.0 XML, limiting interoperability and automation potential.

- [draw.io / diagrams.net](https://www.drawio.com/) - Free, open-source diagramming tool. Has BPMN shapes but exports as XML/SVG, not BPMN 2.0 format.
- [Lucidchart](https://www.lucidchart.com/) - Cloud diagramming with BPMN templates. No BPMN 2.0 XML export.
- [Miro](https://miro.com/) - Collaborative whiteboard with basic BPMN shapes. Not a BPMN-compliant tool.
- [Microsoft Visio](https://www.microsoft.com/en-us/microsoft-365/visio/flowchart-software) - Professional diagramming with BPMN 2.0 stencils and XML export.
- [Visual Paradigm](https://www.visual-paradigm.com/) - Full-featured modeling tool supporting BPMN, UML, and ArchiMate.
- [Enterprise Architect](http://www.sparxsystems.com.au/platforms/business_process_modeling.html) - UML/BPMN modeling suite from Sparx Systems.
- [BESSER](https://editor.besser-pearl.org/)⭐180 - Free, open-source and web-based editor for [BPMN 2.0](https://besser.readthedocs.io/en/latest/buml_language/model_types/bpmn.html) with XML import/export (as well as support for [UML and more](https://besser.readthedocs.io/en/latest/buml_language/model_types.html)). 

## JavaScript / TypeScript Libraries

### Rendering & Editing

- [bpmn-js](https://github.com/bpmn-io/bpmn-js) ⭐9.5k - The standard BPMN 2.0 rendering toolkit and web modeler. Foundation for most custom BPMN editors, including Camunda Modeler.
- [bpmn-js-properties-panel](https://github.com/bpmn-io/bpmn-js-properties-panel) ⭐330 - Properties panel extension for bpmn-js.
- [bpmn-visualization-js](https://github.com/process-analytics/bpmn-visualization-js) ⭐280 - TypeScript library for overlaying execution data on BPMN diagrams.
- [LogicFlow](https://github.com/didi/LogicFlow) ⭐11.2k - Flow chart editing framework by DiDi. Supports BPMN and custom node types.
- [bpmn-vue-activiti](https://github.com/Yiuman/bpmn-vue-activiti) ⭐647 - Vue 3 + bpmn-js process designer for Activiti workflows.
- [react-bpmn](https://github.com/pangchun/react-bpmn) - React integration for bpmn-js with support for Flowable, Activiti, and Camunda extensions.

### Parsing & Serialization

- [bpmn-moddle](https://github.com/bpmn-io/bpmn-moddle) ⭐500 - Read and write BPMN 2.0 XML in JavaScript. The standard parser in the bpmn-io ecosystem.
- [camunda-bpmn-moddle](https://github.com/camunda/camunda-bpmn-moddle) - Camunda-specific moddle extensions for BPMN 2.0.
- [zeebe-bpmn-moddle](https://github.com/camunda/zeebe-bpmn-moddle) - Zeebe (Camunda 8) moddle extensions.
- [bpmn-font](https://github.com/bpmn-io/bpmn-font) - BPMN 2.0 icon font for web applications.

### Validation & Linting

- [bpmnlint](https://github.com/bpmn-io/bpmnlint) - Validate BPMN diagrams with configurable, pluggable lint rules. ([npm](https://www.npmjs.com/package/bpmnlint))
- [bpmn-js-bpmnlint](https://github.com/bpmn-io/bpmn-js-bpmnlint) - Show lint errors directly on the bpmn-js diagram canvas.
- [BPMNspector](https://github.com/uniba-dsg/BPMNspector) - Static analysis for BPMN 2.0 process models.

### Simulation

- [bpmn-js-token-simulation](https://github.com/bpmn-io/bpmn-js-token-simulation) ⭐295 - BPMN 2.0 compliant token simulator. Step through process execution visually.

### Layout

- [bpmn-auto-layout](https://www.npmjs.com/package/bpmn-auto-layout) - Auto-generate diagram layout (DI) for BPMN files that only contain semantic data.

---

## Process Execution Engines

### Node.js

- [bpmn-engine](https://github.com/paed01/bpmn-engine) ⭐963 - Lightweight, event-driven BPMN 2.0 execution engine.
- [bpmn-server](https://github.com/bpmnServer/bpmn-server) ⭐236 - BPMN 2.0 server with persistence, monitoring, and sample UI.
- [bpmn (e2ebridge)](https://github.com/e2ebridge/bpmn) ⭐477 - BPMN 2.0 execution engine for Node.js.
- [workflow-js](https://github.com/vhidvz/workflow-js) ⭐132 - Lightweight BPMN 2.0 workflow library.

### Java

- [Camunda 8 (Zeebe)](https://github.com/camunda/camunda) ⭐4k - Cloud-native process orchestration. The current-generation Camunda platform.
- [Flowable](https://github.com/flowable/flowable-engine) ⭐9.1k - Embeddable BPMN, DMN, and CMMN engines.
- [Activiti](https://github.com/Activiti/Activiti) ⭐10.5k - Light-weight BPM engine. The project that originally spawned Camunda and Flowable.
- [Camunda 7](https://github.com/camunda/camunda-bpm-platform) ⭐4.3k - Mature BPMN engine for the JVM. CE is EOL. Forks: [CIB seven](https://cibseven.org/), [Operaton](https://operaton.org/).
- [jBPM](https://github.com/kiegroup/jbpm) ⭐1.7k - BPM Suite by Red Hat / KIE Group.
- [Apache KIE (Kogito)](https://github.com/apache/incubator-kie-kogito-examples) - Cloud-native business automation, successor to jBPM.
- [Imixs Workflow](https://github.com/imixs/imixs-workflow) ⭐410 - Human-centric open-source workflow engine.
- [Turbo](https://github.com/didi/turbo) ⭐1.2k - Lightweight BPMN flow engine by DiDi.

### Python

- [SpiffWorkflow](https://github.com/sartography/SpiffWorkflow) ⭐1.9k - BPMN 2.0 workflow engine in pure Python. Powers [Spiff Arena](https://github.com/sartography/spiff-arena).
- [viewflow](https://github.com/viewflow/viewflow) ⭐2.9k - Reusable workflow library for Django.
- [processpiper](https://github.com/csgoh/processpiper) ⭐193 - Generate BPMN-style diagrams from code or plain text.

### .NET

- [Elsa Workflows](https://github.com/elsa-workflows/elsa-core) ⭐6.5k+ - Workflow engine with a visual designer. Supports BPMN-style constructs.

### Go

- [Temporal](https://temporal.io/) ([GitHub](https://github.com/temporalio/temporal)) - Microservice orchestration platform. Not BPMN-native but widely used for durable workflow execution.

---

## AI + BPMN

The intersection of LLMs and process modeling: generating, editing, and understanding BPMN diagrams with AI.

- [Crismo AI Discovery](https://www.crismo.io/features/ai-discovery) - AI-assisted process discovery. Generates structured BPMN models from natural language process descriptions, interviews, and documents.
- [bpmn-assistant](https://github.com/jtlicardo/bpmn-assistant) ⭐110 - Open-source LLM-powered tool for creating, editing, and interpreting BPMN diagrams.
- [processpiper](https://github.com/csgoh/processpiper) - Programmatic diagram generation, useful as an LLM output format for process visualization.

---

## Process Mining & Analytics

Discover actual process flows from system event logs. Complements BPMN modeling by showing how processes really run versus how they were designed.

- [Celonis](https://www.celonis.com/) - Market-leading process mining and execution management platform.
- [Disco](https://fluxicon.com/disco/) - Fast desktop process mining tool by Fluxicon.
- [ProM Tools](http://www.promtools.org/doku.php) - Academic process mining framework with the largest collection of algorithms.
- [bpmn-visualization-js](https://github.com/process-analytics/bpmn-visualization-js) ⭐280 - Overlay execution heatmaps and KPIs on BPMN diagrams in the browser.

---

## Converters & Migration

Migrate process knowledge out of non-standard tools and into BPMN 2.0.

- [Crismo draw.io to BPMN Converter](https://www.crismo.io/convert/drawio-to-bpmn) - Free online tool that converts draw.io/diagrams.net files to standards-compliant BPMN 2.0 XML. Rescues process models trapped in general-purpose diagramming tools.
- [bpmn-to-image](https://github.com/bpmn-io/bpmn-to-image) - Render BPMN 2.0 diagrams to PNG/PDF from the command line.
- [Kroki](https://github.com/yuzutech/kroki) ⭐4k - Multi-format diagram renderer. Supports BPMN via bpmn-js.

---

## Standards & Specifications

- [BPMN 2.0.2](http://www.omg.org/spec/BPMN/2.0.2/) - The official OMG standard for Business Process Model and Notation.
- [DMN 1.4](http://www.omg.org/spec/DMN/1.4/) - Decision Model and Notation. Companion standard for modeling business rules and decision logic.
- [CMMN 1.1](http://www.omg.org/spec/CMMN/1.1/) - Case Management Model and Notation for adaptive processes.
- [BPMN Tool Matrix](https://bpmnmatrix.github.io/) - Community comparison of BPMN 2.0 tool compliance.
- [DMN TCK](https://github.com/dmn-tck/tck) - Technology Compatibility Kit for testing DMN engine compliance.

---

## Learning Resources

### BPMN Element References

- [Crismo BPMN Element Library](https://www.crismo.io/bpmn-elements) - Interactive reference for all 75+ BPMN 2.0 elements organized by category: [events](https://www.crismo.io/bpmn-elements/events), [activities](https://www.crismo.io/bpmn-elements/activities), [gateways](https://www.crismo.io/bpmn-elements/gateways), [data](https://www.crismo.io/bpmn-elements/data), [swimlanes](https://www.crismo.io/bpmn-elements/swimlanes), and [connectors](https://www.crismo.io/bpmn-elements/connectors). Each element includes description, use cases, examples, and FAQ.
- [BPMN 2.0 Poster](http://www.bpmb.de/images/BPMN2_0_Poster_EN.pdf) - Visual reference poster with all BPMN 2.0 symbols.
- [Camunda BPMN Examples](https://camunda.org/bpmn/examples/) - Modeling best practices and element usage examples.

### Courses

- [The Practical & Complete BPMN 2.0 Master Class](https://www.udemy.com/course/the-practical-and-complete-bpmn-20-master-class/?referralCode=2E792EE864792D9FF36C) - Most popular BPMN course on Udemy (40,000+ students). Covers all BPMN 2.0 elements with hands-on exercises. Also on [Coursera](https://www.coursera.org/).
- [Advanced Process Modelling with BPMN 2.0](https://www.udemy.com/course/advanced-process-modelling-with-bpmn-20/?referralCode=6AAFF7E3B15B3421BB25) - Deep dive into advanced BPMN patterns: complex gateways, event-driven processes, compensation, and choreography diagrams.
- [BPMN Meets DMN (openHPI)](https://open.hpi.de/courses/bpm2016) - Free course on BPMN and DMN by Prof. Mathias Weske.
- [Fundamentals of BPM (MOOC)](http://fundamentals-of-bpm.org/mooc/) - Academic course based on the Dumas et al. textbook.

### Books

- **Bruce Silver**: *BPMN Method and Style* (2012) - The definitive guide to BPMN modeling methodology. ISBN: [978-0982368114](https://en.wikipedia.org/wiki/Special:BookSources/978-0982368114)
- **Marlon Dumas et al.**: *[Fundamentals of Business Process Management](http://fundamentals-of-bpm.org/)* - Comprehensive textbook used in university BPM courses worldwide. ISBN: [978-3-642-33142-8](https://en.wikipedia.org/wiki/Special:BookSources/978-3-642-33142-8)
- **Jakob Freund**: *Real-Life BPMN* (2014) - Practical guide for applying BPMN 2.0 in real organizations. ISBN: [978-1502972323](https://en.wikipedia.org/wiki/Special:BookSources/978-1502972323)
- **Mathias Weske**: *Business Process Management* (2012) - Academic foundation from theory to implementation. ISBN: [978-3-642-28615-5](https://en.wikipedia.org/wiki/Special:BookSources/978-3-642-28615-5)

### Blogs & Articles

- [Crismo Blog](https://www.crismo.io/blog) - Practical BPMN guides: [gateways explained](https://www.crismo.io/blog/bpmn-gateways-explained-choose-split-wait-react), [lanes vs pools](https://www.crismo.io/blog/bpmn-lanes-vs-pools-guide), [message events](https://www.crismo.io/blog/bpmn-message-events-internal-vs-external), [events demystified](https://www.crismo.io/blog/bpmn-events-demystified-bringing-your-diagrams-to-life).
- [Camunda Blog](https://camunda.com/blog/) - Process automation insights and BPMN tutorials.
- [Flowable Blog](https://blog.flowable.org/) - Workflow engine patterns and BPMN implementation guidance.

---

## Community

- [Camunda Forum](https://forum.camunda.io/) - Active community for BPMN and process automation questions.
- [Stack Overflow [bpmn]](https://stackoverflow.com/questions/tagged/bpmn) - Developer Q&A for BPMN implementation.
- [r/bpm](https://www.reddit.com/r/bpm/) - Reddit community for Business Process Management.
- [BPMN Modeling Guidelines](http://www.modeling-guidelines.org/) - Community-maintained modeling conventions.

---

## Contributing

Contributions welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first.

- Keep descriptions concise (one or two lines)
- Include GitHub links and star counts for open-source projects
- Place tools in the most specific applicable section
- Explain what makes the tool relevant to BPMN developers

## License

[![CC0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)
