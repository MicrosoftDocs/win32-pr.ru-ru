---
description: Протокол PNRP использует функцию Всалукупсервиценекст для сопоставления запросов, указанных в предыдущем вызове функции Всалукупсервицебегин.
ms.assetid: b3e1abf4-ff59-481d-b96e-f8916a47cd52
title: PNRP и Всалукупсервиценекст
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398beca2f16e4920ab7fbe43bb648cbc22d9f336
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663302"
---
# <a name="pnrp-and-wsalookupservicenext"></a><span data-ttu-id="ded1c-103">PNRP и Всалукупсервиценекст</span><span class="sxs-lookup"><span data-stu-id="ded1c-103">PNRP and WSALookupServiceNext</span></span>

<span data-ttu-id="ded1c-104">Протокол PNRP использует функцию [**всалукупсервиценекст**](winsock-nsp-reference-links.md) для сопоставления запросов, указанных в предыдущем вызове функции **всалукупсервицебегин**.</span><span class="sxs-lookup"><span data-stu-id="ded1c-104">PNRP uses the [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function to match queries specified in a previous call to **WSALookupServiceBegin**.</span></span> <span data-ttu-id="ded1c-105">Результаты функции **всалукупсервиценекст** определяются параметрами в структуре **всакуерисет** , переданной в начальном вызове функции **всалукупсервицебегин** .</span><span class="sxs-lookup"><span data-stu-id="ded1c-105">The results of the **WSALookupServiceNext** function are determined by settings in the **WSAQUERYSET** structure passed in the initial **WSALookupServiceBegin** function call.</span></span> <span data-ttu-id="ded1c-106">Эта функция используется для выполнения следующих двух функций:</span><span class="sxs-lookup"><span data-stu-id="ded1c-106">This function is used to perform the following two functions:</span></span>

-   <span data-ttu-id="ded1c-107">Разрешение имени однорангового узла в список адресов</span><span class="sxs-lookup"><span data-stu-id="ded1c-107">Resolving a peer name to a list of addresses</span></span>
-   <span data-ttu-id="ded1c-108">Перечисление сетевых облаков</span><span class="sxs-lookup"><span data-stu-id="ded1c-108">Enumerating network clouds</span></span>

<span data-ttu-id="ded1c-109">С помощью [**всанспиоктл**](winsock-nsp-reference-links.md)службу поиска можно использовать асинхронно.</span><span class="sxs-lookup"><span data-stu-id="ded1c-109">By using [**WSANSPIoctl**](winsock-nsp-reference-links.md), the lookup service can be used asynchronously.</span></span> <span data-ttu-id="ded1c-110">Сведения об асинхронном использовании функций службы поиска см. в разделе [PNRP and всанспиоктл](pnrp-and-wsanspioctl.md).</span><span class="sxs-lookup"><span data-stu-id="ded1c-110">For information about using the lookup service functions asynchronously, see [PNRP and WSANSPIoctl](pnrp-and-wsanspioctl.md).</span></span>

<span data-ttu-id="ded1c-111">Функция [**всалукупсервиценекст**](winsock-nsp-reference-links.md) блокируется, даже если вызывается **всанспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="ded1c-111">The [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function blocks even if **WSANSPIoctl** is called.</span></span> <span data-ttu-id="ded1c-112">Перед вызовом **всалукупсервиценекст** приложение должно подождать, пока оно не получит уведомление, если блокировка является проблемой.</span><span class="sxs-lookup"><span data-stu-id="ded1c-112">Before calling **WSALookupServiceNext**, an application must wait until it receives a notification—if blocking is an issue.</span></span>

## <a name="resolving-a-peer-name-to-a-list-of-addresses"></a><span data-ttu-id="ded1c-113">Разрешение имени однорангового узла в список адресов</span><span class="sxs-lookup"><span data-stu-id="ded1c-113">Resolving a Peer Name to a List of Addresses</span></span>

<span data-ttu-id="ded1c-114">При разрешении имени однорангового узла в список адресов структура [**лпвсакуерисет**](pnrp-and-wsaqueryset.md) , возвращаемая в параметре *лпксресултс* , содержит следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ded1c-114">When resolving a peer name to a list of addresses, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure returned in the *lpqsResults* parameter contains the following values:</span></span>

<dl> <dt>

<span data-ttu-id="ded1c-115"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**двсизе**</span><span class="sxs-lookup"><span data-stu-id="ded1c-115"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="ded1c-116">Возвращает размер структуры.</span><span class="sxs-lookup"><span data-stu-id="ded1c-116">Returns the size of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="ded1c-117"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**лпсзсервицеинстанценаме**</span><span class="sxs-lookup"><span data-stu-id="ded1c-117"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="ded1c-118">Возвращает имя однорангового узла — если **Луп \_ возвращаемое \_ имя**, **Луп \_ возвращает \_ все** или указано **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="ded1c-118">Returns a peer name—if **LUP\_RETURN\_NAME**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> <dt>

<span data-ttu-id="ded1c-119"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**лпсервицеклассид**</span><span class="sxs-lookup"><span data-stu-id="ded1c-119"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="ded1c-120">Возвращает **свЦид \_ пнрпнаме**.</span><span class="sxs-lookup"><span data-stu-id="ded1c-120">Returns **SVCID\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="ded1c-121"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**лпверсион**</span><span class="sxs-lookup"><span data-stu-id="ded1c-121"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="ded1c-122">Возвращает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ded1c-122">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ded1c-123"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**лпсзкоммент**</span><span class="sxs-lookup"><span data-stu-id="ded1c-123"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="ded1c-124">Возвращает комментарий: Если **Луп \_ возвращает \_ Комментарий**, **Луп \_ возвращает \_ все** или задано **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="ded1c-124">Returns a comment—if **LUP\_RETURN\_COMMENT**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> <dt>

<span data-ttu-id="ded1c-125"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**двнамеспаце**</span><span class="sxs-lookup"><span data-stu-id="ded1c-125"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="ded1c-126">Возвращает **\_ пнрпнаме NS**.</span><span class="sxs-lookup"><span data-stu-id="ded1c-126">Returns **NS\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="ded1c-127"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**лпнспровидерид**</span><span class="sxs-lookup"><span data-stu-id="ded1c-127"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="ded1c-128">Возвращает **\_ \_ пнрпнаме поставщика NS**.</span><span class="sxs-lookup"><span data-stu-id="ded1c-128">Returns **NS\_PROVIDER\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="ded1c-129"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**лпсзконтекст**</span><span class="sxs-lookup"><span data-stu-id="ded1c-129"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="ded1c-130">Возвращает имя облака, если **Луп \_ возвращаемое \_ имя**, **Луп \_ возвращает \_ все** или указано **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="ded1c-130">Returns the cloud name if **LUP\_RETURN\_NAME**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> <dt>

<span data-ttu-id="ded1c-131"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**двнумберофпротоколс**</span><span class="sxs-lookup"><span data-stu-id="ded1c-131"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="ded1c-132">Возвращает ноль (0).</span><span class="sxs-lookup"><span data-stu-id="ded1c-132">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="ded1c-133"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**лпсзкуеристринг**</span><span class="sxs-lookup"><span data-stu-id="ded1c-133"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="ded1c-134">Возвращает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ded1c-134">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ded1c-135"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**двнумберофксаддрс**</span><span class="sxs-lookup"><span data-stu-id="ded1c-135"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="ded1c-136">Возвращает количество записей в \_ массиве сведений ксаддр, если **Луп \_ возвращаемый \_ адрес**, **Луп \_ возвращает \_ все** или задано **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="ded1c-136">Returns the number of entries in the CSADDR\_INFO array if **LUP\_RETURN\_ADDR**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span> <span data-ttu-id="ded1c-137">Это значение и сведения в **лпксабуффер** являются ключевыми битами информации, возвращаемой этой структурой.</span><span class="sxs-lookup"><span data-stu-id="ded1c-137">This value and the information in **lpcsaBuffer** are the key bits of information returned in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="ded1c-138"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**лпксабуффер**</span><span class="sxs-lookup"><span data-stu-id="ded1c-138"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="ded1c-139">Возвращает указатель на массив \_ структур ксаддр info, если **Луп \_ возвращает \_ АДР**, **Луп \_ возвращает \_ ALL** или **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="ded1c-139">Returns a pointer to an array of CSADDR\_INFO structures if **LUP\_RETURN\_ADDR**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span> <span data-ttu-id="ded1c-140">Этот буфер и значение в **двнумберофксаддрс** являются ключевыми битами данных, возвращаемыми в этой структуре.</span><span class="sxs-lookup"><span data-stu-id="ded1c-140">This buffer and the value in **dwNumberOfCsAddrs** are the key information bits returned in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="ded1c-141"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**дваутпутфлагс**</span><span class="sxs-lookup"><span data-stu-id="ded1c-141"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="ded1c-142">Возвращает ноль (0).</span><span class="sxs-lookup"><span data-stu-id="ded1c-142">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="ded1c-143"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**лпблоб**</span><span class="sxs-lookup"><span data-stu-id="ded1c-143"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="ded1c-144">Возвращает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ded1c-144">Returns **NULL**.</span></span>

</dd> </dl>

## <a name="enumerating-network-clouds"></a><span data-ttu-id="ded1c-145">Перечисление сетевых облаков</span><span class="sxs-lookup"><span data-stu-id="ded1c-145">Enumerating Network Clouds</span></span>

<span data-ttu-id="ded1c-146">При перечислении облаков структура [**лпвсакуерисет**](pnrp-and-wsaqueryset.md) , возвращаемая в параметре *лпксресултс* , содержит следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ded1c-146">When enumerating clouds, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure returned in the *lpqsResults* parameter contains the following values:</span></span>

<dl> <dt>

<span data-ttu-id="ded1c-147"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**двсизе**</span><span class="sxs-lookup"><span data-stu-id="ded1c-147"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="ded1c-148">Возвращает размер структуры.</span><span class="sxs-lookup"><span data-stu-id="ded1c-148">Returns the size of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="ded1c-149"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**лпсзсервицеинстанценаме**</span><span class="sxs-lookup"><span data-stu-id="ded1c-149"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="ded1c-150">Возвращает имя облака — если **Луп \_ возвращаемое \_ имя**, **Луп \_ возвращает \_ все** или указано **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="ded1c-150">Returns a cloud name—if **LUP\_RETURN\_NAME**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> <dt>

<span data-ttu-id="ded1c-151"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**лпсервицеклассид**</span><span class="sxs-lookup"><span data-stu-id="ded1c-151"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="ded1c-152">Возвращает **свЦид \_ пнрпклауд**.</span><span class="sxs-lookup"><span data-stu-id="ded1c-152">Returns **SVCID\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="ded1c-153"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**лпверсион**</span><span class="sxs-lookup"><span data-stu-id="ded1c-153"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="ded1c-154">Возвращает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ded1c-154">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ded1c-155"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**лпсзкоммент**</span><span class="sxs-lookup"><span data-stu-id="ded1c-155"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="ded1c-156">Возвращает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ded1c-156">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ded1c-157"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**двнамеспаце**</span><span class="sxs-lookup"><span data-stu-id="ded1c-157"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="ded1c-158">Возвращает **\_ пнрпклауд NS**.</span><span class="sxs-lookup"><span data-stu-id="ded1c-158">Returns **NS\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="ded1c-159"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**лпнспровидерид**</span><span class="sxs-lookup"><span data-stu-id="ded1c-159"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="ded1c-160">Возвращает **\_ \_ пнрпклауд поставщика NS**.</span><span class="sxs-lookup"><span data-stu-id="ded1c-160">Returns **NS\_PROVIDER\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="ded1c-161"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**лпсзконтекст**</span><span class="sxs-lookup"><span data-stu-id="ded1c-161"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="ded1c-162">Возвращает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ded1c-162">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ded1c-163"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**двнумберофпротоколс**</span><span class="sxs-lookup"><span data-stu-id="ded1c-163"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="ded1c-164">Возвращает ноль (0).</span><span class="sxs-lookup"><span data-stu-id="ded1c-164">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="ded1c-165"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**лпсзкуеристринг**</span><span class="sxs-lookup"><span data-stu-id="ded1c-165"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="ded1c-166">Возвращает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ded1c-166">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ded1c-167"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**двнумберофксаддрс**</span><span class="sxs-lookup"><span data-stu-id="ded1c-167"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="ded1c-168">Возвращает ноль (0).</span><span class="sxs-lookup"><span data-stu-id="ded1c-168">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="ded1c-169"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**лпксабуффер**</span><span class="sxs-lookup"><span data-stu-id="ded1c-169"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="ded1c-170">Возвращает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ded1c-170">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ded1c-171"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**дваутпутфлагс**</span><span class="sxs-lookup"><span data-stu-id="ded1c-171"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="ded1c-172">Возвращает ноль (0).</span><span class="sxs-lookup"><span data-stu-id="ded1c-172">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="ded1c-173"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**лпблоб**</span><span class="sxs-lookup"><span data-stu-id="ded1c-173"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="ded1c-174">Возвращает указатель на структуру [**больших двоичных объектов**](winsock-nsp-reference-links.md) , указывающую на структуру [**Пнрпклаудинфо**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) : Если **Луп \_ возвращает \_ большой двоичный объект**, **Луп \_ возвратите \_ ALL** или задается **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="ded1c-174">Returns a pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure that points to a [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) structure—if **LUP\_RETURN\_BLOB**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> </dl>

## <a name="pnrpcloudinfo-structure"></a><span data-ttu-id="ded1c-175">Структура ПНРПКЛАУДИНФО</span><span class="sxs-lookup"><span data-stu-id="ded1c-175">PNRPCLOUDINFO Structure</span></span>

<span data-ttu-id="ded1c-176">При перечислении облачных имен в структуре [**пнрпклаудинфо**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) возвращаются следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ded1c-176">When enumerating cloud names, the following values are returned in the [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) structure:</span></span>

<dl> <dt>

<span data-ttu-id="ded1c-177"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**двсизе**</span><span class="sxs-lookup"><span data-stu-id="ded1c-177"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="ded1c-178">Размер этой структуры.</span><span class="sxs-lookup"><span data-stu-id="ded1c-178">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="ded1c-179"><span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Вычислений**</span><span class="sxs-lookup"><span data-stu-id="ded1c-179"><span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Cloud**</span></span>
</dt> <dd>

<span data-ttu-id="ded1c-180">Фактическое значение облака.</span><span class="sxs-lookup"><span data-stu-id="ded1c-180">The actual cloud value.</span></span>

</dd> <dt>

<span data-ttu-id="ded1c-181"><span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**енклаудстате**</span><span class="sxs-lookup"><span data-stu-id="ded1c-181"><span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**</span></span>
</dt> <dd>

<span data-ttu-id="ded1c-182">Текущее состояние облака.</span><span class="sxs-lookup"><span data-stu-id="ded1c-182">The current state of a cloud.</span></span> <span data-ttu-id="ded1c-183">Протокол [**PNRP \_ \_Состояние облака**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_state) указывает допустимые значения.</span><span class="sxs-lookup"><span data-stu-id="ded1c-183">[**PNRP\_CLOUD\_STATE**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_state) specifies the valid values.</span></span>

</dd> <dt>

<span data-ttu-id="ded1c-184"><span id="enCloudFlags"></span><span id="encloudflags"></span><span id="ENCLOUDFLAGS"></span>**енклаудфлагс**</span><span class="sxs-lookup"><span data-stu-id="ded1c-184"><span id="enCloudFlags"></span><span id="encloudflags"></span><span id="ENCLOUDFLAGS"></span>**enCloudFlags**</span></span>
</dt> <dd>

<span data-ttu-id="ded1c-185">Указывает, что имя облака допустимо в сети или допустимо только на текущем компьютере.</span><span class="sxs-lookup"><span data-stu-id="ded1c-185">Indicates that a cloud name is valid on a network, or only valid on a current computer.</span></span> <span data-ttu-id="ded1c-186">Протокол [**PNRP \_ \_Флаги облака**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_flags) указывают допустимые значения.</span><span class="sxs-lookup"><span data-stu-id="ded1c-186">[**PNRP\_CLOUD\_FLAGS**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_flags) specifies the valid values.</span></span> <span data-ttu-id="ded1c-187">Некоторые облачные имена допустимы на любом компьютере в одной сети.</span><span class="sxs-lookup"><span data-stu-id="ded1c-187">Some cloud names are valid on any computer on the same network.</span></span> <span data-ttu-id="ded1c-188">Другие облачные имена действительны только на текущем компьютере и могут быть действительны только в течение определенного периода времени.</span><span class="sxs-lookup"><span data-stu-id="ded1c-188">Other cloud names are valid only on a current computer, and may be valid only for a period of time.</span></span>

-   <span data-ttu-id="ded1c-189">Если для **енклаудфлагс** задано **значение \_ \_ \_ Локальное облачное имя PNRP,** это имя допустимо только локально.</span><span class="sxs-lookup"><span data-stu-id="ded1c-189">If **enCloudFlags** is set to **PNRP\_CLOUD\_NAME\_LOCAL,** the name is only valid locally.</span></span>
-   <span data-ttu-id="ded1c-190">Если **енклаудфлагс** не задан, имя облака можно передать на другие компьютеры.</span><span class="sxs-lookup"><span data-stu-id="ded1c-190">If **enCloudFlags** is not set, then the cloud name can be transferred to other computers.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="ded1c-191">См. также</span><span class="sxs-lookup"><span data-stu-id="ded1c-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ded1c-192">PNRP и BLOB-объект</span><span class="sxs-lookup"><span data-stu-id="ded1c-192">PNRP and BLOB</span></span>](pnrp-and-blob.md)
</dt> <dt>

[<span data-ttu-id="ded1c-193">PNRP и Всалукупсервицеенд</span><span class="sxs-lookup"><span data-stu-id="ded1c-193">PNRP and WSALookupServiceEnd</span></span>](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[<span data-ttu-id="ded1c-194">PNRP и Всанспиоктл</span><span class="sxs-lookup"><span data-stu-id="ded1c-194">PNRP and WSANSPIoctl</span></span>](pnrp-and-wsanspioctl.md)
</dt> <dt>

[<span data-ttu-id="ded1c-195">PNRP и ВСАКУЕРИСЕТ</span><span class="sxs-lookup"><span data-stu-id="ded1c-195">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)
</dt> <dt>

[<span data-ttu-id="ded1c-196">**пнрпклаудинфо**</span><span class="sxs-lookup"><span data-stu-id="ded1c-196">**PNRPCLOUDINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)
</dt> <dt>

[<span data-ttu-id="ded1c-197">**пнрпинфо**</span><span class="sxs-lookup"><span data-stu-id="ded1c-197">**PNRPINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[<span data-ttu-id="ded1c-198">Коды ошибок PNRP NSP</span><span class="sxs-lookup"><span data-stu-id="ded1c-198">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> <dt>

[<span data-ttu-id="ded1c-199">**всалукупсервицебегин**</span><span class="sxs-lookup"><span data-stu-id="ded1c-199">**WSALookupServiceBegin**</span></span>](winsock-nsp-reference-links.md)
</dt> </dl>

 

 



