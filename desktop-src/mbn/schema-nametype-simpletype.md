---
description: Определяет тип строки для профиля мобильного широкополосного подключения.
ms.assetid: a5c14c39-2731-44f0-9fd2-e78d900b66f0
title: простой тип Наметипе (мобильное широкополосное подключение)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
ms.openlocfilehash: d8c6032e17eaf2d067dc23030a7a6279bd41eafa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662415"
---
# <a name="nametype-simple-type-mobile-broadband"></a><span data-ttu-id="e4d21-103">простой тип Наметипе (мобильное широкополосное подключение)</span><span class="sxs-lookup"><span data-stu-id="e4d21-103">nameType simple type (Mobile Broadband)</span></span>

<span data-ttu-id="e4d21-104">Простой тип **наметипе** определяет строковый тип для профиля мобильного широкополосного подключения.</span><span class="sxs-lookup"><span data-stu-id="e4d21-104">The **nameType** simple type defines a string type for the Mobile Broadband profile.</span></span> <span data-ttu-id="e4d21-105">Эта строка состоит по меньшей мере из одного символа и не длиннее 255 символов.</span><span class="sxs-lookup"><span data-stu-id="e4d21-105">This string is at least one character long and at most 255 characters long.</span></span>

``` syntax
<xs:simpleType name="nameType">
    <xs:restriction
        base="normalizedString"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="255"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="e4d21-106">Требования</span><span class="sxs-lookup"><span data-stu-id="e4d21-106">Requirements</span></span>



| <span data-ttu-id="e4d21-107">Требование</span><span class="sxs-lookup"><span data-stu-id="e4d21-107">Requirement</span></span> | <span data-ttu-id="e4d21-108">Значение</span><span class="sxs-lookup"><span data-stu-id="e4d21-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="e4d21-109">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e4d21-109">Minimum supported client</span></span><br/> | <span data-ttu-id="e4d21-110">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="e4d21-110">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="e4d21-111">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e4d21-111">Minimum supported server</span></span><br/> | <span data-ttu-id="e4d21-112">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e4d21-112">None supported</span></span><br/>                         |



 

 




