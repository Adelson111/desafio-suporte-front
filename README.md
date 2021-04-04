## Etapas concluídas

- [x] Parte 1 - Manipulando o DOM
	- [x] 1. Adicione um ícone para Youtube no header apontando para
	- [ ] 2. Modifique o comportamento do menu Whatsapp
    - [x] 3. Modifique o formulário de "Estou Interessado"
    	- [x] 1 Select com as opções: SUV, Senda, Hatch e Pickup
    	- [x] 1 Textarea com placeholder "Mensagem"
	- [ ] 4. Exiba um modal com o escudo do Palmeiras
- [x] Parte 2 - Montando Layouts

-----------

### Parte 1 - Manipulando o DOM

#### 1. Adicione um ícone para Youtube no header
- - - - - - - - - - - - - - - - - - - - - - - - -

	// Seleciona o elemento no DOM
	pai = document.querySelector('.header__networks-list');
	// Seleciona o último filho do elemento
	ultimoFilho = pai.lastChild;
	// Cria tag "a"
	tagA = document.createElement('a');
	tagA.setAttribute('href', 'https://www.youtube.com/channel/UCLI4tg1oh_oLiJJteExJdUQ');
	tagA.setAttribute('target', '_blank');
	// Cria tag "i"
	tagI = document.createElement('i');
	tagI.setAttribute('class', 'icon icon-youtube-header icon--small icon--hover-youtube');
	// Insere a tag "a" na tag "i"
	tagA.appendChild(tagI);
	// Insere a tag "a" depois do último elemento
	pai.insertBefore(tagA, ultimoFilho.nextSibling);

#### 3. Modifique o formulário de "Estou Interessado"
- - - - - - - - - - - - - - - - - - - - - - - - -

> 1 Select com as opções: SUV, Senda, Hatch e Pickup;

	pai = document.querySelector('.form-conversion__body').firstElementChild.firstElementChild;
	pai.insertAdjacentHTML('afterend', '<div class="form-group"><div><select class="form-select" aria-label="Default select example" style="width: 100%; font-size: .875rem; height: 50px; border-radius: .25rem; padding: 10px;"><option selected>SUV</option><option value="1">Senda</option><option value="2">Hatch</option><option value="3">Pickup</option></select></div></div>');


> 1 Textarea com placeholder "Mensagem".

	tag = document.createElement('div');
	tag.setAttribute('class', 'form-group');
	tag.innerHTML = '<textarea class="form-control" name="menssage" required="" type="text" data-bouncer-target="#invalid-menssage" placeholder="Mensagem"></textarea><div id="invalid-menssage" class="invalid-feedback"></div>';
	pai = document.querySelector('.form-conversion__body').firstElementChild;
	pai.insertBefore(tag, pai.lastElementChild.nextSibling);



### Parte 2 - Montando Layouts

Se encontra no arquivo acima.



