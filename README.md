# lesson-2

Tasks
1. Modify existing static loads
    1. Change constant power load on phase A of `load_1` to 48 kW real power and 24 VAr reactive power (See [`main.glm@6`](main.glm#L6-L7)).
    2. Add constant impedance load to phase B of `load_2` at 100 Ohm resistance and 10 Ohm reactance (See [`main.glm@9`](main.glm#L9-L10)).
    3. Remove constant power load on phase C of `load_4` by setting it to 0+0j complex power (See [`main.glm@12`](main.glm#L12-L13)).
2. Create new static loads
     1. Add `load_115` to `load_114` through `line_114to115` (See [`main.glm@15`](main.glm#L15-L32)).
     2. Connect `load_116` directly to `load_115` (See [`main.glm@34`](main.glm#L34-L43)).
