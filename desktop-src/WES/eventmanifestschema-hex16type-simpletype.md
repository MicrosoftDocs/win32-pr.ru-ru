---
title: Простой тип HexInt16Type
description: Определяет 2-байтовый шестнадцатеричный тип.
ms.assetid: d33d24e7-d260-49ea-a8ba-187b9b7a3a9c
keywords:
- Журнал событий простого типа HexInt16Type
topic_type:
- apiref
api_name:
- HexInt16Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6aaa5021fbc5a7de5c16083c0f7744bc4a154c50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492555"
---
# <a name="hexint16type-simple-type"></a><span data-ttu-id="68973-104">Простой тип HexInt16Type</span><span class="sxs-lookup"><span data-stu-id="68973-104">HexInt16Type Simple Type</span></span>

<span data-ttu-id="68973-105">Определяет 2-байтовый шестнадцатеричный тип.</span><span class="sxs-lookup"><span data-stu-id="68973-105">Defines a 2-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt16Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,4}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="68973-106">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="68973-106">Patterns</span></span>

<span data-ttu-id="68973-107">Простой тип **HexInt16Type** — это **строка** , которая ограничена следующим шаблоном:</span><span class="sxs-lookup"><span data-stu-id="68973-107">The **HexInt16Type** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,4}`

    <span data-ttu-id="68973-108">Значение может содержать от одного до четырех шестнадцатеричных символов (например, 0xA или 0xac7b).</span><span class="sxs-lookup"><span data-stu-id="68973-108">The value can contain from one to four hexadecimal characters (for example, 0xa or 0xac7b).</span></span>

## <a name="requirements"></a><span data-ttu-id="68973-109">Требования</span><span class="sxs-lookup"><span data-stu-id="68973-109">Requirements</span></span>



| <span data-ttu-id="68973-110">Требование</span><span class="sxs-lookup"><span data-stu-id="68973-110">Requirement</span></span> | <span data-ttu-id="68973-111">Значение</span><span class="sxs-lookup"><span data-stu-id="68973-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="68973-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68973-112">Minimum supported client</span></span><br/> | <span data-ttu-id="68973-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="68973-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="68973-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68973-114">Minimum supported server</span></span><br/> | <span data-ttu-id="68973-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="68973-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





