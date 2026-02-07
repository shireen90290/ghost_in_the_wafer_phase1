Problem Statement Addressed

Semiconductor wafer inspection generates large volumes of high-resolution images where microscopic defects significantly impact yield and reliability. Existing manual inspection methods are slow, inconsistent, and do not scale with high-throughput manufacturing. Cloud-based AI solutions introduce latency, bandwidth dependency, and often lack explainability, while many automated approaches stop at defect detection without identifying defect sub-types or process causes.

Solution Approach

This project addresses the problem by implementing an edge-deployable, CNN-based defect classification system using transfer learning. The model performs hierarchical defect and sub-type classification directly on-device using a lightweight ONNX model, enabling low-latency inference without cloud dependency. The solution provides explainable outputs with confidence scores and process-level insights, allowing faster corrective actions, improved process control, and scalable deployment in semiconductor manufacturing environments.
