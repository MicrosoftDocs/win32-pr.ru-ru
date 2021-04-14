---
title: Атрибут привязки VML V-Text-Anchor
description: Атрибут привязки VML V-Text-Anchor
ms.assetid: d6e2f60c-5cc7-4340-a9cd-b6c2b0b5b0be
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 603f118a260c8ce9c271128fa642e9e2ae569806
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413313"
---
# <a name="vml-v-text-anchor-attribute"></a><span data-ttu-id="fd866-103">Атрибут привязки VML V-Text-Anchor</span><span class="sxs-lookup"><span data-stu-id="fd866-103">VML V-Text-Anchor Attribute</span></span>

<span data-ttu-id="fd866-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="fd866-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="fd866-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="fd866-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="fd866-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="fd866-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="fd866-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fd866-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="fd866-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="fd866-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="fd866-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="fd866-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="fd866-110">Определяет вертикальную привязку текста в текстовом поле.</span><span class="sxs-lookup"><span data-stu-id="fd866-110">Defines the vertical anchoring of text in a textbox.</span></span> <span data-ttu-id="fd866-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="fd866-111">Read/write.</span></span> <span data-ttu-id="fd866-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="fd866-112">**String**.</span></span>

<span data-ttu-id="fd866-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="fd866-113">**Applies To**</span></span>

[<span data-ttu-id="fd866-114">TextBox</span><span class="sxs-lookup"><span data-stu-id="fd866-114">TextBox</span></span>](msdn-online-vml-textbox-element.md)

<span data-ttu-id="fd866-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="fd866-115">**Tag Syntax**</span></span>

<span data-ttu-id="fd866-116"><v: *элемент* v-Text-Anchor = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="fd866-116"><v: *element* v-text-anchor=" *expression* "></span></span>

<span data-ttu-id="fd866-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="fd866-117">**Remarks**</span></span>

<span data-ttu-id="fd866-118">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="fd866-118">Values include:</span></span>

-   <span data-ttu-id="fd866-119">**Top** (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fd866-119">**top** (default)</span></span>
-   <span data-ttu-id="fd866-120">**отчество**</span><span class="sxs-lookup"><span data-stu-id="fd866-120">**middle**</span></span>
-   <span data-ttu-id="fd866-121">**Нижний**</span><span class="sxs-lookup"><span data-stu-id="fd866-121">**bottom**</span></span>
-   <span data-ttu-id="fd866-122">**сверху по центру**</span><span class="sxs-lookup"><span data-stu-id="fd866-122">**top-center**</span></span>
-   <span data-ttu-id="fd866-123">**посередине по центру**</span><span class="sxs-lookup"><span data-stu-id="fd866-123">**middle-center**</span></span>
-   <span data-ttu-id="fd866-124">**внизу по центру**</span><span class="sxs-lookup"><span data-stu-id="fd866-124">**bottom-center**</span></span>
-   <span data-ttu-id="fd866-125">**сверху — базовый план**</span><span class="sxs-lookup"><span data-stu-id="fd866-125">**top-baseline**</span></span>
-   <span data-ttu-id="fd866-126">**снизу вверх**</span><span class="sxs-lookup"><span data-stu-id="fd866-126">**bottom-baseline**</span></span>
-   <span data-ttu-id="fd866-127">**Верхний Центральный центр — базовый план**</span><span class="sxs-lookup"><span data-stu-id="fd866-127">**top-center-baseline**</span></span>
-   <span data-ttu-id="fd866-128">**Нижняя-Центральная — базовый план**</span><span class="sxs-lookup"><span data-stu-id="fd866-128">**bottom-center-baseline**</span></span>

<span data-ttu-id="fd866-129">Текст будет привязан к вертикальной точке в текстовом поле, как указано в значении атрибута.</span><span class="sxs-lookup"><span data-stu-id="fd866-129">The text will be anchored to a vertical position in the textbox as indicated by the attribute value.</span></span> <span data-ttu-id="fd866-130">Выравнивание привязки к тексту становится очевидном только в том случае, если [MSO-Fit-Text-to-Shape](msdn-online-vml-mso-fit-text-to-shape-attribute.md) имеет **значение false**.</span><span class="sxs-lookup"><span data-stu-id="fd866-130">The alignment of a text anchor only becomes evident if [MSO-Fit-Text-To-Shape](msdn-online-vml-mso-fit-text-to-shape-attribute.md) is **False**.</span></span> <span data-ttu-id="fd866-131">Этот атрибут отличается от атрибута стиля **выравнивания по вертикали** , который используется для идеографических языков.</span><span class="sxs-lookup"><span data-stu-id="fd866-131">This attribute is different from the **Vertical-Align** Style attribute, which is used for ideographic languages.</span></span>

<span data-ttu-id="fd866-132">Этот атрибут используется Microsoft Office для хранения данных в веб-документах, но не отображается в Microsoft Internet Explorer 5 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="fd866-132">This attribute is used by Microsoft Office to store data in Web documents but does not render in Microsoft Internet Explorer 5 or greater.</span></span>

<span data-ttu-id="fd866-133">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="fd866-133">*VML Standard Attribute*</span></span>

<span data-ttu-id="fd866-134">**Пример**</span><span class="sxs-lookup"><span data-stu-id="fd866-134">**Example**</span></span>

<span data-ttu-id="fd866-135">Текст выдается по нижнему краю текстового поля.</span><span class="sxs-lookup"><span data-stu-id="fd866-135">The text is aligned to the bottom of the textbox.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox style="v-text-anchor:bottom" id="mytextbox">
   VML
   </v:textbox/>
   </v:shape>
```



 

 