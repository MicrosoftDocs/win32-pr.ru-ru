---
title: ENTRY, элемент
description: Элемент ENTRY указывает файл Windows Media, который будет отображен как клип.
ms.assetid: 7fd16aff-2eed-4f95-92b3-b48a9d785e7c
keywords:
- Проигрыватель Windows Media, элемент ENTRY
topic_type:
- apiref
api_name:
- ENTRY Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 13da18c72022c916f91bcffe7382f673ba3d4fa4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699185"
---
# <a name="entry-element"></a><span data-ttu-id="53cea-104">ENTRY, элемент</span><span class="sxs-lookup"><span data-stu-id="53cea-104">ENTRY Element</span></span>

<span data-ttu-id="53cea-105">Элемент **entry** указывает файл Windows Media, который будет отображен как клип.</span><span class="sxs-lookup"><span data-stu-id="53cea-105">The **ENTRY** element specifies a Windows Media file to render as a clip.</span></span>

``` syntax
<ENTRY
   CLIENTSKIP = "YES" | "NO"
   SKIPIFREF = "YES" | "NO"
>
</ENTRY>
```

## <a name="attributes"></a><span data-ttu-id="53cea-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="53cea-106">Attributes</span></span>

<span data-ttu-id="53cea-107">**клиентскип**</span><span class="sxs-lookup"><span data-stu-id="53cea-107">**CLIENTSKIP**</span></span>

<span data-ttu-id="53cea-108">Значение, указывающее, может ли пользователь пропускать вперед после клипа.</span><span class="sxs-lookup"><span data-stu-id="53cea-108">Value indicating whether the user can skip forward past the clip.</span></span>

<span data-ttu-id="53cea-109">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="53cea-109">Possible values include the following.</span></span>



| <span data-ttu-id="53cea-110">Значение</span><span class="sxs-lookup"><span data-stu-id="53cea-110">Value</span></span> | <span data-ttu-id="53cea-111">Описание</span><span class="sxs-lookup"><span data-stu-id="53cea-111">Description</span></span>                                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="53cea-112">YES</span><span class="sxs-lookup"><span data-stu-id="53cea-112">YES</span></span>   | <span data-ttu-id="53cea-113">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="53cea-113">Default.</span></span> <span data-ttu-id="53cea-114">Пользователь может пропускать пересылку после клипа.</span><span class="sxs-lookup"><span data-stu-id="53cea-114">User can skip forward past the clip.</span></span> |
| <span data-ttu-id="53cea-115">NO</span><span class="sxs-lookup"><span data-stu-id="53cea-115">NO</span></span>    | <span data-ttu-id="53cea-116">Пользователь не может пропускать вперед после клипа.</span><span class="sxs-lookup"><span data-stu-id="53cea-116">User cannot skip forward past the clip.</span></span>       |



 

<span data-ttu-id="53cea-117">**скипифреф**</span><span class="sxs-lookup"><span data-stu-id="53cea-117">**SKIPIFREF**</span></span>

<span data-ttu-id="53cea-118">Значение, указывающее, должен ли проигрыватель Windows Media пропустить этот клип, если элемент **entry** включен во второй метафайл с помощью элемента **ентриреф** .</span><span class="sxs-lookup"><span data-stu-id="53cea-118">Value indicating whether Windows Media Player should skip this clip when the **ENTRY** element is included in a second metafile through the use of an **ENTRYREF** element.</span></span>

<span data-ttu-id="53cea-119">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="53cea-119">Possible values include the following.</span></span>



| <span data-ttu-id="53cea-120">Значение</span><span class="sxs-lookup"><span data-stu-id="53cea-120">Value</span></span> | <span data-ttu-id="53cea-121">Описание</span><span class="sxs-lookup"><span data-stu-id="53cea-121">Description</span></span>                                                                                 |
|-------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="53cea-122">YES</span><span class="sxs-lookup"><span data-stu-id="53cea-122">YES</span></span>   | <span data-ttu-id="53cea-123">Проигрыватель Windows Media пропустит эту запись при ссылке через элемент **ентриреф** .</span><span class="sxs-lookup"><span data-stu-id="53cea-123">Windows Media Player will ignore this entry, if referenced through an **ENTRYREF** element.</span></span> |
| <span data-ttu-id="53cea-124">NO</span><span class="sxs-lookup"><span data-stu-id="53cea-124">NO</span></span>    | <span data-ttu-id="53cea-125">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="53cea-125">Default.</span></span> <span data-ttu-id="53cea-126">Проигрыватель Windows Media не будет пропускать эту запись.</span><span class="sxs-lookup"><span data-stu-id="53cea-126">Windows Media Player will not ignore this entry.</span></span>                                   |



 

## <a name="parentchild-elements"></a><span data-ttu-id="53cea-127">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="53cea-127">Parent/Child Elements</span></span>



| <span data-ttu-id="53cea-128">Иерархия</span><span class="sxs-lookup"><span data-stu-id="53cea-128">Hierarchy</span></span>       | <span data-ttu-id="53cea-129">Элементы</span><span class="sxs-lookup"><span data-stu-id="53cea-129">Elements</span></span>                                                                                                                                                                                     |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53cea-130">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="53cea-130">Parent elements</span></span> | <span data-ttu-id="53cea-131">**ASX**, **событие**, **Повтор**</span><span class="sxs-lookup"><span data-stu-id="53cea-131">**ASX**, **EVENT**, **REPEAT**</span></span>                                                                                                                                                               |
| <span data-ttu-id="53cea-132">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="53cea-132">Child elements</span></span>  | <span data-ttu-id="53cea-133">**абстрактный**, **Автор**, **баннер**, **базовый**, **авторские права**, **Длительность**, **ендмаркер**, **мореинфо**, **param**, **превиевдуратион**, **ref**, **стартмаркер**, **StartTime**, **Title**</span><span class="sxs-lookup"><span data-stu-id="53cea-133">**ABSTRACT**, **AUTHOR**, **BANNER**, **BASE**, **COPYRIGHT**, **DURATION**, **ENDMARKER**, **MOREINFO**, **PARAM**, **PREVIEWDURATION**, **REF**, **STARTMARKER**, **STARTTIME**, **TITLE**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="53cea-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="53cea-134">Remarks</span></span>

<span data-ttu-id="53cea-135">Этот элемент является фундаментальным конструкцией в метафайле Windows Media.</span><span class="sxs-lookup"><span data-stu-id="53cea-135">This element is the fundamental construct in a Windows Media metafile.</span></span> <span data-ttu-id="53cea-136">Элемент **entry** и связанные с ним атрибуты определяют метаданные для отдельного логического фрагмента содержимого, называемого клипом.</span><span class="sxs-lookup"><span data-stu-id="53cea-136">The **ENTRY** element and its associated attributes define meta-information for a single, logical piece of content, called a clip.</span></span> <span data-ttu-id="53cea-137">Дочерние элементы в области элемента **entry** определяют мультимедийное содержимое проигрывателя Windows Media для открытия (**ref**), сведения о клипе, который проигрыватель Windows Media будет отображать как текст (**Автор**, **авторские права**, **заголовок**) и другие параметры, связанные с этим клипом.</span><span class="sxs-lookup"><span data-stu-id="53cea-137">Child elements within the scope of an **ENTRY** element define media content for Windows Media Player to open (**REF**), information about the clip that Windows Media Player will display as text (**AUTHOR**, **COPYRIGHT**, **TITLE**), and other settings related to the clip.</span></span> <span data-ttu-id="53cea-138">Дочерний элемент **ref** связывает содержимое, которое должно быть передаваться в поток для родительского элемента **entry** .</span><span class="sxs-lookup"><span data-stu-id="53cea-138">The **REF** child element links the content to be streamed for the parent **ENTRY** element.</span></span> <span data-ttu-id="53cea-139">Несмотря на то, что скрипт не будет прерываться, **запись** не имеет смысла без дочернего элемента **ref** .</span><span class="sxs-lookup"><span data-stu-id="53cea-139">Though the script will not break, the **ENTRY** is meaningless without a **REF** child.</span></span>

<span data-ttu-id="53cea-140">Если значение атрибута **клиентскип** равно «нет», то пользователь не сможет пропускать вперед после фрагмента содержимого, определенного элементом **entry** .</span><span class="sxs-lookup"><span data-stu-id="53cea-140">If the value of the **CLIENTSKIP** attribute is NO, the user cannot skip forward past the piece of content defined by the **ENTRY** element.</span></span> <span data-ttu-id="53cea-141">Это не работает, если элемент дочерней **ссылки** ссылается на другой метафайл.</span><span class="sxs-lookup"><span data-stu-id="53cea-141">This does not work if the child **REF** element references another metafile.</span></span> <span data-ttu-id="53cea-142">На вложенные метафайлы следует ссылаться с помощью элемента **ентриреф** .</span><span class="sxs-lookup"><span data-stu-id="53cea-142">Nested metafiles should be referenced using the **ENTRYREF** element.</span></span>

<span data-ttu-id="53cea-143">Атрибут **скипифреф** относится только к элементам **записи** , которые включены во второй метафайл посредством использования элемента **ентриреф** .</span><span class="sxs-lookup"><span data-stu-id="53cea-143">The **SKIPIFREF** attribute pertains only to **ENTRY** elements that are included in a second metafile through the use of an **ENTRYREF** element.</span></span> <span data-ttu-id="53cea-144">Элемент **ентриреф** ссылается на другой метафайл для логического включения в текущий файл.</span><span class="sxs-lookup"><span data-stu-id="53cea-144">The **ENTRYREF** element references another metafile for logical inclusion in the current file.</span></span> <span data-ttu-id="53cea-145">Если значение атрибута **скипифреф** для элемента **entry** из файла метафайла, на который указывает ссылка, равно Yes, проигрыватель Windows Media пропускает эту запись и переходит к следующему элементу **entry** , если он есть.</span><span class="sxs-lookup"><span data-stu-id="53cea-145">If the value of the **SKIPIFREF** attribute for an **ENTRY** element from the referenced metafile file is YES, Windows Media Player ignores this pulled-in entry, and moves on to the next **ENTRY** element, if any.</span></span> <span data-ttu-id="53cea-146">Следующий элемент **entry** может быть следующей записью в исходном файле или следующей записью в метафайле, на который ссылается элемент **ентриреф** .</span><span class="sxs-lookup"><span data-stu-id="53cea-146">The next **ENTRY** element can be the next entry in the original file, or the next entry in the metafile referenced in the **ENTRYREF** element.</span></span>

## <a name="examples"></a><span data-ttu-id="53cea-147">Примеры</span><span class="sxs-lookup"><span data-stu-id="53cea-147">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <TITLE>Example Windows Media Player Show</TITLE>
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <REF HREF="https://example.microsoft.com/media.asf" />
   </ENTRY>
   
   <ENTRY>
      <TITLE>Another Clip</TITLE>
      <REF HREF="https://example.microsoft.com/more_media.asf" />
   </ENTRY>
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="53cea-148">Требования</span><span class="sxs-lookup"><span data-stu-id="53cea-148">Requirements</span></span>



| <span data-ttu-id="53cea-149">Требование</span><span class="sxs-lookup"><span data-stu-id="53cea-149">Requirement</span></span> | <span data-ttu-id="53cea-150">Значение</span><span class="sxs-lookup"><span data-stu-id="53cea-150">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="53cea-151">Версия</span><span class="sxs-lookup"><span data-stu-id="53cea-151">Version</span></span><br/> | <span data-ttu-id="53cea-152">Проигрыватель Windows Media версии 70 или более поздней</span><span class="sxs-lookup"><span data-stu-id="53cea-152">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="53cea-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53cea-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53cea-154">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="53cea-154">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="53cea-155">**Справочник по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="53cea-155">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





