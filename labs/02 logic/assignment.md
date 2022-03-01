# Lab 2: Zelený Tomáš

### 2-bit comparator

1. Karnaugh maps for other two functions:

   Greater than:

   ![274652731_553538739034140_3645315653057985101_n](https://user-images.githubusercontent.com/99410667/156212571-f111e99d-ac44-4b27-9926-9dc647dd76fa.jpg)

   Less than:

   ![274969257_1097822634396374_1203347837643319715_n](https://user-images.githubusercontent.com/99410667/156212767-b5368c10-f9e0-4579-8a76-6865cc51f55b.jpg)


2. Equations of simplified SoP (Sum of the Products) form of the "greater than" function and simplified PoS (Product of the Sums) form of the "less than" function.

   ![274974552_454818166330327_4191378304551397780_n](https://user-images.githubusercontent.com/99410667/156212857-fbf461c3-1429-43c4-baea-66db385d22dc.jpg)
   ![274756341_1287565041764924_1562618091103868369_n](https://user-images.githubusercontent.com/99410667/156212872-ed27f489-3324-47bf-8a1b-8a7caa914e06.jpg)


### 4-bit comparator

1. Listing of VHDL stimulus process from testbench file (`testbench.vhd`) with at least one assert (use BCD codes of your student ID digits as input combinations). Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

   Last two digits of my student ID: **230353**

```vhdl
    p_stimulus : process
    begin
        -- Report a note at the beginning of stimulus process
        report "Stimulus process started" severity note;

        -- First test case
        s_b <= "0101"; -- Digit 5
        s_a <= "0011"; -- Digit 3
        wait for 100 ns;
        -- Expected output
        assert ((s_B_greater_A = '1') and
                (s_B_equals_A  = '0') and
                (s_B_less_A    = '0'))
        -- If false, then report an error
        report "Input combination COMPLETE_THIS_TEXT FAILED" severity error;

        -- Report a note at the end of stimulus process
        report "Stimulus process finished" severity note;
        wait;
    end process p_stimulus;
```

2. Text console screenshot during your simulation, including reports.

   ![your figure]()

3. Link to your public EDA Playground example:

   [https://www.edaplayground.com/...](https://www.edaplayground.com/...)
