---
title: Свойство Command. keytip
description: Представляет keytip для элемента управления.
ms.assetid: 214f69ae-dd35-4abf-b294-d898d7802aa6
keywords:
- Лента Windows для свойства Command. keytip
topic_type:
- apiref
api_name:
- Command.Keytip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab16b9b8e52094d6cdc85890dfc1cf8af63942c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701083"
---
# <a name="commandkeytip-property"></a><span data-ttu-id="1179a-104">Свойство Command. keytip</span><span class="sxs-lookup"><span data-stu-id="1179a-104">Command.Keytip property</span></span>

<span data-ttu-id="1179a-105">Представляет keytip для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="1179a-105">Represents the keytip for a control.</span></span>

## <a name="usage"></a><span data-ttu-id="1179a-106">Использование</span><span class="sxs-lookup"><span data-stu-id="1179a-106">Usage</span></span>

``` syntax
<Command.Keytip>
  child elements
</Command.Keytip>
```

## <a name="attributes"></a><span data-ttu-id="1179a-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1179a-107">Attributes</span></span>

<span data-ttu-id="1179a-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="1179a-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="1179a-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1179a-109">Child elements</span></span>



| <span data-ttu-id="1179a-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="1179a-110">Element</span></span>                                                   | <span data-ttu-id="1179a-111">Описание</span><span class="sxs-lookup"><span data-stu-id="1179a-111">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="1179a-112">**Строка**</span><span class="sxs-lookup"><span data-stu-id="1179a-112">**String**</span></span>](windowsribbon-element-string.md)<br/> | <span data-ttu-id="1179a-113">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="1179a-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="1179a-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="1179a-114">Parent elements</span></span>



| <span data-ttu-id="1179a-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="1179a-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="1179a-116">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="1179a-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="1179a-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1179a-117">Remarks</span></span>

<span data-ttu-id="1179a-118">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="1179a-118">Optional.</span></span>

<span data-ttu-id="1179a-119">Может встречаться не более одного раза для каждого элемента [**Command**](windowsribbon-element-command.md) .</span><span class="sxs-lookup"><span data-stu-id="1179a-119">May occur at most once for each [**Command**](windowsribbon-element-command.md) element.</span></span>

<span data-ttu-id="1179a-120">**Command. KeyTip** может содержать значение типа *xs: String* , ограниченное любой последовательностью символов Юникода, включая пробелы.</span><span class="sxs-lookup"><span data-stu-id="1179a-120">**Command.Keytip** can contain a value of type *xs:string* constrained to any sequence of Unicode characters, including white space.</span></span>

<span data-ttu-id="1179a-121">**Команда. KeyTip** может начинаться с числа, только если оно связано с элементом управления на [вкладке](windowsribbon-controls-tab.md) или на [панели быстрого доступа](windowsribbon-controls-quickaccesstoolbar.md).</span><span class="sxs-lookup"><span data-stu-id="1179a-121">A **Command.Keytip** can begin with a number only when associated with a control within a [Tab](windowsribbon-controls-tab.md) or the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md).</span></span>

<span data-ttu-id="1179a-122">Чтобы отобразить ключевые подсказки, допустимые для текущего состояния ленты, нажмите и удерживайте клавишу ALT.</span><span class="sxs-lookup"><span data-stu-id="1179a-122">To display the keytips that are valid for the current state of the ribbon, press and hold the ALT key.</span></span> <span data-ttu-id="1179a-123">На следующем снимке экрана показан первоначальный или первый уровень, которые отображаются в Microsoft Paint для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1179a-123">The following screen shot shows the initial, or first level, keytips that are displayed in Microsoft Paint for Windows 7.</span></span> <span data-ttu-id="1179a-124">После выбора KeyTip первого уровня отображаются только подсказки для второго уровня.</span><span class="sxs-lookup"><span data-stu-id="1179a-124">After a first-level keytip has been selected, only second-level keytips are displayed.</span></span>

![ключевые подсказки первого уровня в Microsoft Paint для Windows 7](images/properties/ui-pkey-label-keytips.png)

<span data-ttu-id="1179a-126">**Command. KeyTip** выступает в качестве сочетания клавиш для команды, если эта команда не предоставлена через пункт меню.</span><span class="sxs-lookup"><span data-stu-id="1179a-126">**Command.Keytip** acts as the keyboard accelerator for a command unless that command is exposed through a menu item.</span></span> <span data-ttu-id="1179a-127">В этом случае платформа игнорирует значение **Command. KeyTip** и вместо этого использует символ, предшествующий амперсанду, указанный параметром [**Command. лабелтитле**](windowsribbon-element-command-labeltitle.md) или [ \_ \_ подписью PKEY пользовательского интерфейса](windowsribbon-reference-properties-uipkey-label.md).</span><span class="sxs-lookup"><span data-stu-id="1179a-127">In this case, the framework ignores the **Command.Keytip** value and instead uses a character preceded by an ampersand as specified by [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md).</span></span> <span data-ttu-id="1179a-128">Если амперсанд не указан с помощью **команды Command. лабелтитле** или \_ метки PKEY пользовательского интерфейса \_ , то KeyTip или сочетания клавиш не предоставляются.</span><span class="sxs-lookup"><span data-stu-id="1179a-128">If no ampersand is specified by **Command.LabelTitle** or UI\_PKEY\_Label, no keytip or keyboard accelerator is exposed.</span></span>

<span data-ttu-id="1179a-129">Если для **Command. KeyTip** не указано значение, требуется дочерний элемент [**String**](windowsribbon-element-string.md) .</span><span class="sxs-lookup"><span data-stu-id="1179a-129">If no value is supplied for **Command.Keytip**, the [**String**](windowsribbon-element-string.md) child element is required.</span></span>

> [!Note]  
> <span data-ttu-id="1179a-130">Если **Command. KeyTip** содержит как значение, так и дочерний элемент [**String**](windowsribbon-element-string.md) , то приоритет имеет **строка** .</span><span class="sxs-lookup"><span data-stu-id="1179a-130">If **Command.Keytip** contains both a value and a [**String**](windowsribbon-element-string.md) child element, **String** takes precedence.</span></span>

 

<span data-ttu-id="1179a-131">По умолчанию платформа использует следующие буквы для автоматического создания подсказок:</span><span class="sxs-lookup"><span data-stu-id="1179a-131">By default, the following letters are used by the framework to automatically generate keytips:</span></span>

-   <span data-ttu-id="1179a-132">**F** назначается [меню приложение](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="1179a-132">**F** is assigned to the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>
-   <span data-ttu-id="1179a-133">**Y** назначается любой команде, не имеющей KeyTip, указанной приложением.</span><span class="sxs-lookup"><span data-stu-id="1179a-133">**Y** is assigned to any command that does not have a keytip specified by the application.</span></span>
-   <span data-ttu-id="1179a-134">**Z** назначается каждому элементу управления [группы](windowsribbon-controls-group.md) и не может быть настроено.</span><span class="sxs-lookup"><span data-stu-id="1179a-134">**Z** is assigned to each [Group](windowsribbon-controls-group.md) control and cannot be customized.</span></span> <span data-ttu-id="1179a-135">Группа KeyTip отображается, только если [**скалингполици**](windowsribbon-element-scalingpolicy.md) элемента управления указывает параметр размера **всплывающего окна** .</span><span class="sxs-lookup"><span data-stu-id="1179a-135">A Group keytip is displayed only when the [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) for the control specifies a **Popup** size option.</span></span> <span data-ttu-id="1179a-136">Дополнительные сведения см. в разделе [Настройка ленты с помощью определений размеров и политик масштабирования](windowsribbon-templates.md).</span><span class="sxs-lookup"><span data-stu-id="1179a-136">For more information, see [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>

> [!Note]  
> <span data-ttu-id="1179a-137">Ни одна из этих букв не зарезервирована платформой.</span><span class="sxs-lookup"><span data-stu-id="1179a-137">None of these letters are reserved by the framework.</span></span> <span data-ttu-id="1179a-138">Каждый из них может быть назначен одной или нескольким командам по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="1179a-138">Each can be assigned to one or more commands as required.</span></span>

 

<span data-ttu-id="1179a-139">Платформа разрешает конфликты KeyTip следующими способами:</span><span class="sxs-lookup"><span data-stu-id="1179a-139">The framework resolves keytip conflicts in the following ways:</span></span>

-   <span data-ttu-id="1179a-140">Если один или несколько элементов управления ["Вкладка"](windowsribbon-controls-tab.md) связаны с одним и тем же KeyTip, к каждому keytipу добавляется число, начиная с 1 и последовательно увеличивая (2, 3,...) для каждого элемента управления в порядке объявления.</span><span class="sxs-lookup"><span data-stu-id="1179a-140">If one or more [Tab](windowsribbon-controls-tab.md) controls are associated with the same keytip, a number is appended to each keytip, starting at 1, and increasing sequentially (2, 3,...) for each control in the order of declaration.</span></span> <span data-ttu-id="1179a-141">Если любому элементу управления вкладки назначена буква F как KeyTip, [меню приложения](windowsribbon-controls-applicationmenu.md) назначается F1 с остальными подклавишами, скорректированными согласно описанию.</span><span class="sxs-lookup"><span data-stu-id="1179a-141">If any Tab controls are assigned the letter F as a keytip, the [Application Menu](windowsribbon-controls-applicationmenu.md) is assigned F1 with the remaining keytips adjusted as described.</span></span>
-   <span data-ttu-id="1179a-142">При сопоставлении с одним элементом управления на [вкладке](windowsribbon-controls-tab.md)KeyTip F допустим как для элемента управления, так и для [меню приложения](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="1179a-142">When associated with a single control within a [Tab](windowsribbon-controls-tab.md), the keytip F is valid for both the control and the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span> <span data-ttu-id="1179a-143">Меню приложения по умолчанию KeyTip не изменяется, но для элемента управления на активной вкладке приоритет передается.</span><span class="sxs-lookup"><span data-stu-id="1179a-143">The default Application Menu keytip is not changed, but precedence is given to the control on the active tab.</span></span>
-   <span data-ttu-id="1179a-144">Если один или несколько элементов управления на [вкладке](windowsribbon-controls-tab.md) связаны с одним и тем же KeyTip, платформа автоматически переопределяет ключевые подсказки этих элементов управления, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="1179a-144">If one or more controls within a [Tab](windowsribbon-controls-tab.md) are associated with the same keytip, the framework automatically refactors the keytips of those controls, as described previously.</span></span>

> [!Note]  
> <span data-ttu-id="1179a-145">Небольшая разновидность цвета текста используется для выделения рефакторинга подсказок в стандартной реализации ленты.</span><span class="sxs-lookup"><span data-stu-id="1179a-145">A slight variation in text color is used to highlight refactored keytips in a standard ribbon implementation.</span></span> <span data-ttu-id="1179a-146">Для нестандартной реализации ленты, в которой настроен цвет ленты, это поведение платформы переопределяется и все подсказки отображаются с тем же цветом текста.</span><span class="sxs-lookup"><span data-stu-id="1179a-146">For a nonstandard ribbon implementation where the ribbon color has been customized, this framework behavior is overridden and all keytips are displayed with the same text color.</span></span> <span data-ttu-id="1179a-147">Дополнительные сведения см. в разделе [Настройка цветов ленты](ribbon-color.md).</span><span class="sxs-lookup"><span data-stu-id="1179a-147">For more information, see [Customizing Ribbon Colors](ribbon-color.md).</span></span>

 

<span data-ttu-id="1179a-148">Максимальная длина не ограничена.</span><span class="sxs-lookup"><span data-stu-id="1179a-148">The maximum length is unbounded.</span></span>

## <a name="examples"></a><span data-ttu-id="1179a-149">Примеры</span><span class="sxs-lookup"><span data-stu-id="1179a-149">Examples</span></span>

<span data-ttu-id="1179a-150">В следующем примере показана разметка для элемента [**Command**](windowsribbon-element-command.md) с объявлением **Command. KeyTip** .</span><span class="sxs-lookup"><span data-stu-id="1179a-150">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Keytip** declaration.</span></span>


```XML
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
```



## <a name="requirements"></a><span data-ttu-id="1179a-151">Требования</span><span class="sxs-lookup"><span data-stu-id="1179a-151">Requirements</span></span>



| <span data-ttu-id="1179a-152">Требование</span><span class="sxs-lookup"><span data-stu-id="1179a-152">Requirement</span></span> | <span data-ttu-id="1179a-153">Значение</span><span class="sxs-lookup"><span data-stu-id="1179a-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="1179a-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1179a-154">Minimum supported client</span></span><br/> | <span data-ttu-id="1179a-155">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1179a-155">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="1179a-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1179a-156">Minimum supported server</span></span><br/> | <span data-ttu-id="1179a-157">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1179a-157">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1179a-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1179a-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1179a-159">UI \_ PKEY \_ keytip</span><span class="sxs-lookup"><span data-stu-id="1179a-159">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)
</dt> </dl>

 

 





