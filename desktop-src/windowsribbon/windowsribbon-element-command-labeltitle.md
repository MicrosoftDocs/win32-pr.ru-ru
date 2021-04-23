---
title: Свойство Command. Лабелтитле
description: Представляет заголовок метки.
ms.assetid: 97378ec3-7988-4e39-9cf5-c382b246c5c9
keywords:
- Лента Windows для свойства Command. Лабелтитле
topic_type:
- apiref
api_name:
- Command.LabelTitle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed6d6c72ddd60cca63834fdcf21cf8f8b726ad22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535075"
---
# <a name="commandlabeltitle-property"></a><span data-ttu-id="89138-104">Свойство Command. Лабелтитле</span><span class="sxs-lookup"><span data-stu-id="89138-104">Command.LabelTitle property</span></span>

<span data-ttu-id="89138-105">Представляет заголовок метки.</span><span class="sxs-lookup"><span data-stu-id="89138-105">Represents a label title.</span></span>

## <a name="usage"></a><span data-ttu-id="89138-106">Использование</span><span class="sxs-lookup"><span data-stu-id="89138-106">Usage</span></span>

``` syntax
<Command.LabelTitle>
  child elements
</Command.LabelTitle>
```

## <a name="attributes"></a><span data-ttu-id="89138-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="89138-107">Attributes</span></span>

<span data-ttu-id="89138-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="89138-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="89138-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="89138-109">Child elements</span></span>



| <span data-ttu-id="89138-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="89138-110">Element</span></span>                                                   | <span data-ttu-id="89138-111">Описание</span><span class="sxs-lookup"><span data-stu-id="89138-111">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="89138-112">**Строка**</span><span class="sxs-lookup"><span data-stu-id="89138-112">**String**</span></span>](windowsribbon-element-string.md)<br/> | <span data-ttu-id="89138-113">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="89138-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="89138-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="89138-114">Parent elements</span></span>



| <span data-ttu-id="89138-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="89138-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="89138-116">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="89138-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="89138-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="89138-117">Remarks</span></span>

<span data-ttu-id="89138-118">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="89138-118">Optional.</span></span>

<span data-ttu-id="89138-119">Для каждой [**команды**](windowsribbon-element-command.md)может выполняться не более одного раза.</span><span class="sxs-lookup"><span data-stu-id="89138-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="89138-120">**Command. лабелтитле** может содержать значение типа *xs: String* , ограниченное любой последовательностью символов, включая пробелы и символы разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="89138-120">**Command.LabelTitle** can contain a value of type *xs:string* constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="89138-121">Используйте ссылку на символ XML универсальной кодировки (UCS) `&#xA;` для указания разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="89138-121">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="89138-122">Максимальная длина не ограничена.</span><span class="sxs-lookup"><span data-stu-id="89138-122">The maximum length is unbounded.</span></span>

<span data-ttu-id="89138-123">Если для **Command. лабелтитле** не указано значение, требуется дочерний элемент [**String**](windowsribbon-element-string.md) .</span><span class="sxs-lookup"><span data-stu-id="89138-123">If no value is supplied for **Command.LabelTitle**, the [**String**](windowsribbon-element-string.md) child element is required.</span></span>

> [!Note]  
> <span data-ttu-id="89138-124">Если **Command. лабелтитле** содержит как значение, так и дочерний элемент [**String**](windowsribbon-element-string.md) , то приоритет имеет **строка** .</span><span class="sxs-lookup"><span data-stu-id="89138-124">If **Command.LabelTitle** contains both a value and a [**String**](windowsribbon-element-string.md) child element, **String** takes precedence.</span></span>

 

<span data-ttu-id="89138-125">**Command. лабелтитле** поддерживает только выравнивание по левому краю.</span><span class="sxs-lookup"><span data-stu-id="89138-125">**Command.LabelTitle** only supports left alignment.</span></span>

<span data-ttu-id="89138-126">Если команда предоставляется через пункт меню, а значение **Command. лабелтитле** или [ \_ \_ подпись PKEY пользовательского интерфейса](windowsribbon-reference-properties-uipkey-label.md) содержит букву, предшествующую амперсанду, как показано в следующем примере, эта буква рассматривается как KeyTip и сочетание клавиш для этой команды в инфраструктуре Ribbon.</span><span class="sxs-lookup"><span data-stu-id="89138-126">If a Command is exposed through a menu item and the value of **Command.LabelTitle** or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md) contains a letter preceded by an ampersand, as shown in the following example, this letter is treated as both a keytip and a keyboard accelerator for that Command by the Ribbon framework.</span></span>


```XML
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
```



<span data-ttu-id="89138-127">Чтобы отобразить знак амперсанда в метке, необходимо экранировать Специальный символ с двойным амперсандом ( `&&` ), как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="89138-127">To display an ampersand in a label, escape the special character designation with a double ampersand (`&&`) as shown in the following example.</span></span>


```XML
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
```



## <a name="examples"></a><span data-ttu-id="89138-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="89138-128">Examples</span></span>

<span data-ttu-id="89138-129">В следующем примере показана разметка для элемента [**Command**](windowsribbon-element-command.md) с объявлением **Command. лабелтитле** .</span><span class="sxs-lookup"><span data-stu-id="89138-129">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.LabelTitle** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="89138-130">Требования</span><span class="sxs-lookup"><span data-stu-id="89138-130">Requirements</span></span>



| <span data-ttu-id="89138-131">Требование</span><span class="sxs-lookup"><span data-stu-id="89138-131">Requirement</span></span> | <span data-ttu-id="89138-132">Значение</span><span class="sxs-lookup"><span data-stu-id="89138-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="89138-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="89138-133">Minimum supported client</span></span><br/> | <span data-ttu-id="89138-134">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="89138-134">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="89138-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="89138-135">Minimum supported server</span></span><br/> | <span data-ttu-id="89138-136">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="89138-136">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="89138-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89138-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89138-138">\_Метка PKEY пользовательского интерфейса \_</span><span class="sxs-lookup"><span data-stu-id="89138-138">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)
</dt> </dl>

 

 





