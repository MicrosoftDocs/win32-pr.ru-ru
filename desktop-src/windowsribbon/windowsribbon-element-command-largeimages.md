---
title: Свойство Command. Ларжеимажес
description: Представляет контейнер изображений; в этом случае крупные изображения.
ms.assetid: 9fcd3694-7847-43e2-9877-47daf47aae9a
keywords:
- Лента Windows для свойства Command. Ларжеимажес
topic_type:
- apiref
api_name:
- Command.LargeImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf71557506d4b9cced21069473d1a6db9b208b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492522"
---
# <a name="commandlargeimages-property"></a><span data-ttu-id="be3e5-104">Свойство Command. Ларжеимажес</span><span class="sxs-lookup"><span data-stu-id="be3e5-104">Command.LargeImages property</span></span>

<span data-ttu-id="be3e5-105">Представляет контейнер изображений; в этом случае крупные изображения.</span><span class="sxs-lookup"><span data-stu-id="be3e5-105">Represents a container of images; in this case, large images.</span></span>

## <a name="usage"></a><span data-ttu-id="be3e5-106">Использование</span><span class="sxs-lookup"><span data-stu-id="be3e5-106">Usage</span></span>

``` syntax
<Command.LargeImages>
  child elements
</Command.LargeImages>
```

## <a name="attributes"></a><span data-ttu-id="be3e5-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="be3e5-107">Attributes</span></span>

<span data-ttu-id="be3e5-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="be3e5-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="be3e5-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="be3e5-109">Child elements</span></span>



| <span data-ttu-id="be3e5-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="be3e5-110">Element</span></span>                                                 | <span data-ttu-id="be3e5-111">Описание</span><span class="sxs-lookup"><span data-stu-id="be3e5-111">Description</span></span>                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="be3e5-112">**Изображение**</span><span class="sxs-lookup"><span data-stu-id="be3e5-112">**Image**</span></span>](windowsribbon-element-image.md)<br/> | <span data-ttu-id="be3e5-113">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="be3e5-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="be3e5-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="be3e5-114">Parent elements</span></span>



| <span data-ttu-id="be3e5-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="be3e5-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="be3e5-116">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="be3e5-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="be3e5-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be3e5-117">Remarks</span></span>

<span data-ttu-id="be3e5-118">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="be3e5-118">Optional.</span></span>

<span data-ttu-id="be3e5-119">Для каждой [**команды**](windowsribbon-element-command.md)может выполняться не более одного раза.</span><span class="sxs-lookup"><span data-stu-id="be3e5-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="be3e5-120">Ресурсы изображений должны соответствовать стандартному графическому формату точечного рисунка (BMP), используемому в Windows.</span><span class="sxs-lookup"><span data-stu-id="be3e5-120">Image resources must conform to the standard bitmap (BMP) graphics format used in Windows.</span></span>

## <a name="examples"></a><span data-ttu-id="be3e5-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="be3e5-121">Examples</span></span>

<span data-ttu-id="be3e5-122">В следующем примере показана базовая разметка для элемента [**SplitButton**](windowsribbon-element-splitbutton.md) с элементом [**менуграуп**](windowsribbon-element-menugroup.md) .</span><span class="sxs-lookup"><span data-stu-id="be3e5-122">The following example demonstrates the basic markup for the [**SplitButton**](windowsribbon-element-splitbutton.md) with a [**MenuGroup**](windowsribbon-element-menugroup.md) element.</span></span>

<span data-ttu-id="be3e5-123">В этом разделе кода показаны объявления команд [**SplitButton**](windowsribbon-element-splitbutton.md) и [**менуграуп**](windowsribbon-element-menugroup.md) с большим и небольшим ресурсом изображения.</span><span class="sxs-lookup"><span data-stu-id="be3e5-123">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and [**MenuGroup**](windowsribbon-element-menugroup.md) Command declarations with a large and a small image resource.</span></span> <span data-ttu-id="be3e5-124">Также объявлена связанная [**Группа**](windowsribbon-element-group.md) , которая выступает в качестве родительского контейнера для элемента **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="be3e5-124">An associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **SplitButton** element is also declared.</span></span>


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



## <a name="requirements"></a><span data-ttu-id="be3e5-125">Требования</span><span class="sxs-lookup"><span data-stu-id="be3e5-125">Requirements</span></span>



| <span data-ttu-id="be3e5-126">Требование</span><span class="sxs-lookup"><span data-stu-id="be3e5-126">Requirement</span></span> | <span data-ttu-id="be3e5-127">Значение</span><span class="sxs-lookup"><span data-stu-id="be3e5-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="be3e5-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be3e5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="be3e5-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="be3e5-129">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="be3e5-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be3e5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="be3e5-131">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="be3e5-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="be3e5-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be3e5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be3e5-133">Указание ресурсов изображения ленты</span><span class="sxs-lookup"><span data-stu-id="be3e5-133">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> <dt>

[<span data-ttu-id="be3e5-134">UI \_ PKEY \_ ларжеимаже</span><span class="sxs-lookup"><span data-stu-id="be3e5-134">UI\_PKEY\_LargeImage</span></span>](windowsribbon-reference-properties-uipkey-largeimage.md)
</dt> </dl>

 

 





