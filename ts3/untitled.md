# Vlastní IP - TS3

## Přehled

V tomto návodě vám ukážu jak si nastavit DNS záznamy u domény tak aby jste měli vlastní doménu na vašem ts3 serveru. 178.26.96.231:25565 --&gt; ts3.mujserver.eu

## Požadavky:

1. Vlastnit ts3 server  
2. Zakoupenou doménu u jakéhokoliv registrátora domén

## Postup:

1. Zkopírujte IP adresu \(dsX.batcore.eu - místo X zadáte váš ds server.\) z herní administrace - **BEZ PORTU**! \(V tomto případě ds6.batcore.eu\)

![](../.gitbook/assets/image%20%2814%29.png)

1. U registrátora domény **vytvořte** nový **DNS záznam** typu **CNAME**. Do názvu napište jméno subdomény \(Já použiju např. "ts3"\). Do "**Data:**" **vložte IP adresu**, kterou jste v předešlém kroku zkopírovali. Poté **klikněte** na **uložit záznam**.

![](../.gitbook/assets/image%20%2815%29.png)

1. U registrátora domény **vytvořte** další **DNS záznam** typu **SRV**. Do názvu napište "\_ts3.\_udp.vase\_sub\_domena" \(V mém případě "\_ts3.\_udp.ts3"\).

Do "**Data:**" napište "0 1 port\_vaseho\_serveru vase\_konecna\_domena" \(V mém případě "0 1 25700 ts3.lukariosmen.eu"\) . Poté **klikněte** na **uložit záznam**.

![](../.gitbook/assets/image%20%2813%29.png)

1. Poté stačí zmáčknout nahoře tlačítko "Aplikovat změny" a máte hotovo! Nyní se můžete na váš server připojit pomocí vaši domény. \(V mém případě ts3.lukariosmen.eu\)

### **POZOR! Po nastavení DNS záznamů, může chvíli trvat než se budete moct připojit přes doménu na váš server. \(Až 1 hodinu\)**

