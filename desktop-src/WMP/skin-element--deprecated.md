---
title: Элемент SKIN (не рекомендуется)
description: Эта страница описывает функцию, которая может быть недоступна в будущих версиях проигрывателя Windows Media и Windows Media Player SDK.
ms.assetid: 593244c1-f850-46d7-8b84-14dcd59b024e
keywords:
- Элемент SKIN (не рекомендуется) проигрыватель Windows Media
topic_type:
- apiref
api_name:
- SKIN Element (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: abf503706dec131eef411ebaf3625071e2b31098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657607"
---
# <a name="skin-element-deprecated"></a><span data-ttu-id="34e7d-104">Элемент SKIN (не рекомендуется)</span><span class="sxs-lookup"><span data-stu-id="34e7d-104">SKIN Element (deprecated)</span></span>

<span data-ttu-id="34e7d-105">Эта страница описывает функцию, которая может быть недоступна в будущих версиях проигрывателя Windows Media и Windows Media Player SDK.</span><span class="sxs-lookup"><span data-stu-id="34e7d-105">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="34e7d-106">Элемент **Skin** задает URL-адрес границы.</span><span class="sxs-lookup"><span data-stu-id="34e7d-106">The **SKIN** element specifies a URL to a border.</span></span>

``` syntax
<SKIN
   HREF = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="34e7d-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="34e7d-107">Attributes</span></span>

<span data-ttu-id="34e7d-108">**Href** (обязательно)</span><span class="sxs-lookup"><span data-stu-id="34e7d-108">**HREF** (required)</span></span>

<span data-ttu-id="34e7d-109">URL-адрес для файла сжатой границы с расширением WMZ.</span><span class="sxs-lookup"><span data-stu-id="34e7d-109">URL for a compressed border file with a file name extension .wmz.</span></span> <span data-ttu-id="34e7d-110">Для проигрывателя Windows Media 9 Series или более поздней версии это значение может ссылаться только на файлы границ на жестком диске пользователя, расположенные в том же каталоге, что и список воспроизведения метафайлов.</span><span class="sxs-lookup"><span data-stu-id="34e7d-110">For Windows Media Player 9 Series or later, this value can reference only border files on the user's hard disk located in the same directory as the metafile playlist.</span></span> <span data-ttu-id="34e7d-111">См. пример кода.</span><span class="sxs-lookup"><span data-stu-id="34e7d-111">See the example code.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="34e7d-112">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="34e7d-112">Parent/Child Elements</span></span>



| <span data-ttu-id="34e7d-113">Иерархия</span><span class="sxs-lookup"><span data-stu-id="34e7d-113">Hierarchy</span></span>       | <span data-ttu-id="34e7d-114">Элементы</span><span class="sxs-lookup"><span data-stu-id="34e7d-114">Elements</span></span> |
|-----------------|----------|
| <span data-ttu-id="34e7d-115">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="34e7d-115">Parent elements</span></span> | <span data-ttu-id="34e7d-116">**ASX**</span><span class="sxs-lookup"><span data-stu-id="34e7d-116">**ASX**</span></span>  |
| <span data-ttu-id="34e7d-117">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="34e7d-117">Child elements</span></span>  | <span data-ttu-id="34e7d-118">Нет</span><span class="sxs-lookup"><span data-stu-id="34e7d-118">None</span></span>     |



 

## <a name="remarks"></a><span data-ttu-id="34e7d-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="34e7d-119">Remarks</span></span>

<span data-ttu-id="34e7d-120">Элемент **Skin** используется для создания границы, которая аналогична обложке, но отображается в области **Воспроизведение** в проигрывателе Windows Media в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="34e7d-120">The **SKIN** element is used to create a border, which is similar to a skin but is displayed in the **Now Playing** area of the full mode Windows Media Player.</span></span> <span data-ttu-id="34e7d-121">Элемент **Skin** используется только для границ, которые отображаются в проигрывателе Windows Media в полноэкранном режиме, а не для обычных обложек, которые полностью заменяют проигрыватель Windows Media в компактном режиме.</span><span class="sxs-lookup"><span data-stu-id="34e7d-121">The **SKIN** element is used only for borders, which appear inside the full mode Windows Media Player, and not for regular skins, which entirely replace the compact mode Windows Media Player.</span></span>

<span data-ttu-id="34e7d-122">В пакете загрузки Windows Media (с расширением имени файла. WMD) элемент **Skin** позволяет границе иметь содержимое и ссылаться на другие сайты.</span><span class="sxs-lookup"><span data-stu-id="34e7d-122">In a Windows Media Download Package (with a .wmd file name extension), the **SKIN** element enables a border to have content and link to other sites.</span></span> <span data-ttu-id="34e7d-123">Пакет загрузки Windows Media представляет собой сжатый файл, содержащий файл границ и метафайл Windows Media.</span><span class="sxs-lookup"><span data-stu-id="34e7d-123">The Windows Media Download Package is a compressed file that contains a border file and a Windows Media metafile.</span></span> <span data-ttu-id="34e7d-124">Файл границ (с расширением WMZ) сжимается и включает файл определения обложки (с расширением WMS).</span><span class="sxs-lookup"><span data-stu-id="34e7d-124">The border file (with a .wmz file name extension) is compressed, and includes a skin definition file (with a .wms file name extension).</span></span>

<span data-ttu-id="34e7d-125">Элемент **Skin** имеет три компонента:</span><span class="sxs-lookup"><span data-stu-id="34e7d-125">A **SKIN** element has three components:</span></span>

-   <span data-ttu-id="34e7d-126">Обложка</span><span class="sxs-lookup"><span data-stu-id="34e7d-126">A skin</span></span>
-   <span data-ttu-id="34e7d-127">Некоторое содержимое</span><span class="sxs-lookup"><span data-stu-id="34e7d-127">Some content</span></span>
-   <span data-ttu-id="34e7d-128">Метафайл</span><span class="sxs-lookup"><span data-stu-id="34e7d-128">A metafile</span></span>

<span data-ttu-id="34e7d-129">Обложки, входящие в состав пакетов загрузки Windows Media, должны быть прямоугольными в фигуре.</span><span class="sxs-lookup"><span data-stu-id="34e7d-129">Skins included with Windows Media Download Packages must be rectangular in shape.</span></span> <span data-ttu-id="34e7d-130">Создание границ с непрямоугольными обложекми может привести к непредвиденным результатам.</span><span class="sxs-lookup"><span data-stu-id="34e7d-130">Creating borders with skins that are not rectangular may yield unexpected results.</span></span>

## <a name="examples"></a><span data-ttu-id="34e7d-131">Примеры</span><span class="sxs-lookup"><span data-stu-id="34e7d-131">Examples</span></span>


```XML
<ASX version = "3.0">
    <TITLE>A Skin Element</TITLE>
    <SKIN HREF = "YourTest.wmz" />

    <ENTRY>
        <PARAM name="YourAlbumTitle" value="YourTitle.jpg"/>
        <PARAM name="link" value="https://www.proseware.com"/>
        <TITLE>(The Artist)-YourTitle</TITLE>
        <REF HREF="(The Artist)-YourSongTitle.wma"/>
    </ENTRY>

</ASX>
```



## <a name="requirements"></a><span data-ttu-id="34e7d-132">Требования</span><span class="sxs-lookup"><span data-stu-id="34e7d-132">Requirements</span></span>



| <span data-ttu-id="34e7d-133">Требование</span><span class="sxs-lookup"><span data-stu-id="34e7d-133">Requirement</span></span> | <span data-ttu-id="34e7d-134">Значение</span><span class="sxs-lookup"><span data-stu-id="34e7d-134">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="34e7d-135">Версия</span><span class="sxs-lookup"><span data-stu-id="34e7d-135">Version</span></span><br/> | <span data-ttu-id="34e7d-136">Проигрыватель Windows Media версии 70 или более поздней</span><span class="sxs-lookup"><span data-stu-id="34e7d-136">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="34e7d-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34e7d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34e7d-138">**Границы для проигрывателя Windows Media (не рекомендуется)**</span><span class="sxs-lookup"><span data-stu-id="34e7d-138">**Borders for Windows Media Player (deprecated)**</span></span>](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[<span data-ttu-id="34e7d-139">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="34e7d-139">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="34e7d-140">**Справочник по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="34e7d-140">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





