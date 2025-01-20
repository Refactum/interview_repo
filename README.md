# Job Interview Task: Cutting Tool Calculation Program

## Objective
Create a program that calculates and selects a cutting tool and its parameters based on a given geometric feature. The program should implement a class structure that takes a geometric feature object as input and outputs the corresponding machining operations in JSON format.

---

## Requirements

1. **Class Structure:**
    - Develop a robust class structure to handle geometric features, machining operations, and cutting tools.
    - The main input should be a geometric feature object, and the output should include details of the machining operation and cutting tool.

2. **Functionality:**
    - The program should be able to interpret the geometric feature and determine the appropriate machining operations and tools.
    - For each machining operation, include relevant toolpath data, cutting tool specifications, machining parameters, and stock allowance information.

3. **Output Format:**
    - The output should be a JSON object structured as shown in the provided example.
    - Ensure all relevant fields such as toolpath, cutting tool, machining parameters, and stock allowance are correctly populated.

4. **Example Geometric Feature Input:**
    - Define a sample geometric feature that your program will use to demonstrate functionality.

5. **Expected JSON Output:**
    - The JSON output should mirror the provided example, encapsulating all necessary details.


## Evaluation Criteria

- **Code Quality:** Readability, maintainability, and adherence to best practices.
- **Correctness:** Accuracy of the output JSON in matching the given structure.
- **Efficiency:** How well the program handles different inputs and scales.
- **Completeness:** Inclusion of all required fields in the output.
- **Creativity:** Innovative approaches in handling the task requirements.
---

## Example JSON Output Structure

```json
{
    "substeps": [
      {
        "name": "Outer Long",
        "machining_feature": {
          "name": "Feature Name",
          "dimensions": "Feature Dimensions"
        },
        "machining_operations": [
          {
            "type": "contouring_rough_outer_long",
            "name": "Konturschruppen-Außen-Lang",
            "toolpath": [[109.7, 0, 7.8243e-14], [109.99999999999997, 0, -0.3]],
            "cutting_tool": {
              "id": 1,
              "name": "Außendrehmeißel Schruppen",
              "group": "turning_machine_cutting_tool",
              "type": "general_turning_tool",
              "cutting_direction": "outer",
              "length_z": 150,
              "length_x": 32,
              "edge_radius": 0.3969,
              "maximum_depth_of_cut": 3,
              "hand_of_cut": "right",
              "coolant_through_tool": false,
              "supplier_info_holder_name": "PWLNL 2525 M08",
              "supplier_info_insert_name": "WNMG 080408",
              "supplier_info_URI": "https://www.sandvik.coromant.com/en-us/product-details?c=PWLNL%202525M%2008HP&m=6188487"
            },
            "machining_parameter": {
              "tool_direction": "right",
              "retract_plane": 5,
              "safety_distance": 1,
              "cutting_speed": 250,
              "feedrate": 0.27,
              "cutting_depth": 3,
              "previous_diameter": 304.4000002000001
            },
            "stock_allowance": {
              "axial": 0.2,
              "radial": 0.2
            }
          },
          {
            "type": "contouring_finish_outer_long",
            "name": "Konturschlichten-Außen-Lang",
            "toolpath": [[109.7, 0, 7.8243e-14], [109.99999999999997, 0, -0.3]],
            "cutting_tool": {
              "id": 2,
              "name": "Außendrehmeißel Schlichten",
              "group": "turning_machine_cutting_tool",
              "type": "general_turning_tool",
              "cutting_direction": "outer",
              "length_z": 150,
              "length_x": 25,
              "edge_radius": 0.2,
              "maximum_depth_of_cut": 3,
              "hand_of_cut": "right",
              "coolant_through_tool": false,
              "supplier_info_holder_name": "SVJCL 2525 K11",
              "supplier_info_insert_name": "VCGT 110302",
              "supplier_info_URI": "https://www.sandvik.coromant.com/en-us/product-details?c=SVJBL%202525M%2011&m=5751640"
            },
            "machining_parameter": {
              "retract_plane": 5,
              "safety_distance": 1,
              "cutting_speed": 350,
              "feedrate": 0.08,
              "tool_direction": "right",
              "stock_allowance_axial": 0.2,
              "stock_allowance_radial": 0.2
            }
          }
        ]
      }
    ]
  }




