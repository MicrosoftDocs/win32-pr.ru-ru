---
description: Указывает, изменяется ли виртуальная локальная сеть (VLAN), используемая устройством, на основе учетных данных пользователя.
ms.assetid: 4ac92954-adb2-4b0c-9c4e-81f772ea03ed
title: Усербаседвиртуаллан (singleSignOn), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- userBasedVirtualLan
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6ef421e35f7fa121c31e58cfeba4eee969a1b6fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154578"
---
# <a name="userbasedvirtuallan-singlesignon-element"></a><span data-ttu-id="de22c-103">Усербаседвиртуаллан (singleSignOn), элемент</span><span class="sxs-lookup"><span data-stu-id="de22c-103">userBasedVirtualLan (singleSignOn) Element</span></span>

<span data-ttu-id="de22c-104">Элемент Усербаседвиртуаллан (singleSignOn) указывает, изменяется ли виртуальная локальная сеть (VLAN), используемая устройством, на основе учетных данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="de22c-104">The userBasedVirtualLan (singleSignOn) element specifies if the virtual LAN (VLAN) used by the device changes based on the user's credentials.</span></span> <span data-ttu-id="de22c-105">Некоторые устройства сервера сетевого доступа (NAS) изменяют виртуальную локальную сеть после проверки подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="de22c-105">Some network access server (NAS) devices change the VLAN after a user authenticates.</span></span> <span data-ttu-id="de22c-106">Когда Усербаседвиртуаллан имеет значение TRUE, NAS может изменить виртуальную ЛС устройства после проверки подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="de22c-106">When userBasedVirtualLan is TRUE, the NAS may change a device's VLAN after a user authenticates.</span></span>

<span data-ttu-id="de22c-107">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="de22c-107">This element is optional.</span></span> <span data-ttu-id="de22c-108">Если Усербаседвиртуаллан не указан в профиле, используется значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="de22c-108">When userBasedVirtualLan is not specified in a profile, a value of FALSE is used.</span></span>

<span data-ttu-id="de22c-109">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент будет пропущен, если он есть в профиле.</span><span class="sxs-lookup"><span data-stu-id="de22c-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="userBasedVirtualLan"
    type="boolean"
    minOccurs="0"
 />
```

<span data-ttu-id="de22c-110">Элемент **усербаседвиртуаллан** определяется элементом [**singleSignOn**](onexschema-singlesignon-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="de22c-110">The **userBasedVirtualLan** element is defined by the [**singleSignOn**](onexschema-singlesignon-onex-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="de22c-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="de22c-111">Remarks</span></span>

<span data-ttu-id="de22c-112">Этот параметр можно задать в командной строке с помощью команды **netsh wlan set профилепараметер** .</span><span class="sxs-lookup"><span data-stu-id="de22c-112">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="de22c-113">Дополнительные сведения см. в разделе [команды Netsh для беспроводной локальной сети (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="de22c-113">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="de22c-114">Требования</span><span class="sxs-lookup"><span data-stu-id="de22c-114">Requirements</span></span>



| <span data-ttu-id="de22c-115">Требование</span><span class="sxs-lookup"><span data-stu-id="de22c-115">Requirement</span></span> | <span data-ttu-id="de22c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="de22c-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="de22c-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="de22c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="de22c-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="de22c-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="de22c-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="de22c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="de22c-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="de22c-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="de22c-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="de22c-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="de22c-122">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="de22c-122">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="de22c-123">**singleSignOn**</span><span class="sxs-lookup"><span data-stu-id="de22c-123">**singleSignOn**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> <dt>

<span data-ttu-id="de22c-124">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="de22c-124">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="de22c-125">**singleSignOn (OneX)**</span><span class="sxs-lookup"><span data-stu-id="de22c-125">**singleSignOn (OneX)**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 
