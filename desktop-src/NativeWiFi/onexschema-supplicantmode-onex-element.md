---
description: Указывает метод передачи, используемый для сообщений EAPOL-Start.
ms.assetid: 8d49d19a-8122-4191-bb46-92a2016bcfee
title: Элемент Суппликантмоде (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- supplicantMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 33d58bd247a220ca93ed4d2a05886be107afd4c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673654"
---
# <a name="supplicantmode-onex-element"></a><span data-ttu-id="b0a7f-103">Элемент Суппликантмоде (OneX)</span><span class="sxs-lookup"><span data-stu-id="b0a7f-103">supplicantMode (OneX) Element</span></span>

<span data-ttu-id="b0a7f-104">Элемент Суппликантмоде (OneX) указывает метод передачи, используемый для сообщений EAPOL-Start.</span><span class="sxs-lookup"><span data-stu-id="b0a7f-104">The supplicantMode (OneX) element specifies the method of transmission used for EAPOL-Start messages.</span></span> <span data-ttu-id="b0a7f-105">В следующей таблице описаны возможные значения.</span><span class="sxs-lookup"><span data-stu-id="b0a7f-105">The following table describes the possible values.</span></span>



| <span data-ttu-id="b0a7f-106">Значение</span><span class="sxs-lookup"><span data-stu-id="b0a7f-106">Value</span></span>               | <span data-ttu-id="b0a7f-107">Описание</span><span class="sxs-lookup"><span data-stu-id="b0a7f-107">Description</span></span>                                                                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0a7f-108">инхибиттрансмиссион</span><span class="sxs-lookup"><span data-stu-id="b0a7f-108">inhibitTransmission</span></span> | <span data-ttu-id="b0a7f-109">EAPOL-Start сообщения не передаются.</span><span class="sxs-lookup"><span data-stu-id="b0a7f-109">EAPOL-Start messages are not transmitted.</span></span> <span data-ttu-id="b0a7f-110">Допустимо только для профилей проводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="b0a7f-110">Valid for wired LAN profiles only.</span></span>                                                                                             |
| <span data-ttu-id="b0a7f-111">инклуделеарнинг</span><span class="sxs-lookup"><span data-stu-id="b0a7f-111">includeLearning</span></span>     | <span data-ttu-id="b0a7f-112">Клиент определяет, когда следует отсылать пакеты EAPOL-Start на основе сетевых возможностей.</span><span class="sxs-lookup"><span data-stu-id="b0a7f-112">The client determines when to send EAPOL-Start packets based on network capability.</span></span> <span data-ttu-id="b0a7f-113">EAPOL-Start сообщения отправляются только при необходимости.</span><span class="sxs-lookup"><span data-stu-id="b0a7f-113">EAPOL-Start messages are only sent when required.</span></span> <span data-ttu-id="b0a7f-114">Допустимо только для профилей проводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="b0a7f-114">Valid for wired LAN profiles only.</span></span> |
| <span data-ttu-id="b0a7f-115">compliant (соответствует);</span><span class="sxs-lookup"><span data-stu-id="b0a7f-115">compliant</span></span>           | <span data-ttu-id="b0a7f-116">EAPOL-Start сообщения передаются, как указано в 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="b0a7f-116">EAPOL-Start messages are transmitted as specified by 802.1X.</span></span> <span data-ttu-id="b0a7f-117">Допустимо для профилей проводной и беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="b0a7f-117">Valid for both wired and wireless LAN profiles.</span></span>                                                             |



 

<span data-ttu-id="b0a7f-118">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b0a7f-118">This element is optional.</span></span> <span data-ttu-id="b0a7f-119">Если Суппликантмоде не указан в профиле, `compliant` для проводной и беспроводной локальной сети используется значение.</span><span class="sxs-lookup"><span data-stu-id="b0a7f-119">When supplicantMode is not specified in a profile, a value of `compliant` is used for both wired and wireless LAN profiles.</span></span>

<span data-ttu-id="b0a7f-120">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент будет пропущен, если он есть в профиле.</span><span class="sxs-lookup"><span data-stu-id="b0a7f-120">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="supplicantMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="inhibitTransmission"
             />
            <xs:enumeration
                value="includeLearning"
             />
            <xs:enumeration
                value="compliant"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="b0a7f-121">Элемент **суппликантмоде** определяется элементом [**OneX**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b0a7f-121">The **supplicantMode** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0a7f-122">Требования</span><span class="sxs-lookup"><span data-stu-id="b0a7f-122">Requirements</span></span>



| <span data-ttu-id="b0a7f-123">Требование</span><span class="sxs-lookup"><span data-stu-id="b0a7f-123">Requirement</span></span> | <span data-ttu-id="b0a7f-124">Значение</span><span class="sxs-lookup"><span data-stu-id="b0a7f-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b0a7f-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b0a7f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b0a7f-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b0a7f-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b0a7f-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b0a7f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b0a7f-128">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b0a7f-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b0a7f-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0a7f-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="b0a7f-130">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="b0a7f-130">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b0a7f-131">**Таймаут**</span><span class="sxs-lookup"><span data-stu-id="b0a7f-131">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="b0a7f-132">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="b0a7f-132">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b0a7f-133">**Таймаут**</span><span class="sxs-lookup"><span data-stu-id="b0a7f-133">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




