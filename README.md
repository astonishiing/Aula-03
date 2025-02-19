## Modificadores de visibilidade
- Indica o nível de acesso aos componentes internos de uma classe (atributo e métodos)
- A visibilidade padrão do JAVA é públic para pacote ou simplesmente pública (public)
- Você so irá ter problema com isso caso trabalhe com mais de um pacote e nao coloca a visibilidade


## Simbolos  que indicam a visibilidade
```
+ Pública (public)
- Privado (private)
# Protedgido (protected)
```
-------------------------------------------------------------------------------------------------------------------------------------------------
Pública: a classe atual e todas as outras classes, possam ter acesso a ela
(Classe Caneta)
```
c1.cor = "Azul";
```
> Neste caso ira dar CERTO, pois cor tem acesso public a Classe Caneta
-------------------------------------------------------------------------------------------------------------------------------------------------
Privado: No meu método Main eu nao consigo manipular os atributos nem métodos ditos PRIVADOS, somente na **classe atual**
```
c1.ponta = 0.5f;
```
> Neste caso irá dar um [ERROR], pois ponta tem acesso privado a Classe Caneta
-------------------------------------------------------------------------------------------------------------------------------------------------
Protegido: A classe atual e todas as suas sub-classes (herança)

<sup>o código citado abaixo não pertence ao programa, porém pode ser adicionado sem riscos</sup>
```
c1.carga = 80;
```
> Irá dar certo pois a Classe Main esta dentro de uma classe que está utilizando a Classe Caneta

> Então dentro do método "Main" dentro da Classe Main, que esta utilizando um objeto c1 que é uma caneta

> Com isso ele ira deixar manipular um atributo protegido, porque ele está dentro de uma Classe que utiliza a Classe Caneta
```
public class Main {
    public static void main(String[] args) {
        Caneta c1 = new Caneta();
        c1.carga = 80
        c1.status();
    }
}
```
*@astonishiing*

