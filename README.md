# SUBCleaner-X
AI로봇프로그래밍 2조 프로젝트

### 프로젝트 노드 정리
[이동 시스템]
 └── track_controller_node → /cmd_vel → 트랙 제어

[인식 시스템]
 └── camera_node → /image_raw
 └── roboflow_client_node → /detected_targets

[작동 시스템]
 └── target_action_node
     ├── /pose, /detected_targets 구독
     ├── /spray_cmd 퍼블리시
     └── /delete_model (Gazebo)

[경로 이력 시스템]
 └── cleaning_history_node
     ├── /spray_success, /pose 구독
     └── /cleaning_markers 퍼블리시 (RViz)
