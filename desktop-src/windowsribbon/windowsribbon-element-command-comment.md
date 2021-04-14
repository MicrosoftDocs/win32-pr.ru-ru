---
title: Свойство Command. Comment
description: Представляет комментарий или аннотацию для команды.
ms.assetid: 4ac5c7d4-9627-4703-bd3c-594d9497ba24
keywords:
- Лента Windows для свойства Command. Comment
topic_type:
- apiref
api_name:
- Command.Comment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f7df2131234623dd30fc90339634a932eca5bd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415993"
---
# <a name="commandcomment-property"></a><span data-ttu-id="98e19-104">Свойство Command. Comment</span><span class="sxs-lookup"><span data-stu-id="98e19-104">Command.Comment property</span></span>

<span data-ttu-id="98e19-105">Представляет комментарий или аннотацию для команды.</span><span class="sxs-lookup"><span data-stu-id="98e19-105">Represents a comment, or annotation, for a Command.</span></span>

## <a name="usage"></a><span data-ttu-id="98e19-106">Использование</span><span class="sxs-lookup"><span data-stu-id="98e19-106">Usage</span></span>

``` syntax
<Command.Comment/>
```

## <a name="attributes"></a><span data-ttu-id="98e19-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="98e19-107">Attributes</span></span>

<span data-ttu-id="98e19-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="98e19-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="98e19-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="98e19-109">Child elements</span></span>

<span data-ttu-id="98e19-110">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="98e19-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="98e19-111">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="98e19-111">Parent elements</span></span>



| <span data-ttu-id="98e19-112">Элемент</span><span class="sxs-lookup"><span data-stu-id="98e19-112">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="98e19-113">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="98e19-113">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="98e19-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="98e19-114">Remarks</span></span>

<span data-ttu-id="98e19-115">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="98e19-115">Optional.</span></span>

<span data-ttu-id="98e19-116">Для каждой [**команды**](windowsribbon-element-command.md)может выполняться не более одного раза.</span><span class="sxs-lookup"><span data-stu-id="98e19-116">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="98e19-117">Комментарий связан с определением команды в файле заголовка ленты, например `#define cmdSave 25003 /* Save */` .</span><span class="sxs-lookup"><span data-stu-id="98e19-117">The comment is associated with a Command definition in the Ribbon header file, for example, `#define cmdSave 25003 /* Save */`.</span></span>

<span data-ttu-id="98e19-118">Этот элемент содержит значение типа *xs: String*.</span><span class="sxs-lookup"><span data-stu-id="98e19-118">This element contains a value of type *xs:string*.</span></span>

<span data-ttu-id="98e19-119">Максимальная длина составляет 250 символов.</span><span class="sxs-lookup"><span data-stu-id="98e19-119">The maximum length is 250 characters.</span></span>

## <a name="examples"></a><span data-ttu-id="98e19-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="98e19-120">Examples</span></span>

<span data-ttu-id="98e19-121">В следующем примере показана разметка для элемента [**Command**](windowsribbon-element-command.md) с объявлением **Command. Comment** .</span><span class="sxs-lookup"><span data-stu-id="98e19-121">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Comment** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="98e19-122">Требования</span><span class="sxs-lookup"><span data-stu-id="98e19-122">Requirements</span></span>



| <span data-ttu-id="98e19-123">Требование</span><span class="sxs-lookup"><span data-stu-id="98e19-123">Requirement</span></span> | <span data-ttu-id="98e19-124">Значение</span><span class="sxs-lookup"><span data-stu-id="98e19-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="98e19-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="98e19-125">Minimum supported client</span></span><br/> | <span data-ttu-id="98e19-126">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="98e19-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="98e19-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="98e19-127">Minimum supported server</span></span><br/> | <span data-ttu-id="98e19-128">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="98e19-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





