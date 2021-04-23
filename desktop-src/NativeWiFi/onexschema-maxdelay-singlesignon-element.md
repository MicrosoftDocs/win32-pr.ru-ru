---
description: Указывает максимальную задержку в секундах, по истечении которой попытка подключения единого входа завершается неудачей.
ms.assetid: ba8c137e-dd05-4ebc-9a83-cd612f65d4dc
title: Максделай (singleSignOn), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxDelay
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8efd069687a2db4b06b90aa594ec31132ce6fc9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909431"
---
# <a name="maxdelay-singlesignon-element"></a><span data-ttu-id="71925-103">Максделай (singleSignOn), элемент</span><span class="sxs-lookup"><span data-stu-id="71925-103">maxDelay (singleSignOn) Element</span></span>

<span data-ttu-id="71925-104">Элемент Максделай (singleSignOn) указывает в секундах максимальную задержку перед неудачной попыткой подключения единого входа.</span><span class="sxs-lookup"><span data-stu-id="71925-104">The maxDelay (singleSignOn) element specifies, in seconds, the maximum delay before the single sign on connection attempt fails.</span></span>

<span data-ttu-id="71925-105">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="71925-105">This element is optional.</span></span> <span data-ttu-id="71925-106">Если Максделай не указан в профиле, используется значение 10 секунд.</span><span class="sxs-lookup"><span data-stu-id="71925-106">When maxDelay is not specified in a profile, a value of 10 seconds is used.</span></span>

<span data-ttu-id="71925-107">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент будет пропущен, если он есть в профиле.</span><span class="sxs-lookup"><span data-stu-id="71925-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="maxDelay">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="0"
             />
            <xs:enumeration
                value="120"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="71925-108">Элемент **максделай** определяется элементом [**singleSignOn**](onexschema-singlesignon-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="71925-108">The **maxDelay** element is defined by the [**singleSignOn**](onexschema-singlesignon-onex-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="71925-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="71925-109">Remarks</span></span>

<span data-ttu-id="71925-110">Этот параметр можно задать в командной строке с помощью команды **netsh wlan set профилепараметер** .</span><span class="sxs-lookup"><span data-stu-id="71925-110">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="71925-111">Дополнительные сведения см. в разделе [команды Netsh для беспроводной локальной сети (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="71925-111">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="71925-112">Требования</span><span class="sxs-lookup"><span data-stu-id="71925-112">Requirements</span></span>



| <span data-ttu-id="71925-113">Требование</span><span class="sxs-lookup"><span data-stu-id="71925-113">Requirement</span></span> | <span data-ttu-id="71925-114">Значение</span><span class="sxs-lookup"><span data-stu-id="71925-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="71925-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="71925-115">Minimum supported client</span></span><br/> | <span data-ttu-id="71925-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="71925-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="71925-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="71925-117">Minimum supported server</span></span><br/> | <span data-ttu-id="71925-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="71925-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="71925-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71925-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="71925-120">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="71925-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="71925-121">**singleSignOn**</span><span class="sxs-lookup"><span data-stu-id="71925-121">**singleSignOn**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> <dt>

<span data-ttu-id="71925-122">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="71925-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="71925-123">**singleSignOn (OneX)**</span><span class="sxs-lookup"><span data-stu-id="71925-123">**singleSignOn (OneX)**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 
