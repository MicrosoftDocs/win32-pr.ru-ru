---
title: Ошибка метки ARIA
description: Ошибка метки ARIA
ms.assetid: DF45E38D-9AD3-48C8-911E-8C6233F17F43
keywords:
- ариалабелеррорид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1091c46dbb660c4c3568d24bfca34d94ef869f1e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "104070790"
---
# <a name="aria-label-error"></a>Ошибка метки ARIA

## <a name="text"></a>Текст

Элемент имеет тип **input**, **Button**, **Image-Button** или **ориентир** , но не имеет доступного имени.

## <a name="type"></a>Тип

Ошибка

## <a name="description"></a>Описание

Эта ошибка относится к следующим:

-   Поля ввода формы:
    -   HTML-теги **: input \[ Type = "Text \| password \| CheckBox \| \| File \| e-mail \| Tel \| Color \| Date \| DateTime \| -местного \| времени \| неделя \| номер месяца \| диапазон номеров месяцев для \| \| поиска \| \]**, **SELECT**, **DataList** и **textarea**.
    -   ОЖИДАТЬ-ARIA Roles —**CheckBox**, **ComboBox**, **ListBox**, **RadioGroup**, **Radio**, **TextBox**, **дерево**, **ползунок** и **спинбуттон**.
-   Изображения/кнопки изображения/кнопки
    -   HTML-теги —**img**, **input \[ Type = " \| кнопка изображения \] "** и **кнопка**.
    -   ОЖИДАТЬ — роли ARIA —**img** и **Button**.
-   Ориентиры
    -   ОЖИДАТЬ-ARIA Roles —**регион**, **баннер**, **дополнение**, **контентинфо**, **форма**, **Главная**, **Навигация** и **Поиск**.

> [!Note]  
> Аккчеккер отображает эту ошибку даже для элементов, для которых доступное имя задано по умолчанию на основе внутреннего содержимого HTML (см. элемент **баннера** в приведенном выше примере). В таких случаях эти ошибки можно отключить.

 

Все семантически важные элементы пользовательского интерфейса, такие как поля формы (например, **входные данные**, **SELECT**, **textarea**), изображения, кнопки и ориентиры (Теги, представляющие логические регионы), должны иметь доступное имя, чтобы средства чтения с экрана могли правильно объявлять их.

Чтобы устранить эту ошибку, задайте доступное имя одним из следующих способов (перечисленных в порядке предпочтения).

-   Поля формы: Используйте тег **Label** и присвойте атрибуту **for** значение **идентификатора** целевого поля.
-   Кнопка "изображение/изображение": Задайте атрибут **ALT** .
-   Кнопки: Задайте текст заголовка для кнопки.
-   Для любого элемента:
    -   [**ARIA — атрибут лабелледби**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) : задайте значение **идентификатора** элемента, содержащего строку с доступным именем.
    -   [**ARIA — атрибут Label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) : Укажите строку с доступным именем.
    -   атрибут [**Title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) : Укажите строку с доступным именем (также можно создать **подсказку**).

## <a name="example"></a>Пример


```HTML
<!-- For landmark tags, set the accessible name by using the aria-labelledby 
attribute to reference the visible headers. -->
<h1 id="formHeader">Application Form</h1>
<form aria-labelledby="formHeader">

  <!-- For input fields, use the LABEL tag with the for attribute. -->
  <label for="fullName">Full Name</label>
  <input id="fullName" type="text" />

  <!-- If there is no visible text that can be referenced, set the accessible 
  name by using aria-label or title attributes. -->
  <input type="file" aria-label="Your photo"/>

  <!-- For images, use the alt attribute. -->
  <img src="…" alt="Uploaded photo" />

  <!-- For buttons, caption text is also used as the accessible name. -->
  <button onclick="processForm()">Send</button>

  <!-- For image buttons, use the alt attribute to define the accessible name. -->
  <input type="image" src="images/moreinfo.png" alt="Show more info"/>

  <!-- For elements with inner text this error can be suppressed because the 
  accessible name is set by default. -->
  <div role="banner">Accessible name set by default</div>
</form >
```



 

 




