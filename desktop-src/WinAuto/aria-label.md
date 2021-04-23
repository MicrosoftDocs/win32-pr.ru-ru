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
# <a name="aria-label-error"></a><span data-ttu-id="7b51f-104">Ошибка метки ARIA</span><span class="sxs-lookup"><span data-stu-id="7b51f-104">ARIA Label Error</span></span>

## <a name="text"></a><span data-ttu-id="7b51f-105">Текст</span><span class="sxs-lookup"><span data-stu-id="7b51f-105">Text</span></span>

<span data-ttu-id="7b51f-106">Элемент имеет тип **input**, **Button**, **Image-Button** или **ориентир** , но не имеет доступного имени.</span><span class="sxs-lookup"><span data-stu-id="7b51f-106">Element is of type **input**, **button**, **image-button** or **landmark** but doesn't have an accessible name.</span></span>

## <a name="type"></a><span data-ttu-id="7b51f-107">Тип</span><span class="sxs-lookup"><span data-stu-id="7b51f-107">Type</span></span>

<span data-ttu-id="7b51f-108">Ошибка</span><span class="sxs-lookup"><span data-stu-id="7b51f-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="7b51f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="7b51f-109">Description</span></span>

<span data-ttu-id="7b51f-110">Эта ошибка относится к следующим:</span><span class="sxs-lookup"><span data-stu-id="7b51f-110">This error applies to:</span></span>

-   <span data-ttu-id="7b51f-111">Поля ввода формы:</span><span class="sxs-lookup"><span data-stu-id="7b51f-111">Form input fields:</span></span>
    -   <span data-ttu-id="7b51f-112">HTML-теги **: input \[ Type = "Text \| password \| CheckBox \| \| File \| e-mail \| Tel \| Color \| Date \| DateTime \| -местного \| времени \| неделя \| номер месяца \| диапазон номеров месяцев для \| \| поиска \| \]**, **SELECT**, **DataList** и **textarea**.</span><span class="sxs-lookup"><span data-stu-id="7b51f-112">HTML tags—**input\[type= "text\|password\|checkbox\|radio\|file\|email\|tel\|color\|date\|datetime\|datetime-local\|time\|week\|month\|number\|range\|search\|url"\]**, **select**, **datalist**, and **textarea**.</span></span>
    -   <span data-ttu-id="7b51f-113">ОЖИДАТЬ-ARIA Roles —**CheckBox**, **ComboBox**, **ListBox**, **RadioGroup**, **Radio**, **TextBox**, **дерево**, **ползунок** и **спинбуттон**.</span><span class="sxs-lookup"><span data-stu-id="7b51f-113">WAI-ARIA roles—**checkbox**, **combobox**, **listbox**, **radiogroup**, **radio**, **textbox**, **tree**, **slider**, and **spinbutton**.</span></span>
-   <span data-ttu-id="7b51f-114">Изображения/кнопки изображения/кнопки</span><span class="sxs-lookup"><span data-stu-id="7b51f-114">Images/image buttons/ buttons</span></span>
    -   <span data-ttu-id="7b51f-115">HTML-теги —**img**, **input \[ Type = " \| кнопка изображения \] "** и **кнопка**.</span><span class="sxs-lookup"><span data-stu-id="7b51f-115">HTML tags—**img**, **input\[type="image\|button"\]**, and **button**.</span></span>
    -   <span data-ttu-id="7b51f-116">ОЖИДАТЬ — роли ARIA —**img** и **Button**.</span><span class="sxs-lookup"><span data-stu-id="7b51f-116">WAI-ARIA roles—**img** and **button**.</span></span>
-   <span data-ttu-id="7b51f-117">Ориентиры</span><span class="sxs-lookup"><span data-stu-id="7b51f-117">Landmarks</span></span>
    -   <span data-ttu-id="7b51f-118">ОЖИДАТЬ-ARIA Roles —**регион**, **баннер**, **дополнение**, **контентинфо**, **форма**, **Главная**, **Навигация** и **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="7b51f-118">WAI-ARIA roles—**region**, **banner**, **complementary**, **contentinfo**, **form**, **main**, **navigation**, and **search**.</span></span>

> [!Note]  
> <span data-ttu-id="7b51f-119">Аккчеккер отображает эту ошибку даже для элементов, для которых доступное имя задано по умолчанию на основе внутреннего содержимого HTML (см. элемент **баннера** в приведенном выше примере).</span><span class="sxs-lookup"><span data-stu-id="7b51f-119">AccChecker shows this error even for elements for which the accessible name is set by default based on inner HTML content (see the **banner** element in the above example).</span></span> <span data-ttu-id="7b51f-120">В таких случаях эти ошибки можно отключить.</span><span class="sxs-lookup"><span data-stu-id="7b51f-120">For these cases, you can suppress this errors.</span></span>

 

<span data-ttu-id="7b51f-121">Все семантически важные элементы пользовательского интерфейса, такие как поля формы (например, **входные данные**, **SELECT**, **textarea**), изображения, кнопки и ориентиры (Теги, представляющие логические регионы), должны иметь доступное имя, чтобы средства чтения с экрана могли правильно объявлять их.</span><span class="sxs-lookup"><span data-stu-id="7b51f-121">All semantically important UI elements such as form fields (for example, **input**, **select**, **textarea**), images, buttons and landmarks (tags representing logical regions) must have the accessible name to allow screen readers to correctly announce them.</span></span>

<span data-ttu-id="7b51f-122">Чтобы устранить эту ошибку, задайте доступное имя одним из следующих способов (перечисленных в порядке предпочтения).</span><span class="sxs-lookup"><span data-stu-id="7b51f-122">To fix this error, set the accessible name in one of the following ways (listed in the order of preference).</span></span>

-   <span data-ttu-id="7b51f-123">Поля формы: Используйте тег **Label** и присвойте атрибуту **for** значение **идентификатора** целевого поля.</span><span class="sxs-lookup"><span data-stu-id="7b51f-123">Form fields: Use the **label** tag and set the **for** attribute to the **id** value of the target field.</span></span>
-   <span data-ttu-id="7b51f-124">Кнопка "изображение/изображение": Задайте атрибут **ALT** .</span><span class="sxs-lookup"><span data-stu-id="7b51f-124">Image/image button: Set the **alt** attribute.</span></span>
-   <span data-ttu-id="7b51f-125">Кнопки: Задайте текст заголовка для кнопки.</span><span class="sxs-lookup"><span data-stu-id="7b51f-125">Buttons: Set the button caption text.</span></span>
-   <span data-ttu-id="7b51f-126">Для любого элемента:</span><span class="sxs-lookup"><span data-stu-id="7b51f-126">For any element:</span></span>
    -   <span data-ttu-id="7b51f-127">[**ARIA — атрибут лабелледби**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) : задайте значение **идентификатора** элемента, содержащего строку с доступным именем.</span><span class="sxs-lookup"><span data-stu-id="7b51f-127">[**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute: Set to the **id** value of the element containing the accessible name string.</span></span>
    -   <span data-ttu-id="7b51f-128">[**ARIA — атрибут Label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) : Укажите строку с доступным именем.</span><span class="sxs-lookup"><span data-stu-id="7b51f-128">[**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute: Set to the accessible name string.</span></span>
    -   <span data-ttu-id="7b51f-129">атрибут [**Title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) : Укажите строку с доступным именем (также можно создать **подсказку**).</span><span class="sxs-lookup"><span data-stu-id="7b51f-129">[**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) attribute: Set to the accessible name string (also create a **tooltip**).</span></span>

## <a name="example"></a><span data-ttu-id="7b51f-130">Пример</span><span class="sxs-lookup"><span data-stu-id="7b51f-130">Example</span></span>


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



 

 




