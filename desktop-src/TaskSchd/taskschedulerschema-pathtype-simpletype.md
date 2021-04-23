---
title: Простой тип Пастипе
description: Определяет минимальное и максимальное число символов для строки, определяющей путь к файлу.
ms.assetid: 09908f75-ba7b-4e31-877e-80fabea6bd27
keywords:
- планировщик задач простого типа Пастипе
topic_type:
- apiref
api_name:
- pathType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a75ef7d85eba2aa39e0c3c768fec0908c7ea16b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682131"
---
# <a name="pathtype-simple-type"></a><span data-ttu-id="5173c-104">Простой тип Пастипе</span><span class="sxs-lookup"><span data-stu-id="5173c-104">pathType Simple Type</span></span>

<span data-ttu-id="5173c-105">Определяет минимальное и максимальное число символов для строки, определяющей путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="5173c-105">Defines the minimum and maximum number of characters for a string that defines a file path.</span></span> <span data-ttu-id="5173c-106">Путь не может быть пустой строкой и должен содержать менее 260 символов.</span><span class="sxs-lookup"><span data-stu-id="5173c-106">The path cannot be an empty string, and must be less than 260 characters.</span></span>

``` syntax
<xs:simpleType name="pathType">
    <xs:restriction
        base="nonEmptyString"
    >
        <xs:maxLength
            value="260"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="5173c-107">Требования</span><span class="sxs-lookup"><span data-stu-id="5173c-107">Requirements</span></span>



| <span data-ttu-id="5173c-108">Требование</span><span class="sxs-lookup"><span data-stu-id="5173c-108">Requirement</span></span> | <span data-ttu-id="5173c-109">Значение</span><span class="sxs-lookup"><span data-stu-id="5173c-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5173c-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5173c-110">Minimum supported client</span></span><br/> | <span data-ttu-id="5173c-111">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5173c-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5173c-112">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5173c-112">Minimum supported server</span></span><br/> | <span data-ttu-id="5173c-113">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5173c-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





