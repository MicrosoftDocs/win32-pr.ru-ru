---
title: Атрибут src (Вмлфраме) (VML)
description: Атрибут src (Вмлфраме) (VML)
ms.assetid: 6ac7a3b5-3c1d-43a0-ab92-a03e3bd45733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a9c3ec4849098c9469fba56f26d4c3dd514746
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337953"
---
# <a name="src-attribute-vmlframevml"></a><span data-ttu-id="c39e3-103">Атрибут src (Вмлфраме) (VML)</span><span class="sxs-lookup"><span data-stu-id="c39e3-103">Src Attribute (VMLFrame)(VML)</span></span>

<span data-ttu-id="c39e3-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c39e3-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c39e3-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="c39e3-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c39e3-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="c39e3-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c39e3-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c39e3-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c39e3-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c39e3-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c39e3-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c39e3-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c39e3-110">Определяет источник данных для кадра.</span><span class="sxs-lookup"><span data-stu-id="c39e3-110">Defines the source of data for the frame.</span></span> <span data-ttu-id="c39e3-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="c39e3-111">Read/write.</span></span> <span data-ttu-id="c39e3-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="c39e3-112">**String**.</span></span>

<span data-ttu-id="c39e3-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="c39e3-113">**Applies To**</span></span>

[<span data-ttu-id="c39e3-114">вмлфраме</span><span class="sxs-lookup"><span data-stu-id="c39e3-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="c39e3-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="c39e3-115">**Tag Syntax**</span></span>

<span data-ttu-id="c39e3-116"><v: *элемент* src = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="c39e3-116"><v: *element* src=" *expression* "></span></span>

<span data-ttu-id="c39e3-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="c39e3-117">**Script Syntax**</span></span>

<span data-ttu-id="c39e3-118">*element* . src = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="c39e3-118">*element* .src="*expression*"</span></span>

<span data-ttu-id="c39e3-119">*выражение* = *элемент*. src</span><span class="sxs-lookup"><span data-stu-id="c39e3-119">*expression*=*element*.src</span></span>

<span data-ttu-id="c39e3-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="c39e3-120">**Remarks**</span></span>

<span data-ttu-id="c39e3-121">Атрибут **src** может содержать следующие синтаксисы:</span><span class="sxs-lookup"><span data-stu-id="c39e3-121">The **Src** attribute can involve the following syntaxes:</span></span>

-   <span data-ttu-id="c39e3-122">URL-адрес внешнего файла.</span><span class="sxs-lookup"><span data-stu-id="c39e3-122">URL to external file.</span></span> <span data-ttu-id="c39e3-123">Файл должен быть XML-файлом в следующем формате:</span><span class="sxs-lookup"><span data-stu-id="c39e3-123">The file must be an XML file with the following format:</span></span>
    ```HTML
       <xml xmlns:v = "urn:schemas-microsoft-com:vml">
       .
       .
       .
       </xml>
    ```

    

-   <span data-ttu-id="c39e3-124">Внутри файла необходимо иметь одну или несколько фигур VML с допустимыми идентификаторами, на которые можно ссылаться с помощью этого синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="c39e3-124">Inside the file you must have one or more VML shapes with valid IDs that can be referenced by using this syntax:</span></span>
    ```HTML
       filename#shapename
    ```

    

-   <span data-ttu-id="c39e3-125">В следующей ссылке внешние файлы имеют расширение. VML, но можно использовать любое расширение:</span><span class="sxs-lookup"><span data-stu-id="c39e3-125">In the following reference, external files have the .vml extension, but any extension can be used:</span></span>
    ```HTML
       external.vml#image01
    ```

    

-   <span data-ttu-id="c39e3-126">Вы можете ссылаться на фигуру в том же файле с помощью следующего синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="c39e3-126">You can reference a shape within the same file by using the following syntax:</span></span>
    ```HTML
       #shapename
    ```

    

<span data-ttu-id="c39e3-127">Если значение **Clip** равно **false**, фигура будет масштабироваться в соответствии с размерами рамки.</span><span class="sxs-lookup"><span data-stu-id="c39e3-127">If **Clip** is **False**, the shape will scale to fit the frame.</span></span> <span data-ttu-id="c39e3-128">Если **значение равно true**, то все части фигуры, находящиеся за пределами рамки, не будут отображаться.</span><span class="sxs-lookup"><span data-stu-id="c39e3-128">If **True**, any parts of the shape that are outside the frame will not be displayed.</span></span>

<span data-ttu-id="c39e3-129">Обратите внимание, что [источник](origin-attribute--vmlframe--vml.md) и [Размер](size-attribute--vmlframe.md) не будут использоваться, если только значение **Clip** не равно **true**.</span><span class="sxs-lookup"><span data-stu-id="c39e3-129">Note that [Origin](origin-attribute--vmlframe--vml.md) and [Size](size-attribute--vmlframe.md) won't be used unless **Clip** is **True**.</span></span>

<span data-ttu-id="c39e3-130">**Стандартный атрибут VML**</span><span class="sxs-lookup"><span data-stu-id="c39e3-130">**VML Standard Attribute**</span></span>

<span data-ttu-id="c39e3-131">**Пример**</span><span class="sxs-lookup"><span data-stu-id="c39e3-131">**Example**</span></span>

<span data-ttu-id="c39e3-132">Изображение, определенное во внешнем файле, будет обрезано.</span><span class="sxs-lookup"><span data-stu-id="c39e3-132">The image defined in the external file will be clipped.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 