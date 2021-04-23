---
title: String.Id, свойство
description: Представляет уникальный идентификатор строкового ресурса.
ms.assetid: 393da279-bdf6-4796-a546-1931cbe49113
keywords:
- Лента Windows для свойства String.Id
topic_type:
- apiref
api_name:
- String.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3ab87327ed4f11a901fb8a201e72137ab62c7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137194"
---
# <a name="stringid-property"></a><span data-ttu-id="36537-104">String.Id, свойство</span><span class="sxs-lookup"><span data-stu-id="36537-104">String.Id property</span></span>

<span data-ttu-id="36537-105">Представляет уникальный идентификатор строкового ресурса.</span><span class="sxs-lookup"><span data-stu-id="36537-105">Represents the unique ID of a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="36537-106">Использование</span><span class="sxs-lookup"><span data-stu-id="36537-106">Usage</span></span>

``` syntax
<String.Id/>
```

## <a name="attributes"></a><span data-ttu-id="36537-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="36537-107">Attributes</span></span>

<span data-ttu-id="36537-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="36537-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="36537-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="36537-109">Child elements</span></span>

<span data-ttu-id="36537-110">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="36537-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="36537-111">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="36537-111">Parent elements</span></span>



| <span data-ttu-id="36537-112">Элемент</span><span class="sxs-lookup"><span data-stu-id="36537-112">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="36537-113">**Строка**</span><span class="sxs-lookup"><span data-stu-id="36537-113">**String**</span></span>](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="36537-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36537-114">Remarks</span></span>

<span data-ttu-id="36537-115">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="36537-115">Optional.</span></span>

<span data-ttu-id="36537-116">Может встречаться не более одного раза для каждого элемента [**строки**](windowsribbon-element-string.md) .</span><span class="sxs-lookup"><span data-stu-id="36537-116">May occur at most once for each [**String**](windowsribbon-element-string.md) element.</span></span>

<span data-ttu-id="36537-117">Значение для **String.ID** должно быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="36537-117">The value for **String.Id** must be unique.</span></span>

<span data-ttu-id="36537-118">Идентификатор связан с определением строки в файле заголовка ленты, например `#define strSave 59999` .</span><span class="sxs-lookup"><span data-stu-id="36537-118">The ID is associated with a string definition in the Ribbon header file, for example, `#define strSave 59999`.</span></span>

<span data-ttu-id="36537-119">Этот элемент содержит значение из объединения типов *xs: поситивеинтежер* и *xs: String*.</span><span class="sxs-lookup"><span data-stu-id="36537-119">This element contains a value from the union of types *xs:positiveInteger* and *xs:string*.</span></span> <span data-ttu-id="36537-120">Значение ограничивается целым числом от 2 до 59999, включительно или 0x2 и 0xea5f в шестнадцатеричном, включающем.</span><span class="sxs-lookup"><span data-stu-id="36537-120">The value is constrained to a integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span>

<span data-ttu-id="36537-121">Максимальная длина — 10 символов с необязательными нулями в начале.</span><span class="sxs-lookup"><span data-stu-id="36537-121">The maximum length is 10 characters with optional leading zeros.</span></span>

## <a name="examples"></a><span data-ttu-id="36537-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="36537-122">Examples</span></span>

<span data-ttu-id="36537-123">В следующем примере показана разметка для элемента [**Command. лабелтитле**](windowsribbon-element-command-labeltitle.md) с объявлением **String.ID** .</span><span class="sxs-lookup"><span data-stu-id="36537-123">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String.Id** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="requirements"></a><span data-ttu-id="36537-124">Требования</span><span class="sxs-lookup"><span data-stu-id="36537-124">Requirements</span></span>



| <span data-ttu-id="36537-125">Требование</span><span class="sxs-lookup"><span data-stu-id="36537-125">Requirement</span></span> | <span data-ttu-id="36537-126">Значение</span><span class="sxs-lookup"><span data-stu-id="36537-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="36537-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36537-127">Minimum supported client</span></span><br/> | <span data-ttu-id="36537-128">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="36537-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="36537-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36537-129">Minimum supported server</span></span><br/> | <span data-ttu-id="36537-130">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="36537-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





