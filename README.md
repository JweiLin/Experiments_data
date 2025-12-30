# Experiments Data

This repository contains the benchmark datasets and experimental results used in our paper.  
The result data can be validated using binary files provided by the industrial vendor, ensuring both correctness and authenticity.

## Contents
- `TestCase/` : Benchmark testcases from the Die-Level Routing Contest 2023 and industrial vendor.
- `with_rerouting_result/`  
  Contains the outputs of our algorithm **with the rerouting module enabled**.  
  These results demonstrate how the delay-constrained rerouting strategy improves routing quality.

- `without_rerouting_result/`  
  Contains the outputs of our algorithm **without the rerouting module**.  
  These results serve as a baseline, allowing direct comparison to highlight the contribution of rerouting.

- `route_checker_1201` : Binary tool provided by the vendor for result validation.

## How to Run

To validate the routing results, use the vendor-provided binary tool:

```bash
./route_checker_1201 \
  -input_design_dir ./TestCase/testcase1 \
  -output_route_out_dir ./with_rerouting_result/testcase1 \
  -output_tdm_out_dir ./with_rerouting_result/testcase1
