# AI-DLC (AI-Driven Development Life Cycle)

An intelligent software development workflow that adapts to your needs, maintains quality standards, and keeps you in control of the process. For learning more about AI-DLC Methodology, read this [official blog](https://aws.amazon.com/blogs/devops/ai-driven-development-life-cycle/) and the [Method Definition Paper](https://prod.d13rzhkk8cj2z0.amplifyapp.com/) referred in it. 

## Quick Start

### Installation

AI-DLC uses [Amazon Q Rules](https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/context-project-rules.html) to implement its intelligent workflow. To activate AI-DLC in your project, copy the rules to your project's *project-root*/.amazonq/ folder.

```bash
git clone https://github.com/aws-samples/sample-aidlc-workflows.git
cd my-project
cp -R ../sample-aidlc-workflows/amazonq .amazonq
```

To confirm that the Amazon Q Rules are correctly loaded in your IDE, follow these steps:

1. In the Amazon Q Chat window, locate the `Rules` button in the lower right corner and click on it.

2. Verify that you see an entry for `.amazonq/rules/aws-aidlc` in the displayed list of rules.

If you do not see the `aws-aidlc` rules loaded, please check the directory where you previously issued the `cp` command. Ensure that the rules file was successfully copied to the correct location. The `.amazonq` directory must sit directly below the project root.

![](./q_rules.png?raw=true "AI-DLC Rules in Q Developer")




### Usage
1. Start any software development project by stating your intent in the chat (Amazon Q IDE Extension or in Q CLI). AI-DLC automatically activates and guides you from there.
2. Answer structured questions that AI-DLC asks you
3. Carefully review every plan that AI generates. Provide your oversight and validation.
4. Review the execution plan to see which stages will run
5. Carefully review the artifacts and approve each stage to maintain control
6. All the artifacts will be generated in the `aidlc-docs/` directory

## Three-Phase Adaptive Workflow

AI-DLC follows a structured three-phase approach that adapts to your project's complexity:

- **🔵 INCEPTION PHASE**: Determines **WHAT** to build and **WHY**
  - Requirements analysis and validation
  - User story creation (when applicable)
  - Application Design and creating units of work for parallel development
  - Risk assessment and complexity evaluation

- **🟢 CONSTRUCTION PHASE**: Determines **HOW** to build it
  - Detailed component design
  - Code generation and implementation
  - Build configuration and testing strategies
  - Quality assurance and validation

- **🟡 OPERATIONS PHASE**: Deployment and monitoring (future)
  - Deployment automation and infrastructure
  - Monitoring and observability setup
  - Production readiness validation

## Key Features

- **Adaptive Intelligence**: Only executes stages that add value to your specific request
- **Context-Aware**: Analyzes existing codebase and complexity requirements
- **Risk-Based**: Complex changes get comprehensive treatment, simple changes stay efficient
- **Question-Driven**: Structured multiple-choice questions in files, not chat
- **Always in Control**: Review execution plans and approve each phase

## Prerequisites

- Amazon Q Developer IDE plugin, Q CLI
- Supported platforms: Amazon Q Developer IDE, Q CLI (Kiro support coming soon)

---

**AI-DLC**: Intelligent software development that adapts to your work, not the other way around.