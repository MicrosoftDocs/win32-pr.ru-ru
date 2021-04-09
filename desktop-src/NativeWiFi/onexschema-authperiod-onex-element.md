---
description: Указывает максимальный интервал времени (в секундах), в течение которого клиент ожидает ответа от средства проверки подлинности.
ms.assetid: 5cb2e164-913f-4c35-854f-aac8ed180c46
title: Элемент Ауспериод (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 098391a672eedd2657dbd7ad5913fef13fde98cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080758"
---
# <a name="authperiod-onex-element"></a><span data-ttu-id="ea295-103">Элемент Ауспериод (OneX)</span><span class="sxs-lookup"><span data-stu-id="ea295-103">authPeriod (OneX) Element</span></span>

<span data-ttu-id="ea295-104">Элемент Ауспериод (OneX) задает максимальный интервал времени в секундах, в течение которого клиент ожидает ответа от средства проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="ea295-104">The authPeriod (OneX) element specifies the maximum length of time, in seconds, in which a client waits for a response from the authenticator.</span></span> <span data-ttu-id="ea295-105">Если ответ не получен в течение указанного периода, клиент предполагает, что в сети отсутствует средство проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="ea295-105">If a response is not received within the specified period, the client assumes that there is no authenticator present on the network.</span></span>

<span data-ttu-id="ea295-106">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="ea295-106">This element is optional.</span></span> <span data-ttu-id="ea295-107">Если Ауспериод не указан в профиле, используется значение 18 секунд.</span><span class="sxs-lookup"><span data-stu-id="ea295-107">When authPeriod is not specified in a profile, a value of 18 seconds is used.</span></span>

<span data-ttu-id="ea295-108">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент будет пропущен, если он есть в профиле.</span><span class="sxs-lookup"><span data-stu-id="ea295-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="authPeriod">
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

<span data-ttu-id="ea295-109">Элемент **ауспериод** определяется элементом [**OneX**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ea295-109">The **authPeriod** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea295-110">Требования</span><span class="sxs-lookup"><span data-stu-id="ea295-110">Requirements</span></span>



| <span data-ttu-id="ea295-111">Требование</span><span class="sxs-lookup"><span data-stu-id="ea295-111">Requirement</span></span> | <span data-ttu-id="ea295-112">Значение</span><span class="sxs-lookup"><span data-stu-id="ea295-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ea295-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ea295-113">Minimum supported client</span></span><br/> | <span data-ttu-id="ea295-114">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ea295-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ea295-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ea295-115">Minimum supported server</span></span><br/> | <span data-ttu-id="ea295-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ea295-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ea295-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ea295-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="ea295-118">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="ea295-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ea295-119">**Таймаут**</span><span class="sxs-lookup"><span data-stu-id="ea295-119">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="ea295-120">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="ea295-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ea295-121">**Таймаут**</span><span class="sxs-lookup"><span data-stu-id="ea295-121">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




