---
title: Простой тип HexInt32Type (схема события)
description: Определяет 4-байтовый шестнадцатеричный тип. | Простой тип HexInt32Type (схема события)
ms.assetid: f4b5226d-2a5e-4756-b4c5-30cfbf13568e
keywords:
- Журнал событий простого типа HexInt32Type
topic_type:
- apiref
api_name:
- HexInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5c9bd7a11d0e648cc451ec837f0f8711ca334d59
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000132"
---
# <a name="hexint32type-simple-type-event-schema"></a><span data-ttu-id="fb266-105">Простой тип HexInt32Type (схема события)</span><span class="sxs-lookup"><span data-stu-id="fb266-105">HexInt32Type Simple Type (Event Schema)</span></span>

<span data-ttu-id="fb266-106">Определяет 4-байтовый шестнадцатеричный тип.</span><span class="sxs-lookup"><span data-stu-id="fb266-106">Defines a 4-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt32Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,8}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="fb266-107">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="fb266-107">Patterns</span></span>

<span data-ttu-id="fb266-108">Простой тип **HexInt32Type** — это **строка** , которая ограничена следующим шаблоном:</span><span class="sxs-lookup"><span data-stu-id="fb266-108">The **HexInt32Type** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,8}`

    <span data-ttu-id="fb266-109">Значение может содержать от одного до восьми шестнадцатеричных символов (например, 0xA или 0xac7bd361).</span><span class="sxs-lookup"><span data-stu-id="fb266-109">The value can contain from one to eight hexadecimal characters (for example, 0xa or 0xac7bd361).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb266-110">Требования</span><span class="sxs-lookup"><span data-stu-id="fb266-110">Requirements</span></span>



| <span data-ttu-id="fb266-111">Требование</span><span class="sxs-lookup"><span data-stu-id="fb266-111">Requirement</span></span> | <span data-ttu-id="fb266-112">Значение</span><span class="sxs-lookup"><span data-stu-id="fb266-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fb266-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fb266-113">Minimum supported client</span></span><br/> | <span data-ttu-id="fb266-114">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fb266-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fb266-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fb266-115">Minimum supported server</span></span><br/> | <span data-ttu-id="fb266-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fb266-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





