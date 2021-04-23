---
title: Метод Имстскаксевентс с отключением
description: Вызывается, когда клиентский элемент управления был отключен от сервера узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов).
ms.assetid: f01086e7-61d1-41df-ba0a-4eecfa57d492
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода OnDisconnection
- Службы удаленных рабочих столов метода ondisconnectо, интерфейс Имстскаксевентс
- Интерфейс Имстскаксевентс службы удаленных рабочих столов, отключенный метод
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnDisconnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 372ad98c73b1b0e90753891e01e46c61a78c23dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672726"
---
# <a name="imstscaxeventsondisconnected-method"></a><span data-ttu-id="0bcea-106">Имстскаксевентс:: ondisconnectный метод</span><span class="sxs-lookup"><span data-stu-id="0bcea-106">IMsTscAxEvents::OnDisconnected method</span></span>

<span data-ttu-id="0bcea-107">Вызывается, когда клиентский элемент управления был отключен от сервера узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="0bcea-107">Called when the client control has been disconnected from the Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bcea-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0bcea-108">Syntax</span></span>


```C++
void OnDisconnected(
  [in] long discReason
);
```



## <a name="parameters"></a><span data-ttu-id="0bcea-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0bcea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bcea-110">*дискреасон* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0bcea-110">*discReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bcea-111">Указывает причину отключения.</span><span class="sxs-lookup"><span data-stu-id="0bcea-111">Specifies the reason for the disconnection.</span></span> <span data-ttu-id="0bcea-112">Ниже приведен список кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="0bcea-112">The following is a list of error codes.</span></span> <span data-ttu-id="0bcea-113">Некоторые из этих кодов ошибок определены в Винкред. h.</span><span class="sxs-lookup"><span data-stu-id="0bcea-113">Some of these error codes are defined in Wincred.h.</span></span>

<dt>

<span id="disconnectReasonAtClientWinsockFDCLOSE"></span><span id="disconnectreasonatclientwinsockfdclose"></span><span id="DISCONNECTREASONATCLIENTWINSOCKFDCLOSE"></span>

<span data-ttu-id="0bcea-114"><span id="disconnectReasonAtClientWinsockFDCLOSE"></span><span id="disconnectreasonatclientwinsockfdclose"></span><span id="DISCONNECTREASONATCLIENTWINSOCKFDCLOSE"></span>**дисконнектреасонатклиентвинсоккфдклосе** (2308 (0x904))</span><span class="sxs-lookup"><span data-stu-id="0bcea-114"><span id="disconnectReasonAtClientWinsockFDCLOSE"></span><span id="disconnectreasonatclientwinsockfdclose"></span><span id="DISCONNECTREASONATCLIENTWINSOCKFDCLOSE"></span>**disconnectReasonAtClientWinsockFDCLOSE** (2308 (0x904))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-115">Сокет закрыт.</span><span class="sxs-lookup"><span data-stu-id="0bcea-115">Socket closed.</span></span>

</dd> <dt>

<span id="disconnectReasonByServer"></span><span id="disconnectreasonbyserver"></span><span id="DISCONNECTREASONBYSERVER"></span>

<span data-ttu-id="0bcea-116"><span id="disconnectReasonByServer"></span><span id="disconnectreasonbyserver"></span><span id="DISCONNECTREASONBYSERVER"></span>**дисконнектреасонбисервер** (3 (0x3))</span><span class="sxs-lookup"><span data-stu-id="0bcea-116"><span id="disconnectReasonByServer"></span><span id="disconnectreasonbyserver"></span><span id="DISCONNECTREASONBYSERVER"></span>**disconnectReasonByServer** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-117">Удаленное отключение от сервера.</span><span class="sxs-lookup"><span data-stu-id="0bcea-117">Remote disconnection by server.</span></span> <span data-ttu-id="0bcea-118">Это не код ошибки.</span><span class="sxs-lookup"><span data-stu-id="0bcea-118">This is not an error code.</span></span>

</dd> <dt>

<span id="disconnectReasonClientDecompressionError"></span><span id="disconnectreasonclientdecompressionerror"></span><span id="DISCONNECTREASONCLIENTDECOMPRESSIONERROR"></span>

<span data-ttu-id="0bcea-119"><span id="disconnectReasonClientDecompressionError"></span><span id="disconnectreasonclientdecompressionerror"></span><span id="DISCONNECTREASONCLIENTDECOMPRESSIONERROR"></span>**дисконнектреасонклиентдекомпрессионеррор** (3080 (0xC08))</span><span class="sxs-lookup"><span data-stu-id="0bcea-119"><span id="disconnectReasonClientDecompressionError"></span><span id="disconnectreasonclientdecompressionerror"></span><span id="DISCONNECTREASONCLIENTDECOMPRESSIONERROR"></span>**disconnectReasonClientDecompressionError** (3080 (0xC08))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-120">Ошибка распаковки.</span><span class="sxs-lookup"><span data-stu-id="0bcea-120">Decompression error.</span></span>

</dd> <dt>

<span id="disconnectReasonConnectionTimedOut"></span><span id="disconnectreasonconnectiontimedout"></span><span id="DISCONNECTREASONCONNECTIONTIMEDOUT"></span>

<span data-ttu-id="0bcea-121"><span id="disconnectReasonConnectionTimedOut"></span><span id="disconnectreasonconnectiontimedout"></span><span id="DISCONNECTREASONCONNECTIONTIMEDOUT"></span>**дисконнектреасонконнектионтимедаут** (264 (0x108))</span><span class="sxs-lookup"><span data-stu-id="0bcea-121"><span id="disconnectReasonConnectionTimedOut"></span><span id="disconnectreasonconnectiontimedout"></span><span id="DISCONNECTREASONCONNECTIONTIMEDOUT"></span>**disconnectReasonConnectionTimedOut** (264 (0x108))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-122">Время ожидания для подключения истекло.</span><span class="sxs-lookup"><span data-stu-id="0bcea-122">Connection timed out.</span></span>

</dd> <dt>

<span id="disconnectReasonDecryptionError"></span><span id="disconnectreasondecryptionerror"></span><span id="DISCONNECTREASONDECRYPTIONERROR"></span>

<span data-ttu-id="0bcea-123"><span id="disconnectReasonDecryptionError"></span><span id="disconnectreasondecryptionerror"></span><span id="DISCONNECTREASONDECRYPTIONERROR"></span>**дисконнектреасондекриптионеррор** (3078 (0xC06))</span><span class="sxs-lookup"><span data-stu-id="0bcea-123"><span id="disconnectReasonDecryptionError"></span><span id="disconnectreasondecryptionerror"></span><span id="DISCONNECTREASONDECRYPTIONERROR"></span>**disconnectReasonDecryptionError** (3078 (0xC06))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-124">Ошибка расшифровки.</span><span class="sxs-lookup"><span data-stu-id="0bcea-124">Decryption error.</span></span>

</dd> <dt>

<span id="disconnectReasonDNSLookupFailed"></span><span id="disconnectreasondnslookupfailed"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED"></span>

<span data-ttu-id="0bcea-125"><span id="disconnectReasonDNSLookupFailed"></span><span id="disconnectreasondnslookupfailed"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED"></span>**дисконнектреасонднслукупфаилед** (260 (0x104))</span><span class="sxs-lookup"><span data-stu-id="0bcea-125"><span id="disconnectReasonDNSLookupFailed"></span><span id="disconnectreasondnslookupfailed"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED"></span>**disconnectReasonDNSLookupFailed** (260 (0x104))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-126">Ошибка уточняющего запроса DNS-имени.</span><span class="sxs-lookup"><span data-stu-id="0bcea-126">DNS name lookup failure.</span></span>

</dd> <dt>

<span id="disconnectReasonDNSLookupFailed2"></span><span id="disconnectreasondnslookupfailed2"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED2"></span>

<span data-ttu-id="0bcea-127"><span id="disconnectReasonDNSLookupFailed2"></span><span id="disconnectreasondnslookupfailed2"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED2"></span>**disconnectReasonDNSLookupFailed2** (1288 (0x508))</span><span class="sxs-lookup"><span data-stu-id="0bcea-127"><span id="disconnectReasonDNSLookupFailed2"></span><span id="disconnectreasondnslookupfailed2"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED2"></span>**disconnectReasonDNSLookupFailed2** (1288 (0x508))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-128">Сбой уточняющего запроса DNS.</span><span class="sxs-lookup"><span data-stu-id="0bcea-128">DNS lookup failed.</span></span>

</dd> <dt>

<span id="disconnectReasonEncryptionError"></span><span id="disconnectreasonencryptionerror"></span><span id="DISCONNECTREASONENCRYPTIONERROR"></span>

<span data-ttu-id="0bcea-129"><span id="disconnectReasonEncryptionError"></span><span id="disconnectreasonencryptionerror"></span><span id="DISCONNECTREASONENCRYPTIONERROR"></span>**дисконнектреасоненкриптионеррор** (2822 (0xB06))</span><span class="sxs-lookup"><span data-stu-id="0bcea-129"><span id="disconnectReasonEncryptionError"></span><span id="disconnectreasonencryptionerror"></span><span id="DISCONNECTREASONENCRYPTIONERROR"></span>**disconnectReasonEncryptionError** (2822 (0xB06))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-130">Ошибка шифрования.</span><span class="sxs-lookup"><span data-stu-id="0bcea-130">Encryption error.</span></span>

</dd> <dt>

<span id="disconnectReasonGetHostByNameFailed"></span><span id="disconnectreasongethostbynamefailed"></span><span id="DISCONNECTREASONGETHOSTBYNAMEFAILED"></span>

<span data-ttu-id="0bcea-131"><span id="disconnectReasonGetHostByNameFailed"></span><span id="disconnectreasongethostbynamefailed"></span><span id="DISCONNECTREASONGETHOSTBYNAMEFAILED"></span>**дисконнектреасонжесостбинамефаилед** (1540 (0x604))</span><span class="sxs-lookup"><span data-stu-id="0bcea-131"><span id="disconnectReasonGetHostByNameFailed"></span><span id="disconnectreasongethostbynamefailed"></span><span id="DISCONNECTREASONGETHOSTBYNAMEFAILED"></span>**disconnectReasonGetHostByNameFailed** (1540 (0x604))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-132">Сбой вызова [**gethostbyname**](/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname) сокетов Windows.</span><span class="sxs-lookup"><span data-stu-id="0bcea-132">Windows Sockets [**gethostbyname**](/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname) call failed.</span></span>

</dd> <dt>

<span id="disconnectReasonHostNotFound"></span><span id="disconnectreasonhostnotfound"></span><span id="DISCONNECTREASONHOSTNOTFOUND"></span>

<span data-ttu-id="0bcea-133"><span id="disconnectReasonHostNotFound"></span><span id="disconnectreasonhostnotfound"></span><span id="DISCONNECTREASONHOSTNOTFOUND"></span>**дисконнектреасонхостнотфаунд** (520 (0x208))</span><span class="sxs-lookup"><span data-stu-id="0bcea-133"><span id="disconnectReasonHostNotFound"></span><span id="disconnectreasonhostnotfound"></span><span id="DISCONNECTREASONHOSTNOTFOUND"></span>**disconnectReasonHostNotFound** (520 (0x208))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-134">Ошибка "узел не найден".</span><span class="sxs-lookup"><span data-stu-id="0bcea-134">Host not found error.</span></span>

</dd> <dt>

<span id="disconnectReasonInternalError"></span><span id="disconnectreasoninternalerror"></span><span id="DISCONNECTREASONINTERNALERROR"></span>

<span data-ttu-id="0bcea-135"><span id="disconnectReasonInternalError"></span><span id="disconnectreasoninternalerror"></span><span id="DISCONNECTREASONINTERNALERROR"></span>**дисконнектреасонинтерналеррор** (1032 (0x408))</span><span class="sxs-lookup"><span data-stu-id="0bcea-135"><span id="disconnectReasonInternalError"></span><span id="disconnectreasoninternalerror"></span><span id="DISCONNECTREASONINTERNALERROR"></span>**disconnectReasonInternalError** (1032 (0x408))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-136">Внутренняя ошибка.</span><span class="sxs-lookup"><span data-stu-id="0bcea-136">Internal error.</span></span>

</dd> <dt>

<span id="disconnectReasonInternalSecurityError"></span><span id="disconnectreasoninternalsecurityerror"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR"></span>

<span data-ttu-id="0bcea-137"><span id="disconnectReasonInternalSecurityError"></span><span id="disconnectreasoninternalsecurityerror"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR"></span>**дисконнектреасонинтерналсекуритеррор** (2310 (0x906))</span><span class="sxs-lookup"><span data-stu-id="0bcea-137"><span id="disconnectReasonInternalSecurityError"></span><span id="disconnectreasoninternalsecurityerror"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR"></span>**disconnectReasonInternalSecurityError** (2310 (0x906))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-138">Внутренняя ошибка безопасности.</span><span class="sxs-lookup"><span data-stu-id="0bcea-138">Internal security error.</span></span>

</dd> <dt>

<span id="disconnectReasonInternalSecurityError2"></span><span id="disconnectreasoninternalsecurityerror2"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR2"></span>

<span data-ttu-id="0bcea-139"><span id="disconnectReasonInternalSecurityError2"></span><span id="disconnectreasoninternalsecurityerror2"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR2"></span>**disconnectReasonInternalSecurityError2** (2566 (0xA06))</span><span class="sxs-lookup"><span data-stu-id="0bcea-139"><span id="disconnectReasonInternalSecurityError2"></span><span id="disconnectreasoninternalsecurityerror2"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR2"></span>**disconnectReasonInternalSecurityError2** (2566 (0xA06))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-140">Внутренняя ошибка безопасности.</span><span class="sxs-lookup"><span data-stu-id="0bcea-140">Internal security error.</span></span>

</dd> <dt>

<span id="disconnectReasonInvalidEncryption"></span><span id="disconnectreasoninvalidencryption"></span><span id="DISCONNECTREASONINVALIDENCRYPTION"></span>

<span data-ttu-id="0bcea-141"><span id="disconnectReasonInvalidEncryption"></span><span id="disconnectreasoninvalidencryption"></span><span id="DISCONNECTREASONINVALIDENCRYPTION"></span>**дисконнектреасонинвалиденкриптион** (1286 (0x506))</span><span class="sxs-lookup"><span data-stu-id="0bcea-141"><span id="disconnectReasonInvalidEncryption"></span><span id="disconnectreasoninvalidencryption"></span><span id="DISCONNECTREASONINVALIDENCRYPTION"></span>**disconnectReasonInvalidEncryption** (1286 (0x506))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-142">Указан недопустимый метод шифрования.</span><span class="sxs-lookup"><span data-stu-id="0bcea-142">The encryption method specified is not valid.</span></span>

</dd> <dt>

<span id="disconnectReasonInvalidIP"></span><span id="disconnectreasoninvalidip"></span><span id="DISCONNECTREASONINVALIDIP"></span>

<span data-ttu-id="0bcea-143"><span id="disconnectReasonInvalidIP"></span><span id="disconnectreasoninvalidip"></span><span id="DISCONNECTREASONINVALIDIP"></span>**дисконнектреасонинвалидип** (2052 (0x804))</span><span class="sxs-lookup"><span data-stu-id="0bcea-143"><span id="disconnectReasonInvalidIP"></span><span id="disconnectreasoninvalidip"></span><span id="DISCONNECTREASONINVALIDIP"></span>**disconnectReasonInvalidIP** (2052 (0x804))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-144">Указан неверный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="0bcea-144">Bad IP address specified.</span></span>

</dd> <dt>

<span id="disconnectReasonInvalidServerSecurityInfo"></span><span id="disconnectreasoninvalidserversecurityinfo"></span><span id="DISCONNECTREASONINVALIDSERVERSECURITYINFO"></span>

<span data-ttu-id="0bcea-145"><span id="disconnectReasonInvalidServerSecurityInfo"></span><span id="disconnectreasoninvalidserversecurityinfo"></span><span id="DISCONNECTREASONINVALIDSERVERSECURITYINFO"></span>**дисконнектреасонинвалидсерверсекуритинфо** (1542 (0x606))</span><span class="sxs-lookup"><span data-stu-id="0bcea-145"><span id="disconnectReasonInvalidServerSecurityInfo"></span><span id="disconnectreasoninvalidserversecurityinfo"></span><span id="DISCONNECTREASONINVALIDSERVERSECURITYINFO"></span>**disconnectReasonInvalidServerSecurityInfo** (1542 (0x606))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-146">Недопустимые данные безопасности сервера.</span><span class="sxs-lookup"><span data-stu-id="0bcea-146">Server security data is not valid.</span></span>

</dd> <dt>

<span id="disconnectReasonInvalidSecurityData"></span><span id="disconnectreasoninvalidsecuritydata"></span><span id="DISCONNECTREASONINVALIDSECURITYDATA"></span>

<span data-ttu-id="0bcea-147"><span id="disconnectReasonInvalidSecurityData"></span><span id="disconnectreasoninvalidsecuritydata"></span><span id="DISCONNECTREASONINVALIDSECURITYDATA"></span>**дисконнектреасонинвалидсекуритидата** (1030 (0x406))</span><span class="sxs-lookup"><span data-stu-id="0bcea-147"><span id="disconnectReasonInvalidSecurityData"></span><span id="disconnectreasoninvalidsecuritydata"></span><span id="DISCONNECTREASONINVALIDSECURITYDATA"></span>**disconnectReasonInvalidSecurityData** (1030 (0x406))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-148">Недопустимые данные безопасности.</span><span class="sxs-lookup"><span data-stu-id="0bcea-148">Security data is not valid.</span></span>

</dd> <dt>

<span id="disconnectReasonInvalidIPAddr"></span><span id="disconnectreasoninvalidipaddr"></span><span id="DISCONNECTREASONINVALIDIPADDR"></span>

<span data-ttu-id="0bcea-149"><span id="disconnectReasonInvalidIPAddr"></span><span id="disconnectreasoninvalidipaddr"></span><span id="DISCONNECTREASONINVALIDIPADDR"></span>**дисконнектреасонинвалидипаддр** (776 (0x308))</span><span class="sxs-lookup"><span data-stu-id="0bcea-149"><span id="disconnectReasonInvalidIPAddr"></span><span id="disconnectreasoninvalidipaddr"></span><span id="DISCONNECTREASONINVALIDIPADDR"></span>**disconnectReasonInvalidIPAddr** (776 (0x308))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-150">Указан недопустимый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="0bcea-150">The IP address specified is not valid.</span></span>

</dd> <dt>

<span id="disconnectReasonLicensingFailed"></span><span id="disconnectreasonlicensingfailed"></span><span id="DISCONNECTREASONLICENSINGFAILED"></span>

<span data-ttu-id="0bcea-151"><span id="disconnectReasonLicensingFailed"></span><span id="disconnectreasonlicensingfailed"></span><span id="DISCONNECTREASONLICENSINGFAILED"></span>**дисконнектреасонлиценсингфаилед** (2056 (0x808))</span><span class="sxs-lookup"><span data-stu-id="0bcea-151"><span id="disconnectReasonLicensingFailed"></span><span id="disconnectreasonlicensingfailed"></span><span id="DISCONNECTREASONLICENSINGFAILED"></span>**disconnectReasonLicensingFailed** (2056 (0x808))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-152">Сбой согласования лицензии.</span><span class="sxs-lookup"><span data-stu-id="0bcea-152">License negotiation failed.</span></span>

</dd> <dt>

<span id="disconnectReasonLicensingTimeout"></span><span id="disconnectreasonlicensingtimeout"></span><span id="DISCONNECTREASONLICENSINGTIMEOUT"></span>

<span data-ttu-id="0bcea-153"><span id="disconnectReasonLicensingTimeout"></span><span id="disconnectreasonlicensingtimeout"></span><span id="DISCONNECTREASONLICENSINGTIMEOUT"></span>**дисконнектреасонлиценсингтимеаут** (2312 (0x908))</span><span class="sxs-lookup"><span data-stu-id="0bcea-153"><span id="disconnectReasonLicensingTimeout"></span><span id="disconnectreasonlicensingtimeout"></span><span id="DISCONNECTREASONLICENSINGTIMEOUT"></span>**disconnectReasonLicensingTimeout** (2312 (0x908))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-154">Время ожидания лицензирования.</span><span class="sxs-lookup"><span data-stu-id="0bcea-154">Licensing time-out.</span></span>

</dd> <dt>

<span id="disconnectReasonLocalNotError"></span><span id="disconnectreasonlocalnoterror"></span><span id="DISCONNECTREASONLOCALNOTERROR"></span>

<span data-ttu-id="0bcea-155"><span id="disconnectReasonLocalNotError"></span><span id="disconnectreasonlocalnoterror"></span><span id="DISCONNECTREASONLOCALNOTERROR"></span>**дисконнектреасонлокалнотеррор** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="0bcea-155"><span id="disconnectReasonLocalNotError"></span><span id="disconnectreasonlocalnoterror"></span><span id="DISCONNECTREASONLOCALNOTERROR"></span>**disconnectReasonLocalNotError** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-156">Локальное отключение.</span><span class="sxs-lookup"><span data-stu-id="0bcea-156">Local disconnection.</span></span> <span data-ttu-id="0bcea-157">Это не код ошибки.</span><span class="sxs-lookup"><span data-stu-id="0bcea-157">This is not an error code.</span></span>

</dd> <dt>

<span id="disconnectReasonNoInfo"></span><span id="disconnectreasonnoinfo"></span><span id="DISCONNECTREASONNOINFO"></span>

<span data-ttu-id="0bcea-158"><span id="disconnectReasonNoInfo"></span><span id="disconnectreasonnoinfo"></span><span id="DISCONNECTREASONNOINFO"></span>**дисконнектреасонноинфо** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="0bcea-158"><span id="disconnectReasonNoInfo"></span><span id="disconnectreasonnoinfo"></span><span id="DISCONNECTREASONNOINFO"></span>**disconnectReasonNoInfo** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-159">Сведения недоступны.</span><span class="sxs-lookup"><span data-stu-id="0bcea-159">No information is available.</span></span>

</dd> <dt>

<span id="disconnectReasonOutOfMemory"></span><span id="disconnectreasonoutofmemory"></span><span id="DISCONNECTREASONOUTOFMEMORY"></span>

<span data-ttu-id="0bcea-160"><span id="disconnectReasonOutOfMemory"></span><span id="disconnectreasonoutofmemory"></span><span id="DISCONNECTREASONOUTOFMEMORY"></span>**дисконнектреасонаутофмемори** (262 (0x106))</span><span class="sxs-lookup"><span data-stu-id="0bcea-160"><span id="disconnectReasonOutOfMemory"></span><span id="disconnectreasonoutofmemory"></span><span id="DISCONNECTREASONOUTOFMEMORY"></span>**disconnectReasonOutOfMemory** (262 (0x106))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-161">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="0bcea-161">Out of memory.</span></span>

</dd> <dt>

<span id="disconnectReasonOutOfMemory2"></span><span id="disconnectreasonoutofmemory2"></span><span id="DISCONNECTREASONOUTOFMEMORY2"></span>

<span data-ttu-id="0bcea-162"><span id="disconnectReasonOutOfMemory2"></span><span id="disconnectreasonoutofmemory2"></span><span id="DISCONNECTREASONOUTOFMEMORY2"></span>**disconnectReasonOutOfMemory2** (518 (0x206))</span><span class="sxs-lookup"><span data-stu-id="0bcea-162"><span id="disconnectReasonOutOfMemory2"></span><span id="disconnectreasonoutofmemory2"></span><span id="DISCONNECTREASONOUTOFMEMORY2"></span>**disconnectReasonOutOfMemory2** (518 (0x206))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-163">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="0bcea-163">Out of memory.</span></span>

</dd> <dt>

<span id="disconnectReasonOutOfMemory3"></span><span id="disconnectreasonoutofmemory3"></span><span id="DISCONNECTREASONOUTOFMEMORY3"></span>

<span data-ttu-id="0bcea-164"><span id="disconnectReasonOutOfMemory3"></span><span id="disconnectreasonoutofmemory3"></span><span id="DISCONNECTREASONOUTOFMEMORY3"></span>**disconnectReasonOutOfMemory3** (774 (0x306))</span><span class="sxs-lookup"><span data-stu-id="0bcea-164"><span id="disconnectReasonOutOfMemory3"></span><span id="disconnectreasonoutofmemory3"></span><span id="DISCONNECTREASONOUTOFMEMORY3"></span>**disconnectReasonOutOfMemory3** (774 (0x306))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-165">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="0bcea-165">Out of memory.</span></span>

</dd> <dt>

<span id="disconnectReasonRemoteByUser"></span><span id="disconnectreasonremotebyuser"></span><span id="DISCONNECTREASONREMOTEBYUSER"></span>

<span data-ttu-id="0bcea-166"><span id="disconnectReasonRemoteByUser"></span><span id="disconnectreasonremotebyuser"></span><span id="DISCONNECTREASONREMOTEBYUSER"></span>**дисконнектреасонремотебюсер** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="0bcea-166"><span id="disconnectReasonRemoteByUser"></span><span id="disconnectreasonremotebyuser"></span><span id="DISCONNECTREASONREMOTEBYUSER"></span>**disconnectReasonRemoteByUser** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-167">Удаленное отключение от пользователя.</span><span class="sxs-lookup"><span data-stu-id="0bcea-167">Remote disconnection by user.</span></span> <span data-ttu-id="0bcea-168">Это не код ошибки.</span><span class="sxs-lookup"><span data-stu-id="0bcea-168">This is not an error code.</span></span>

</dd> <dt>

<span id="disconnectReasonServerCertificateUnpackErr"></span><span id="disconnectreasonservercertificateunpackerr"></span><span id="DISCONNECTREASONSERVERCERTIFICATEUNPACKERR"></span>

<span data-ttu-id="0bcea-169"><span id="disconnectReasonServerCertificateUnpackErr"></span><span id="disconnectreasonservercertificateunpackerr"></span><span id="DISCONNECTREASONSERVERCERTIFICATEUNPACKERR"></span>**дисконнектреасонсерверцертификатеунпаккерр** (1798 (0x706))</span><span class="sxs-lookup"><span data-stu-id="0bcea-169"><span id="disconnectReasonServerCertificateUnpackErr"></span><span id="disconnectreasonservercertificateunpackerr"></span><span id="DISCONNECTREASONSERVERCERTIFICATEUNPACKERR"></span>**disconnectReasonServerCertificateUnpackErr** (1798 (0x706))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-170">Не удалось распаковать сертификат сервера.</span><span class="sxs-lookup"><span data-stu-id="0bcea-170">Failed to unpack server certificate.</span></span>

</dd> <dt>

<span id="disconnectReasonSocketConnectFailed"></span><span id="disconnectreasonsocketconnectfailed"></span><span id="DISCONNECTREASONSOCKETCONNECTFAILED"></span>

<span data-ttu-id="0bcea-171"><span id="disconnectReasonSocketConnectFailed"></span><span id="disconnectreasonsocketconnectfailed"></span><span id="DISCONNECTREASONSOCKETCONNECTFAILED"></span>**дисконнектреасонсоккетконнектфаилед** (516 (0x204))</span><span class="sxs-lookup"><span data-stu-id="0bcea-171"><span id="disconnectReasonSocketConnectFailed"></span><span id="disconnectreasonsocketconnectfailed"></span><span id="DISCONNECTREASONSOCKETCONNECTFAILED"></span>**disconnectReasonSocketConnectFailed** (516 (0x204))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-172">Сбой [**подключения**](/windows/desktop/api/winsock2/nf-winsock2-connect) сокетов Windows.</span><span class="sxs-lookup"><span data-stu-id="0bcea-172">Windows Sockets [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) failed.</span></span>

</dd> <dt>

<span id="disconnectReasonSocketRecvFailed"></span><span id="disconnectreasonsocketrecvfailed"></span><span id="DISCONNECTREASONSOCKETRECVFAILED"></span>

<span data-ttu-id="0bcea-173"><span id="disconnectReasonSocketRecvFailed"></span><span id="disconnectreasonsocketrecvfailed"></span><span id="DISCONNECTREASONSOCKETRECVFAILED"></span>**дисконнектреасонсоккетреквфаилед** (1028 (0x404))</span><span class="sxs-lookup"><span data-stu-id="0bcea-173"><span id="disconnectReasonSocketRecvFailed"></span><span id="disconnectreasonsocketrecvfailed"></span><span id="DISCONNECTREASONSOCKETRECVFAILED"></span>**disconnectReasonSocketRecvFailed** (1028 (0x404))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-174">Сбой вызова метода [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) для сокетов Windows.</span><span class="sxs-lookup"><span data-stu-id="0bcea-174">Windows Sockets [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) call failed.</span></span>

</dd> <dt>

<span id="disconnectReasonTimeoutOccurred"></span><span id="disconnectreasontimeoutoccurred"></span><span id="DISCONNECTREASONTIMEOUTOCCURRED"></span>

<span data-ttu-id="0bcea-175"><span id="disconnectReasonTimeoutOccurred"></span><span id="disconnectreasontimeoutoccurred"></span><span id="DISCONNECTREASONTIMEOUTOCCURRED"></span>**дисконнектреасонтимеаутоккурред** (1796 (0x704))</span><span class="sxs-lookup"><span data-stu-id="0bcea-175"><span id="disconnectReasonTimeoutOccurred"></span><span id="disconnectreasontimeoutoccurred"></span><span id="DISCONNECTREASONTIMEOUTOCCURRED"></span>**disconnectReasonTimeoutOccurred** (1796 (0x704))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-176">Истекло время ожидания.</span><span class="sxs-lookup"><span data-stu-id="0bcea-176">Time-out occurred.</span></span>

</dd> <dt>

<span id="disconnectReasonTimerError"></span><span id="disconnectreasontimererror"></span><span id="DISCONNECTREASONTIMERERROR"></span>

<span data-ttu-id="0bcea-177"><span id="disconnectReasonTimerError"></span><span id="disconnectreasontimererror"></span><span id="DISCONNECTREASONTIMERERROR"></span>**дисконнектреасонтимереррор** (1544 (0x608))</span><span class="sxs-lookup"><span data-stu-id="0bcea-177"><span id="disconnectReasonTimerError"></span><span id="disconnectreasontimererror"></span><span id="DISCONNECTREASONTIMERERROR"></span>**disconnectReasonTimerError** (1544 (0x608))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-178">Внутренняя ошибка таймера.</span><span class="sxs-lookup"><span data-stu-id="0bcea-178">Internal timer error.</span></span>

</dd> <dt>

<span id="disconnectReasonWinsockSendFailed"></span><span id="disconnectreasonwinsocksendfailed"></span><span id="DISCONNECTREASONWINSOCKSENDFAILED"></span>

<span data-ttu-id="0bcea-179"><span id="disconnectReasonWinsockSendFailed"></span><span id="disconnectreasonwinsocksendfailed"></span><span id="DISCONNECTREASONWINSOCKSENDFAILED"></span>**дисконнектреасонвинсокксендфаилед** (772 (0x304))</span><span class="sxs-lookup"><span data-stu-id="0bcea-179"><span id="disconnectReasonWinsockSendFailed"></span><span id="disconnectreasonwinsocksendfailed"></span><span id="DISCONNECTREASONWINSOCKSENDFAILED"></span>**disconnectReasonWinsockSendFailed** (772 (0x304))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-180">Не удалось вызвать [**отправку**](/windows/desktop/api/winsock2/nf-winsock2-send) сокетов Windows.</span><span class="sxs-lookup"><span data-stu-id="0bcea-180">Windows Sockets [**send**](/windows/desktop/api/winsock2/nf-winsock2-send) call failed.</span></span>

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_DISABLED"></span><span id="ssl_err_account_disabled"></span>

<span data-ttu-id="0bcea-181"><span id="SSL_ERR_ACCOUNT_DISABLED"></span><span id="ssl_err_account_disabled"></span>**Протокол SSL \_ \_Учетная запись Err \_ отключена** (2823 (0xB07))</span><span class="sxs-lookup"><span data-stu-id="0bcea-181"><span id="SSL_ERR_ACCOUNT_DISABLED"></span><span id="ssl_err_account_disabled"></span>**SSL\_ERR\_ACCOUNT\_DISABLED** (2823 (0xB07))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-182">Учетная запись отключена.</span><span class="sxs-lookup"><span data-stu-id="0bcea-182">The account is disabled.</span></span>

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_EXPIRED"></span><span id="ssl_err_account_expired"></span>

<span data-ttu-id="0bcea-183"><span id="SSL_ERR_ACCOUNT_EXPIRED"></span><span id="ssl_err_account_expired"></span>**Протокол SSL \_ \_ \_ Срок действия учетной записи ERR истек** (3591 (0xE07))</span><span class="sxs-lookup"><span data-stu-id="0bcea-183"><span id="SSL_ERR_ACCOUNT_EXPIRED"></span><span id="ssl_err_account_expired"></span>**SSL\_ERR\_ACCOUNT\_EXPIRED** (3591 (0xE07))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-184">Срок действия учетной записи истек.</span><span class="sxs-lookup"><span data-stu-id="0bcea-184">The account is expired.</span></span>

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_LOCKED_OUT"></span><span id="ssl_err_account_locked_out"></span>

<span data-ttu-id="0bcea-185"><span id="SSL_ERR_ACCOUNT_LOCKED_OUT"></span><span id="ssl_err_account_locked_out"></span>**Протокол SSL \_ \_Учетная запись Err \_ заблокирована \_** (3335 (0xD07))</span><span class="sxs-lookup"><span data-stu-id="0bcea-185"><span id="SSL_ERR_ACCOUNT_LOCKED_OUT"></span><span id="ssl_err_account_locked_out"></span>**SSL\_ERR\_ACCOUNT\_LOCKED\_OUT** (3335 (0xD07))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-186">Учетная запись заблокирована.</span><span class="sxs-lookup"><span data-stu-id="0bcea-186">The account is locked out.</span></span>

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_RESTRICTION"></span><span id="ssl_err_account_restriction"></span>

<span data-ttu-id="0bcea-187"><span id="SSL_ERR_ACCOUNT_RESTRICTION"></span><span id="ssl_err_account_restriction"></span>**Протокол SSL \_ \_ \_ Ограничение учетной записи ERR** (3079 (0xC07))</span><span class="sxs-lookup"><span data-stu-id="0bcea-187"><span id="SSL_ERR_ACCOUNT_RESTRICTION"></span><span id="ssl_err_account_restriction"></span>**SSL\_ERR\_ACCOUNT\_RESTRICTION** (3079 (0xC07))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-188">Учетная запись ограничена.</span><span class="sxs-lookup"><span data-stu-id="0bcea-188">The account is restricted.</span></span>

</dd> <dt>

<span id="SSL_ERR_CERT_EXPIRED"></span><span id="ssl_err_cert_expired"></span>

<span data-ttu-id="0bcea-189"><span id="SSL_ERR_CERT_EXPIRED"></span><span id="ssl_err_cert_expired"></span>**Протокол SSL \_ \_ \_ Истек срок действия сертификата ERR** (6919 (0x1B07))</span><span class="sxs-lookup"><span data-stu-id="0bcea-189"><span id="SSL_ERR_CERT_EXPIRED"></span><span id="ssl_err_cert_expired"></span>**SSL\_ERR\_CERT\_EXPIRED** (6919 (0x1B07))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-190">Срок действия полученного сертификата истек.</span><span class="sxs-lookup"><span data-stu-id="0bcea-190">The received certificate is expired.</span></span>

</dd> <dt>

<span id="SSL_ERR_DELEGATION_POLICY"></span><span id="ssl_err_delegation_policy"></span>

<span data-ttu-id="0bcea-191"><span id="SSL_ERR_DELEGATION_POLICY"></span><span id="ssl_err_delegation_policy"></span>**Протокол SSL \_ \_ \_ Политика делегирования ERR** (5639 (0x1607))</span><span class="sxs-lookup"><span data-stu-id="0bcea-191"><span id="SSL_ERR_DELEGATION_POLICY"></span><span id="ssl_err_delegation_policy"></span>**SSL\_ERR\_DELEGATION\_POLICY** (5639 (0x1607))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-192">Политика не поддерживает делегирование учетных данных на целевой сервер.</span><span class="sxs-lookup"><span data-stu-id="0bcea-192">The policy does not support delegation of credentials to the target server.</span></span>

</dd> <dt>

<span id="SSL_ERR_FRESH_CRED_REQUIRED_BY_SERVER"></span><span id="ssl_err_fresh_cred_required_by_server"></span>

<span data-ttu-id="0bcea-193"><span id="SSL_ERR_FRESH_CRED_REQUIRED_BY_SERVER"></span><span id="ssl_err_fresh_cred_required_by_server"></span>**Протокол SSL \_ \_ \_ \_ \_ Для \_ сервера требуется новое подсчета Err** (8455 (0x2107))</span><span class="sxs-lookup"><span data-stu-id="0bcea-193"><span id="SSL_ERR_FRESH_CRED_REQUIRED_BY_SERVER"></span><span id="ssl_err_fresh_cred_required_by_server"></span>**SSL\_ERR\_FRESH\_CRED\_REQUIRED\_BY\_SERVER** (8455 (0x2107))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-194">Политика проверки подлинности сервера не разрешает запросы на подключение с использованием сохраненных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="0bcea-194">The server authentication policy does not allow connection requests using saved credentials.</span></span> <span data-ttu-id="0bcea-195">Пользователь должен ввести новые учетные данные.</span><span class="sxs-lookup"><span data-stu-id="0bcea-195">The user must enter new credentials.</span></span>

</dd> <dt>

<span id="SSL_ERR_LOGON_FAILURE"></span><span id="ssl_err_logon_failure"></span>

<span data-ttu-id="0bcea-196"><span id="SSL_ERR_LOGON_FAILURE"></span><span id="ssl_err_logon_failure"></span>**Протокол SSL \_ Ошибка \_ входа \_ ERR** (2055 (0x807))</span><span class="sxs-lookup"><span data-stu-id="0bcea-196"><span id="SSL_ERR_LOGON_FAILURE"></span><span id="ssl_err_logon_failure"></span>**SSL\_ERR\_LOGON\_FAILURE** (2055 (0x807))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-197">Ошибка входа.</span><span class="sxs-lookup"><span data-stu-id="0bcea-197">Login failed.</span></span>

</dd> <dt>

<span id="SSL_ERR_NO_AUTHENTICATING_AUTHORITY"></span><span id="ssl_err_no_authenticating_authority"></span>

<span data-ttu-id="0bcea-198"><span id="SSL_ERR_NO_AUTHENTICATING_AUTHORITY"></span><span id="ssl_err_no_authenticating_authority"></span>**Протокол SSL \_ Ошибка \_ без \_ \_ центра проверки подлинности** (6151 (0x1807))</span><span class="sxs-lookup"><span data-stu-id="0bcea-198"><span id="SSL_ERR_NO_AUTHENTICATING_AUTHORITY"></span><span id="ssl_err_no_authenticating_authority"></span>**SSL\_ERR\_NO\_AUTHENTICATING\_AUTHORITY** (6151 (0x1807))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-199">Не удалось связаться с центром сертификации для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="0bcea-199">No authority could be contacted for authentication.</span></span> <span data-ttu-id="0bcea-200">Доменное имя проверяющей стороны может быть неверным, домен может быть недоступен или произошла ошибка отношения доверия.</span><span class="sxs-lookup"><span data-stu-id="0bcea-200">The domain name of the authenticating party could be wrong, the domain could be unreachable, or there might have been a trust relationship failure.</span></span>

</dd> <dt>

<span id="SSL_ERR_NO_SUCH_USER"></span><span id="ssl_err_no_such_user"></span>

<span data-ttu-id="0bcea-201"><span id="SSL_ERR_NO_SUCH_USER"></span><span id="ssl_err_no_such_user"></span>**Протокол SSL \_ Ошибка \_ нет \_ такого \_ пользователя** (2567 (0xA07))</span><span class="sxs-lookup"><span data-stu-id="0bcea-201"><span id="SSL_ERR_NO_SUCH_USER"></span><span id="ssl_err_no_such_user"></span>**SSL\_ERR\_NO\_SUCH\_USER** (2567 (0xA07))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-202">Указанный пользователь не имеет учетной записи.</span><span class="sxs-lookup"><span data-stu-id="0bcea-202">The specified user has no account.</span></span>

</dd> <dt>

<span id="SSL_ERR_PASSWORD_EXPIRED"></span><span id="ssl_err_password_expired"></span>

<span data-ttu-id="0bcea-203"><span id="SSL_ERR_PASSWORD_EXPIRED"></span><span id="ssl_err_password_expired"></span>**Протокол SSL \_ \_ \_ Истек срок действия пароля ERR** (3847 (0xF07))</span><span class="sxs-lookup"><span data-stu-id="0bcea-203"><span id="SSL_ERR_PASSWORD_EXPIRED"></span><span id="ssl_err_password_expired"></span>**SSL\_ERR\_PASSWORD\_EXPIRED** (3847 (0xF07))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-204">Срок действия пароля истек.</span><span class="sxs-lookup"><span data-stu-id="0bcea-204">The password is expired.</span></span>

</dd> <dt>

<span id="SSL_ERR_PASSWORD_MUST_CHANGE"></span><span id="ssl_err_password_must_change"></span>

<span data-ttu-id="0bcea-205"><span id="SSL_ERR_PASSWORD_MUST_CHANGE"></span><span id="ssl_err_password_must_change"></span>**Протокол SSL \_ \_Пароль Err \_ должен \_ измениться** (4615 (0x1207))</span><span class="sxs-lookup"><span data-stu-id="0bcea-205"><span id="SSL_ERR_PASSWORD_MUST_CHANGE"></span><span id="ssl_err_password_must_change"></span>**SSL\_ERR\_PASSWORD\_MUST\_CHANGE** (4615 (0x1207))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-206">Перед первым входом в систему необходимо изменить пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="0bcea-206">The user password must be changed before logging on for the first time.</span></span>

</dd> <dt>

<span id="SSL_ERR_POLICY_NTLM_ONLY"></span><span id="ssl_err_policy_ntlm_only"></span>

<span data-ttu-id="0bcea-207"><span id="SSL_ERR_POLICY_NTLM_ONLY"></span><span id="ssl_err_policy_ntlm_only"></span>**Протокол SSL \_ \_ \_ \_ Только политика ERR NTLM** (5895 (0x1707))</span><span class="sxs-lookup"><span data-stu-id="0bcea-207"><span id="SSL_ERR_POLICY_NTLM_ONLY"></span><span id="ssl_err_policy_ntlm_only"></span>**SSL\_ERR\_POLICY\_NTLM\_ONLY** (5895 (0x1707))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-208">Делегирование учетных данных на целевой сервер не разрешено, если не достигнута взаимная проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="0bcea-208">Delegation of credentials to the target server is not allowed unless mutual authentication has been achieved.</span></span>

</dd> <dt>

<span id="SSL_ERR_SMARTCARD_CARD_BLOCKED"></span><span id="ssl_err_smartcard_card_blocked"></span>

<span data-ttu-id="0bcea-209"><span id="SSL_ERR_SMARTCARD_CARD_BLOCKED"></span><span id="ssl_err_smartcard_card_blocked"></span>**Протокол SSL \_ \_ \_ \_ Заблокированная смарт-карта Err** (8711 (0x2207))</span><span class="sxs-lookup"><span data-stu-id="0bcea-209"><span id="SSL_ERR_SMARTCARD_CARD_BLOCKED"></span><span id="ssl_err_smartcard_card_blocked"></span>**SSL\_ERR\_SMARTCARD\_CARD\_BLOCKED** (8711 (0x2207))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-210">Смарт-карта заблокирована.</span><span class="sxs-lookup"><span data-stu-id="0bcea-210">The smart card is blocked.</span></span>

</dd> <dt>

<span id="SSL_ERR_SMARTCARD_WRONG_PIN"></span><span id="ssl_err_smartcard_wrong_pin"></span>

<span data-ttu-id="0bcea-211"><span id="SSL_ERR_SMARTCARD_WRONG_PIN"></span><span id="ssl_err_smartcard_wrong_pin"></span>**Протокол SSL \_ \_ \_ Неправильный \_ ПИН-код** (7175 (0x1C07))</span><span class="sxs-lookup"><span data-stu-id="0bcea-211"><span id="SSL_ERR_SMARTCARD_WRONG_PIN"></span><span id="ssl_err_smartcard_wrong_pin"></span>**SSL\_ERR\_SMARTCARD\_WRONG\_PIN** (7175 (0x1C07))</span></span>


</dt> <dd>

<span data-ttu-id="0bcea-212">Смарт-карте предоставлен неверный ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="0bcea-212">An incorrect PIN was presented to the smart card.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bcea-213">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0bcea-213">Return value</span></span>

<span data-ttu-id="0bcea-214">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="0bcea-214">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bcea-215">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0bcea-215">Remarks</span></span>

<span data-ttu-id="0bcea-216">Чтобы получить описание ошибки отключения, вызовите метод [**жетеррордескриптион**](imsrdpclient5-geterrordescription.md) и передайте ему параметр *Дискреасон* и свойство [**екстендеддисконнектреасон**](imsrdpclient-extendeddisconnectreason.md) интерфейса [**имсрдпклиент**](imsrdpclient-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="0bcea-216">To retrieve a description of the disconnect error, call the [**GetErrorDescription**](imsrdpclient5-geterrordescription.md) method and pass it the *discReason* parameter and the [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md) property of the [**IMsRdpClient**](imsrdpclient-interface.md) interface.</span></span>

<span data-ttu-id="0bcea-217">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0bcea-217">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0bcea-218">Требования</span><span class="sxs-lookup"><span data-stu-id="0bcea-218">Requirements</span></span>



| <span data-ttu-id="0bcea-219">Требование</span><span class="sxs-lookup"><span data-stu-id="0bcea-219">Requirement</span></span> | <span data-ttu-id="0bcea-220">Значение</span><span class="sxs-lookup"><span data-stu-id="0bcea-220">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0bcea-221">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0bcea-221">Minimum supported client</span></span><br/> | <span data-ttu-id="0bcea-222">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0bcea-222">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0bcea-223">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0bcea-223">Minimum supported server</span></span><br/> | <span data-ttu-id="0bcea-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0bcea-224">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0bcea-225">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="0bcea-225">Type library</span></span><br/>             | <dl> <span data-ttu-id="0bcea-226"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0bcea-226"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0bcea-227">DLL</span><span class="sxs-lookup"><span data-stu-id="0bcea-227">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0bcea-228"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0bcea-228"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0bcea-229">IID</span><span class="sxs-lookup"><span data-stu-id="0bcea-229">IID</span></span><br/>                      | <span data-ttu-id="0bcea-230">Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="0bcea-230">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="0bcea-231">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0bcea-231">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bcea-232">**имстскаксевентс**</span><span class="sxs-lookup"><span data-stu-id="0bcea-232">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

