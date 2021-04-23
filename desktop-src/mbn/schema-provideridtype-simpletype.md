---
description: Определяет тип для элемента ProviderID профиля мобильного широкополосного подключения.
ms.assetid: 84193749-c98d-4313-bf99-3da1c74d7cc4
title: Простой тип Провидеридтипе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerIdType
api_type:
- Schema
ms.openlocfilehash: ec3c952395be048d18305172e64618fa26313f46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144788"
---
# <a name="provideridtype-simple-type"></a><span data-ttu-id="f17ea-103">Простой тип Провидеридтипе</span><span class="sxs-lookup"><span data-stu-id="f17ea-103">providerIdType Simple Type</span></span>

<span data-ttu-id="f17ea-104">Простой тип **провидеридтипе** определяет тип для элемента [**ProviderID**](schema-providerid-providertype-element.md) профиля мобильного широкополосного подключения.</span><span class="sxs-lookup"><span data-stu-id="f17ea-104">The **providerIdType** simple type defines a type for the [**ProviderID**](schema-providerid-providertype-element.md) element of the Mobile Broadband profile.</span></span> <span data-ttu-id="f17ea-105">Этот тип представляет собой набор цифр длиной не менее одной цифры и не более 6 цифр.</span><span class="sxs-lookup"><span data-stu-id="f17ea-105">This type is a collection of digits at least one digit long and at most 6 digits long.</span></span>

``` syntax
<xs:simpleType name="providerIdType">
    <xs:restriction
        base="token"
    >
        <xs:pattern
            value="\d{1,6}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="f17ea-106">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="f17ea-106">Patterns</span></span>

<span data-ttu-id="f17ea-107">Простой тип **провидеридтипе** — это токен, который ограничен следующим шаблоном:</span><span class="sxs-lookup"><span data-stu-id="f17ea-107">The **providerIdType** simple type is a token that is restricted by the following pattern:</span></span>

-   `\d{1,6}`

## <a name="requirements"></a><span data-ttu-id="f17ea-108">Требования</span><span class="sxs-lookup"><span data-stu-id="f17ea-108">Requirements</span></span>



| <span data-ttu-id="f17ea-109">Требование</span><span class="sxs-lookup"><span data-stu-id="f17ea-109">Requirement</span></span> | <span data-ttu-id="f17ea-110">Значение</span><span class="sxs-lookup"><span data-stu-id="f17ea-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="f17ea-111">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f17ea-111">Minimum supported client</span></span><br/> | <span data-ttu-id="f17ea-112">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="f17ea-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="f17ea-113">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f17ea-113">Minimum supported server</span></span><br/> | <span data-ttu-id="f17ea-114">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f17ea-114">None supported</span></span><br/>                         |



 

 




