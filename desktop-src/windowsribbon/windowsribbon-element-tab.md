---
title: Элемент Tab
description: Представляет базовую или контекстную вкладку.
ms.assetid: 2e73a89c-4d31-4075-93c8-e43213a20791
keywords:
- Лента Windows для элемента вкладки
topic_type:
- apiref
api_name:
- Tab
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e54abc7e13906ada69c1e10f81878c77c4bf5d8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070405"
---
# <a name="tab-element"></a><span data-ttu-id="ba23f-104">Элемент Tab</span><span class="sxs-lookup"><span data-stu-id="ba23f-104">Tab element</span></span>

<span data-ttu-id="ba23f-105">Представляет [базовую](windowsribbon-controls-tab.md) или [контекстную](windowsribbon-controls-tabgroup.md) вкладку.</span><span class="sxs-lookup"><span data-stu-id="ba23f-105">Represents a [core](windowsribbon-controls-tab.md) or [contextual](windowsribbon-controls-tabgroup.md) tab.</span></span>

## <a name="usage"></a><span data-ttu-id="ba23f-106">Использование</span><span class="sxs-lookup"><span data-stu-id="ba23f-106">Usage</span></span>

``` syntax
<Tab
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Tab>
```

## <a name="attributes"></a><span data-ttu-id="ba23f-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ba23f-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ba23f-108">attribute</span><span class="sxs-lookup"><span data-stu-id="ba23f-108">Attribute</span></span></th>
<th><span data-ttu-id="ba23f-109">Тип</span><span class="sxs-lookup"><span data-stu-id="ba23f-109">Type</span></span></th>
<th><span data-ttu-id="ba23f-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="ba23f-110">Required</span></span></th>
<th><span data-ttu-id="ba23f-111">Описание</span><span class="sxs-lookup"><span data-stu-id="ba23f-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ba23f-112"><strong>аппликатионмодес</strong></span><span class="sxs-lookup"><span data-stu-id="ba23f-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="ba23f-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="ba23f-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="ba23f-114">Нет</span><span class="sxs-lookup"><span data-stu-id="ba23f-114">No</span></span><br/></td>
<td><span data-ttu-id="ba23f-115">Допустимо, только если <a href="windowsribbon-element-menugroup.md"><strong>менуграуп</strong></a> является родительским элементом.</span><span class="sxs-lookup"><span data-stu-id="ba23f-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="ba23f-116">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="ba23f-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="ba23f-117">Строка, содержащая разделенный запятыми список целых чисел от 0 до 31.</span><span class="sxs-lookup"><span data-stu-id="ba23f-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="ba23f-118">Пробелы допустимы и пропускаются.</span><span class="sxs-lookup"><span data-stu-id="ba23f-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="ba23f-119">Максимальная длина: 250 символов.</span><span class="sxs-lookup"><span data-stu-id="ba23f-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba23f-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="ba23f-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="ba23f-121">xs: Поситивеинтежер или xs: String</span><span class="sxs-lookup"><span data-stu-id="ba23f-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="ba23f-122">Нет</span><span class="sxs-lookup"><span data-stu-id="ba23f-122">No</span></span><br/></td>
<td><span data-ttu-id="ba23f-123">Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ba23f-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="ba23f-124">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)</span><span class="sxs-lookup"><span data-stu-id="ba23f-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="ba23f-125">Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно.</span><span class="sxs-lookup"><span data-stu-id="ba23f-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="ba23f-126">Значение должно быть уникальным в XML-документе ленты.</span><span class="sxs-lookup"><span data-stu-id="ba23f-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="ba23f-127">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="ba23f-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="ba23f-128">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ba23f-128">Child elements</span></span>



| <span data-ttu-id="ba23f-129">Элемент</span><span class="sxs-lookup"><span data-stu-id="ba23f-129">Element</span></span>                                                                         | <span data-ttu-id="ba23f-130">Описание</span><span class="sxs-lookup"><span data-stu-id="ba23f-130">Description</span></span>                                        |
|---------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="ba23f-131">**Сгруппировать**</span><span class="sxs-lookup"><span data-stu-id="ba23f-131">**Group**</span></span>](windowsribbon-element-group.md)<br/>                         | <span data-ttu-id="ba23f-132">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="ba23f-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="ba23f-133">**TAB. Скалингполици**</span><span class="sxs-lookup"><span data-stu-id="ba23f-133">**Tab.ScalingPolicy**</span></span>](windowsribbon-element-tab-scalingpolicy.md)<br/> | <span data-ttu-id="ba23f-134">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="ba23f-134">May occur at most once</span></span><br/> <br/>      |



## <a name="parent-elements"></a><span data-ttu-id="ba23f-135">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="ba23f-135">Parent elements</span></span>



| <span data-ttu-id="ba23f-136">Элемент</span><span class="sxs-lookup"><span data-stu-id="ba23f-136">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| [<span data-ttu-id="ba23f-137">**Лента. вкладки**</span><span class="sxs-lookup"><span data-stu-id="ba23f-137">**Ribbon.Tabs**</span></span>](windowsribbon-element-ribbon-tabs.md)<br/> |
| [<span data-ttu-id="ba23f-138">**Группа вкладок**</span><span class="sxs-lookup"><span data-stu-id="ba23f-138">**TabGroup**</span></span>](windowsribbon-element-tabgroup.md)<br/>       |



## <a name="remarks"></a><span data-ttu-id="ba23f-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ba23f-139">Remarks</span></span>

<span data-ttu-id="ba23f-140">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="ba23f-140">Required.</span></span>

<span data-ttu-id="ba23f-141">Должен быть хотя бы один раз для каждого элемента [**Ribbon. Табуляторы**](windowsribbon-element-ribbon-tabs.md) или [**табграуп**](windowsribbon-element-tabgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="ba23f-141">Must occur at least once for each [**Ribbon.Tabs**](windowsribbon-element-ribbon-tabs.md) or [**TabGroup**](windowsribbon-element-tabgroup.md) element.</span></span>

<span data-ttu-id="ba23f-142">**Вкладка** поддерживает [режимы приложений](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="ba23f-142">**Tab** supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="ba23f-143">Если для элемента **Tab** имеется [**скалингполици. идеалсизес**](windowsribbon-element-scalingpolicy-idealsizes.md) , то в **скалингполици. идеалсизес** требуется запись для каждого элемента [**группы**](windowsribbon-element-group.md) и его идеальный размер.</span><span class="sxs-lookup"><span data-stu-id="ba23f-143">If [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) is present for the **Tab** element, then an entry for each [**Group**](windowsribbon-element-group.md) element and its ideal size is required under **ScalingPolicy.IdealSizes**.</span></span>

## <a name="examples"></a><span data-ttu-id="ba23f-144">Примеры</span><span class="sxs-lookup"><span data-stu-id="ba23f-144">Examples</span></span>

<span data-ttu-id="ba23f-145">В следующем примере показана базовая разметка для элемента **вкладки** .</span><span class="sxs-lookup"><span data-stu-id="ba23f-145">The following example demonstrates the basic markup for the **Tab** element.</span></span>

<span data-ttu-id="ba23f-146">В этом разделе кода показаны объявления команд **вкладки** для вкладки " **Главная** ".</span><span class="sxs-lookup"><span data-stu-id="ba23f-146">This section of code shows the **Tab** Command declarations for a **Home** tab.</span></span>


```XML
<Command Name="cmdHomeTab"
         LabelTitle="Home"
         Keytip="H" />
<Command Name="cmdClipboardGroup"
         Symbol="IDR_CMD_CLIPBOARD"
         Id="10000"
         Comment="Command definition for clipboard group"
         LabelTitle="Clipboard"
         Keytip="CB" />
<Command Name="cmdCopy"
         Symbol="IDR_CMD_COPY"
         LabelTitle="Copy"
         LabelDescription="Copy"
         Keytip="C"
         TooltipTitle="Copy"
         TooltipDescription="Click to copy">
  <Command.SmallImages>
    <Image>res/copyS_16.bmp</Image>
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/copyL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdPaste"
         Symbol="IDR_CMD_PASTE" >
  <Command.LabelTitle>Paste</Command.LabelTitle>
  <Command.LabelDescription>
    <String Content="Paste contents of clipboard"
            Id="10001"
            Symbol="IDR_RES_LABELDESC_PASTE" />
  </Command.LabelDescription>
  <Command.Keytip>P</Command.Keytip>
  <Command.TooltipTitle>
    <String Content="Paste contents of clipboard"
            Id="10002"
            Symbol="IDR_RES_TOOLTIP_PASTE"/>
  </Command.TooltipTitle>
  <Command.TooltipDescription>
    <String Content="Click to paste contents of clipboard"/>
  </Command.TooltipDescription>
  <Command.SmallImages>
    <Image
      Id="10010"
      MinDPI="96"
      Symbol="IDR_RES_SMALL_IMAGE96">
      <Image.Source>res/pasteS_96bpp.bmp</Image.Source>
    </Image>
    <Image Source="res/pasteS_120bpp.bmp"
           Id="10011"
           MinDPI="120"
           Symbol="IDR_RES_SMALL_IMAGE120" />
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/pasteL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdMinimize"
         Symbol="IDR_CMD_MINIMIZE"
         Id="10001"
         LabelTitle="Minimize" />
```



<span data-ttu-id="ba23f-147">В этом разделе кода показаны объявления элементов управления **вкладки** .</span><span class="sxs-lookup"><span data-stu-id="ba23f-147">This section of code shows the **Tab** control declarations.</span></span>


```XML
<Tab CommandName="cmdHomeTab">
  <Group CommandName="cmdClipboardGroup" 
         SizeDefinition="ThreeButtons">
    <Button CommandName="cmdCopy"/>
    <Button CommandName="cmdPaste"/>
    <ToggleButton CommandName="cmdMinimize"/>
  </Group>
</Tab>
```



## <a name="element-information"></a><span data-ttu-id="ba23f-148">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ba23f-148">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="ba23f-149">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="ba23f-149">Minimum supported system</span></span><br/> | <span data-ttu-id="ba23f-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ba23f-150">Windows 7</span></span> |
| <span data-ttu-id="ba23f-151">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="ba23f-151">Can be empty</span></span>                        | <span data-ttu-id="ba23f-152">Нет</span><span class="sxs-lookup"><span data-stu-id="ba23f-152">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="ba23f-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba23f-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba23f-154">Элемент управления табуляции</span><span class="sxs-lookup"><span data-stu-id="ba23f-154">Tab control</span></span>](windowsribbon-controls-tab.md)
</dt> <dt>

[<span data-ttu-id="ba23f-155">Элемент управления группы вкладок</span><span class="sxs-lookup"><span data-stu-id="ba23f-155">Tab Group control</span></span>](windowsribbon-controls-tabgroup.md)
</dt> <dt>

[<span data-ttu-id="ba23f-156">**сетмодес**</span><span class="sxs-lookup"><span data-stu-id="ba23f-156">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

