---
title: Простой тип HexInt32Type (схема Евентманифест)
description: Определяет 4-байтовый шестнадцатеричный тип. | Простой тип HexInt32Type (схема Евентманифест)
ms.assetid: b1006593-c6f2-4669-b242-758ce9977565
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
ms.openlocfilehash: 4630bc4d7d513a0fedad2191c63ca71571ce655a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694004"
---
# <a name="hexint32type-simple-type-eventmanifest-schema"></a><span data-ttu-id="fc3ed-105">Простой тип HexInt32Type (схема Евентманифест)</span><span class="sxs-lookup"><span data-stu-id="fc3ed-105">HexInt32Type Simple Type (EventManifest Schema)</span></span>

<span data-ttu-id="fc3ed-106">Определяет 4-байтовый шестнадцатеричный тип.</span><span class="sxs-lookup"><span data-stu-id="fc3ed-106">Defines a 4-byte hexadecimal type.</span></span>

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

## <a name="patterns"></a><span data-ttu-id="fc3ed-107">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="fc3ed-107">Patterns</span></span>

<span data-ttu-id="fc3ed-108">Простой тип **HexInt32Type** — это **строка** , которая ограничена следующим шаблоном:</span><span class="sxs-lookup"><span data-stu-id="fc3ed-108">The **HexInt32Type** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,8}`

    <span data-ttu-id="fc3ed-109">Значение может содержать от одного до восьми шестнадцатеричных символов (например, 0xA или 0xac7bd361).</span><span class="sxs-lookup"><span data-stu-id="fc3ed-109">The value can contain from one to eight hexadecimal characters (for example, 0xa or 0xac7bd361).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc3ed-110">Требования</span><span class="sxs-lookup"><span data-stu-id="fc3ed-110">Requirements</span></span>



| <span data-ttu-id="fc3ed-111">Требование</span><span class="sxs-lookup"><span data-stu-id="fc3ed-111">Requirement</span></span> | <span data-ttu-id="fc3ed-112">Значение</span><span class="sxs-lookup"><span data-stu-id="fc3ed-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fc3ed-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fc3ed-113">Minimum supported client</span></span><br/> | <span data-ttu-id="fc3ed-114">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fc3ed-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fc3ed-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fc3ed-115">Minimum supported server</span></span><br/> | <span data-ttu-id="fc3ed-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fc3ed-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





