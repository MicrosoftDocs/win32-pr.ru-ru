---
description: Определяет тип глобального уникального идентификатора в формате реестра.
ms.assetid: 2be73c57-b6b6-46ab-93e1-d70f8655c30e
title: Простой тип Гуидтипе (счетчики производительности)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 758509a564c26db493fa2e9ed971aba71878cdbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909716"
---
# <a name="guidtype-simple-type-performance-counters"></a><span data-ttu-id="4d2f2-103">Простой тип Гуидтипе (счетчики производительности)</span><span class="sxs-lookup"><span data-stu-id="4d2f2-103">GUIDType Simple Type (Performance Counters)</span></span>

<span data-ttu-id="4d2f2-104">Определяет тип глобального уникального идентификатора в формате реестра.</span><span class="sxs-lookup"><span data-stu-id="4d2f2-104">Defines a globally unique identifier type, in Registry format.</span></span>

``` syntax
<xs:simpleType name="GUIDType">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="4d2f2-105">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="4d2f2-105">Patterns</span></span>

<span data-ttu-id="4d2f2-106">Простой тип **гуидтипе** — это **Строка типа xs: String** , которая ограничена следующим шаблоном:</span><span class="sxs-lookup"><span data-stu-id="4d2f2-106">The **GUIDType** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    <span data-ttu-id="4d2f2-107">Значение должно быть глобально уникальным идентификатором в формате реестра.</span><span class="sxs-lookup"><span data-stu-id="4d2f2-107">The value must be a globally unique identifier type in Registry format.</span></span> <span data-ttu-id="4d2f2-108">Например, {5b2fc63a-8AF4-44cb-960c-aefdced908d6}.</span><span class="sxs-lookup"><span data-stu-id="4d2f2-108">For example, {5b2fc63a-8af4-44cb-960c-aefdced908d6}.</span></span> <span data-ttu-id="4d2f2-109">Для создания идентификатора GUID используйте GUIDGen.exe или UUIDGen.exe.</span><span class="sxs-lookup"><span data-stu-id="4d2f2-109">Use GUIDGen.exe or UUIDGen.exe to create a GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d2f2-110">Требования</span><span class="sxs-lookup"><span data-stu-id="4d2f2-110">Requirements</span></span>



| <span data-ttu-id="4d2f2-111">Требование</span><span class="sxs-lookup"><span data-stu-id="4d2f2-111">Requirement</span></span> | <span data-ttu-id="4d2f2-112">Значение</span><span class="sxs-lookup"><span data-stu-id="4d2f2-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4d2f2-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4d2f2-113">Minimum supported client</span></span><br/> | <span data-ttu-id="4d2f2-114">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4d2f2-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4d2f2-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4d2f2-115">Minimum supported server</span></span><br/> | <span data-ttu-id="4d2f2-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4d2f2-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




