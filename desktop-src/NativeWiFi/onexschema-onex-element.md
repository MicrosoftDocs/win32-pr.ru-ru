---
description: Указывает сведения о конфигурации 802.1 X для профиля проводной или беспроводной локальной сети.
ms.assetid: 4528fcb5-ee8e-4824-a69e-8d67622c4b4d
title: OneX, элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4b3e3d91087a394efb7909d36d6244bfbf6115e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663045"
---
# <a name="onex-element"></a><span data-ttu-id="c31fa-103">OneX, элемент</span><span class="sxs-lookup"><span data-stu-id="c31fa-103">OneX Element</span></span>

<span data-ttu-id="c31fa-104">Элемент OneX указывает сведения о конфигурации 802.1 X для профиля проводной или беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="c31fa-104">The OneX element specifies 802.1X configuration information for a wired or wireless LAN profile.</span></span> <span data-ttu-id="c31fa-105">Этот элемент является уникальным корневым элементом для профиля 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="c31fa-105">This element is the unique root element for an 802.1X profile.</span></span>

<span data-ttu-id="c31fa-106">Целевым пространством имен для элемента OneX является `https://www.microsoft.com/networking/OneX/v1` .</span><span class="sxs-lookup"><span data-stu-id="c31fa-106">The target namespace for the OneX element is `https://www.microsoft.com/networking/OneX/v1`.</span></span> <span data-ttu-id="c31fa-107">Большинство дочерних элементов элемента OneX находятся в `OneX` пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="c31fa-107">Most child elements of the OneX element are in the `OneX` namespace.</span></span> <span data-ttu-id="c31fa-108">Существует одно исключение: элемент [**еапконфиг**](onexschema-eapconfig-onex-element.md) находится в `https://www.microsoft.com/provisioning/EapHostConfig` пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="c31fa-108">There is one exception: the [**EAPConfig**](onexschema-eapconfig-onex-element.md) element is in the `https://www.microsoft.com/provisioning/EapHostConfig` namespace.</span></span>

<span data-ttu-id="c31fa-109">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Поддерживается только элемент [**еапконфиг**](onexschema-eapconfig-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c31fa-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** Only the [**EAPConfig**](onexschema-eapconfig-onex-element.md) element is supported.</span></span> <span data-ttu-id="c31fa-110">Другие элементы, если они есть в профиле, будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="c31fa-110">Other elements, if present in a profile, will be ignored.</span></span>

``` syntax
<xs:element name="OneX">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="cacheUserData"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="heldPeriod"
                minOccurs="0"
            >
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
            <xs:element name="authPeriod"
                minOccurs="0"
            >
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
            <xs:element name="startPeriod"
                minOccurs="0"
            >
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
            <xs:element name="maxStart"
                minOccurs="0"
            >
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
            <xs:element name="maxAuthFailures"
                minOccurs="0"
            >
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
            <xs:element name="supplicantMode"
                minOccurs="0"
            >
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
            <xs:element name="authMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="machineOrUser"
                         />
                        <xs:enumeration
                            value="machine"
                         />
                        <xs:enumeration
                            value="user"
                         />
                        <xs:enumeration
                            value="guest"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="singleSignOn"
                minOccurs="0"
            >
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
            <xs:element name="EAPConfig">
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            minOccurs="1"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="c31fa-111">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c31fa-111">Child elements</span></span>



| <span data-ttu-id="c31fa-112">Элемент</span><span class="sxs-lookup"><span data-stu-id="c31fa-112">Element</span></span>                                                                            | <span data-ttu-id="c31fa-113">Тип</span><span class="sxs-lookup"><span data-stu-id="c31fa-113">Type</span></span>    | <span data-ttu-id="c31fa-114">Описание</span><span class="sxs-lookup"><span data-stu-id="c31fa-114">Description</span></span>                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c31fa-115">**аусмоде**</span><span class="sxs-lookup"><span data-stu-id="c31fa-115">**authMode**</span></span>](onexschema-authmode-onex-element.md)                               |         | <span data-ttu-id="c31fa-116">Указывает тип учетных данных, используемых для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="c31fa-116">Specifies the type of credentials used for authentication.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="c31fa-117">**ауспериод**</span><span class="sxs-lookup"><span data-stu-id="c31fa-117">**authPeriod**</span></span>](onexschema-authperiod-onex-element.md)                           |         | <span data-ttu-id="c31fa-118">Указывает максимальный интервал времени (в секундах), в течение которого клиент ожидает ответа от средства проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="c31fa-118">Specifies the maximum length of time, in seconds, in which a client waits for a response from the authenticator.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="c31fa-119">**качеусердата**</span><span class="sxs-lookup"><span data-stu-id="c31fa-119">**cacheUserData**</span></span>](onexschema-cacheuserdata-onex-element.md)                     | <span data-ttu-id="c31fa-120">Логическое</span><span class="sxs-lookup"><span data-stu-id="c31fa-120">boolean</span></span> | <span data-ttu-id="c31fa-121">Указывает, кэшируются ли учетные данные пользователя для последующих подключений.</span><span class="sxs-lookup"><span data-stu-id="c31fa-121">Specifies whether the user credentials are cached for subsequent connections.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="c31fa-122">**еапконфиг**</span><span class="sxs-lookup"><span data-stu-id="c31fa-122">**EAPConfig**</span></span>](onexschema-eapconfig-onex-element.md)                             |         | <span data-ttu-id="c31fa-123">Задает конфигурацию EAPHost.</span><span class="sxs-lookup"><span data-stu-id="c31fa-123">Specifies the EAPHost configuration.</span></span><br/>                                                                                                                                                                              |
| [<span data-ttu-id="c31fa-124">**хелдпериод**</span><span class="sxs-lookup"><span data-stu-id="c31fa-124">**heldPeriod**</span></span>](onexschema-heldperiod-onex-element.md)                           |         | <span data-ttu-id="c31fa-125">Указывает период времени в секундах, в течение которого клиент не будет повторно пытаться пройти проверку подлинности после неудачной попытки проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="c31fa-125">Specifies the length of time, in seconds, in which a client will not re-attempt authentication after a failed authentication attempt.</span></span><br/>                                                                             |
| [<span data-ttu-id="c31fa-126">**максаусфаилурес**</span><span class="sxs-lookup"><span data-stu-id="c31fa-126">**maxAuthFailures**</span></span>](onexschema-maxauthfailures-onex-element.md)                 |         | <span data-ttu-id="c31fa-127">Указывает максимальное количество ошибок проверки подлинности, разрешенных для набора учетных данных.</span><span class="sxs-lookup"><span data-stu-id="c31fa-127">Specifies the maximum number of authentication failures allowed for a set of credentials.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="c31fa-128">**максделай**</span><span class="sxs-lookup"><span data-stu-id="c31fa-128">**maxDelay**</span></span>](onexschema-maxdelay-singlesignon-element.md)                       |         | <span data-ttu-id="c31fa-129">Указывает максимальную задержку в секундах, по истечении которой попытка подключения единого входа завершится неудачей.</span><span class="sxs-lookup"><span data-stu-id="c31fa-129">Specifies, in seconds, the maximum delay before the single sign-on connection attempt fails.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="c31fa-130">**максстарт**</span><span class="sxs-lookup"><span data-stu-id="c31fa-130">**maxStart**</span></span>](onexschema-maxstart-onex-element.md)                               |         | <span data-ttu-id="c31fa-131">Указывает максимальное число отправленных сообщений EAPOL-Start.</span><span class="sxs-lookup"><span data-stu-id="c31fa-131">Specifies the maximum number of EAPOL-Start messages sent.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="c31fa-132">**singleSignOn**</span><span class="sxs-lookup"><span data-stu-id="c31fa-132">**singleSignOn**</span></span>](onexschema-singlesignon-onex-element.md)                       |         | <span data-ttu-id="c31fa-133">Задает сведения о конфигурации сети для единого входа.</span><span class="sxs-lookup"><span data-stu-id="c31fa-133">Specifies single sign-on network configuration information.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="c31fa-134">**стартпериод**</span><span class="sxs-lookup"><span data-stu-id="c31fa-134">**startPeriod**</span></span>](onexschema-startperiod-onex-element.md)                         |         | <span data-ttu-id="c31fa-135">Указывает период времени (в секундах) ожидания перед отправкой EAPOL-Start.</span><span class="sxs-lookup"><span data-stu-id="c31fa-135">Specifies the length of time, in seconds, to wait before an EAPOL-Start is sent.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="c31fa-136">**суппликантмоде**</span><span class="sxs-lookup"><span data-stu-id="c31fa-136">**supplicantMode**</span></span>](onexschema-supplicantmode-onex-element.md)                   |         | <span data-ttu-id="c31fa-137">Указывает метод передачи, используемый для пакетов EAPOL.</span><span class="sxs-lookup"><span data-stu-id="c31fa-137">Specifies the method of transmission used for EAPOL packets.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="c31fa-138">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c31fa-138">**type**</span></span>](onexschema-type-singlesignon-element.md)                               |         | <span data-ttu-id="c31fa-139">Указывает, когда выполняется единый вход.</span><span class="sxs-lookup"><span data-stu-id="c31fa-139">Specifies when single sign-on is performed.</span></span> <span data-ttu-id="c31fa-140">Если задано значение `preLogon` , единый вход выполняется до входа пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="c31fa-140">When set to `preLogon`, single sign-on is performed before the user logs on.</span></span> <span data-ttu-id="c31fa-141">Если задано значение `postLogon` , единый вход выполняется сразу после входа пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="c31fa-141">When set to `postLogon`, single sign-on is performed immediately after the user logs on.</span></span><br/> |
| [<span data-ttu-id="c31fa-142">**усербаседвиртуаллан**</span><span class="sxs-lookup"><span data-stu-id="c31fa-142">**userBasedVirtualLan**</span></span>](onexschema-userbasedvirtuallan-singlesignon-element.md) | <span data-ttu-id="c31fa-143">Логическое</span><span class="sxs-lookup"><span data-stu-id="c31fa-143">boolean</span></span> | <span data-ttu-id="c31fa-144">Указывает, изменяется ли виртуальная локальная сеть (VLAN), используемая устройством, на основе учетных данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="c31fa-144">Specifies if the virtual LAN (VLAN) used by the device changes based on the user's credentials.</span></span><br/>                                                                                                                   |



## <a name="remarks"></a><span data-ttu-id="c31fa-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c31fa-145">Remarks</span></span>

<span data-ttu-id="c31fa-146">Сведения о просмотре списка дочерних элементов в древовидной структуре см. в разделе [элементы схемы OneX](onexschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="c31fa-146">To view the list of child elements in a tree-like structure, see [OneX Schema Elements](onexschema-elements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c31fa-147">Требования</span><span class="sxs-lookup"><span data-stu-id="c31fa-147">Requirements</span></span>



| <span data-ttu-id="c31fa-148">Требование</span><span class="sxs-lookup"><span data-stu-id="c31fa-148">Requirement</span></span> | <span data-ttu-id="c31fa-149">Значение</span><span class="sxs-lookup"><span data-stu-id="c31fa-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="c31fa-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c31fa-150">Minimum supported client</span></span><br/> | <span data-ttu-id="c31fa-151">Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c31fa-151">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c31fa-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c31fa-152">Minimum supported server</span></span><br/> | <span data-ttu-id="c31fa-153">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c31fa-153">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="c31fa-154">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="c31fa-154">Redistributable</span></span><br/>          | <span data-ttu-id="c31fa-155">Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="c31fa-155">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



 

 




