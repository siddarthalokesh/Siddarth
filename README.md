<div align="center">

```
[BOOT] Initializing engineering profile...
[BOOT] Loading identity.bin ......... OK
[BOOT] Mounting /dev/verilog ........ OK
[BOOT] Linking RTL toolchain ........ OK
```

<img src="https://readme-typing-svg.demolab.com/?font=JetBrains+Mono&size=20&pause=1000&color=00E5FF&center=true&vCenter=true&width=560&lines=SYSTEM+ONLINE;RTL+ENGINEER+IN+PROGRESS;FPGA+%7C+VERILOG+%7C+DIGITAL+DESIGN;BUILDING+HARDWARE%2C+ONE+BIT+AT+A+TIME" alt="typing banner" />

</div>

<br>

```
┌──────────────────────────────────────────────────────────┐
│  REG_0x00  NAME        SIDDH                              │
│  REG_0x01  DOMAIN       ELECTRONICS & COMMUNICATION ENGG  │
│  REG_0x02  MODE         LEARNING + BUILDING                │
│  REG_0x03  HDL          VERILOG                             │
│  REG_0x04  TARGET       FPGA                                │
│  REG_0x05  STAGE        RTL DESIGN → VERIFICATION           │
│  REG_0x06  TRACK        HAL (CBT) — CORE ELECTRONICS PREP   │
│  STATUS                 [ ONLINE ]                          │
└──────────────────────────────────────────────────────────┘
```

### `> about.this`

ECE student, working bottom-up: gates → RTL → simulation → hardware.
Current focus is writing correct Verilog, reasoning about timing and
synchronization, and closing the loop with verification — not just
getting a design to "look right" in a waveform once. Also preparing
for the HAL recruitment CBT, which keeps me anchored in the core
electronics and control-systems fundamentals alongside the RTL work.

<br>

## `> current_build` — Synchronous FIFO (Verilog)

**Status: `IN PROGRESS`**

```
        WRITE                                   READ
          │                                       │
          ▼                                       ▼
   ┌─────────────┐                         ┌─────────────┐
   │ WRITE PTR   │──────┐           ┌──────│  READ PTR   │
   │  (w_ptr)    │      │           │      │  (r_ptr)    │
   └─────────────┘      ▼           ▼      └─────────────┘
                  ┌───────────────────────┐
                  │      MEMORY (RAM)     │
                  │   depth = 2^N words   │
                  └───────────────────────┘

   FULL   : w_ptr[N] != r_ptr[N]  &&  w_ptr[N-1:0] == r_ptr[N-1:0]
   EMPTY  : w_ptr     == r_ptr
```

- Single clock domain, pointer width = `N+1` bits (extra MSB resolves
  the full/empty ambiguity instead of wasting a memory slot)
- Verilog RTL, currently exercised with directed testbenches
- Formal/constrained-random verification: **not yet done** — noted
  as a next step, not claimed as complete

<br>

## `> toolbox`

**RTL / Digital Design**
`Verilog` · `FSM Design` · `Digital Logic` — Familiar
`RTL Verification` — Learning

**FPGA**
`RTL-to-Gate Flow Concepts` — Learning
`Synthesis Fundamentals` — Exploring

**Embedded / Software**
`C` · `Git` — Familiar
`Embedded C` · `Linux` — Exploring

**Hardware**
`PCB Design` · `KiCad` — Exploring
`Control Systems` · `Instrumentation` — Learning (HAL CBT prep)

<br>

## `> focus_level` (self-assessed, not a benchmark)

```
DIGITAL DESIGN     [██████████████░░░░░░]  
VERILOG            [████████████░░░░░░░░]  
RTL DESIGN         [███████████░░░░░░░░░]  
FPGA               [████████░░░░░░░░░░░░]  
VERIFICATION       [██████░░░░░░░░░░░░░░]  
CONTROL SYSTEMS    [███████░░░░░░░░░░░░░]  
```

<br>

## `> pipeline`

```
IDEA → SPEC → RTL ARCHITECTURE → VERILOG → SIMULATION
     → VERIFICATION → SYNTHESIS → FPGA → HARDWARE
```

<br>

## `> roadmap`

| # | Project | Status |
|---|---------|--------|
| 01 | Synchronous FIFO | `IN PROGRESS` |
| 02 | Asynchronous FIFO (CDC, Gray-coded pointers) | `PLANNED` |
| 03 | UART Transceiver | `PLANNED` |
| 04 | SPI Controller | `PLANNED` |
| 05 | I²C Controller | `PLANNED` |
| 06 | FSM-Based Controllers | `PLANNED` |
| 07 | Small FPGA Digital System | `PLANNED` |
| 08 | RTL Verification Practice (assertions/coverage) | `PLANNED` |

<br>

## `> boot_log` — last simulation run

```
[ 0.00 ns ]  reset asserted ................ rst = 1
[10.00 ns ]  reset released ................ rst = 0
[15.00 ns ]  clock domain locked ........... clk = OK
[20.00 ns ]  write enable observed ......... wr_en = 1
[25.00 ns ]  fifo not empty ................ empty = 0
[40.00 ns ]  fifo full flag ................ full  = 1
[55.00 ns ]  read enable observed .......... rd_en = 1
[60.00 ns ]  pointers converge ............. empty = 1
[ END ]      simulation halted, no assertion failures logged
```

<br>

## `> telemetry`

<div align="center">
<img height="165" src="https://github-readme-stats.vercel.app/api?username=YOUR_GITHUB_USERNAME&show_icons=true&theme=dark&hide_border=true&bg_color=0D1117&title_color=00E5FF&icon_color=00E5FF&text_color=C9D1D9" />
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=YOUR_GITHUB_USERNAME&layout=compact&theme=dark&hide_border=true&bg_color=0D1117&title_color=00E5FF&text_color=C9D1D9" />
</div>

<br>

## `> uplink`

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/siddartha-l-75120738a/)
[![Email](https://img.shields.io/badge/Email-00E5FF?style=for-the-badge&logo=gmail&logoColor=black)](mailto:siddarthalokesh@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/siddarthalokesh)

</div>

<br>

```verilog
always @(posedge clk) begin
  learn  <= 1'b1;
  build  <= 1'b1;
  debug  <= ~debug;
end
```

<div align="center">
<sub>SYSTEM STATUS: ONLINE — LAST SYNTHESIZED FOR HUMAN REVIEW</sub>
</div>
