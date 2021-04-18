---
title: Свойство Command. Смаллхигхконтрастимажес
description: Представляет контейнер изображений; в данном случае это небольшие изображения для использования с параметрами системы с высокой контрастностью.
ms.assetid: d1c441eb-885a-4dc1-b98d-5a36cab2f837
keywords:
- Лента Windows для свойства Command. Смаллхигхконтрастимажес
topic_type:
- apiref
api_name:
- Command.SmallHighContrastImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56291ad4e56e5f941fe4cb2790ac6afab27ad67b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672809"
---
# <a name="commandsmallhighcontrastimages-property"></a><span data-ttu-id="367f6-104">Свойство Command. Смаллхигхконтрастимажес</span><span class="sxs-lookup"><span data-stu-id="367f6-104">Command.SmallHighContrastImages property</span></span>

<span data-ttu-id="367f6-105">Представляет контейнер изображений; в данном случае это небольшие изображения для использования с параметрами системы с высокой контрастностью.</span><span class="sxs-lookup"><span data-stu-id="367f6-105">Represents a container of images; in this case, small images for use with high-contrast system settings.</span></span>

## <a name="usage"></a><span data-ttu-id="367f6-106">Использование</span><span class="sxs-lookup"><span data-stu-id="367f6-106">Usage</span></span>

``` syntax
<Command.SmallHighContrastImages>
  child elements
</Command.SmallHighContrastImages>
```

## <a name="attributes"></a><span data-ttu-id="367f6-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="367f6-107">Attributes</span></span>

<span data-ttu-id="367f6-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="367f6-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="367f6-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="367f6-109">Child elements</span></span>



| <span data-ttu-id="367f6-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="367f6-110">Element</span></span>                                                 | <span data-ttu-id="367f6-111">Описание</span><span class="sxs-lookup"><span data-stu-id="367f6-111">Description</span></span>                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="367f6-112">**Изображение**</span><span class="sxs-lookup"><span data-stu-id="367f6-112">**Image**</span></span>](windowsribbon-element-image.md)<br/> | <span data-ttu-id="367f6-113">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="367f6-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="367f6-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="367f6-114">Parent elements</span></span>



| <span data-ttu-id="367f6-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="367f6-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="367f6-116">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="367f6-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="367f6-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="367f6-117">Remarks</span></span>

<span data-ttu-id="367f6-118">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="367f6-118">Optional.</span></span>

<span data-ttu-id="367f6-119">Для каждой [**команды**](windowsribbon-element-command.md)может выполняться не более одного раза.</span><span class="sxs-lookup"><span data-stu-id="367f6-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="367f6-120">Ресурсы изображений должны соответствовать стандартному графическому формату точечного рисунка (BMP), используемому в Windows.</span><span class="sxs-lookup"><span data-stu-id="367f6-120">Image resources must conform to the standard bitmap (BMP) graphics format used in Windows.</span></span>

## <a name="examples"></a><span data-ttu-id="367f6-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="367f6-121">Examples</span></span>

<span data-ttu-id="367f6-122">В следующем примере показана базовая разметка для элемента [**SplitButton**](windowsribbon-element-splitbutton.md) с элементом [**менуграуп**](windowsribbon-element-menugroup.md) .</span><span class="sxs-lookup"><span data-stu-id="367f6-122">The following example demonstrates the basic markup for the [**SplitButton**](windowsribbon-element-splitbutton.md) with a [**MenuGroup**](windowsribbon-element-menugroup.md) element.</span></span>

<span data-ttu-id="367f6-123">В этом разделе кода показаны объявления команд [**SplitButton**](windowsribbon-element-splitbutton.md) и [**менуграуп**](windowsribbon-element-menugroup.md) с большими и малыми изображениями с высокой контрастностью.</span><span class="sxs-lookup"><span data-stu-id="367f6-123">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and [**MenuGroup**](windowsribbon-element-menugroup.md) Command declarations with large and small high contrast image resources.</span></span> <span data-ttu-id="367f6-124">Также объявлена связанная [**Группа**](windowsribbon-element-group.md) , которая выступает в качестве родительского контейнера для элемента **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="367f6-124">An associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **SplitButton** element is also declared.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="367f6-125">Требования</span><span class="sxs-lookup"><span data-stu-id="367f6-125">Requirements</span></span>



| <span data-ttu-id="367f6-126">Требование</span><span class="sxs-lookup"><span data-stu-id="367f6-126">Requirement</span></span> | <span data-ttu-id="367f6-127">Значение</span><span class="sxs-lookup"><span data-stu-id="367f6-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="367f6-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="367f6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="367f6-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="367f6-129">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="367f6-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="367f6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="367f6-131">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="367f6-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="367f6-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="367f6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="367f6-133">Указание ресурсов изображения ленты</span><span class="sxs-lookup"><span data-stu-id="367f6-133">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> <dt>

[<span data-ttu-id="367f6-134">UI \_ PKEY \_ смаллхигхконтрастимаже</span><span class="sxs-lookup"><span data-stu-id="367f6-134">UI\_PKEY\_SmallHighContrastImage</span></span>](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md)
</dt> </dl>

 

 





