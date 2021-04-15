---
title: Синтаксис объекта (DN-String)
description: Строка октета, которая содержит строковое значение и различающееся имя.
ms.assetid: 7a5ce9f3-ac97-4936-868a-6b18f202972f
ms.tgt_platform: multiple
keywords:
- Схема AD синтаксиса объекта (DN-строки)
topic_type:
- apiref
api_name:
- Object(DN-String)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 823da21325abdc426d5f58df4cdf04de19fc68b6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654777"
---
# <a name="objectdn-string-syntax"></a><span data-ttu-id="d64b5-104">Синтаксис объекта (DN-String)</span><span class="sxs-lookup"><span data-stu-id="d64b5-104">Object(DN-String) syntax</span></span>

<span data-ttu-id="d64b5-105">Строка октета, которая содержит строковое значение и различающееся имя.</span><span class="sxs-lookup"><span data-stu-id="d64b5-105">An octet string that contains a string value and a DN.</span></span>



| <span data-ttu-id="d64b5-106">Ввод</span><span class="sxs-lookup"><span data-stu-id="d64b5-106">Entry</span></span> | <span data-ttu-id="d64b5-107">Значение</span><span class="sxs-lookup"><span data-stu-id="d64b5-107">Value</span></span> |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d64b5-108">Имя</span><span class="sxs-lookup"><span data-stu-id="d64b5-108">Name</span></span>         | <span data-ttu-id="d64b5-109">Object(строка_DN)</span><span class="sxs-lookup"><span data-stu-id="d64b5-109">Object(DN-String)</span></span>                                                                  |
| <span data-ttu-id="d64b5-110">Идентификатор синтаксиса</span><span class="sxs-lookup"><span data-stu-id="d64b5-110">Syntax ID</span></span>    | <span data-ttu-id="d64b5-111">2.5.5.14</span><span class="sxs-lookup"><span data-stu-id="d64b5-111">2.5.5.14</span></span>                                                                           |
| <span data-ttu-id="d64b5-112">ИДЕНТИФИКАТОР OM</span><span class="sxs-lookup"><span data-stu-id="d64b5-112">OM ID</span></span>        | <span data-ttu-id="d64b5-113">127</span><span class="sxs-lookup"><span data-stu-id="d64b5-113">127</span></span>                                                                                |
| <span data-ttu-id="d64b5-114">Тип MAPI</span><span class="sxs-lookup"><span data-stu-id="d64b5-114">MAPI Type</span></span>    | \-                                                                                 |
| <span data-ttu-id="d64b5-115">Тип ADS</span><span class="sxs-lookup"><span data-stu-id="d64b5-115">ADS Type</span></span>     | <span data-ttu-id="d64b5-116">АДСТИПЕ \_ DN \_ со \_ строкой</span><span class="sxs-lookup"><span data-stu-id="d64b5-116">ADSTYPE\_DN\_WITH\_STRING</span></span>                                                          |
| <span data-ttu-id="d64b5-117">Тип варианта</span><span class="sxs-lookup"><span data-stu-id="d64b5-117">Variant Type</span></span> | <span data-ttu-id="d64b5-118">\_Диспетчер VT</span><span class="sxs-lookup"><span data-stu-id="d64b5-118">VT\_DISPATCH</span></span>                                                                       |
| <span data-ttu-id="d64b5-119">Тип SDS</span><span class="sxs-lookup"><span data-stu-id="d64b5-119">SDS Type</span></span>     | <span data-ttu-id="d64b5-120">COM-объект, который можно привести к [**иадсднвисстринг**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring).</span><span class="sxs-lookup"><span data-stu-id="d64b5-120">A COM object that can be cast to an [**IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring).</span></span> |



## <a name="remarks"></a><span data-ttu-id="d64b5-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d64b5-121">Remarks</span></span>

<span data-ttu-id="d64b5-122">Значение с этим синтаксисом имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="d64b5-122">A value with this syntax has the following format:</span></span>

``` syntax
S:<char count>:<string value>:<object DN>
```

<span data-ttu-id="d64b5-123">где " &lt; число &gt; символов" — это число знаков в &lt; строке "строковое значение" &gt; , а " &lt; Object DN &gt; " — это различающееся имя объекта в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d64b5-123">where "&lt;char count&gt;" is the number of characters in the "&lt;string value&gt;" string, and "&lt;object DN&gt;" is a distinguished name of an object in Active Directory.</span></span> <span data-ttu-id="d64b5-124">Active Directory обновляет DN, если объект, на который он ссылается, перемещается или переименовывается.</span><span class="sxs-lookup"><span data-stu-id="d64b5-124">Active Directory updates the DN if the object that it refers to is moved or renamed.</span></span>

## <a name="see-also"></a><span data-ttu-id="d64b5-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d64b5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d64b5-126">**IADsDNWithString**</span><span class="sxs-lookup"><span data-stu-id="d64b5-126">**IADsDNWithString**</span></span>](/windows/desktop/api/iads/nn-iads-iadsdnwithstring)
</dt> </dl>

 

 
