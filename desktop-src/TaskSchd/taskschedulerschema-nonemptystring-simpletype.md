---
title: Простой тип Нонемптистрингтипе
description: Определяет значения, используемые для непустой строки текста.
ms.assetid: cb3b1ca6-4531-467c-a27a-b27a62233514
keywords:
- планировщик задач простого типа Нонемптистринг
topic_type:
- apiref
api_name:
- nonEmptyString
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab9c9fa84c510fc4e67f6f63664a58d6d4093709
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415784"
---
# <a name="nonemptystringtype-simple-type"></a><span data-ttu-id="12641-104">Простой тип Нонемптистрингтипе</span><span class="sxs-lookup"><span data-stu-id="12641-104">nonEmptyStringType Simple Type</span></span>

<span data-ttu-id="12641-105">Определяет значения, используемые для непустой строки текста.</span><span class="sxs-lookup"><span data-stu-id="12641-105">Defines the values used for a non-empty string of text.</span></span>

``` syntax
<xs:simpleType name="nonEmptyString">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="12641-106">Значения перечисления</span><span class="sxs-lookup"><span data-stu-id="12641-106">Enumeration values</span></span>

<span data-ttu-id="12641-107">Простой тип **нонемптистринг** определяет следующее значение.</span><span class="sxs-lookup"><span data-stu-id="12641-107">The **nonEmptyString** simple type defines the following value.</span></span>



| <span data-ttu-id="12641-108">Значение</span><span class="sxs-lookup"><span data-stu-id="12641-108">Value</span></span> | <span data-ttu-id="12641-109">Описание</span><span class="sxs-lookup"><span data-stu-id="12641-109">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="12641-110">1</span><span class="sxs-lookup"><span data-stu-id="12641-110">1</span></span>     | <span data-ttu-id="12641-111">Строка содержит по крайней мере один символ.</span><span class="sxs-lookup"><span data-stu-id="12641-111">The string contains at least one character.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="12641-112">Требования</span><span class="sxs-lookup"><span data-stu-id="12641-112">Requirements</span></span>



| <span data-ttu-id="12641-113">Требование</span><span class="sxs-lookup"><span data-stu-id="12641-113">Requirement</span></span> | <span data-ttu-id="12641-114">Значение</span><span class="sxs-lookup"><span data-stu-id="12641-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="12641-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="12641-115">Minimum supported client</span></span><br/> | <span data-ttu-id="12641-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="12641-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="12641-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="12641-117">Minimum supported server</span></span><br/> | <span data-ttu-id="12641-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="12641-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





