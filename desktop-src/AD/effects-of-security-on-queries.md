---
title: Влияние безопасности при поиске
description: Безопасность — это неявный фильтр при выполнении поиска, перечислении контейнеров или чтении свойств.
ms.assetid: 4a027069-8c3d-4a95-a04b-c9c59200a9ed
ms.tgt_platform: multiple
keywords:
- влияние безопасности при поиске Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26feee840c0668b2ea9412932a27927bb1c00012
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773235"
---
# <a name="effects-of-security-on-searching"></a><span data-ttu-id="b8587-104">Влияние безопасности при поиске</span><span class="sxs-lookup"><span data-stu-id="b8587-104">Effects of Security on Searching</span></span>

<span data-ttu-id="b8587-105">Безопасность — это неявный фильтр при выполнении поиска, перечислении контейнеров или чтении свойств.</span><span class="sxs-lookup"><span data-stu-id="b8587-105">Security is an implicit filter when performing searches, enumerating containers, or reading properties.</span></span>

<span data-ttu-id="b8587-106">ADSI может не возвращать \_ такие \_ свойства или \_ \_ ошибки объектов, даже если объект существует, если у вас нет доступа на чтение атрибутов объекта.</span><span class="sxs-lookup"><span data-stu-id="b8587-106">ADSI can return NO\_SUCH\_PROPERTY or NO\_SUCH\_OBJECT errors even when the object exists if you do not have access to read attributes on the object.</span></span>

<span data-ttu-id="b8587-107">Например, вызывающий объект может иметь возможность перечислить дочерние объекты в контейнере, так как вызывающий объект имеет \_ права на содержимое списка в контейнере.</span><span class="sxs-lookup"><span data-stu-id="b8587-107">For example, a caller may be able to enumerate the child objects in a container because the caller has LIST\_CONTENTS rights on the container.</span></span> <span data-ttu-id="b8587-108">Но один и тот же вызывающий объект может не иметь доступа к перечисленным объектам, если вызывающий объект не имеет доступа на чтение к дочерним объектам.</span><span class="sxs-lookup"><span data-stu-id="b8587-108">But the same caller may not be able to access the enumerated objects if the caller does not have read access to the child objects.</span></span> <span data-ttu-id="b8587-109">В этом случае запрос дочернего объекта может не возвращать \_ такой \_ объект, даже если вызывающий объект успешно выполнил перечисление объекта.</span><span class="sxs-lookup"><span data-stu-id="b8587-109">In this case, a query for a child object may return NO\_SUCH\_OBJECT even though the caller successfully enumerated the object.</span></span>

<span data-ttu-id="b8587-110">Если вызывающий объект не имеет достаточных прав, могут возвращаться следующие коды возврата:</span><span class="sxs-lookup"><span data-stu-id="b8587-110">If the caller does not have sufficient rights, the following return codes may be returned:</span></span>

<span data-ttu-id="b8587-111">E \_ ADS \_ Недопустимый \_ \_ объект домена</span><span class="sxs-lookup"><span data-stu-id="b8587-111">E\_ADS\_INVALID\_DOMAIN\_OBJECT</span></span>

<span data-ttu-id="b8587-112">\_свойство E \_ ADS \_ не \_ поддерживается</span><span class="sxs-lookup"><span data-stu-id="b8587-112">E\_ADS\_PROPERTY\_NOT\_SUPPORTED</span></span>

<span data-ttu-id="b8587-113">\_ \_ \_ не \_ найдено свойство E ADS</span><span class="sxs-lookup"><span data-stu-id="b8587-113">E\_ADS\_PROPERTY\_NOT\_FOUND</span></span>

 

 




