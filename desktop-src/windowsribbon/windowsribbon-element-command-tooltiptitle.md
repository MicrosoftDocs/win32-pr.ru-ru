---
title: Свойство Command. Тултиптитле
description: Представляет заголовок подсказки.
ms.assetid: b06a7a6a-fbdd-464b-b804-e62912d6e176
keywords:
- Лента Windows для свойства Command. Тултиптитле
topic_type:
- apiref
api_name:
- Command.TooltipTitle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c60f4ddea77fbf88a15d5d27e90ca5660bc0edb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492510"
---
# <a name="commandtooltiptitle-property"></a><span data-ttu-id="26782-104">Свойство Command. Тултиптитле</span><span class="sxs-lookup"><span data-stu-id="26782-104">Command.TooltipTitle property</span></span>

<span data-ttu-id="26782-105">Представляет заголовок подсказки.</span><span class="sxs-lookup"><span data-stu-id="26782-105">Represents a tooltip title.</span></span>

## <a name="usage"></a><span data-ttu-id="26782-106">Использование</span><span class="sxs-lookup"><span data-stu-id="26782-106">Usage</span></span>

``` syntax
<Command.TooltipTitle>
  child elements
</Command.TooltipTitle>
```

## <a name="attributes"></a><span data-ttu-id="26782-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="26782-107">Attributes</span></span>

<span data-ttu-id="26782-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="26782-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="26782-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="26782-109">Child elements</span></span>



| <span data-ttu-id="26782-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="26782-110">Element</span></span>                                                   | <span data-ttu-id="26782-111">Описание</span><span class="sxs-lookup"><span data-stu-id="26782-111">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="26782-112">**Строка**</span><span class="sxs-lookup"><span data-stu-id="26782-112">**String**</span></span>](windowsribbon-element-string.md)<br/> | <span data-ttu-id="26782-113">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="26782-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="26782-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="26782-114">Parent elements</span></span>



| <span data-ttu-id="26782-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="26782-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="26782-116">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="26782-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="26782-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="26782-117">Remarks</span></span>

<span data-ttu-id="26782-118">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="26782-118">Optional.</span></span>

<span data-ttu-id="26782-119">Для каждой [**команды**](windowsribbon-element-command.md)может выполняться не более одного раза.</span><span class="sxs-lookup"><span data-stu-id="26782-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="26782-120">**Command. тултиптитле** может содержать значение типа *xs: String* , ограниченное любой последовательностью символов, включая пробелы и символы разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="26782-120">**Command.TooltipTitle** can contain a value of type *xs:string* constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="26782-121">Используйте ссылку на символ XML универсальной кодировки (UCS) `&#xA;` для указания разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="26782-121">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="26782-122">Максимальная длина не ограничена.</span><span class="sxs-lookup"><span data-stu-id="26782-122">The maximum length is unbounded.</span></span>

<span data-ttu-id="26782-123">Если для **Command. тултиптитле** не указано значение, требуется дочерний элемент [**String**](windowsribbon-element-string.md) .</span><span class="sxs-lookup"><span data-stu-id="26782-123">If no value is supplied for **Command.TooltipTitle**, the [**String**](windowsribbon-element-string.md) child element is required.</span></span>

> [!Note]  
> <span data-ttu-id="26782-124">Если **Command. тултиптитле** содержит как значение, так и дочерний элемент [**String**](windowsribbon-element-string.md) , то приоритет имеет **строка** .</span><span class="sxs-lookup"><span data-stu-id="26782-124">If **Command.TooltipTitle** contains both a value and a [**String**](windowsribbon-element-string.md) child element, **String** takes precedence.</span></span>

 

<span data-ttu-id="26782-125">**Command. тултиптитле** поддерживает только выравнивание по левому краю.</span><span class="sxs-lookup"><span data-stu-id="26782-125">**Command.TooltipTitle** only supports left alignment.</span></span>

## <a name="examples"></a><span data-ttu-id="26782-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="26782-126">Examples</span></span>

<span data-ttu-id="26782-127">В следующем примере показана разметка для элемента [**Command**](windowsribbon-element-command.md) с объявлением **Command. тултиптитле** .</span><span class="sxs-lookup"><span data-stu-id="26782-127">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.TooltipTitle** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="26782-128">Требования</span><span class="sxs-lookup"><span data-stu-id="26782-128">Requirements</span></span>



| <span data-ttu-id="26782-129">Требование</span><span class="sxs-lookup"><span data-stu-id="26782-129">Requirement</span></span> | <span data-ttu-id="26782-130">Значение</span><span class="sxs-lookup"><span data-stu-id="26782-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="26782-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="26782-131">Minimum supported client</span></span><br/> | <span data-ttu-id="26782-132">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="26782-132">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="26782-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="26782-133">Minimum supported server</span></span><br/> | <span data-ttu-id="26782-134">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="26782-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="26782-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26782-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26782-136">UI \_ PKEY \_ тултиптитле</span><span class="sxs-lookup"><span data-stu-id="26782-136">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)
</dt> </dl>

 

 





