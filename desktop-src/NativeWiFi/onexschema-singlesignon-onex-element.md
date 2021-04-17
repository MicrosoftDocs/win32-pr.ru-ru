---
description: Задает сведения о конфигурации сети единого входа (SSO).
ms.assetid: c0a26f15-77fd-43e9-a6af-54e9b46f03fa
title: Элемент singleSignOn (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- singleSignOn
api_type:
- Schema
api_location: ''
ms.openlocfilehash: fd25767ed311e9a6f0e75f8dec090d4b80d3f0af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673655"
---
# <a name="singlesignon-onex-element"></a><span data-ttu-id="db4f4-103">Элемент singleSignOn (OneX)</span><span class="sxs-lookup"><span data-stu-id="db4f4-103">singleSignOn (OneX) Element</span></span>

<span data-ttu-id="db4f4-104">Элемент singleSignOn (OneX) задает сведения о конфигурации сети единого входа (SSO).</span><span class="sxs-lookup"><span data-stu-id="db4f4-104">The singleSignOn (OneX) element specifies single sign-on (SSO) network configuration information.</span></span>

<span data-ttu-id="db4f4-105">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="db4f4-105">This element is optional.</span></span> <span data-ttu-id="db4f4-106">Не используйте элемент singleSignOn в профиле, если он не требуется в сети.</span><span class="sxs-lookup"><span data-stu-id="db4f4-106">Do not use the singleSignOn element in a profile if the network does not require it.</span></span>

<span data-ttu-id="db4f4-107">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент будет пропущен, если он есть в профиле.</span><span class="sxs-lookup"><span data-stu-id="db4f4-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="singleSignOn">
    <xs:complexType>
        <xs:sequence>
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
            <xs:element name="maxDelay"
                minOccurs="0"
            >
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
            <xs:element name="userBasedVirtualLan"
                type="boolean"
                minOccurs="0"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="db4f4-108">Элемент **singleSignOn** определяется элементом [**OneX**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="db4f4-108">The **singleSignOn** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="db4f4-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="db4f4-109">Child elements</span></span>



| <span data-ttu-id="db4f4-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="db4f4-110">Element</span></span>                                                                            | <span data-ttu-id="db4f4-111">Тип</span><span class="sxs-lookup"><span data-stu-id="db4f4-111">Type</span></span>    | <span data-ttu-id="db4f4-112">Описание</span><span class="sxs-lookup"><span data-stu-id="db4f4-112">Description</span></span>                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="db4f4-113">**максделай**</span><span class="sxs-lookup"><span data-stu-id="db4f4-113">**maxDelay**</span></span>](onexschema-maxdelay-singlesignon-element.md)                       |         | <span data-ttu-id="db4f4-114">Указывает максимальную задержку в секундах, по истечении которой попытка подключения единого входа завершится неудачей.</span><span class="sxs-lookup"><span data-stu-id="db4f4-114">Specifies, in seconds, the maximum delay before the single sign-on connection attempt fails.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="db4f4-115">**Тип**</span><span class="sxs-lookup"><span data-stu-id="db4f4-115">**type**</span></span>](onexschema-type-singlesignon-element.md)                               |         | <span data-ttu-id="db4f4-116">Указывает, когда выполняется единый вход.</span><span class="sxs-lookup"><span data-stu-id="db4f4-116">Specifies when single sign-on is performed.</span></span> <span data-ttu-id="db4f4-117">Если задано значение `preLogon` , единый вход выполняется до входа пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="db4f4-117">When set to `preLogon`, single sign-on is performed before the user logs on.</span></span> <span data-ttu-id="db4f4-118">Если задано значение `postLogon` , единый вход выполняется сразу после входа пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="db4f4-118">When set to `postLogon`, single sign-on is performed immediately after the user logs on.</span></span><br/> |
| [<span data-ttu-id="db4f4-119">**усербаседвиртуаллан**</span><span class="sxs-lookup"><span data-stu-id="db4f4-119">**userBasedVirtualLan**</span></span>](onexschema-userbasedvirtuallan-singlesignon-element.md) | <span data-ttu-id="db4f4-120">Логическое</span><span class="sxs-lookup"><span data-stu-id="db4f4-120">boolean</span></span> | <span data-ttu-id="db4f4-121">Указывает, изменяется ли виртуальная локальная сеть (VLAN), используемая устройством, на основе учетных данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="db4f4-121">Specifies if the virtual LAN (VLAN) used by the device changes based on the user's credentials.</span></span><br/>                                                                                                                   |



## <a name="remarks"></a><span data-ttu-id="db4f4-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="db4f4-122">Remarks</span></span>

<span data-ttu-id="db4f4-123">Этот параметр можно задать в командной строке с помощью команды **netsh wlan set профилепараметер** .</span><span class="sxs-lookup"><span data-stu-id="db4f4-123">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="db4f4-124">Дополнительные сведения см. в разделе [команды Netsh для беспроводной локальной сети (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="db4f4-124">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="db4f4-125">Требования</span><span class="sxs-lookup"><span data-stu-id="db4f4-125">Requirements</span></span>



| <span data-ttu-id="db4f4-126">Требование</span><span class="sxs-lookup"><span data-stu-id="db4f4-126">Requirement</span></span> | <span data-ttu-id="db4f4-127">Значение</span><span class="sxs-lookup"><span data-stu-id="db4f4-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="db4f4-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="db4f4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="db4f4-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="db4f4-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="db4f4-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="db4f4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="db4f4-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="db4f4-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="db4f4-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="db4f4-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="db4f4-133">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="db4f4-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="db4f4-134">**Таймаут**</span><span class="sxs-lookup"><span data-stu-id="db4f4-134">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="db4f4-135">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="db4f4-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="db4f4-136">**Таймаут**</span><span class="sxs-lookup"><span data-stu-id="db4f4-136">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 
