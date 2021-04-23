---
title: Свойство String. Symbol
description: Представляет имя строкового ресурса.
ms.assetid: 7c1d0197-2c9b-4f42-afba-73fd1c366deb
keywords:
- Лента для свойства String. Symbol
topic_type:
- apiref
api_name:
- String.Symbol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7bf7d30ddd8677b1c5ff0a5e55d4b9c119795ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891525"
---
# <a name="stringsymbol-property"></a><span data-ttu-id="a385b-104">Свойство String. Symbol</span><span class="sxs-lookup"><span data-stu-id="a385b-104">String.Symbol property</span></span>

<span data-ttu-id="a385b-105">Представляет имя строкового ресурса.</span><span class="sxs-lookup"><span data-stu-id="a385b-105">Represents the name of a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="a385b-106">Использование</span><span class="sxs-lookup"><span data-stu-id="a385b-106">Usage</span></span>

``` syntax
<String.Symbol/>
```

## <a name="attributes"></a><span data-ttu-id="a385b-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a385b-107">Attributes</span></span>

<span data-ttu-id="a385b-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="a385b-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a385b-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a385b-109">Child elements</span></span>

<span data-ttu-id="a385b-110">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="a385b-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="a385b-111">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="a385b-111">Parent elements</span></span>



| <span data-ttu-id="a385b-112">Элемент</span><span class="sxs-lookup"><span data-stu-id="a385b-112">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="a385b-113">**Строка**</span><span class="sxs-lookup"><span data-stu-id="a385b-113">**String**</span></span>](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="a385b-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a385b-114">Remarks</span></span>

<span data-ttu-id="a385b-115">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="a385b-115">Optional.</span></span>

<span data-ttu-id="a385b-116">Может встречаться не более одного раза для каждого элемента [**строки**](windowsribbon-element-string.md) .</span><span class="sxs-lookup"><span data-stu-id="a385b-116">May occur at most once for each [**String**](windowsribbon-element-string.md) element.</span></span>

<span data-ttu-id="a385b-117">Символ связан с определением строки в файле заголовка ленты, например `#define strSave 59999` .</span><span class="sxs-lookup"><span data-stu-id="a385b-117">The symbol is associated with a string definition in the Ribbon header file, for example, `#define strSave 59999`.</span></span>

<span data-ttu-id="a385b-118">Этот элемент содержит значение типа *xs: String*.</span><span class="sxs-lookup"><span data-stu-id="a385b-118">This element contains a value of type *xs:string*.</span></span> <span data-ttu-id="a385b-119">Значение ограничивается строкой, состоящей из буквы или символа подчеркивания, за которой следует любая последовательность букв, цифр или знаков подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="a385b-119">The value is constrained to a string composed of a letter or underscore followed by any sequence of letters, digits, or underscores.</span></span>

<span data-ttu-id="a385b-120">Максимальная длина — 100 символов.</span><span class="sxs-lookup"><span data-stu-id="a385b-120">The maximum length is 100 characters.</span></span>

## <a name="examples"></a><span data-ttu-id="a385b-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="a385b-121">Examples</span></span>

<span data-ttu-id="a385b-122">В следующем примере показана разметка для элемента [**Command. лабелтитле**](windowsribbon-element-command-labeltitle.md) с объявлением **String. Symbol** .</span><span class="sxs-lookup"><span data-stu-id="a385b-122">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String.Symbol** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="requirements"></a><span data-ttu-id="a385b-123">Требования</span><span class="sxs-lookup"><span data-stu-id="a385b-123">Requirements</span></span>



| <span data-ttu-id="a385b-124">Требование</span><span class="sxs-lookup"><span data-stu-id="a385b-124">Requirement</span></span> | <span data-ttu-id="a385b-125">Значение</span><span class="sxs-lookup"><span data-stu-id="a385b-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="a385b-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a385b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a385b-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a385b-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="a385b-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a385b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a385b-129">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a385b-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





