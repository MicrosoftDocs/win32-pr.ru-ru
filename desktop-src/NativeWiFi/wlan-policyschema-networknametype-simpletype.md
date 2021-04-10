---
description: Определяет строковый тип для идентификаторов набора служб (SSID).
ms.assetid: c9e79a3d-7d5c-4320-ade2-40124de00920
title: Простой тип Нетворкнаметипе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkNameType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6b6463644e1bd174be256d51b34ae2ae4ad9ce07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999316"
---
# <a name="networknametype-simple-type"></a><span data-ttu-id="5ac30-103">Простой тип Нетворкнаметипе</span><span class="sxs-lookup"><span data-stu-id="5ac30-103">networkNameType Simple Type</span></span>

<span data-ttu-id="5ac30-104">Простой тип Нетворкнаметипе определяет строковый тип для идентификаторов набора служб (SSID).</span><span class="sxs-lookup"><span data-stu-id="5ac30-104">The networkNameType simple type defines a string type for service set identifiers (SSIDs).</span></span> <span data-ttu-id="5ac30-105">Идентификатор SSID — это строка, которая состоит по крайней мере из одного символа и не длиннее 32 символов.</span><span class="sxs-lookup"><span data-stu-id="5ac30-105">A SSID is a string that is at least one character long and at most 32 characters long.</span></span>

``` syntax
<xs:simpleType name="networkNameType">
    <xs:restriction
        base="string"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="32"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="5ac30-106">Требования</span><span class="sxs-lookup"><span data-stu-id="5ac30-106">Requirements</span></span>



| <span data-ttu-id="5ac30-107">Требование</span><span class="sxs-lookup"><span data-stu-id="5ac30-107">Requirement</span></span> | <span data-ttu-id="5ac30-108">Значение</span><span class="sxs-lookup"><span data-stu-id="5ac30-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5ac30-109">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5ac30-109">Minimum supported client</span></span><br/> | <span data-ttu-id="5ac30-110">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5ac30-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5ac30-111">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5ac30-111">Minimum supported server</span></span><br/> | <span data-ttu-id="5ac30-112">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5ac30-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




