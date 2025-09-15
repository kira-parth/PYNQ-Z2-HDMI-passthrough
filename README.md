# PYNQ-Z2-HDMI-passthrough
This project implements HDMI passthrough functionality on the PYNQ-Z2 board, allowing you to:
  1.Receive HDMI input and pass it through to HDMI output
  2. Convert video signals to AXI4-Stream format for processing
  3. Integrate Test Pattern Generator (TPG) and Video DMA (VDMA)
      Process 1080p video in real-time
# You need ips ad this ip in vivado from this github https://github.com/Xilinx/PYNQ
# Vivado Block Design
  ZYNQ7 Processing System
First, set up the ZYNQ7 Processing System and run "Run Block Automation"—the default settings are sufficient.

<img width="740" height="465" alt="image" src="https://github.com/user-attachments/assets/b02951dc-c86c-4bba-99de-c11874dfb699" />

Next, add the RGB to DVI Video Encoder and the DVI to RGB Video Decoder ip's.
# RGB to DVI Video Encoder
For the HDMI TX function, the serial clock is generated from the internal pixel clock and configured for 1080p.

# DVI to RGB Video Decoder
The DDC ROM offers preset resolution options, specifically the four resolutions listed below, and we also select 1080p.

# Clocking Wizard
Since the DVI to RGB Video Decoder's refclk requires 200MHz, we configured a 200MHz output using the Clocking Wizard.
<img width="740" height="539" alt="image" src="https://github.com/user-attachments/assets/4653ec6b-8f08-4f22-8822-9bf7a7266541" />

# IP Connection
Next, we can proceed with the preliminary connections of the various IP cores and the configuration of the input/output ports.
<img width="740" height="422" alt="image" src="https://github.com/user-attachments/assets/43be61d3-6b67-43dc-a04c-045ee7f3f5ae" />

# Add the xdc file and result is shown below 
<img width="740" height="234" alt="image" src="https://github.com/user-attachments/assets/db8c2c77-a4a3-48bb-a5f5-cc6b278104dd" />


