library ieee;
use ieee.std_logic_1164.all;
use ieee.std_logic_arith.all;
use ieee.std_logic_unsigned.all;
 
entity JK_FF is
PORT( J,K,CLOCK: in std_logic;
Q, QB: out std_logic);
end JK_FF;
 
Architecture behavioral of JK_FF is
begin
PROCESS(CLOCK)
variable TMP: std_logic;
begin
if(CLOCK=&#39;1&#39;) then
if(J=&#39;0&#39; and K=&#39;0&#39;)then
TMP:=TMP;
elsif(J=&#39;1&#39; and K=&#39;1&#39;)then
TMP:= not TMP;
elsif(J=&#39;0&#39; and K=&#39;1&#39;)then
TMP:=&#39;0&#39;;
else
TMP:=&#39;1&#39;;
end if;
end if;
Q&lt;=TMP;
QB&lt;=not TMP;
end PROCESS;
end behavioral;
