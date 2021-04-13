---
title: Простой тип HexInt8Type
description: Определяет 1-байтовый шестнадцатеричный тип.
ms.assetid: 390acf84-7b5c-45e7-83bd-9f3115099568
keywords:
- Журнал событий простого типа HexInt8Type
topic_type:
- apiref
api_name:
- HexInt8Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e68e56340ee535531fb6711dcf01a72d92665cbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493095"
---
# <a name="hexint8type-simple-type"></a><span data-ttu-id="5008f-104">Простой тип HexInt8Type</span><span class="sxs-lookup"><span data-stu-id="5008f-104">HexInt8Type Simple Type</span></span>

<span data-ttu-id="5008f-105">Определяет 1-байтовый шестнадцатеричный тип.</span><span class="sxs-lookup"><span data-stu-id="5008f-105">Defines a 1-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt8Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,2}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="5008f-106">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="5008f-106">Patterns</span></span>

<span data-ttu-id="5008f-107">Простой тип **HexInt8Type** — это [строка](/dotnet/api/system.string) , которая ограничена следующим шаблоном:</span><span class="sxs-lookup"><span data-stu-id="5008f-107">The **HexInt8Type** simple type is a [string](/dotnet/api/system.string) that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,2}`

    <span data-ttu-id="5008f-108">Значение может содержать от одного до двух шестнадцатеричных символов (например, 0xA или 0xac).</span><span class="sxs-lookup"><span data-stu-id="5008f-108">The value can contain from one to two hexadecimal characters (for example, 0xa or 0xac).</span></span>

## <a name="requirements"></a><span data-ttu-id="5008f-109">Требования</span><span class="sxs-lookup"><span data-stu-id="5008f-109">Requirements</span></span>



| <span data-ttu-id="5008f-110">Требование</span><span class="sxs-lookup"><span data-stu-id="5008f-110">Requirement</span></span> | <span data-ttu-id="5008f-111">Значение</span><span class="sxs-lookup"><span data-stu-id="5008f-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5008f-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5008f-112">Minimum supported client</span></span><br/> | <span data-ttu-id="5008f-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5008f-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5008f-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5008f-114">Minimum supported server</span></span><br/> | <span data-ttu-id="5008f-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5008f-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

