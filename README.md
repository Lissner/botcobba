# botcobba
<context>
  <input pattern="(hola|hi) *">
    <output value="Hola $UserName!" if="full($UserName)"/>

    <context if="empty($UserName)">
      <output value="Hola! Cual es tu nombre?"/>

      <input pattern="$Text">
        <var name="UserName" value="$Text" scope="user"/>
        <output value="Nice to meet you $UserName!"/>
      </input>

    </context>
  </input>
</context>
