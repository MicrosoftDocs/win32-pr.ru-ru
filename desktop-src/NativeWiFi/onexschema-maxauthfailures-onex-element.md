---
description: Указывает максимальное количество ошибок проверки подлинности, разрешенных для набора учетных данных.
ms.assetid: 191b6b03-8b27-4b35-8623-1ccec632f208
title: Элемент Максаусфаилурес (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxAuthFailures
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 31dae7a8805275254a1d398108128380b1aa2e54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545399"
---
# <a name="maxauthfailures-onex-element"></a><span data-ttu-id="241d8-103">Элемент Максаусфаилурес (OneX)</span><span class="sxs-lookup"><span data-stu-id="241d8-103">maxAuthFailures (OneX) Element</span></span>

<span data-ttu-id="241d8-104">Элемент Максаусфаилурес (OneX) указывает максимальное количество ошибок проверки подлинности, разрешенных для набора учетных данных.</span><span class="sxs-lookup"><span data-stu-id="241d8-104">The maxAuthFailures (OneX) element specifies the maximum number of authentication failures allowed for a set of credentials.</span></span>

<span data-ttu-id="241d8-105">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="241d8-105">This element is optional.</span></span> <span data-ttu-id="241d8-106">Если Максаусфаилурес не указан в профиле, используется значение, равное единице.</span><span class="sxs-lookup"><span data-stu-id="241d8-106">When maxAuthFailures is not specified in a profile, a value of one is used.</span></span>

<span data-ttu-id="241d8-107">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент будет пропущен, если он есть в профиле.</span><span class="sxs-lookup"><span data-stu-id="241d8-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="maxAuthFailures">
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

<span data-ttu-id="241d8-108">Элемент **максаусфаилурес** определяется элементом [**OneX**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="241d8-108">The **maxAuthFailures** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="241d8-109">Требования</span><span class="sxs-lookup"><span data-stu-id="241d8-109">Requirements</span></span>



| <span data-ttu-id="241d8-110">Требование</span><span class="sxs-lookup"><span data-stu-id="241d8-110">Requirement</span></span> | <span data-ttu-id="241d8-111">Значение</span><span class="sxs-lookup"><span data-stu-id="241d8-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="241d8-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="241d8-112">Minimum supported client</span></span><br/> | <span data-ttu-id="241d8-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="241d8-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="241d8-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="241d8-114">Minimum supported server</span></span><br/> | <span data-ttu-id="241d8-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="241d8-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="241d8-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="241d8-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="241d8-117">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="241d8-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="241d8-118">**Таймаут**</span><span class="sxs-lookup"><span data-stu-id="241d8-118">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="241d8-119">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="241d8-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="241d8-120">**Таймаут**</span><span class="sxs-lookup"><span data-stu-id="241d8-120">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




