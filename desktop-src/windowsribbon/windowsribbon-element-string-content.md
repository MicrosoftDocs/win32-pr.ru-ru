---
title: Свойство String. Content
description: Представляет содержимое строкового ресурса.
ms.assetid: 86f34cdc-1311-4f52-979f-201d71bbb9e9
keywords:
- Лента Windows свойства String. Content
topic_type:
- apiref
api_name:
- String.Content
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8912264e4f55568c190212227d2e305f9d676a1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701035"
---
# <a name="stringcontent-property"></a><span data-ttu-id="28b62-104">Свойство String. Content</span><span class="sxs-lookup"><span data-stu-id="28b62-104">String.Content property</span></span>

<span data-ttu-id="28b62-105">Представляет содержимое строкового ресурса.</span><span class="sxs-lookup"><span data-stu-id="28b62-105">Represents the content of a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="28b62-106">Использование</span><span class="sxs-lookup"><span data-stu-id="28b62-106">Usage</span></span>

``` syntax
<String.Content/>
```

## <a name="attributes"></a><span data-ttu-id="28b62-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="28b62-107">Attributes</span></span>

<span data-ttu-id="28b62-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="28b62-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="28b62-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="28b62-109">Child elements</span></span>

<span data-ttu-id="28b62-110">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="28b62-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="28b62-111">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="28b62-111">Parent elements</span></span>



| <span data-ttu-id="28b62-112">Элемент</span><span class="sxs-lookup"><span data-stu-id="28b62-112">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="28b62-113">**Строка**</span><span class="sxs-lookup"><span data-stu-id="28b62-113">**String**</span></span>](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="28b62-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="28b62-114">Remarks</span></span>

<span data-ttu-id="28b62-115">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="28b62-115">Optional.</span></span>

<span data-ttu-id="28b62-116">Может встречаться не более одного раза для каждого элемента [**строки**](windowsribbon-element-string.md) .</span><span class="sxs-lookup"><span data-stu-id="28b62-116">May occur at most once for each [**String**](windowsribbon-element-string.md) element.</span></span>

<span data-ttu-id="28b62-117">Этот элемент содержит значение типа *xs: String*.</span><span class="sxs-lookup"><span data-stu-id="28b62-117">This element contains a value of type *xs:string*.</span></span> <span data-ttu-id="28b62-118">Значение ограничено строкой, состоящей из любой последовательности символов, включая пробелы и символы разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="28b62-118">The value is constrained to a string composed of any sequence of characters, including white space and line-break characters.</span></span>

<span data-ttu-id="28b62-119">Максимальная длина не ограничена.</span><span class="sxs-lookup"><span data-stu-id="28b62-119">The maximum length is unbounded.</span></span>

## <a name="examples"></a><span data-ttu-id="28b62-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="28b62-120">Examples</span></span>

<span data-ttu-id="28b62-121">В следующем примере показана разметка для элемента [**Command. лабелтитле**](windowsribbon-element-command-labeltitle.md) с объявлением **String. Content** .</span><span class="sxs-lookup"><span data-stu-id="28b62-121">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String.Content** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="requirements"></a><span data-ttu-id="28b62-122">Требования</span><span class="sxs-lookup"><span data-stu-id="28b62-122">Requirements</span></span>



| <span data-ttu-id="28b62-123">Требование</span><span class="sxs-lookup"><span data-stu-id="28b62-123">Requirement</span></span> | <span data-ttu-id="28b62-124">Значение</span><span class="sxs-lookup"><span data-stu-id="28b62-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="28b62-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="28b62-125">Minimum supported client</span></span><br/> | <span data-ttu-id="28b62-126">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="28b62-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="28b62-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="28b62-127">Minimum supported server</span></span><br/> | <span data-ttu-id="28b62-128">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="28b62-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





