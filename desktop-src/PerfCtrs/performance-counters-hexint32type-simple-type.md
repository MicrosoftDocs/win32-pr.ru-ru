---
description: Определяет 4-байтовый шестнадцатеричный тип.
ms.assetid: d0e538c1-f22e-4905-ba73-b670fa7eb174
title: Простой тип HexInt32Type (счетчики производительности)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2d2392f2240ca9ca61525b27993e16bcab979a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663188"
---
# <a name="hexint32type-simple-type-performance-counters"></a><span data-ttu-id="e8b07-103">Простой тип HexInt32Type (счетчики производительности)</span><span class="sxs-lookup"><span data-stu-id="e8b07-103">HexInt32Type Simple Type (Performance Counters)</span></span>

<span data-ttu-id="e8b07-104">Определяет 4-байтовый шестнадцатеричный тип.</span><span class="sxs-lookup"><span data-stu-id="e8b07-104">Defines a 4-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt32Type">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,8}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="e8b07-105">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="e8b07-105">Patterns</span></span>

<span data-ttu-id="e8b07-106">Простой тип **HexInt32Type** — это **Строка типа xs: String** , которая ограничена следующим шаблоном:</span><span class="sxs-lookup"><span data-stu-id="e8b07-106">The **HexInt32Type** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,8}`

    <span data-ttu-id="e8b07-107">Значение может содержать от одного до восьми шестнадцатеричных символов (например, 0xA или 0xac7bd361).</span><span class="sxs-lookup"><span data-stu-id="e8b07-107">The value can contain from one to eight hexadecimal characters (for example, 0xa or 0xac7bd361).</span></span>

## <a name="requirements"></a><span data-ttu-id="e8b07-108">Требования</span><span class="sxs-lookup"><span data-stu-id="e8b07-108">Requirements</span></span>



| <span data-ttu-id="e8b07-109">Требование</span><span class="sxs-lookup"><span data-stu-id="e8b07-109">Requirement</span></span> | <span data-ttu-id="e8b07-110">Значение</span><span class="sxs-lookup"><span data-stu-id="e8b07-110">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e8b07-111">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8b07-111">Minimum supported client</span></span><br/> | <span data-ttu-id="e8b07-112">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e8b07-112">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e8b07-113">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8b07-113">Minimum supported server</span></span><br/> | <span data-ttu-id="e8b07-114">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e8b07-114">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




