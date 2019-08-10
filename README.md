# Documentação para a Importação de Anúncios da OLX Brasil

A OLX hoje suporta dois tipos de importação de anúncios, para anunciantes que querem gerenciar seus anúncios a partir de um software terceiro (ou seja, sem passar pelas interfaces nativas da OLX para gestão de inventário): via API ou via arquivo (JSON ou XML).


## Status das Integrações da OLX

| Modelo de Integração | Versão em produção | Categorias atendidas | Próximos passos |
|----------------------|----------------------------|----------------------|---------------------------------------------------------------------------------------|
| API | Deprecada | Autos e Imóveis | Nova versão que suporta todas as categorias em desenvolvimento, com rollout iminente. |
| [JSON](https://github.com/olxbr/ad_integration/blob/master/json/readme.md) | Estável | Todas as categorias | Escrever documentação de categorias não-documentadas. |
| [XML](https://github.com/olxbr/ad_integration/blob/master/xml/real_estate/readme.md) | Estável | Imóveis | Nenhuma evolução prevista. |


## Status das Integrações da OLX

Nem todas as categorias de anúncios na OLX são suportadas pelas integrações existentes:

| Categoria | Subcategoria | JSON | XML | API |
|-------------------------|-----------------------------------------|------|-----|-----|
| Imóveis | Apartamentos | Sim* | Sim | Sim** |
| Imóveis | Casas | Sim* | Sim | Sim** |
| Imóveis | Aluguel de quartos | Sim* | Não | Não** |
| Imóveis | Temporada | Sim* | Sim | Sim** |
| Imóveis | Terrenos sítios e fazendas | Sim* | Sim | Sim** |
| Imóveis | Comércio e indústria | Sim* | Sim | Sim** |
| Autos e peças | Carros vans e utilitários | Sim* | Não | Sim** |
| Autos e peças | Motos | Sim* | Não | Sim** |
| Autos e peças | Ônibus | Sim* | Não | Não** |
| Autos e peças | Caminhões | [Sim](https://github.com/olxbr/ad_integration/master/blob/json/auto/readme.md) | Não | Não** |
| Autos e peças | Barcos e aeronaves | Sim* | Não | Não** |
| Peças e acessórios | Carros vans e utilitários | [Sim](https://github.com/olxbr/ad_integration/master/blob/json/autoparts/readme.md) | Não | Não** |
| Peças e acessórios | Motos | [Sim](https://github.com/olxbr/ad_integration/master/blob/json/autoparts/readme.md) | Não | Não** |
| Peças e acessórios | Ônibus | [Sim](https://github.com/olxbr/ad_integration/master/blob/json/autoparts/readme.md) | Não | Não** |
| Peças e acessórios | Caminhões | [Sim](https://github.com/olxbr/ad_integration/master/blob/json/autoparts/readme.md) | Não | Não** |
| Peças e acessórios | Barcos e aeronaves | [Sim](https://github.com/olxbr/ad_integration/master/blob/json/autoparts/readme.md) | Não | Não** |
| Para a sua casa | Móveis | Sim* | Não | Não** |
| Para a sua casa | Eletrodomésticos | Sim* | Não | Não** |
| Para a sua casa | Materiais de construção e jardim | Sim* | Não | Não** |
| Para a sua casa | Utilidades domésticas | Sim* | Não | Não** |
| Para a sua casa | Objetos de decoração | Sim* | Não | Não** |
| Eletrônicos e celulares | Videogames | Sim* | Não | Não** |
| Eletrônicos e celulares | Computadores e acessórios | Sim* | Não | Não** |
| Eletrônicos e celulares | Celulares e telefonia | Sim* | Não | Não** |
| Eletrônicos e celulares | Áudio TV vídeo e fotografia | Sim* | Não | Não** |
| Música e hobbies | Instrumentos musicais | Sim* | Não | Não** |
| Música e hobbies | CDs DVDs etc | Sim* | Não | Não** |
| Música e hobbies | Livros e revistas | Sim* | Não | Não** |
| Música e hobbies | Antiguidades | Sim* | Não | Não** |
| Música e hobbies | Hobbies e coleções | Sim* | Não | Não** |
| Esportes e lazer | Esportes e ginástica | Sim* | Não | Não** |
| Esportes e lazer | Ciclismo | Sim* | Não | Não** |
| Artigos infantis |  | Sim* | Não | Não** |
| Animais de estimação | Cachorros e acessórios | Sim* | Não | Não** |
| Animais de estimação | Gatos e acessórios | Sim* | Não | Não** |
| Animais de estimação | Cavalos e acessórios | Sim* | Não | Não** |
| Animais de estimação | Aquários e acessórios | Sim* | Não | Não** |
| Animais de estimação | Roedores e acessórios | Sim* | Não | Não** |
| Animais de estimação | Outros animais e acessórios | Sim* | Não | Não** |
| Moda e beleza | Beleza e saúde | Sim* | Não | Não** |
| Moda e beleza | Roupas e calçados | Sim* | Não | Não** |
| Moda e beleza | Bolsas malas e mochilas | Sim* | Não | Não** |
| Moda e beleza | Bijouterias relógios e acessórios | Sim* | Não | Não** |
| Agro e indústria | Tratores e máquinas agrícolas | [Sim](https://github.com/olxbr/ad_integration/master/blob/json/agro/readme.md) | Não | Não** |
| Agro e indústria | Máquinas pesadas para construção | [Sim](https://github.com/olxbr/ad_integration/master/blob/json/agro/readme.md) | Não | Não** |
| Agro e indústria | Máquinas para produção industrial | [Sim](https://github.com/olxbr/ad_integration/master/blob/json/agro/readme.md) | Não | Não** |
| Agro e indústria | Peças para tratores e máquinas | [Sim](https://github.com/olxbr/ad_integration/master/blob/json/agro/readme.md) | Não | Não** |
| Agro e indústria | Animais para agropecuária | [Sim](https://github.com/olxbr/ad_integration/master/blob/json/agro/readme.md) | Não | Não** |
| Agro e indústria | Produção Rural | [Sim](https://github.com/olxbr/ad_integration/master/blob/json/agro/readme.md) | Não | Não** |
| Agro e indústria | Outros itens para agro e indústria | [Sim](https://github.com/olxbr/ad_integration/master/blob/json/agro/readme.md) | Não | Não** |
| Comércio e escritório | Equipamentos e mobiliário | Sim* | Não | Não** |
| Comércio e escritório | Trailers e carrinhos comerciais | Sim* | Não | Não** |
| Comércio e escritório | Outros itens para comércio e escritório | Sim* | Não | Não** |
| Serviços |  | Sim* | Não | Não** |
| Vagas de emprego |  | Sim* | Não | Não** |

`*` A OLX suporta atualmente integração via JSON para essa categoria, mas a documentação ainda não está atualizada. Se deseja integrar com essa categoria, entre em contato com suporterintegrador@olxbr.com ou abra uma issue nesse repositório.<br>
`**` Uma nova versão da API de Integração da OLX está em desenvolvimento, com rollout iminente.

### Integração via Arquivo (JSON ou XML)

Para integração via Arquivo, temos dois formatos diferentes: JSON e XML. O formato JSON suporta qualquer categoria na OLX, enquanto XML é um formato específico para a Categoria `Imóveis`.

A documentação para essas integrações está a seguir:

- [Importação de Anúncios via Arquivo JSON (Todas as Categorias)](https://github.com/olxbr/ad_integration/blob/master/docs/json.md)
- [Importação de Anúncios via Arquivo XML (Categoria Imóveis)](https://github.com/olxbr/ad_integration/blob/master/docs/xml.md)<br>


### Integração via API

Atualmente a OLX tem uma API para integração, que suporta apenas as categorias `Imóveis`, `Carros, vans e utilitários` e `Motos`. Uma nova versão está em desenvolvimento e será publicada aqui assim que disponível.

Para ter informações sobre a integração via API atual (chamada de Autoupload), contate suporteintegrador@olxbr.com.


## Dúvidas, sugestões e comentários

Caso você queria um suporte para sua integração, pode enviar email para suporteintegrador@olxbr.com.

Ou você pode [abrir uma Issue neste repo](https://github.com/olxbr/ad_integration/issues), que a equipe técnica da OLX vai olhar e responder a issue.

**Importante**: Esta documentação está focada na importação de anúncios para o portal OLX Brasil. Para importação de anúncios para os portais Autoshift e Storia Imóveis, contate suporteintegrador@olxbr.com.
