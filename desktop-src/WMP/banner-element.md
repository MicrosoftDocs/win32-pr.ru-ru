---
title: Элемент БАННЕРа
description: Элемент БАННЕРа определяет URL-адрес графического файла, который будет отображаться на панели отображения.
ms.assetid: 8b4a3369-a687-40a8-b5df-afb0e0518cd1
keywords:
- Элемент БАННЕРа проигрыватель Windows Media
topic_type:
- apiref
api_name:
- BANNER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e257c14e5908482cdf8de458c259bc64a55c6d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698871"
---
# <a name="banner-element"></a><span data-ttu-id="01c78-104">Элемент БАННЕРа</span><span class="sxs-lookup"><span data-stu-id="01c78-104">BANNER Element</span></span>

<span data-ttu-id="01c78-105">Элемент **баннера** определяет URL-адрес графического файла, который будет отображаться на панели отображения.</span><span class="sxs-lookup"><span data-stu-id="01c78-105">The **BANNER** element defines a URL to a graphic file that will appear in the display panel.</span></span>

``` syntax
<BANNER
   HREF = "URL"
>
</BANNER>
```

## <a name="attributes"></a><span data-ttu-id="01c78-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="01c78-106">Attributes</span></span>

<span data-ttu-id="01c78-107">**Href** (обязательно)</span><span class="sxs-lookup"><span data-stu-id="01c78-107">**HREF** (required)</span></span>

<span data-ttu-id="01c78-108">URL-адрес графического файла, отображаемого на панели отображения.</span><span class="sxs-lookup"><span data-stu-id="01c78-108">URL to a graphic file that is displayed in the display panel.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="01c78-109">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="01c78-109">Parent/Child Elements</span></span>



| <span data-ttu-id="01c78-110">Иерархия</span><span class="sxs-lookup"><span data-stu-id="01c78-110">Hierarchy</span></span>       | <span data-ttu-id="01c78-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="01c78-111">Elements</span></span>                   |
|-----------------|----------------------------|
| <span data-ttu-id="01c78-112">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="01c78-112">Parent elements</span></span> | <span data-ttu-id="01c78-113">**ASX**, **запись**</span><span class="sxs-lookup"><span data-stu-id="01c78-113">**ASX**, **ENTRY**</span></span>         |
| <span data-ttu-id="01c78-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="01c78-114">Child elements</span></span>  | <span data-ttu-id="01c78-115">**abstract**, **мореинфо**</span><span class="sxs-lookup"><span data-stu-id="01c78-115">**ABSTRACT**, **MOREINFO**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="01c78-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01c78-116">Remarks</span></span>

<span data-ttu-id="01c78-117">Этот элемент определяет URL-адрес графического файла, который отображается на панели отображения проигрывателя Windows Media под содержимым видео.</span><span class="sxs-lookup"><span data-stu-id="01c78-117">This element defines a URL to a graphic file that appears in the Windows Media Player display panel, beneath the video content.</span></span> <span data-ttu-id="01c78-118">Если носитель имеет только аудио, отображается баннер.</span><span class="sxs-lookup"><span data-stu-id="01c78-118">If the media is audio only, the banner graphic is displayed by itself.</span></span> <span data-ttu-id="01c78-119">Проигрыватель Windows Media резервирует пространство 32 пикселей высотой до 194 пикселей в ширину (заголовке) для графика.</span><span class="sxs-lookup"><span data-stu-id="01c78-119">Windows Media Player reserves a space 32 pixels high by 194 pixels wide (the banner bar) for the graphic.</span></span> <span data-ttu-id="01c78-120">Если рисунок, определенный в URL-адресе, меньше указанного, он отображается в исходном размере.</span><span class="sxs-lookup"><span data-stu-id="01c78-120">If the graphic defined in the URL is smaller than that, it displays at its original size.</span></span> <span data-ttu-id="01c78-121">Если изображение превышает зарезервированное пространство, проигрыватель Windows Media обработает изображение в соответствии с пространством.</span><span class="sxs-lookup"><span data-stu-id="01c78-121">If the graphic is larger than the reserved space, Windows Media Player will crop the image to fit the space.</span></span>

<span data-ttu-id="01c78-122">Можно использовать **абстрактный** элемент в области элемента **баннера** для отображения текста в виде подсказки, когда пользователь приостанавливает указатель мыши над изображением баннера.</span><span class="sxs-lookup"><span data-stu-id="01c78-122">You can use an **ABSTRACT** element within the scope of the **BANNER** element to display text as a ToolTip when the user pauses the mouse pointer over the banner graphic.</span></span> <span data-ttu-id="01c78-123">Элемент **мореинфо** внутри элемента **баннера** определяет URL-адрес, на который пользователь выполняет, когда пользователь щелкает рисунок баннера.</span><span class="sxs-lookup"><span data-stu-id="01c78-123">A **MOREINFO** element within a **BANNER** element defines a URL to which the user is taken when the user clicks the banner graphic.</span></span> <span data-ttu-id="01c78-124">(URL-адрес может быть любым путем или протоколом, например ссылкой на электронную почту, URL-адресом HTTP для веб-сайта или даже с командой Microsoft JScript.) Когда указатель перемещается над графиком, он становится рельефным и выглядит как кнопка.</span><span class="sxs-lookup"><span data-stu-id="01c78-124">(The URL can be any path or protocol, such as an email link, a Hypertext Transfer Protocol (HTTP) URL to a website, or even a Microsoft JScript command.) When the pointer is moved over the graphic, the graphic becomes embossed and looks like a button.</span></span>

<span data-ttu-id="01c78-125">Элемент **баннера** , определенный для элемента **ASX** , отображается во время воспроизведения всех клипов в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="01c78-125">A **BANNER** element defined for an **ASX** element displays while all clips in the playlist are playing.</span></span> <span data-ttu-id="01c78-126">Элемент **баннера** , определенный в элементе **entry** , отображается только во время воспроизведения клипа, и в течение этого времени все баннеры, определенные в родительском элементе **ASX** , переопределяются.</span><span class="sxs-lookup"><span data-stu-id="01c78-126">A **BANNER** element defined in an **ENTRY** element displays only while that clip is playing, and during that time overrides any banner defined within the parent **ASX** element.</span></span> <span data-ttu-id="01c78-127">Можно указать, каким способом проигрыватель Windows Media резервирует пространство для баннера, задавая атрибут **баннербар** элемента **ASX** .</span><span class="sxs-lookup"><span data-stu-id="01c78-127">You can specify how Windows Media Player reserves space for the banner by setting the **BANNERBAR** attribute of the **ASX** element.</span></span>

<span data-ttu-id="01c78-128">Изображения баннеров не поддерживаются в файлах DRM, или если проигрыватель Windows Media внедрен в веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="01c78-128">Banner images are not supported with DRM files or when Windows Media Player is embedded in a webpage.</span></span>

## <a name="examples"></a><span data-ttu-id="01c78-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="01c78-129">Examples</span></span>

<span data-ttu-id="01c78-130">Ниже приведен пример элемента **баннера** без дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="01c78-130">The following is an example of a **BANNER** element without child elements:</span></span>


```XML
<BANNER HREF="https://sample.microsoft.com/art/banner1.bmp" />
```



<span data-ttu-id="01c78-131">Ниже приведен пример элемента **баннера** , содержащего **абстрактные** и **мореинфо** элементы.</span><span class="sxs-lookup"><span data-stu-id="01c78-131">The following is an example of a **BANNER** element containing **ABSTRACT** and **MOREINFO** elements.</span></span>


```XML
<BANNER HREF="https://www.proseware.com/logos/banner1.bmp">
    <ABSTRACT>Click here to go to our website.</ABSTRACT>
    <MOREINFO HREF="https://sample.microsoft.com" />
    <!-- The text in the Abstract element displays as a 
         ToolTip when the mouse hovers over the banner 
         graphic. When a user clicks the banner, the URL 
         given in the MoreInfo element opens in the 
         browser. -->
</BANNER>
```



## <a name="requirements"></a><span data-ttu-id="01c78-132">Требования</span><span class="sxs-lookup"><span data-stu-id="01c78-132">Requirements</span></span>



| <span data-ttu-id="01c78-133">Требование</span><span class="sxs-lookup"><span data-stu-id="01c78-133">Requirement</span></span> | <span data-ttu-id="01c78-134">Значение</span><span class="sxs-lookup"><span data-stu-id="01c78-134">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="01c78-135">Версия</span><span class="sxs-lookup"><span data-stu-id="01c78-135">Version</span></span><br/> | <span data-ttu-id="01c78-136">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="01c78-136">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="01c78-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01c78-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01c78-138">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="01c78-138">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="01c78-139">**Справочник по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="01c78-139">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





