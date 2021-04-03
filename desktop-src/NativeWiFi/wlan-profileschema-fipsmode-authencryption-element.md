---
description: Указывает, включен ли режим федеральной информационной обработки (FIPS).
ms.assetid: 4c62c96c-82e7-4174-b833-95ee10b29344
title: Фипсмоде (Аусенкриптион), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FIPSMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 62a60670622084e3179e9720022c68ad5909ab4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810378"
---
# <a name="fipsmode-authencryption-element"></a><span data-ttu-id="25b37-103">Фипсмоде (Аусенкриптион), элемент</span><span class="sxs-lookup"><span data-stu-id="25b37-103">FIPSMode (authEncryption) Element</span></span>

<span data-ttu-id="25b37-104">Элемент **фипсмоде** (аусенкриптион) указывает, включен ли режим федеральной информационной обработки (FIPS).</span><span class="sxs-lookup"><span data-stu-id="25b37-104">The **FIPSMode** (authEncryption) element indicates whether Federal Information Processing Standards (FIPS) mode is enabled.</span></span> <span data-ttu-id="25b37-105">Если беспроводное подключение работает в режиме FIPS, уровень безопасности подключения соответствует стандарту FIPS 140-2.</span><span class="sxs-lookup"><span data-stu-id="25b37-105">When a wireless connection is operating in FIPS mode, the security level of the connection complies with the FIPS 140-2 standard.</span></span> <span data-ttu-id="25b37-106">Дополнительные сведения о FIPS см. на [домашней странице FIPS](https://www.itl.nist.gov/fipspubs/).</span><span class="sxs-lookup"><span data-stu-id="25b37-106">For more information about FIPS, see the [FIPS Home Page](https://www.itl.nist.gov/fipspubs/).</span></span>

<span data-ttu-id="25b37-107">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="25b37-107">This element is optional.</span></span> <span data-ttu-id="25b37-108">Если этот элемент не указан в профиле, то режим FIPS не включен.</span><span class="sxs-lookup"><span data-stu-id="25b37-108">If this element is not specified in a profile, then FIPS mode is not enabled.</span></span>

<span data-ttu-id="25b37-109">**Фипсмоде** может иметь значение true только при соблюдении следующих условий.</span><span class="sxs-lookup"><span data-stu-id="25b37-109">**FIPSMode** can be set to TRUE only when the following conditions are met:</span></span>

-   <span data-ttu-id="25b37-110">Элемент [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) имеет значение `ESS` (то есть соединение является подключением инфраструктуры).</span><span class="sxs-lookup"><span data-stu-id="25b37-110">The [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) element has a value of `ESS` (that is, the connection is an infrastructure connection).</span></span>
-   <span data-ttu-id="25b37-111">Элемент [**authentication**](wlan-profileschema-authentication-authencryption-element.md) имеет значение `WPA2` или `WPA2PSK` .</span><span class="sxs-lookup"><span data-stu-id="25b37-111">The [**authentication**](wlan-profileschema-authentication-authencryption-element.md) element has a value of `WPA2` or `WPA2PSK`.</span></span>
-   <span data-ttu-id="25b37-112">Элемент [**ENCRYPTION**](wlan-profileschema-encryption-authencryption-element.md) имеет значение `AES` .</span><span class="sxs-lookup"><span data-stu-id="25b37-112">The [**encryption**](wlan-profileschema-encryption-authencryption-element.md) element has a value of `AES`.</span></span>

<span data-ttu-id="25b37-113">В отличие от большинства элементов в \_ схеме профиля WLAN этот элемент находится в `https://www.microsoft.com/networking/WLAN/profile/v2` пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="25b37-113">Unlike most elements in the WLAN\_profile schema, this element is in the `https://www.microsoft.com/networking/WLAN/profile/v2` namespace.</span></span>

<span data-ttu-id="25b37-114">Значение элемента **фипсмоде** игнорируется, если драйвер минипорта для беспроводного интерфейса не поддерживает режим FIPS.</span><span class="sxs-lookup"><span data-stu-id="25b37-114">The value of the **FIPSMode** element is ignored if the miniport driver for the wireless interface does not support FIPS mode.</span></span>

<span data-ttu-id="25b37-115">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="25b37-115">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span> <span data-ttu-id="25b37-116">Если **фипсмоде** есть в профиле, элемент игнорируется.</span><span class="sxs-lookup"><span data-stu-id="25b37-116">If **FIPSMode** is present in a profile, the element is ignored.</span></span>

``` syntax
<xs:element name="FIPSMode"
    type="boolean"
 />
```

<span data-ttu-id="25b37-117">Элемент определяется элементом [**аусенкриптион**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="25b37-117">The element is defined by the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="25b37-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="25b37-118">Remarks</span></span>

<span data-ttu-id="25b37-119">Этот параметр можно задать в командной строке с помощью команды **netsh wlan set профилепараметер** .</span><span class="sxs-lookup"><span data-stu-id="25b37-119">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="25b37-120">Дополнительные сведения см. в разделе [команды Netsh для беспроводной локальной сети (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="25b37-120">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="examples"></a><span data-ttu-id="25b37-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="25b37-121">Examples</span></span>

<span data-ttu-id="25b37-122">Пример профиля, в котором используется элемент **фипсмоде** , см. в разделе [пример профиля FIPS](fips-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="25b37-122">To view a sample profile that uses the **FIPSMode** element, see [FIPS Profile Sample](fips-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="25b37-123">Требования</span><span class="sxs-lookup"><span data-stu-id="25b37-123">Requirements</span></span>



| <span data-ttu-id="25b37-124">Требование</span><span class="sxs-lookup"><span data-stu-id="25b37-124">Requirement</span></span> | <span data-ttu-id="25b37-125">Значение</span><span class="sxs-lookup"><span data-stu-id="25b37-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="25b37-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="25b37-126">Minimum supported client</span></span><br/> | <span data-ttu-id="25b37-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="25b37-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="25b37-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="25b37-128">Minimum supported server</span></span><br/> | <span data-ttu-id="25b37-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="25b37-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="25b37-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25b37-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="25b37-131">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="25b37-131">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="25b37-132">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="25b37-132">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

<span data-ttu-id="25b37-133">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="25b37-133">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="25b37-134">**Аусенкриптион (безопасность)**</span><span class="sxs-lookup"><span data-stu-id="25b37-134">**authEncryption (security)**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 
