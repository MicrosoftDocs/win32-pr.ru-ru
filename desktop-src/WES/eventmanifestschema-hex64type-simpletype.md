---
title: Простой тип HexInt64Type
description: Определяет 8-байтовый шестнадцатеричный тип. | Простой тип HexInt64Type
ms.assetid: 2e81ec2b-cf67-42df-92a0-bf45b6dca051
keywords:
- Журнал событий простого типа HexInt64Type
topic_type:
- apiref
api_name:
- HexInt64Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8947e594bb067140510b0b5d2046a898018a291e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104424209"
---
# <a name="hexint64type-simple-type"></a><span data-ttu-id="26d69-105">Простой тип HexInt64Type</span><span class="sxs-lookup"><span data-stu-id="26d69-105">HexInt64Type Simple Type</span></span>

<span data-ttu-id="26d69-106">Определяет 8-байтовый шестнадцатеричный тип.</span><span class="sxs-lookup"><span data-stu-id="26d69-106">Defines an 8-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt64Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,16}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="26d69-107">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="26d69-107">Patterns</span></span>

<span data-ttu-id="26d69-108">Простой тип **HexInt64Type** — это [строка](/dotnet/api/system.string) , которая ограничена следующим шаблоном:</span><span class="sxs-lookup"><span data-stu-id="26d69-108">The **HexInt64Type** simple type is a [string](/dotnet/api/system.string) that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,16}`

    <span data-ttu-id="26d69-109">Значение может содержать от одного до шестнадцати шестнадцатеричных символов (например, 0xA или 0xac7bd361004fe190).</span><span class="sxs-lookup"><span data-stu-id="26d69-109">The value can contain from one to sixteen hexadecimal characters (for example, 0xa or 0xac7bd361004fe190).</span></span>

## <a name="requirements"></a><span data-ttu-id="26d69-110">Требования</span><span class="sxs-lookup"><span data-stu-id="26d69-110">Requirements</span></span>



| <span data-ttu-id="26d69-111">Требование</span><span class="sxs-lookup"><span data-stu-id="26d69-111">Requirement</span></span> | <span data-ttu-id="26d69-112">Значение</span><span class="sxs-lookup"><span data-stu-id="26d69-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="26d69-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="26d69-113">Minimum supported client</span></span><br/> | <span data-ttu-id="26d69-114">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="26d69-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="26d69-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="26d69-115">Minimum supported server</span></span><br/> | <span data-ttu-id="26d69-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="26d69-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

