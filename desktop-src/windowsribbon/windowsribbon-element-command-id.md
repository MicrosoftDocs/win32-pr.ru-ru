---
title: Command.Id, свойство
description: Представляет уникальный идентификатор для команды.
ms.assetid: 937ca9d6-6910-4133-9cfa-d7e3f895f876
keywords:
- Лента Windows для свойства Command.Id
topic_type:
- apiref
api_name:
- Command.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13e259e5fd74e3037afde3d4c001000b5a17a9bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492531"
---
# <a name="commandid-property"></a><span data-ttu-id="eb65d-104">Command.Id, свойство</span><span class="sxs-lookup"><span data-stu-id="eb65d-104">Command.Id property</span></span>

<span data-ttu-id="eb65d-105">Представляет уникальный идентификатор для команды.</span><span class="sxs-lookup"><span data-stu-id="eb65d-105">Represents a unique ID for a Command.</span></span>

## <a name="usage"></a><span data-ttu-id="eb65d-106">Использование</span><span class="sxs-lookup"><span data-stu-id="eb65d-106">Usage</span></span>

``` syntax
<Command.Id/>
```

## <a name="attributes"></a><span data-ttu-id="eb65d-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="eb65d-107">Attributes</span></span>

<span data-ttu-id="eb65d-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="eb65d-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="eb65d-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="eb65d-109">Child elements</span></span>

<span data-ttu-id="eb65d-110">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="eb65d-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="eb65d-111">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="eb65d-111">Parent elements</span></span>



| <span data-ttu-id="eb65d-112">Элемент</span><span class="sxs-lookup"><span data-stu-id="eb65d-112">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="eb65d-113">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="eb65d-113">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="eb65d-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eb65d-114">Remarks</span></span>

<span data-ttu-id="eb65d-115">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="eb65d-115">Optional.</span></span>

<span data-ttu-id="eb65d-116">Для каждой [**команды**](windowsribbon-element-command.md)может выполняться не более одного раза.</span><span class="sxs-lookup"><span data-stu-id="eb65d-116">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="eb65d-117">Идентификатор связан с определением команды в файле заголовка ленты, например `#define cmdSave 25003 /* Save */` .</span><span class="sxs-lookup"><span data-stu-id="eb65d-117">The ID is associated with a Command definition in the Ribbon header file, for example, `#define cmdSave 25003 /* Save */`.</span></span>

<span data-ttu-id="eb65d-118">Этот элемент содержит значение из объединения типов *xs: поситивеинтежер* и *xs: String* , ограничивающее целочисленное значение от 2 до 59999, включительно или 0x2 и 0xea5f в шестнадцатеричном виде включительно.</span><span class="sxs-lookup"><span data-stu-id="eb65d-118">This element contains a value from the union of types *xs:positiveInteger* and *xs:string* constrained to an integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span>

<span data-ttu-id="eb65d-119">Максимальная длина — 10 символов, включая необязательные нули в начале.</span><span class="sxs-lookup"><span data-stu-id="eb65d-119">The maximum length is 10 characters, including optional leading zeros.</span></span>

## <a name="examples"></a><span data-ttu-id="eb65d-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="eb65d-120">Examples</span></span>

<span data-ttu-id="eb65d-121">В следующем примере показана разметка для элемента [**Command**](windowsribbon-element-command.md) с объявлением **Command.ID** .</span><span class="sxs-lookup"><span data-stu-id="eb65d-121">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Id** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="eb65d-122">Требования</span><span class="sxs-lookup"><span data-stu-id="eb65d-122">Requirements</span></span>



| <span data-ttu-id="eb65d-123">Требование</span><span class="sxs-lookup"><span data-stu-id="eb65d-123">Requirement</span></span> | <span data-ttu-id="eb65d-124">Значение</span><span class="sxs-lookup"><span data-stu-id="eb65d-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="eb65d-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eb65d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="eb65d-126">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="eb65d-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="eb65d-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eb65d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="eb65d-128">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="eb65d-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





