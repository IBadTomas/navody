# Vlastní IP - Minecraft serveru

## **Přehled**

V tomto návodě vám ukážu jak si nastavit DNS záznamy u domény tak aby jste měli vlastní doménu na vašem serveru. 178.211.151.211:25565 --&gt; play.mujserver.eu

## **Požadavky:**

1. Zakoupený minecraft server  
2. Zakoupenou doménu u jakéhokoliv registrátora domén

## Postup:

1. Zkopírujte IP adresu _\(`dsX.batcore.eu` - místo X zadáte váš ds server.\)_ z herní administrace - **BEZ PORTU!** \(V tomto případě `ds2.batcore.eu`\)

![](../.gitbook/assets/image%20%283%29.png)

1. U registrátora domény **vytvořte** nový **DNS záznam** typu **CNAME**. Do názvu napište jméno subdomény \(Já použiju např. "play"\). 

Do "**Data:**" **vložte IP adresu**, kterou jste v předešlém kroku zkopírovali. Poté **klikněte** na **uložit záznam**.

![](../.gitbook/assets/image%20%284%29.png)

1. U registrátora domény **vytvořte** další **DNS záznam** typu **SRV**. Do názvu napište `_minecraft._tcp.vase_sub_domena` _\(V mém případě `_minecraft._tcp.play`\)._

Do "Data:" napište `0 5 port_vaseho_serveru vase_konecna_domena` \(V mém případě `0 5 25800 play.lukariosmen.eu`\) . Poté **klikněte** na **uložit záznam**.

\(V případě kdy využíváte jiného registrátora domén, který nemá možnost "Data" tak napište:  
Priority: `0` \| váha \(Weight\): `5` \| Port: `Port_serveru` \| Target: `Finální doména`.\)

![](../.gitbook/assets/image%20%285%29.png)

1. Poté stačí zmáčknout nahoře tlačítko "Aplikovat změny" a máte hotovo! Nyní se můžete na váš server připojit pomocí vaši domény. \(V mém případě `play.lukariosmen.eu`\)

{% hint style="danger" %}
### Po nastavení DNS záznamů, může chvíli trvat než se budete moct připojit přes doménu na váš server. \(Až 1 hodinu\)
{% endhint %}

