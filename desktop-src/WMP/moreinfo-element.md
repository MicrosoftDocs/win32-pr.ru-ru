---
title: МОРЕИНФО, элемент
description: Элемент МОРЕИНФО указывает URL-адрес веб-сайта, адрес электронной почты или команду сценария, связанные с показом, обрезками или баннером.
ms.assetid: b817ef1d-4ca0-45f4-942b-695eaf537110
keywords:
- Проигрыватель Windows Media, элемент МОРЕИНФО
topic_type:
- apiref
api_name:
- MOREINFO Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: efc54fe9745566ec7eaa87b7f0f4645b07a055f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704167"
---
# <a name="moreinfo-element"></a><span data-ttu-id="90f0d-104">МОРЕИНФО, элемент</span><span class="sxs-lookup"><span data-stu-id="90f0d-104">MOREINFO Element</span></span>

<span data-ttu-id="90f0d-105">Элемент **мореинфо** указывает URL-адрес веб-сайта, адрес электронной почты или команду сценария, связанные с показом, обрезками или баннером.</span><span class="sxs-lookup"><span data-stu-id="90f0d-105">The **MOREINFO** element specifies a URL to a website, email address, or script command associated with a show, clip, or banner.</span></span>

``` syntax
<MOREINFO
   HREF = "URL"
   TARGET = "Frame"
/>
```

## <a name="attributes"></a><span data-ttu-id="90f0d-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="90f0d-106">Attributes</span></span>

<span data-ttu-id="90f0d-107">**Href** (обязательно)</span><span class="sxs-lookup"><span data-stu-id="90f0d-107">**HREF** (required)</span></span>

<span data-ttu-id="90f0d-108">URL-адрес веб-сайта, адрес электронной почты или команда сценария.</span><span class="sxs-lookup"><span data-stu-id="90f0d-108">URL to a website, email address, or script command.</span></span>

<span data-ttu-id="90f0d-109">**МИШЕНЬ**</span><span class="sxs-lookup"><span data-stu-id="90f0d-109">**TARGET**</span></span>

<span data-ttu-id="90f0d-110">Значение, определяющее фрейм или окно, в котором браузер откроет страницу, определенную атрибутом **href** .</span><span class="sxs-lookup"><span data-stu-id="90f0d-110">Value defining the frame or window in which the browser will open the page defined by the **HREF** attribute.</span></span>

<span data-ttu-id="90f0d-111">Это может быть строка, содержащая имя окна, или одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="90f0d-111">This can be a string containing a window name, or one of the following values.</span></span>



| <span data-ttu-id="90f0d-112">Значение</span><span class="sxs-lookup"><span data-stu-id="90f0d-112">Value</span></span>    | <span data-ttu-id="90f0d-113">Описание</span><span class="sxs-lookup"><span data-stu-id="90f0d-113">Description</span></span>                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90f0d-114">\_свобод</span><span class="sxs-lookup"><span data-stu-id="90f0d-114">\_blank</span></span>  | <span data-ttu-id="90f0d-115">Документ загружается в новое окно браузера.</span><span class="sxs-lookup"><span data-stu-id="90f0d-115">The document loads in a new browser window.</span></span>                                                                              |
| <span data-ttu-id="90f0d-116">\_самообслуживания</span><span class="sxs-lookup"><span data-stu-id="90f0d-116">\_self</span></span>   | <span data-ttu-id="90f0d-117">Документ загружается в том же кадре, что и текущий документ, содержащий элемент управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="90f0d-117">The document loads in the same frame as the current document containing the Windows Media Player control.</span></span>                |
| <span data-ttu-id="90f0d-118">\_источника</span><span class="sxs-lookup"><span data-stu-id="90f0d-118">\_parent</span></span> | <span data-ttu-id="90f0d-119">Документ загружается в непосредственный родительский кадр текущего кадра или в текущий кадр, если родительский фрейм отсутствует.</span><span class="sxs-lookup"><span data-stu-id="90f0d-119">The document loads in the immediate parent frame of the current frame, or the current frame if there is no parent frame.</span></span> |
| <span data-ttu-id="90f0d-120">\_Вверх</span><span class="sxs-lookup"><span data-stu-id="90f0d-120">\_top</span></span>    | <span data-ttu-id="90f0d-121">Документ загружается в полном окне браузера, заменяя все остальные фреймы или документы.</span><span class="sxs-lookup"><span data-stu-id="90f0d-121">The document loads in the full browser window, replacing all other frames or documents.</span></span>                                  |



 

## <a name="parentchild-elements"></a><span data-ttu-id="90f0d-122">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="90f0d-122">Parent/Child Elements</span></span>



| <span data-ttu-id="90f0d-123">Иерархия</span><span class="sxs-lookup"><span data-stu-id="90f0d-123">Hierarchy</span></span>       | <span data-ttu-id="90f0d-124">Элементы</span><span class="sxs-lookup"><span data-stu-id="90f0d-124">Elements</span></span>                       |
|-----------------|--------------------------------|
| <span data-ttu-id="90f0d-125">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="90f0d-125">Parent elements</span></span> | <span data-ttu-id="90f0d-126">**ASX**, **запись**, **баннер**</span><span class="sxs-lookup"><span data-stu-id="90f0d-126">**ASX**, **ENTRY**, **BANNER**</span></span> |
| <span data-ttu-id="90f0d-127">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="90f0d-127">Child elements</span></span>  | <span data-ttu-id="90f0d-128">Нет</span><span class="sxs-lookup"><span data-stu-id="90f0d-128">None</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="90f0d-129">Remarks</span><span class="sxs-lookup"><span data-stu-id="90f0d-129">Remarks</span></span>

<span data-ttu-id="90f0d-130">Этот элемент задает URL-адрес для сайта, адреса электронной почты **или команды сценария. Пользователь может получить доступ к целевому объекту URL-адреса, щелкнув рисунок или текст, связанный с элементом МОРЕИНФО** .</span><span class="sxs-lookup"><span data-stu-id="90f0d-130">This element specifies a URL to a website, email address, **or script command. The user can access the target of the URL by clicking on the graphic or text associated with the MOREINFO** element.</span></span> <span data-ttu-id="90f0d-131">Сведения зависят от родительского элемента элемента **мореинфо** :</span><span class="sxs-lookup"><span data-stu-id="90f0d-131">The details depend on the parent element of the **MOREINFO** element:</span></span>

-   <span data-ttu-id="90f0d-132">Если элемент **мореинфо** является дочерним по отношению к элементу **ASX** , пользователь может получить доступ к URL-адресу, щелкнув заголовок "показывать".</span><span class="sxs-lookup"><span data-stu-id="90f0d-132">If the **MOREINFO** element is the child of an **ASX** element, the user can access the URL by clicking the show title.</span></span>
-   <span data-ttu-id="90f0d-133">Если элемент **мореинфо** является дочерним по отношению к элементу **entry** , пользователь может получить доступ к URL-адресу, щелкнув заголовок клипа.</span><span class="sxs-lookup"><span data-stu-id="90f0d-133">If the **MOREINFO** element is the child of an **ENTRY** element, the user can access the URL by clicking the clip title.</span></span>
-   <span data-ttu-id="90f0d-134">Если элемент **мореинфо** является дочерним по отношению к элементу **баннера** , пользователь может получить доступ к URL-адресу, щелкнув рисунок баннера.</span><span class="sxs-lookup"><span data-stu-id="90f0d-134">If the **MOREINFO** element is the child of a **BANNER** element, the user can access the URL by clicking the banner graphic.</span></span>

<span data-ttu-id="90f0d-135">Если в атрибуте **href** указан URL-адрес веб-сайта, браузер открывается и переходит по URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="90f0d-135">If the **HREF** attribute specifies a URL to a website, the browser opens and navigates to the URL.</span></span> <span data-ttu-id="90f0d-136">Если атрибут **href** указывает адрес электронной почты, запускается приложение электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="90f0d-136">If the **HREF** attribute specifies an email address, the user's email application starts.</span></span> <span data-ttu-id="90f0d-137">Если атрибут **href** задает команду сценария, команда сценария выполняется в браузере.</span><span class="sxs-lookup"><span data-stu-id="90f0d-137">If the **HREF** attribute specifies a script command, the script command executes in the browser.</span></span>

<span data-ttu-id="90f0d-138">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="90f0d-138">**Note**</span></span>

<span data-ttu-id="90f0d-139">Если элемент **мореинфо** появляется внутри элемента **ASX** или **entry** , то при помещении курсора мыши над заголовком показа (для элемента **ASX** ) или Clip (для элемента **entry** ) URL-адрес, определенный в атрибуте **href** , может быть выбран и доступен проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="90f0d-139">If the **MOREINFO** element appears within an **ASX** or **ENTRY** element, when the mouse cursor is held over the title of the show (for an **ASX** element) or clip (for an **ENTRY** element), the URL defined in the **HREF** attribute can be selected and accessed by Windows Media Player.</span></span>

<span data-ttu-id="90f0d-140">Атрибут **Target** определяет фрейм или окно, в котором браузер откроет страницу, определенную атрибутом **href** .</span><span class="sxs-lookup"><span data-stu-id="90f0d-140">The **TARGET** attribute defines the frame or window in which the browser will open the page defined by the **HREF** attribute.</span></span> <span data-ttu-id="90f0d-141">Значения этого атрибута следуют стандартному синтаксису и определениям HTML.</span><span class="sxs-lookup"><span data-stu-id="90f0d-141">The values for this attribute follow standard HTML syntax and definitions.</span></span> <span data-ttu-id="90f0d-142">Если в случае элемента управления, внедренного в веб-страницу, не определен **целевой** атрибут, URL-адрес загружает текущее окно браузера и заменяет существующую страницу, что означает, что содержимое перестает воспроизводиться.</span><span class="sxs-lookup"><span data-stu-id="90f0d-142">In the case of a control embedded in a webpage, if no **TARGET** attribute is defined, the URL loads the current browser window and replaces the existing page, which means the content stops playing.</span></span> <span data-ttu-id="90f0d-143">Поэтому при внедрении элемента управления проигрывателя Windows Media в веб-страницу рекомендуется всегда указывать **целевой** атрибут.</span><span class="sxs-lookup"><span data-stu-id="90f0d-143">Therefore, it is recommended that you always specify a **TARGET** attribute when embedding the Windows Media Player control in a webpage.</span></span>

<span data-ttu-id="90f0d-144">Если метафайл открыт в изолированном проигрывателе Windows Media, **целевой** атрибут игнорируется, а URL-адрес загружается в существующее окно браузера.</span><span class="sxs-lookup"><span data-stu-id="90f0d-144">If the metafile is opened in the stand-alone Windows Media Player, the **TARGET** attribute is ignored, and the URL loads in an existing browser window.</span></span> <span data-ttu-id="90f0d-145">Если окно браузера в настоящий момент не открыто, URL-адрес загружается в новое окно браузера.</span><span class="sxs-lookup"><span data-stu-id="90f0d-145">If there is no browser window currently open, the URL loads in a new browser window.</span></span>

## <a name="examples"></a><span data-ttu-id="90f0d-146">Примеры</span><span class="sxs-lookup"><span data-stu-id="90f0d-146">Examples</span></span>


```XML
<ASX VERSION="3.0">

   <TITLE>Example Media Player Show</TITLE>
   <MOREINFO HREF="https://example.microsoft.com/info/show_info.htm" />
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <MOREINFO HREF="https://example.microsoft.com/info/clip1_info.htm" />
      <REF HREF="mms://example.microsoft.com/media.asf" />
   </ENTRY>
   
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="90f0d-147">Требования</span><span class="sxs-lookup"><span data-stu-id="90f0d-147">Requirements</span></span>



| <span data-ttu-id="90f0d-148">Требование</span><span class="sxs-lookup"><span data-stu-id="90f0d-148">Requirement</span></span> | <span data-ttu-id="90f0d-149">Значение</span><span class="sxs-lookup"><span data-stu-id="90f0d-149">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="90f0d-150">Версия</span><span class="sxs-lookup"><span data-stu-id="90f0d-150">Version</span></span><br/> | <span data-ttu-id="90f0d-151">Проигрыватель Windows Media версии 70 или более поздней</span><span class="sxs-lookup"><span data-stu-id="90f0d-151">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="90f0d-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90f0d-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90f0d-153">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="90f0d-153">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="90f0d-154">**Справочник по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="90f0d-154">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





