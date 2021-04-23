---
title: Command.Name, свойство
description: Представляет имя команды.
ms.assetid: 36fb0b93-143f-4706-8c32-e6c818cce16f
keywords:
- Лента Windows для свойства Command.Name
topic_type:
- apiref
api_name:
- Command.Name
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d93b830e29ca271052a4693b00ba64eee94309f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071918"
---
# <a name="commandname-property"></a><span data-ttu-id="abffd-104">Command.Name, свойство</span><span class="sxs-lookup"><span data-stu-id="abffd-104">Command.Name property</span></span>

<span data-ttu-id="abffd-105">Представляет имя команды.</span><span class="sxs-lookup"><span data-stu-id="abffd-105">Represents the name of a Command.</span></span>

## <a name="usage"></a><span data-ttu-id="abffd-106">Использование</span><span class="sxs-lookup"><span data-stu-id="abffd-106">Usage</span></span>

``` syntax
<Command.Name/>
```

## <a name="attributes"></a><span data-ttu-id="abffd-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="abffd-107">Attributes</span></span>

<span data-ttu-id="abffd-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="abffd-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="abffd-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="abffd-109">Child elements</span></span>

<span data-ttu-id="abffd-110">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="abffd-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="abffd-111">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="abffd-111">Parent elements</span></span>



| <span data-ttu-id="abffd-112">Элемент</span><span class="sxs-lookup"><span data-stu-id="abffd-112">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="abffd-113">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="abffd-113">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="abffd-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="abffd-114">Remarks</span></span>

<span data-ttu-id="abffd-115">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="abffd-115">Optional.</span></span>

<span data-ttu-id="abffd-116">Для каждой [**команды**](windowsribbon-element-command.md)может выполняться не более одного раза.</span><span class="sxs-lookup"><span data-stu-id="abffd-116">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="abffd-117">На **Command.Name** имеется ссылка в разметке для связывания команды с элементом управления через атрибут *CommandName* элемента управления.</span><span class="sxs-lookup"><span data-stu-id="abffd-117">**Command.Name** is referenced in markup to associate a Command with a control through the *CommandName* attribute of the control.</span></span>

<span data-ttu-id="abffd-118">Этот элемент содержит значение типа *xs: String*.</span><span class="sxs-lookup"><span data-stu-id="abffd-118">This element contains a value of type *xs:string*.</span></span>

<span data-ttu-id="abffd-119">Значение ограничено строкой, состоящей из буквы или символа подчеркивания, за которой следует любая последовательность букв, цифр и знаков подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="abffd-119">The value is constrained to a string that consists of a letter or underscore followed by any sequence of letters, digits, and underscores.</span></span>

<span data-ttu-id="abffd-120">Максимальная длина — 100 символов.</span><span class="sxs-lookup"><span data-stu-id="abffd-120">The maximum length is 100 characters.</span></span>

## <a name="examples"></a><span data-ttu-id="abffd-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="abffd-121">Examples</span></span>

<span data-ttu-id="abffd-122">В следующем примере показана разметка для элемента [**Command**](windowsribbon-element-command.md) с объявлением **Command.Name** .</span><span class="sxs-lookup"><span data-stu-id="abffd-122">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Name** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="abffd-123">Требования</span><span class="sxs-lookup"><span data-stu-id="abffd-123">Requirements</span></span>



| <span data-ttu-id="abffd-124">Требование</span><span class="sxs-lookup"><span data-stu-id="abffd-124">Requirement</span></span> | <span data-ttu-id="abffd-125">Значение</span><span class="sxs-lookup"><span data-stu-id="abffd-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="abffd-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="abffd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="abffd-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="abffd-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="abffd-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="abffd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="abffd-129">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="abffd-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





