# Nome do projeto

<!---Esses são exemplos. Veja https://shields.io para outras pessoas ou para personalizar este conjunto de escudos. Você pode querer incluir dependências, status do projeto e informações de licença aqui--->

![GitHub repo size](https://img.shields.io/github/repo-size/iuricode/README-template?style=for-the-badge)
![GitHub language count](https://img.shields.io/github/languages/count/iuricode/README-template?style=for-the-badge)
![GitHub forks](https://img.shields.io/github/forks/iuricode/README-template?style=for-the-badge)
![Bitbucket open issues](https://img.shields.io/bitbucket/issues/iuricode/README-template?style=for-the-badge)
![Bitbucket open pull requests](https://img.shields.io/bitbucket/pr-raw/iuricode/README-template?style=for-the-badge)

<img src="exemplo-image.png" alt="exemplo imagem">

> Linha adicional de texto informativo sobre o que o projeto faz. Sua introdução deve ter cerca de 2 ou 3 linhas. Não exagere, as pessoas não vão ler.

### Ajustes e melhorias

O projeto ainda está em desenvolvimento e as próximas atualizações serão voltadas nas seguintes tarefas:

- [x] Tarefa 1
- [x] Tarefa 2
- [x] Tarefa 3
- [ ] Tarefa 4
- [ ] Tarefa 5

## 💻 Pré-requisitos

Antes de começar, verifique se você atendeu aos seguintes requisitos:
<!---Estes são apenas requisitos de exemplo. Adicionar, duplicar ou remover conforme necessário--->
* Você instalou a versão mais recente de `<linguagem / dependência / requeridos>`
* Você tem uma máquina `<Windows / Linux / Mac>`. Indique qual sistema operacional é compatível / não compatível.
* Você leu `<guia / link / documentação_relacionada_ao_projeto>`.

## 🚀 Instalando <nome_do_projeto>

Para instalar o <nome_do_projeto>, siga estas etapas:

Linux e macOS:
```
<comando_de_instalação>
```

Windows:
```
<comando_de_instalação>
```

## ☕ Usando <nome_do_projeto>

Para usar <nome_do_projeto>, siga estas etapas:

```
<exemplo_de_uso>
```

Adicione comandos de execução e exemplos que você acha que os usuários acharão úteis. Fornece uma referência de opções para pontos de bônus!

## 📫 Contribuindo para <nome_do_projeto>
<!---Se o seu README for longo ou se você tiver algum processo ou etapas específicas que deseja que os contribuidores sigam, considere a criação de um arquivo CONTRIBUTING.md separado--->
Para contribuir com <nome_do_projeto>, siga estas etapas:

1. Bifurque este repositório.
2. Crie um branch: `git checkout -b <nome_branch>`.
3. Faça suas alterações e confirme-as: `git commit -m '<mensagem_commit>'`
4. Envie para o branch original: `git push origin <nome_do_projeto> / <local>`
5. Crie a solicitação de pull.

Como alternativa, consulte a documentação do GitHub em [como criar uma solicitação pull](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request).

## 🤝 Colaboradores

Agradecemos às seguintes pessoas que contribuíram para este projeto:

<table>
  <tr>
    <td align="center">
      <a href="#">
        <img src="https://avatars3.githubusercontent.com/u/31936044" width="100px;" alt="Foto do Iuri Silva no GitHub"/><br>
        <sub>
          <b>Iuri Silva</b>
        </sub>
      </a>
    </td>
    <td align="center">
      <a href="#">
        <img src="https://s2.glbimg.com/FUcw2usZfSTL6yCCGj3L3v3SpJ8=/smart/e.glbimg.com/og/ed/f/original/2019/04/25/zuckerberg_podcast.jpg" width="100px;" alt="Foto do Mark Zuckerberg"/><br>
        <sub>
          <b>Mark Zuckerberg</b>
        </sub>
      </a>
    </td>
    <td align="center">
      <a href="#">
        <img src="https://miro.medium.com/max/360/0*1SkS3mSorArvY9kS.jpg" width="100px;" alt="Foto do Steve Jobs"/><br>
        <sub>
          <b>Steve Jobs</b>
        </sub>
      </a>
    </td>
  </tr>
</table>


## 😄 Seja um dos contribuidores<br>

Quer fazer parte desse projeto? Clique [AQUI](CONTRIBUTING.md) e leia como contribuir.

## 📝 Licença

Esse projeto está sob licença. Veja o arquivo [LICENÇA](LICENSE.md) para mais detalhes.

[⬆ Voltar ao topo](#nome-do-projeto)<br>




# Orange workflows for s-SNOM data processing

In this repository you find Orange workflows for processing s-SNOM data. An example dataset including point spectra, spectral linescan and hyperspectral data is provided for educational purposes. All data provided was measured at a synchrotron light source and are a courtesy of F. Feres et al. [1].

## Guidlines for downloading and oppening the examples files:

1. Go to https://github.com/raul-freitas/imbuia_workflows
2. Click on CODE and then Download the ZIP;
   - Download the ZIP;
    - This will take a while, because it is a large file.
   - Select the folder and extract;
   - Open orange;
    - If you do not have orange spectroscopy installed, download [Quasar](https://quasar.codes) or [Orange](https://orangedatamining.com).
   - After running Orange, open the example;
      - File >> Open >> example
   - Now you need to indicate the file, in this example we have the filename and the reference written at the top of the orange desktop;
   - And follow the instructions...

## s-SNOM files types

In this equipament is possible to generate 3 main types of data, with a better descrition of this types in this respective folders.

 - [Point Spectrum](point-spectrum/):

	This is just a spectrum measured in just one position.

	This data has a full spectrum data, wavenumber approximately 600 cm<sup>-1</sup> up to 2000 cm<sup>-1</sup>, but in only one pixel.

 - [Linescan](linescan/):

 	In this case, a full spectrum of each pixel along a path choose is during the experiment.


 - [Hyperspectral Image](hyper/):

 	In the last type is a full spectrum on each pixel inside an area.


![example image](imgs/sample_example.png)


References:

[1] - 'F. H. Feres, R. A. Mayer, L. Wehmeier, F. C. B. Maia, E. R. Viana, A. Malachias, H. A. Bechtel, J. M. Klopf, L. M. Eng, S. C. Kehr, J. C. González, R. O. Freitas, I. D. Barcelos, Nat. Commun. 2021, 12, 1995. DOI: [10.1038/s41467-021-22209-w](https://doi.org/10.1038/s41467-021-22209-w).'

[⬆ Voltar ao topo](#Orange-workflows-for-s-SNOM-data-processing)<br>
