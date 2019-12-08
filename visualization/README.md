visualization
=================

Interfaces to publish data to the ROS rviz visualizer.

## Depth Point Cloud visualization

Support display of depth point clouds observed at each vertex. The point cloud is converted from the raw image source attached to each vertex. User can adjust display setting using the following flags:

* **vis_publish_depth_points**: If set to true, display depth point clouds. 
    **Default**: True
* **vis_depth_points_vertex_visualized_count**: Set the number of vertex point cloud to process. 
    **Default**: 5
* **vis_depth_points_from_consecutive_vertices**: If set to true, display depth point clouds from consecutive vertices. If set to false, display evenly sampled vertices along the trajectory. 
    **Default**: True
* **vis_depth_points_first_vertex_index**: Set the starting index of vertex to display. This flag works if FLAGS_vis_depth_points_from_consecutive_vertices is set to True. 
    **Default**: 0

Depth cloud points published under topic: /vi_map_depth_points

Pose of processed vertices published under: /vi_map_depth_edges/viwls

Direct edge between processed vertices published under: /vi_map_depth_vertices

Trajectory distance and Euclidean distance displayed in console log. 