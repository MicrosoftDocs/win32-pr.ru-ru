---
title: Свойство Command. Тултипдескриптион
description: Представляет описание подсказки.
ms.assetid: 2d3ea497-2d96-4420-8fcf-39ac2c472bf1
keywords:
- Лента Windows для свойства Command. Тултипдескриптион
topic_type:
- apiref
api_name:
- Command.TooltipDescription
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 288578e74420912b7454be5037c4b2651918ac6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701077"
---
# <a name="commandtooltipdescription-property"></a><span data-ttu-id="cc53e-104">Свойство Command. Тултипдескриптион</span><span class="sxs-lookup"><span data-stu-id="cc53e-104">Command.TooltipDescription property</span></span>

<span data-ttu-id="cc53e-105">Представляет описание подсказки.</span><span class="sxs-lookup"><span data-stu-id="cc53e-105">Represents a tooltip description.</span></span>

## <a name="usage"></a><span data-ttu-id="cc53e-106">Использование</span><span class="sxs-lookup"><span data-stu-id="cc53e-106">Usage</span></span>

``` syntax
<Command.TooltipDescription>
  child elements
</Command.TooltipDescription>
```

## <a name="attributes"></a><span data-ttu-id="cc53e-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="cc53e-107">Attributes</span></span>

<span data-ttu-id="cc53e-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="cc53e-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="cc53e-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="cc53e-109">Child elements</span></span>



| <span data-ttu-id="cc53e-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="cc53e-110">Element</span></span>                                                   | <span data-ttu-id="cc53e-111">Описание</span><span class="sxs-lookup"><span data-stu-id="cc53e-111">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="cc53e-112">**Строка**</span><span class="sxs-lookup"><span data-stu-id="cc53e-112">**String**</span></span>](windowsribbon-element-string.md)<br/> | <span data-ttu-id="cc53e-113">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="cc53e-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="cc53e-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="cc53e-114">Parent elements</span></span>



| <span data-ttu-id="cc53e-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="cc53e-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="cc53e-116">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="cc53e-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="cc53e-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cc53e-117">Remarks</span></span>

<span data-ttu-id="cc53e-118">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="cc53e-118">Optional.</span></span>

<span data-ttu-id="cc53e-119">Для каждой [**команды**](windowsribbon-element-command.md)может выполняться не более одного раза.</span><span class="sxs-lookup"><span data-stu-id="cc53e-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="cc53e-120">**Command. тултипдескриптион** может содержать значение типа *xs: String* , ограниченное любой последовательностью символов, включая пробелы и символы разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="cc53e-120">**Command.TooltipDescription** can contain a value of type *xs:string* constrained to any sequence of characters, including white space and line-break characters .</span></span>

> [!Note]  
> <span data-ttu-id="cc53e-121">Используйте ссылку на символ XML универсальной кодировки (UCS) `&#xA;` для указания разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="cc53e-121">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="cc53e-122">Максимальная длина не ограничена.</span><span class="sxs-lookup"><span data-stu-id="cc53e-122">The maximum length is unbounded.</span></span>

<span data-ttu-id="cc53e-123">Если для **Command. тултипдескриптион** не указано значение, требуется дочерний элемент [**String**](windowsribbon-element-string.md) .</span><span class="sxs-lookup"><span data-stu-id="cc53e-123">If no value is supplied for **Command.TooltipDescription**, the [**String**](windowsribbon-element-string.md) child element is required.</span></span>

> [!Note]  
> <span data-ttu-id="cc53e-124">Если **Command. тултипдескриптион** содержит как значение, так и дочерний элемент [**String**](windowsribbon-element-string.md) , то приоритет имеет **строка** .</span><span class="sxs-lookup"><span data-stu-id="cc53e-124">If **Command.TooltipDescription** contains both a value and a [**String**](windowsribbon-element-string.md) child element, **String** takes precedence.</span></span>

 

<span data-ttu-id="cc53e-125">**Command. тултипдескриптион** поддерживает только выравнивание по левому краю.</span><span class="sxs-lookup"><span data-stu-id="cc53e-125">**Command.TooltipDescription** only supports left alignment.</span></span>

## <a name="examples"></a><span data-ttu-id="cc53e-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="cc53e-126">Examples</span></span>

<span data-ttu-id="cc53e-127">В следующем примере показана разметка для элемента [**Command**](windowsribbon-element-command.md) с объявлением **Command. тултипдескриптион** .</span><span class="sxs-lookup"><span data-stu-id="cc53e-127">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.TooltipDescription** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="cc53e-128">Требования</span><span class="sxs-lookup"><span data-stu-id="cc53e-128">Requirements</span></span>



| <span data-ttu-id="cc53e-129">Требование</span><span class="sxs-lookup"><span data-stu-id="cc53e-129">Requirement</span></span> | <span data-ttu-id="cc53e-130">Значение</span><span class="sxs-lookup"><span data-stu-id="cc53e-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="cc53e-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cc53e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="cc53e-132">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="cc53e-132">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="cc53e-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cc53e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="cc53e-134">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="cc53e-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cc53e-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc53e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc53e-136">UI \_ PKEY \_ тултипдескриптион</span><span class="sxs-lookup"><span data-stu-id="cc53e-136">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md)
</dt> </dl>

 

 





