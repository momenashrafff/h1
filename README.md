<rule id="200185" level="12">
  <if_sid>200111</if_sid>
  <field name="audit.execve.a0">unzip</field>
  <field name="audit.execve.a1">.jpg$|.png$</field>
  <description>Detects extracting of zip file from image file.</description>
  <mitre><id>T1027</id></mitre>
  <group>execve</group>
</rule>
