---
title: Свойство Command. Symbol
description: Представляет имя команды, на которую можно ссылаться извне.
ms.assetid: affa5f3f-f641-4bec-9165-6102509cf355
keywords:
- Лента Windows для свойства Command. Symbol
topic_type:
- apiref
api_name:
- Command.Symbol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b88dccb71a90feca7348ca9731ca5966b012c9c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701078"
---
# <a name="commandsymbol-property"></a><span data-ttu-id="9fbe7-104">Свойство Command. Symbol</span><span class="sxs-lookup"><span data-stu-id="9fbe7-104">Command.Symbol property</span></span>

<span data-ttu-id="9fbe7-105">Представляет имя [**команды**](windowsribbon-element-command.md) , на которую можно ссылаться извне.</span><span class="sxs-lookup"><span data-stu-id="9fbe7-105">Represents the name of a [**Command**](windowsribbon-element-command.md) that can be referenced externally.</span></span>

## <a name="usage"></a><span data-ttu-id="9fbe7-106">Использование</span><span class="sxs-lookup"><span data-stu-id="9fbe7-106">Usage</span></span>

``` syntax
<Command.Symbol/>
```

## <a name="attributes"></a><span data-ttu-id="9fbe7-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="9fbe7-107">Attributes</span></span>

<span data-ttu-id="9fbe7-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="9fbe7-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="9fbe7-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9fbe7-109">Child elements</span></span>

<span data-ttu-id="9fbe7-110">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="9fbe7-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="9fbe7-111">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="9fbe7-111">Parent elements</span></span>



| <span data-ttu-id="9fbe7-112">Элемент</span><span class="sxs-lookup"><span data-stu-id="9fbe7-112">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="9fbe7-113">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="9fbe7-113">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="9fbe7-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9fbe7-114">Remarks</span></span>

<span data-ttu-id="9fbe7-115">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="9fbe7-115">Optional.</span></span>

<span data-ttu-id="9fbe7-116">Для каждой [**команды**](windowsribbon-element-command.md)может выполняться не более одного раза.</span><span class="sxs-lookup"><span data-stu-id="9fbe7-116">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="9fbe7-117">Символ связан с определением команды в файле заголовка ленты, например `#define cmdSave 25003 /* Save */` .</span><span class="sxs-lookup"><span data-stu-id="9fbe7-117">The symbol is associated with a Command definition in the Ribbon header file, for example, `#define cmdSave 25003 /* Save */`.</span></span>

<span data-ttu-id="9fbe7-118">Этот элемент содержит значение типа *xs: String*.</span><span class="sxs-lookup"><span data-stu-id="9fbe7-118">This element contains a value of type *xs:string*.</span></span>

<span data-ttu-id="9fbe7-119">Значение ограничено строкой, состоящей из буквы или символа подчеркивания, за которой следует любая последовательность букв, цифр и знаков подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="9fbe7-119">The value is constrained to a string that consists of a letter or underscore followed by any sequence of letters, digits, and underscores.</span></span>

<span data-ttu-id="9fbe7-120">Максимальная длина — 100 символов.</span><span class="sxs-lookup"><span data-stu-id="9fbe7-120">The maximum length is 100 characters.</span></span>

## <a name="examples"></a><span data-ttu-id="9fbe7-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="9fbe7-121">Examples</span></span>

<span data-ttu-id="9fbe7-122">В следующем примере показана разметка для элемента [**Command**](windowsribbon-element-command.md) с объявлением **команды. Symbol** .</span><span class="sxs-lookup"><span data-stu-id="9fbe7-122">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Symbol** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="9fbe7-123">Требования</span><span class="sxs-lookup"><span data-stu-id="9fbe7-123">Requirements</span></span>



| <span data-ttu-id="9fbe7-124">Требование</span><span class="sxs-lookup"><span data-stu-id="9fbe7-124">Requirement</span></span> | <span data-ttu-id="9fbe7-125">Значение</span><span class="sxs-lookup"><span data-stu-id="9fbe7-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="9fbe7-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9fbe7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9fbe7-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9fbe7-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="9fbe7-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9fbe7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9fbe7-129">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9fbe7-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





