---
description: Определяет тип для элемента СимикЦид профиля мобильного широкополосного подключения.
ms.assetid: ce77180e-71e2-4cef-84e0-32397216385f
title: Простой тип СимикЦидтипе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- simIccIDType
api_type:
- Schema
ms.openlocfilehash: 410145e659a4845c9c96aaeb76d522de3e0c7b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662409"
---
# <a name="simiccidtype-simple-type"></a><span data-ttu-id="16a1c-103">Простой тип СимикЦидтипе</span><span class="sxs-lookup"><span data-stu-id="16a1c-103">simIccIDType Simple Type</span></span>

<span data-ttu-id="16a1c-104">Простой тип **симикЦидтипе** определяет тип для элемента [**СимикЦид**](schema-simiccid-mbnprofile-element.md) профиля мобильного широкополосного подключения.</span><span class="sxs-lookup"><span data-stu-id="16a1c-104">The **simIccIDType** simple type defines a type for the [**SimIccID**](schema-simiccid-mbnprofile-element.md) element of the Mobile Broadband profile.</span></span> <span data-ttu-id="16a1c-105">Этот тип представляет собой набор цифр и (или) букв верхнего и нижнего регистра, по крайней мере один символ и длину не более 20 символов.</span><span class="sxs-lookup"><span data-stu-id="16a1c-105">This type is a collection of digits and/or upper- and lower-case letters, at least one character long and at most 20 characters long.</span></span>

``` syntax
<xs:simpleType name="simIccIDType">
    <xs:restriction
        base="token"
    >
        <xs:pattern
            value="[a-zA-Z\d]{1,20}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="16a1c-106">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="16a1c-106">Patterns</span></span>

<span data-ttu-id="16a1c-107">Простой тип **симикЦидтипе** — это токен, который ограничен следующим шаблоном:</span><span class="sxs-lookup"><span data-stu-id="16a1c-107">The **simIccIDType** simple type is a token that is restricted by the following pattern:</span></span>

-   `[a-zA-Z\d]{1,20}`

## <a name="requirements"></a><span data-ttu-id="16a1c-108">Требования</span><span class="sxs-lookup"><span data-stu-id="16a1c-108">Requirements</span></span>



| <span data-ttu-id="16a1c-109">Требование</span><span class="sxs-lookup"><span data-stu-id="16a1c-109">Requirement</span></span> | <span data-ttu-id="16a1c-110">Значение</span><span class="sxs-lookup"><span data-stu-id="16a1c-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="16a1c-111">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="16a1c-111">Minimum supported client</span></span><br/> | <span data-ttu-id="16a1c-112">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="16a1c-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="16a1c-113">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="16a1c-113">Minimum supported server</span></span><br/> | <span data-ttu-id="16a1c-114">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="16a1c-114">None supported</span></span><br/>                         |



 

 




