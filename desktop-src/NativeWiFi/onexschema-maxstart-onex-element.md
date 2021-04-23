---
description: Указывает максимальное число отправленных сообщений EAPOL-Start.
ms.assetid: 4e48f8b6-46eb-426e-ad22-3aa53cb66a17
title: Элемент Максстарт (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxStart
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 14bf40538eafb3c8e78b68b7a435d0d37d401960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673656"
---
# <a name="maxstart-onex-element"></a><span data-ttu-id="17666-103">Элемент Максстарт (OneX)</span><span class="sxs-lookup"><span data-stu-id="17666-103">maxStart (OneX) Element</span></span>

<span data-ttu-id="17666-104">Элемент Максстарт (OneX) указывает максимальное число отправленных сообщений EAPOL-Start.</span><span class="sxs-lookup"><span data-stu-id="17666-104">The maxStart (OneX) element specifies the maximum number of EAPOL-Start messages sent.</span></span> <span data-ttu-id="17666-105">После отправки максимального числа EAPOL-Start сообщений клиент предполагает, что в сети отсутствует средство проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="17666-105">After the maximum number of EAPOL-Start messages has been sent, the client assumes that there is no authenticator present on the network.</span></span>

<span data-ttu-id="17666-106">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="17666-106">This element is optional.</span></span> <span data-ttu-id="17666-107">Если Максстарт не указан в профиле, используется значение 3 сообщения.</span><span class="sxs-lookup"><span data-stu-id="17666-107">When maxStart is not specified in a profile, a value of 3 messages is used.</span></span>

<span data-ttu-id="17666-108">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент будет пропущен, если он есть в профиле.</span><span class="sxs-lookup"><span data-stu-id="17666-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="maxStart">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="100"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="17666-109">Элемент **максстарт** определяется элементом [**OneX**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="17666-109">The **maxStart** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="17666-110">Требования</span><span class="sxs-lookup"><span data-stu-id="17666-110">Requirements</span></span>



| <span data-ttu-id="17666-111">Требование</span><span class="sxs-lookup"><span data-stu-id="17666-111">Requirement</span></span> | <span data-ttu-id="17666-112">Значение</span><span class="sxs-lookup"><span data-stu-id="17666-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="17666-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="17666-113">Minimum supported client</span></span><br/> | <span data-ttu-id="17666-114">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="17666-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="17666-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="17666-115">Minimum supported server</span></span><br/> | <span data-ttu-id="17666-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="17666-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="17666-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="17666-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="17666-118">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="17666-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="17666-119">**Таймаут**</span><span class="sxs-lookup"><span data-stu-id="17666-119">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="17666-120">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="17666-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="17666-121">**Таймаут**</span><span class="sxs-lookup"><span data-stu-id="17666-121">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




