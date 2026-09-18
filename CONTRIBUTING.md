# Contributing to MindIE Agent

Send implementation changes to the owning component. Architecture and domain boundaries belong in
[mindie-agent](https://github.com/mindie-agent/mindie-agent), Harness integration in its adapter repository,
knowledge/experience/feedback runtime in `knowledge`, domain content in `knowledge-vllm-ascend`,
remote I/O and jobs in `remote-dev`, managed execution in `coordinator`, diagnostic support in
`diagnostics`, and read-only fleet observation in `npu-top`.

Keep commits scoped and describe the trigger, changed behavior and actual validation.
Public reports must omit credentials, private endpoints and raw user task contents.
Knowledge references need sources and applicable conditions. Experience is advisory;
usefulness feedback is a separate record, not a certification of truth.

The former workspace scaffold is retired. Do not add compatibility aliases, bootstrap hooks,
business-source ownership or a second installation path. Preserve unrelated user capabilities.
