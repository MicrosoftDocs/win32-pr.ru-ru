---
description: Указывает период времени в секундах, в течение которого клиент не будет повторно пытаться пройти проверку подлинности после неудачной попытки проверки подлинности.
ms.assetid: a6b32e88-da36-4aea-a01d-f5f7bc37d171
title: Элемент Хелдпериод (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- heldPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: f8664543a9ea5b0f3b290168129e589e9ccd68ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663047"
---
# <a name="heldperiod-onex-element"></a><span data-ttu-id="968ca-103">Элемент Хелдпериод (OneX)</span><span class="sxs-lookup"><span data-stu-id="968ca-103">heldPeriod (OneX) Element</span></span>

<span data-ttu-id="968ca-104">Элемент Хелдпериод (OneX) указывает продолжительность времени в секундах, в течение которого клиент не будет повторно пытаться пройти проверку подлинности после неудачной попытки проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="968ca-104">The heldPeriod (OneX) element specifies the length of time, in seconds, in which a client will not re-attempt authentication after a failed authentication attempt.</span></span>

<span data-ttu-id="968ca-105">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="968ca-105">This element is optional.</span></span> <span data-ttu-id="968ca-106">Если Хелдпериод не указан в профиле, используется значение, равное 1 секунде.</span><span class="sxs-lookup"><span data-stu-id="968ca-106">When heldPeriod is not specified in a profile, a value of 1 second is used.</span></span>

<span data-ttu-id="968ca-107">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент будет пропущен, если он есть в профиле.</span><span class="sxs-lookup"><span data-stu-id="968ca-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="heldPeriod">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="3600"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="968ca-108">Элемент **хелдпериод** определяется элементом [**OneX**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="968ca-108">The **heldPeriod** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="968ca-109">Требования</span><span class="sxs-lookup"><span data-stu-id="968ca-109">Requirements</span></span>



| <span data-ttu-id="968ca-110">Требование</span><span class="sxs-lookup"><span data-stu-id="968ca-110">Requirement</span></span> | <span data-ttu-id="968ca-111">Значение</span><span class="sxs-lookup"><span data-stu-id="968ca-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="968ca-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="968ca-112">Minimum supported client</span></span><br/> | <span data-ttu-id="968ca-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="968ca-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="968ca-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="968ca-114">Minimum supported server</span></span><br/> | <span data-ttu-id="968ca-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="968ca-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="968ca-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="968ca-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="968ca-117">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="968ca-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="968ca-118">**Таймаут**</span><span class="sxs-lookup"><span data-stu-id="968ca-118">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="968ca-119">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="968ca-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="968ca-120">**Таймаут**</span><span class="sxs-lookup"><span data-stu-id="968ca-120">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




