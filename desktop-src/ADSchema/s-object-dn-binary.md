---
title: Синтаксис объекта (DN-Binary)
description: Строка октета, которая содержит двоичное значение и различающееся имя (DN).
ms.assetid: 1d7efc17-a99a-41bf-9812-9e8a2b2b6644
ms.tgt_platform: multiple
keywords:
- Схема AD синтаксиса объекта (DN-Binary)
topic_type:
- apiref
api_name:
- Object(DN-Binary)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e96f640ad729f203362df906bcc6afe6b82e7e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104137914"
---
# <a name="objectdn-binary-syntax"></a><span data-ttu-id="baa04-104">Синтаксис объекта (DN-Binary)</span><span class="sxs-lookup"><span data-stu-id="baa04-104">Object(DN-Binary) syntax</span></span>

<span data-ttu-id="baa04-105">Строка октета, которая содержит двоичное значение и различающееся имя (DN).</span><span class="sxs-lookup"><span data-stu-id="baa04-105">An octet string that contains a binary value and a distinguished name (DN).</span></span>



| <span data-ttu-id="baa04-106">Ввод</span><span class="sxs-lookup"><span data-stu-id="baa04-106">Entry</span></span> | <span data-ttu-id="baa04-107">Значение</span><span class="sxs-lookup"><span data-stu-id="baa04-107">Value</span></span> |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="baa04-108">Имя</span><span class="sxs-lookup"><span data-stu-id="baa04-108">Name</span></span>         | <span data-ttu-id="baa04-109">Object(двоичный_DN)</span><span class="sxs-lookup"><span data-stu-id="baa04-109">Object(DN-Binary)</span></span>                                                                  |
| <span data-ttu-id="baa04-110">Идентификатор синтаксиса</span><span class="sxs-lookup"><span data-stu-id="baa04-110">Syntax ID</span></span>    | <span data-ttu-id="baa04-111">2.5.5.7</span><span class="sxs-lookup"><span data-stu-id="baa04-111">2.5.5.7</span></span>                                                                            |
| <span data-ttu-id="baa04-112">ИДЕНТИФИКАТОР OM</span><span class="sxs-lookup"><span data-stu-id="baa04-112">OM ID</span></span>        | <span data-ttu-id="baa04-113">127</span><span class="sxs-lookup"><span data-stu-id="baa04-113">127</span></span>                                                                                |
| <span data-ttu-id="baa04-114">Тип MAPI</span><span class="sxs-lookup"><span data-stu-id="baa04-114">MAPI Type</span></span>    | <span data-ttu-id="baa04-115">тстринг</span><span class="sxs-lookup"><span data-stu-id="baa04-115">TSTRING</span></span>                                                                            |
| <span data-ttu-id="baa04-116">Тип ADS</span><span class="sxs-lookup"><span data-stu-id="baa04-116">ADS Type</span></span>     | <span data-ttu-id="baa04-117">АДСТИПЕ \_ DN \_ с \_ двоичными данными</span><span class="sxs-lookup"><span data-stu-id="baa04-117">ADSTYPE\_DN\_WITH\_BINARY</span></span>                                                          |
| <span data-ttu-id="baa04-118">Тип варианта</span><span class="sxs-lookup"><span data-stu-id="baa04-118">Variant Type</span></span> | <span data-ttu-id="baa04-119">\_Диспетчер VT</span><span class="sxs-lookup"><span data-stu-id="baa04-119">VT\_DISPATCH</span></span>                                                                       |
| <span data-ttu-id="baa04-120">Тип SDS</span><span class="sxs-lookup"><span data-stu-id="baa04-120">SDS Type</span></span>     | <span data-ttu-id="baa04-121">COM-объект, который можно привести к [**иадсднвисбинари**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary).</span><span class="sxs-lookup"><span data-stu-id="baa04-121">A COM object that can be cast to an [**IADsDNWithBinary**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary).</span></span> |



## <a name="remarks"></a><span data-ttu-id="baa04-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="baa04-122">Remarks</span></span>

<span data-ttu-id="baa04-123">Значение с этим синтаксисом имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="baa04-123">A value with this syntax has the following format:</span></span>

``` syntax
B:<char count>:<binary value>:<object DN>
```

<span data-ttu-id="baa04-124">где " &lt; число символов &gt; " — это число шестнадцатеричных цифр в " &lt; двоичное значение" &gt; , " &lt; двоичное значение &gt; " — шестнадцатеричное представление двоичного значения, а " &lt; объект DN &gt; " — различающееся имя.</span><span class="sxs-lookup"><span data-stu-id="baa04-124">where "&lt;char count&gt;" is the number of hexadecimal digits in "&lt;binary value&gt;", "&lt;binary value&gt;" is the hexadecimal representation of the binary value, and "&lt;object DN&gt;" is a distinguished name.</span></span> <span data-ttu-id="baa04-125">Active Directory автоматически обновляет DN, если объект, на который он ссылается, перемещается или переименовывается.</span><span class="sxs-lookup"><span data-stu-id="baa04-125">Active Directory automatically updates the DN if the object that it refers to is moved or renamed.</span></span> <span data-ttu-id="baa04-126">Дополнительные сведения и пример кода, в котором используется этот синтаксис, см. в разделе [Включение безопасного переименования с помощью свойства otherWellKnownObjects](/windows/desktop/AD/enabling-rename-safe-binding-with-the-otherwellknownobjects-property).</span><span class="sxs-lookup"><span data-stu-id="baa04-126">For more information and a code example that uses this syntax, see [Enabling Rename-safe Binding with the otherWellKnownObjects Property](/windows/desktop/AD/enabling-rename-safe-binding-with-the-otherwellknownobjects-property).</span></span>

## <a name="see-also"></a><span data-ttu-id="baa04-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="baa04-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baa04-128">**IADsDNWithBinary**</span><span class="sxs-lookup"><span data-stu-id="baa04-128">**IADsDNWithBinary**</span></span>](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary)
</dt> </dl>

 

 
