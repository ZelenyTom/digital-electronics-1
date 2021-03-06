# Lab 5: Tomáš Zelený

### Flip-flops

1. Listing of VHDL architecture for T-type flip-flop. Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

```vhdl
architecture Behavioral of t_ff_rst is
    signal s_q : std_logic;
begin
    --------------------------------------------------------
    -- p_d_ff_rst:
    -- D type flip-flop with a high-active sync reset,
    -- rising-edge clk.
    -- q(n+1) = d
    --------------------------------------------------------
    p_d_ff_rst : process(clk)
    begin
        if rising_edge(clk) then  -- Synchronous process
                if (rst = '1')then
                
                    q <= '0';
                    q_bar <= '1';  
                    s_q <= '0';              
                
                else
                    s_q <= (not t and s_q) or ( t and not s_q);
                    
                    q <= s_q;
                    q_bar <= not s_q;
                end if;
        end if;
    end process p_d_ff_rst;
end architecture Behavioral;
```

2. Screenshot with simulated time waveforms. Try to simulate both flip-flops in a single testbench with a maximum duration of 200 ns, including reset. Always display all inputs and outputs (display the inputs at the top of the image, the outputs below them) at the appropriate time scale!

   ![image](https://user-images.githubusercontent.com/99410667/157691922-9a770a4b-bbc5-4ec2-bfa9-a127e28fb9e9.png)

### Shift register

1. Image of the shift register `top` level schematic. The image can be drawn on a computer or by hand. Always name all inputs, outputs, components and internal signals!

   ![275730017_659250028623073_573677874164846580_n](https://user-images.githubusercontent.com/99410667/158609609-616915f2-174a-49bc-b8a3-67d159f0c386.jpg)

