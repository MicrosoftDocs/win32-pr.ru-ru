---
description: Определяет тип для элемента Субскриберид профиля мобильного широкополосного подключения.
ms.assetid: b36df4d3-f558-4af8-8f63-e4991c34990f
title: Простой тип Субскриберидтипе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- subscriberIdType
api_type:
- Schema
ms.openlocfilehash: c3c776bbd721bbb03b4f5549f87d48248a35206b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072723"
---
# <a name="subscriberidtype-simple-type"></a><span data-ttu-id="07c52-103">Простой тип Субскриберидтипе</span><span class="sxs-lookup"><span data-stu-id="07c52-103">subscriberIdType Simple Type</span></span>

<span data-ttu-id="07c52-104">Простой тип **субскриберидтипе** определяет тип для элемента [**Субскриберид**](schema-subscriberid-mbnprofile-element.md) профиля мобильного широкополосного подключения.</span><span class="sxs-lookup"><span data-stu-id="07c52-104">The **subscriberIdType** simple type defines a type for the [**SubscriberID**](schema-subscriberid-mbnprofile-element.md) element of the Mobile Broadband profile.</span></span> <span data-ttu-id="07c52-105">Этот тип представляет собой коллекцию из одного или нескольких символов.</span><span class="sxs-lookup"><span data-stu-id="07c52-105">This type is a collection of one or more characters.</span></span>

``` syntax
<xs:simpleType name="subscriberIdType">
    <xs:restriction
        base="token"
    >
        <xs:minLength
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="07c52-106">Требования</span><span class="sxs-lookup"><span data-stu-id="07c52-106">Requirements</span></span>



| <span data-ttu-id="07c52-107">Требование</span><span class="sxs-lookup"><span data-stu-id="07c52-107">Requirement</span></span> | <span data-ttu-id="07c52-108">Значение</span><span class="sxs-lookup"><span data-stu-id="07c52-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="07c52-109">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="07c52-109">Minimum supported client</span></span><br/> | <span data-ttu-id="07c52-110">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="07c52-110">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="07c52-111">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="07c52-111">Minimum supported server</span></span><br/> | <span data-ttu-id="07c52-112">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="07c52-112">None supported</span></span><br/>                         |



 

 




