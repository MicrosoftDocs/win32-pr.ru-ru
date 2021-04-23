---
title: Простой тип Гуидтипе (схема Евентманифест)
description: Определяет тип глобального уникального идентификатора в формате реестра. | Простой тип Гуидтипе (схема Евентманифест)
ms.assetid: c35fa54b-5a2e-46de-a1c7-fc408b00ee68
keywords:
- Журнал событий простого типа Гуидтипе
topic_type:
- apiref
api_name:
- GUIDType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 474715cf4e9c11536ca227ecdb5609b13be7e222
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694078"
---
# <a name="guidtype-simple-type-eventmanifest-schema"></a><span data-ttu-id="50b4a-105">Простой тип Гуидтипе (схема Евентманифест)</span><span class="sxs-lookup"><span data-stu-id="50b4a-105">GUIDType Simple Type (EventManifest Schema)</span></span>

<span data-ttu-id="50b4a-106">Определяет тип глобального уникального идентификатора в формате реестра.</span><span class="sxs-lookup"><span data-stu-id="50b4a-106">Defines a globally unique identifier type, in Registry format.</span></span>

``` syntax
<xs:simpleType name="GUIDType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="50b4a-107">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="50b4a-107">Patterns</span></span>

<span data-ttu-id="50b4a-108">Простой тип **гуидтипе** — это строка, которая ограничена следующим шаблоном:</span><span class="sxs-lookup"><span data-stu-id="50b4a-108">The **GUIDType** simple type is a string that is restricted by the following pattern:</span></span>

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    <span data-ttu-id="50b4a-109">Значение должно быть глобально уникальным идентификатором в формате реестра.</span><span class="sxs-lookup"><span data-stu-id="50b4a-109">The value must be a globally unique identifier type in Registry format.</span></span> <span data-ttu-id="50b4a-110">Например, {5b2fc63a-8AF4-44cb-960c-aefdced908d6}.</span><span class="sxs-lookup"><span data-stu-id="50b4a-110">For example, {5b2fc63a-8af4-44cb-960c-aefdced908d6}.</span></span> <span data-ttu-id="50b4a-111">Для создания идентификатора GUID используйте GUIDGen.exe или UUIDGen.exe.</span><span class="sxs-lookup"><span data-stu-id="50b4a-111">Use GUIDGen.exe or UUIDGen.exe to create a GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="50b4a-112">Требования</span><span class="sxs-lookup"><span data-stu-id="50b4a-112">Requirements</span></span>



| <span data-ttu-id="50b4a-113">Требование</span><span class="sxs-lookup"><span data-stu-id="50b4a-113">Requirement</span></span> | <span data-ttu-id="50b4a-114">Значение</span><span class="sxs-lookup"><span data-stu-id="50b4a-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="50b4a-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="50b4a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="50b4a-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="50b4a-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="50b4a-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="50b4a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="50b4a-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="50b4a-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





