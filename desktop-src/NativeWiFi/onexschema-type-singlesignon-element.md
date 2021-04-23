---
description: Указывает, когда выполняется единый вход.
ms.assetid: 23a7ab31-b29d-4f45-a384-bb2d2c18230f
title: Элемент Type (singleSignOn)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- type
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 947c8801e5b2534f4c3b4e548a2a2f2c7a4250d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673335"
---
# <a name="type-singlesignon-element"></a><span data-ttu-id="4ddf9-103">Элемент Type (singleSignOn)</span><span class="sxs-lookup"><span data-stu-id="4ddf9-103">type (singleSignOn) Element</span></span>

<span data-ttu-id="4ddf9-104">Элемент Type (singleSignOn) определяет, когда выполняется единый вход.</span><span class="sxs-lookup"><span data-stu-id="4ddf9-104">The type (singleSignOn) element specifies when single sign on is performed.</span></span> <span data-ttu-id="4ddf9-105">Если задано значение `preLogon` , единый вход выполняется до входа пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="4ddf9-105">When set to `preLogon`, single sign on is performed before the user logs on.</span></span> <span data-ttu-id="4ddf9-106">Если задано значение `postLogon` , единый вход выполняется сразу после входа пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="4ddf9-106">When set to `postLogon`, single sign on is performed immediately after the user logs on.</span></span>

<span data-ttu-id="4ddf9-107">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент будет пропущен, если он есть в профиле.</span><span class="sxs-lookup"><span data-stu-id="4ddf9-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="type"
    minOccurs="1"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="preLogon"
             />
            <xs:enumeration
                value="postLogon"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="4ddf9-108">Элемент **Type** определяется элементом [**singleSignOn**](onexschema-singlesignon-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="4ddf9-108">The **type** element is defined by the [**singleSignOn**](onexschema-singlesignon-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ddf9-109">Требования</span><span class="sxs-lookup"><span data-stu-id="4ddf9-109">Requirements</span></span>



| <span data-ttu-id="4ddf9-110">Требование</span><span class="sxs-lookup"><span data-stu-id="4ddf9-110">Requirement</span></span> | <span data-ttu-id="4ddf9-111">Значение</span><span class="sxs-lookup"><span data-stu-id="4ddf9-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4ddf9-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4ddf9-112">Minimum supported client</span></span><br/> | <span data-ttu-id="4ddf9-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4ddf9-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4ddf9-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4ddf9-114">Minimum supported server</span></span><br/> | <span data-ttu-id="4ddf9-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4ddf9-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4ddf9-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4ddf9-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="4ddf9-117">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="4ddf9-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="4ddf9-118">**singleSignOn**</span><span class="sxs-lookup"><span data-stu-id="4ddf9-118">**singleSignOn**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> <dt>

<span data-ttu-id="4ddf9-119">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="4ddf9-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="4ddf9-120">**singleSignOn (OneX)**</span><span class="sxs-lookup"><span data-stu-id="4ddf9-120">**singleSignOn (OneX)**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 




