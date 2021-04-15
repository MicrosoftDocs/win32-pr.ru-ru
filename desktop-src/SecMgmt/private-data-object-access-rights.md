---
description: Содержит список и описание прав доступа к закрытому объекту данных.
ms.assetid: 82be57d0-487c-4eb7-83d5-0dd2d53a452b
title: Права доступа к закрытому объекту данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 142aecfe133a9c04237aacf58413e026c4cb3164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497187"
---
# <a name="private-data-object-access-rights"></a><span data-ttu-id="7bca4-103">Права доступа к закрытому объекту данных</span><span class="sxs-lookup"><span data-stu-id="7bca4-103">Private Data Object Access Rights</span></span>

<span data-ttu-id="7bca4-104">Типы доступа для этого типа объектов:</span><span class="sxs-lookup"><span data-stu-id="7bca4-104">The access types of this object type are:</span></span>



| <span data-ttu-id="7bca4-105">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="7bca4-105">Access type</span></span>          | <span data-ttu-id="7bca4-106">Описание</span><span class="sxs-lookup"><span data-stu-id="7bca4-106">Description</span></span>                                      |
|----------------------|--------------------------------------------------|
| <span data-ttu-id="7bca4-107">значение СЕКРЕТного \_ запроса \_</span><span class="sxs-lookup"><span data-stu-id="7bca4-107">SECRET\_QUERY\_VALUE</span></span> | <span data-ttu-id="7bca4-108">Этот тип доступа необходим для получения секрета.</span><span class="sxs-lookup"><span data-stu-id="7bca4-108">This access type is needed to retrieve a secret.</span></span> |
| <span data-ttu-id="7bca4-109">\_значение набора секретов \_</span><span class="sxs-lookup"><span data-stu-id="7bca4-109">SECRET\_SET\_VALUE</span></span>   | <span data-ttu-id="7bca4-110">Этот тип доступа необходим для изменения секрета.</span><span class="sxs-lookup"><span data-stu-id="7bca4-110">This access type is needed to modify a secret.</span></span>   |



 

## <a name="generic-access-masks"></a><span data-ttu-id="7bca4-111">Универсальные маски доступа</span><span class="sxs-lookup"><span data-stu-id="7bca4-111">Generic Access Masks</span></span>

<span data-ttu-id="7bca4-112">Этот тип объекта имеет следующие универсальные сопоставления доступа:</span><span class="sxs-lookup"><span data-stu-id="7bca4-112">This object type has the following generic access mappings:</span></span>

``` syntax
    GENERIC_READ    STANDARD_RIGHTS_READ |
                    SECRET_QUERY_VALUE

    GENERIC_WRITE   STANDARD_RIGHTS_WRITE |
                    SECRET_SET_VALUE

    GENERIC_EXECUTE STANDARD_RIGHTS_EXECUTE
```

## <a name="standard-access-types"></a><span data-ttu-id="7bca4-113">Стандартные типы доступа:</span><span class="sxs-lookup"><span data-stu-id="7bca4-113">Standard Access Types:</span></span>

<span data-ttu-id="7bca4-114">Этот объект не поддерживает (необязательно) СИНХРОНИЗАЦИю стандартного типа доступа.</span><span class="sxs-lookup"><span data-stu-id="7bca4-114">This object does not support the (optional) SYNCHRONIZE standard access type.</span></span> <span data-ttu-id="7bca4-115">Поддерживаются все необходимые типы доступа.</span><span class="sxs-lookup"><span data-stu-id="7bca4-115">All required access types are supported.</span></span> <span data-ttu-id="7bca4-116">Маска всех поддерживаемых типов доступа для этого типа объектов:</span><span class="sxs-lookup"><span data-stu-id="7bca4-116">The mask of all supported access types for this object type is:</span></span>

``` syntax
    SECRET_ALL_ACCESS    STANDARD_RIGHTS_REQUIRED |
                    SECRET_QUERY_VALUE |
                    SECRET_SET_VALUE
```

 

 



