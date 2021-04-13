---
description: Указывает период времени (в секундах) ожидания перед отправкой EAPOL-Start.
ms.assetid: 6163eeb9-23a8-4e34-ad3f-016946e241e2
title: Элемент Стартпериод (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- startPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a583403a354cbefe93387be2d5af06958bbf6b28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345345"
---
# <a name="startperiod-onex-element"></a><span data-ttu-id="07de7-103">Элемент Стартпериод (OneX)</span><span class="sxs-lookup"><span data-stu-id="07de7-103">startPeriod (OneX) Element</span></span>

<span data-ttu-id="07de7-104">Элемент Стартпериод (OneX) указывает время ожидания (в секундах) перед отправкой EAPOL-Start.</span><span class="sxs-lookup"><span data-stu-id="07de7-104">The startPeriod (OneX) element specifies the length of time, in seconds, to wait before an EAPOL-Start is sent.</span></span> <span data-ttu-id="07de7-105">Для запуска процесса проверки подлинности 802.1 X отправляется сообщение EAPOL-Start.</span><span class="sxs-lookup"><span data-stu-id="07de7-105">An EAPOL-Start message is sent to start the 802.1X authentication process.</span></span>

<span data-ttu-id="07de7-106">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="07de7-106">This element is optional.</span></span> <span data-ttu-id="07de7-107">Если Стартпериод не указан в профиле, используется значение 5 секунд.</span><span class="sxs-lookup"><span data-stu-id="07de7-107">When startPeriod is not specified in a profile, a value of 5 seconds is used.</span></span>

<span data-ttu-id="07de7-108">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент будет пропущен, если он есть в профиле.</span><span class="sxs-lookup"><span data-stu-id="07de7-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="startPeriod">
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

<span data-ttu-id="07de7-109">Элемент **стартпериод** определяется элементом [**OneX**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="07de7-109">The **startPeriod** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="07de7-110">Требования</span><span class="sxs-lookup"><span data-stu-id="07de7-110">Requirements</span></span>



| <span data-ttu-id="07de7-111">Требование</span><span class="sxs-lookup"><span data-stu-id="07de7-111">Requirement</span></span> | <span data-ttu-id="07de7-112">Значение</span><span class="sxs-lookup"><span data-stu-id="07de7-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="07de7-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="07de7-113">Minimum supported client</span></span><br/> | <span data-ttu-id="07de7-114">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="07de7-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="07de7-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="07de7-115">Minimum supported server</span></span><br/> | <span data-ttu-id="07de7-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="07de7-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="07de7-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07de7-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="07de7-118">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="07de7-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="07de7-119">**Таймаут**</span><span class="sxs-lookup"><span data-stu-id="07de7-119">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="07de7-120">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="07de7-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="07de7-121">**Таймаут**</span><span class="sxs-lookup"><span data-stu-id="07de7-121">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




