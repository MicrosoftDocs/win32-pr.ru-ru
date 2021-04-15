---
title: Синтаксис интервала
description: Представляет значение интервала времени.
ms.assetid: e41b71da-cd05-4a4a-8b97-9210dbe314de
ms.tgt_platform: multiple
keywords:
- Схема AD синтаксиса интервала
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59b92961deecde7faa879dbbda6bfd24560ad705
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104416193"
---
# <a name="interval-syntax"></a><span data-ttu-id="f1b7f-104">Синтаксис интервала</span><span class="sxs-lookup"><span data-stu-id="f1b7f-104">Interval syntax</span></span>

<span data-ttu-id="f1b7f-105">Представляет значение интервала времени.</span><span class="sxs-lookup"><span data-stu-id="f1b7f-105">Represents a time interval value.</span></span> <span data-ttu-id="f1b7f-106">Фактические единицы времени зависят от того, какой атрибут использует этот синтаксис.</span><span class="sxs-lookup"><span data-stu-id="f1b7f-106">The actual time units depend on which attribute is using this syntax.</span></span> <span data-ttu-id="f1b7f-107">Этот синтаксис идентичен синтаксису [**ларжеинтежер**](s-largeinteger.md) , за исключением того, что значения High и Low являются целыми числами без знака.</span><span class="sxs-lookup"><span data-stu-id="f1b7f-107">This syntax is identical to the [**LargeInteger**](s-largeinteger.md) syntax, except the high and low values are unsigned integers.</span></span>



| <span data-ttu-id="f1b7f-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="f1b7f-108">Entry</span></span> | <span data-ttu-id="f1b7f-109">Значение</span><span class="sxs-lookup"><span data-stu-id="f1b7f-109">Value</span></span> |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f1b7f-110">Имя</span><span class="sxs-lookup"><span data-stu-id="f1b7f-110">Name</span></span>         | <span data-ttu-id="f1b7f-111">Интервал</span><span class="sxs-lookup"><span data-stu-id="f1b7f-111">Interval</span></span>                                                                           |
| <span data-ttu-id="f1b7f-112">Идентификатор синтаксиса</span><span class="sxs-lookup"><span data-stu-id="f1b7f-112">Syntax ID</span></span>    | <span data-ttu-id="f1b7f-113">2.5.5.16</span><span class="sxs-lookup"><span data-stu-id="f1b7f-113">2.5.5.16</span></span>                                                                           |
| <span data-ttu-id="f1b7f-114">ИДЕНТИФИКАТОР OM</span><span class="sxs-lookup"><span data-stu-id="f1b7f-114">OM ID</span></span>        | <span data-ttu-id="f1b7f-115">65</span><span class="sxs-lookup"><span data-stu-id="f1b7f-115">65</span></span>                                                                                 |
| <span data-ttu-id="f1b7f-116">Тип MAPI</span><span class="sxs-lookup"><span data-stu-id="f1b7f-116">MAPI Type</span></span>    | \-                                                                                 |
| <span data-ttu-id="f1b7f-117">Тип ADS</span><span class="sxs-lookup"><span data-stu-id="f1b7f-117">ADS Type</span></span>     | <span data-ttu-id="f1b7f-118">АДСТИПЕ \_ большое \_ целое</span><span class="sxs-lookup"><span data-stu-id="f1b7f-118">ADSTYPE\_LARGE\_INTEGER</span></span>                                                            |
| <span data-ttu-id="f1b7f-119">Тип варианта</span><span class="sxs-lookup"><span data-stu-id="f1b7f-119">Variant Type</span></span> | <span data-ttu-id="f1b7f-120">\_Диспетчер VT</span><span class="sxs-lookup"><span data-stu-id="f1b7f-120">VT\_DISPATCH</span></span>                                                                       |
| <span data-ttu-id="f1b7f-121">Тип SDS</span><span class="sxs-lookup"><span data-stu-id="f1b7f-121">SDS Type</span></span>     | <span data-ttu-id="f1b7f-122">COM-объект, который можно привести к [**иадсларжеинтежер**](/windows/desktop/api/iads/nn-iads-iadslargeinteger).</span><span class="sxs-lookup"><span data-stu-id="f1b7f-122">A COM object that can be cast to an [**IADsLargeInteger**](/windows/desktop/api/iads/nn-iads-iadslargeinteger).</span></span> |



## <a name="see-also"></a><span data-ttu-id="f1b7f-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1b7f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1b7f-124">**IADsLargeInteger**</span><span class="sxs-lookup"><span data-stu-id="f1b7f-124">**IADsLargeInteger**</span></span>](/windows/desktop/api/iads/nn-iads-iadslargeinteger)
</dt> <dt>

[<span data-ttu-id="f1b7f-125">**ларжеинтежер**</span><span class="sxs-lookup"><span data-stu-id="f1b7f-125">**LargeInteger**</span></span>](s-largeinteger.md)
</dt> </dl>

 

 
