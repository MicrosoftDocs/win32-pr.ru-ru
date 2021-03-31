---
title: add sslcert
description: Добавляет новую привязку сертификата сервера SSL (SSL) и соответствующие политики сертификата клиента для IP-адреса и порта.
ms.assetid: 4ba3d2cb-050f-46e3-81f9-5f7e360b19fb
keywords:
- Добавить sslcert HTTP
topic_type:
- apiref
api_name:
- add sslcert
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a43569edd400b824876dff991f95e79cbfd6a96
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "104412035"
---
# <a name="add-sslcert"></a><span data-ttu-id="a0f61-104">add sslcert</span><span class="sxs-lookup"><span data-stu-id="a0f61-104">add sslcert</span></span>

<span data-ttu-id="a0f61-105">Добавляет новую привязку сертификата сервера SSL (SSL) и соответствующие политики сертификата клиента для IP-адреса и порта.</span><span class="sxs-lookup"><span data-stu-id="a0f61-105">Adds a new Secure Sockets Layer (SSL) server certificate binding and the corresponding client certificate policies for an IP address and port.</span></span>

``` syntax
add sslcert [ipport=]IP Address:port
            [certhash=]string
            [appid=]GUID
            [certstorename=]string
            [verifyclientcertrevocation={enable|disable}]
            [verifyrevocationwithcachedclientcertonly={enable|disable}]
            [usagecheck={enable|disable}]
            [revocationfreshnesstime=]u-int
            [urlretrievaltimeout=]u-int
            [sslctlidentifier=]string
            [sslctlstorename=]string
            [dsmapperusage={enable|disable}]
            [clientcertnegotiation={enable|disable}]

 
```

## <a name="parameters"></a><span data-ttu-id="a0f61-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0f61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0f61-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>\**\[иппорт = \] \* \* \* IP-адрес: порт*</span><span class="sxs-lookup"><span data-stu-id="a0f61-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>\**\[ipport=\]\*\*\*IP Address:port*</span></span>
</dt> <dd>

<span data-ttu-id="a0f61-108">Указывает IP-адрес и порт для привязки.</span><span class="sxs-lookup"><span data-stu-id="a0f61-108">Specifies the IP address and port for the binding.</span></span>

</dd> <dt>

<span data-ttu-id="a0f61-109"><span id="_certhash__string"></span><span id="_CERTHASH__STRING"></span>\**\[certhash = \] \* \* \* строка*</span><span class="sxs-lookup"><span data-stu-id="a0f61-109"><span id="_certhash__string"></span><span id="_CERTHASH__STRING"></span>\**\[certhash=\]\*\*\*string*</span></span>
</dt> <dd>

<span data-ttu-id="a0f61-110">Указывает хэш SHA сертификата.</span><span class="sxs-lookup"><span data-stu-id="a0f61-110">Specifies the SHA hash of the certificate.</span></span> <span data-ttu-id="a0f61-111">Этот хэш имеет длину 20 байт и задается в виде шестнадцатеричной строки.</span><span class="sxs-lookup"><span data-stu-id="a0f61-111">This hash is 20 bytes long and specified as a hexadecimal string.</span></span>

</dd> <dt>

<span data-ttu-id="a0f61-112"><span id="_appid__GUID"></span><span id="_appid__guid"></span><span id="_APPID__GUID"></span>\**\[AppID = \] \* \* \* GUID*</span><span class="sxs-lookup"><span data-stu-id="a0f61-112"><span id="_appid__GUID"></span><span id="_appid__guid"></span><span id="_APPID__GUID"></span>\**\[appid=\]\*\*\*GUID*</span></span>
</dt> <dd>

<span data-ttu-id="a0f61-113">Указывает GUID для обозначения приложения-владельца.</span><span class="sxs-lookup"><span data-stu-id="a0f61-113">Specifies the GUID to identify the owning application.</span></span>

</dd> <dt>

<span data-ttu-id="a0f61-114"><span id="_certstorename__string"></span><span id="_CERTSTORENAME__STRING"></span>\**\[цертсторенаме = \] \* \* \* строка*</span><span class="sxs-lookup"><span data-stu-id="a0f61-114"><span id="_certstorename__string"></span><span id="_CERTSTORENAME__STRING"></span>\**\[certstorename=\]\*\*\*string*</span></span>
</dt> <dd>

<span data-ttu-id="a0f61-115">Указывает имя для хранения сертификата.</span><span class="sxs-lookup"><span data-stu-id="a0f61-115">Specifies the store name for the certificate.</span></span> <span data-ttu-id="a0f61-116">По умолчанию — MY.</span><span class="sxs-lookup"><span data-stu-id="a0f61-116">Defaults to MY.</span></span> <span data-ttu-id="a0f61-117">Сертификат должен храниться в контексте локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="a0f61-117">Certificate must be stored in the local computer context.</span></span>

</dd> <dt>

<span data-ttu-id="a0f61-118"><span id="_verifyclientcertrevocation__enable_disable__"></span><span id="_VERIFYCLIENTCERTREVOCATION__ENABLE_DISABLE__"></span>**\[верификлиентцертревокатион = {включить \| Отключение}\]**</span><span class="sxs-lookup"><span data-stu-id="a0f61-118"><span id="_verifyclientcertrevocation__enable_disable__"></span><span id="_VERIFYCLIENTCERTREVOCATION__ENABLE_DISABLE__"></span>**\[verifyclientcertrevocation={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="a0f61-119">Включает или турнсофф проверку отзыва сертификатов клиента.</span><span class="sxs-lookup"><span data-stu-id="a0f61-119">Turns on or turnsoff verification of revocation of client certificates.</span></span>

</dd> <dt>

<span data-ttu-id="a0f61-120"><span id="_verifyrevocationwithcachedclientcertonly__enable_disable__"></span><span id="_VERIFYREVOCATIONWITHCACHEDCLIENTCERTONLY__ENABLE_DISABLE__"></span>**\[верифиревокатионвискачедклиентцертонли = {включить \| Отключение}\]**</span><span class="sxs-lookup"><span data-stu-id="a0f61-120"><span id="_verifyrevocationwithcachedclientcertonly__enable_disable__"></span><span id="_VERIFYREVOCATIONWITHCACHEDCLIENTCERTONLY__ENABLE_DISABLE__"></span>**\[verifyrevocationwithcachedclientcertonly={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="a0f61-121">Включает или выключает использование только кэшированного сертификата клиента для проверки отзыва.</span><span class="sxs-lookup"><span data-stu-id="a0f61-121">Turns on or turns off usage of only cached client certificate for revocation checking.</span></span>

</dd> <dt>

<span data-ttu-id="a0f61-122"><span id="_usagecheck__enable_disable__"></span><span id="_USAGECHECK__ENABLE_DISABLE__"></span>**\[усажечекк = {включить \| Отключение}\]**</span><span class="sxs-lookup"><span data-stu-id="a0f61-122"><span id="_usagecheck__enable_disable__"></span><span id="_USAGECHECK__ENABLE_DISABLE__"></span>**\[usagecheck={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="a0f61-123">Включает или выключает проверку использования.</span><span class="sxs-lookup"><span data-stu-id="a0f61-123">Turns on or turns off usage check.</span></span> <span data-ttu-id="a0f61-124">По умолчанию она включена.</span><span class="sxs-lookup"><span data-stu-id="a0f61-124">Default is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="a0f61-125"><span id="_revocationfreshnesstime__u-int"></span><span id="_REVOCATIONFRESHNESSTIME__U-INT"></span>\**\[ревокатионфрешнесстиме = \] \* \* \* u-int*</span><span class="sxs-lookup"><span data-stu-id="a0f61-125"><span id="_revocationfreshnesstime__u-int"></span><span id="_REVOCATIONFRESHNESSTIME__U-INT"></span>\**\[revocationfreshnesstime=\]\*\*\*u-int*</span></span>
</dt> <dd>

<span data-ttu-id="a0f61-126">Указывает интервал времени для проверки обновленного списка отзыва сертификатов (CRL).</span><span class="sxs-lookup"><span data-stu-id="a0f61-126">Specifies the time interval to check for an updated certificate revocation list (CRL).</span></span> <span data-ttu-id="a0f61-127">Если это значение равно 0, то новый список отзыва сертификатов обновляется только в том случае, если предыдущий срок истекает (в секундах).</span><span class="sxs-lookup"><span data-stu-id="a0f61-127">If this value is 0, then the new CRL is updated only if the previous one expires (in seconds).</span></span>

</dd> <dt>

<span data-ttu-id="a0f61-128"><span id="_urlretrievaltimeout__u-int"></span><span id="_URLRETRIEVALTIMEOUT__U-INT"></span>\**\[урлретриевалтимеаут = \] \* \* \* u-int*</span><span class="sxs-lookup"><span data-stu-id="a0f61-128"><span id="_urlretrievaltimeout__u-int"></span><span id="_URLRETRIEVALTIMEOUT__U-INT"></span>\**\[urlretrievaltimeout=\]\*\*\*u-int*</span></span>
</dt> <dd>

<span data-ttu-id="a0f61-129">Указывает интервал времени ожидания при попытке получить список отзыва сертификатов для удаленного URL-адреса (в миллисекундах).</span><span class="sxs-lookup"><span data-stu-id="a0f61-129">Specifies the timeout interval on attempts to retrieve the certificate revocation list for the remote URL (in milliseconds).</span></span>

</dd> <dt>

<span data-ttu-id="a0f61-130"><span id="_sslctlidentifier__string"></span><span id="_SSLCTLIDENTIFIER__STRING"></span>\**\[сслктлидентифиер = \] \* \* \* строка*</span><span class="sxs-lookup"><span data-stu-id="a0f61-130"><span id="_sslctlidentifier__string"></span><span id="_SSLCTLIDENTIFIER__STRING"></span>\**\[sslctlidentifier=\]\*\*\*string*</span></span>
</dt> <dd>

<span data-ttu-id="a0f61-131">Список издателей сертификатов, которые могут быть доверенными.</span><span class="sxs-lookup"><span data-stu-id="a0f61-131">Lists the certificate issuers that can be trusted.</span></span> <span data-ttu-id="a0f61-132">Этот список может быть подмножеством издателей сертификатов, которые являются доверенными для компьютера.</span><span class="sxs-lookup"><span data-stu-id="a0f61-132">This list can be a subset of the certificate issuers that are trusted by the computer.</span></span>

</dd> <dt>

<span data-ttu-id="a0f61-133"><span id="_sslctlstorename__string"></span><span id="_SSLCTLSTORENAME__STRING"></span>\**\[сслктлсторенаме = \] \* \* \* строка*</span><span class="sxs-lookup"><span data-stu-id="a0f61-133"><span id="_sslctlstorename__string"></span><span id="_SSLCTLSTORENAME__STRING"></span>\**\[sslctlstorename=\]\*\*\*string*</span></span>
</dt> <dd>

<span data-ttu-id="a0f61-134">Указывает имя хранилища на локальном \_ компьютере, где хранится сслктлидентифиер.</span><span class="sxs-lookup"><span data-stu-id="a0f61-134">Specifies the store name under LOCAL\_MACHINE where SslCtlIdentifier is stored.</span></span>

</dd> <dt>

<span data-ttu-id="a0f61-135"><span id="_dsmapperusage__enable_disable__"></span><span id="_DSMAPPERUSAGE__ENABLE_DISABLE__"></span>**\[дсмапперусаже = {включить \| Отключение}\]**</span><span class="sxs-lookup"><span data-stu-id="a0f61-135"><span id="_dsmapperusage__enable_disable__"></span><span id="_DSMAPPERUSAGE__ENABLE_DISABLE__"></span>**\[dsmapperusage={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="a0f61-136">Включает или выключает модули сопоставления DS.</span><span class="sxs-lookup"><span data-stu-id="a0f61-136">Turns on or turns off DS mappers.</span></span> <span data-ttu-id="a0f61-137">По умолчанию оно отключено.</span><span class="sxs-lookup"><span data-stu-id="a0f61-137">Default is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="a0f61-138"><span id="_clientcertnegotiation__enable_disable__"></span><span id="_CLIENTCERTNEGOTIATION__ENABLE_DISABLE__"></span>**\[клиентцертнеготиатион = {включить \| Отключение}\]**</span><span class="sxs-lookup"><span data-stu-id="a0f61-138"><span id="_clientcertnegotiation__enable_disable__"></span><span id="_CLIENTCERTNEGOTIATION__ENABLE_DISABLE__"></span>**\[clientcertnegotiation={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="a0f61-139">Включает или отключает согласование сертификата.</span><span class="sxs-lookup"><span data-stu-id="a0f61-139">Turns on or turns off negotiation of certificate.</span></span> <span data-ttu-id="a0f61-140">По умолчанию оно отключено.</span><span class="sxs-lookup"><span data-stu-id="a0f61-140">Default is disabled.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="a0f61-141">Примеры</span><span class="sxs-lookup"><span data-stu-id="a0f61-141">Examples</span></span>

<span data-ttu-id="a0f61-142">**add sslcert иппорт = 1.1.1.1:443**</span><span class="sxs-lookup"><span data-stu-id="a0f61-142">**add sslcert ipport=1.1.1.1:443**</span></span>

<span data-ttu-id="a0f61-143">**certhash = 0102030405060708090A0B0C0D0E0F1011121314**</span><span class="sxs-lookup"><span data-stu-id="a0f61-143">**certhash=0102030405060708090A0B0C0D0E0F1011121314**</span></span>

<span data-ttu-id="a0f61-144">**AppID = {00112233-4455-6677-8899-AABBCCDDEEFF}**</span><span class="sxs-lookup"><span data-stu-id="a0f61-144">**appid={00112233-4455-6677-8899-AABBCCDDEEFF}**</span></span>

 

 




