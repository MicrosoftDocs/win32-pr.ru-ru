---
description: Протокол PNRP использует функцию Всалукупсервицебегин для запуска процесса, который позволяет приложению выполнить следующие действия.
ms.assetid: 71cca892-89e7-44d1-920d-987587eeed50
title: PNRP и Всалукупсервицебегин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78efd0ee28284cb41866795aea8a2a8d5f17e871
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "105664949"
---
# <a name="pnrp-and-wsalookupservicebegin"></a><span data-ttu-id="1bb48-103">PNRP и Всалукупсервицебегин</span><span class="sxs-lookup"><span data-stu-id="1bb48-103">PNRP and WSALookupServiceBegin</span></span>

<span data-ttu-id="1bb48-104">Протокол PNRP использует функцию [**всалукупсервицебегин**](winsock-nsp-reference-links.md) для запуска процесса, который позволяет приложению выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="1bb48-104">PNRP uses the [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) function to start the process that allows an application to do the following:</span></span>

-   [<span data-ttu-id="1bb48-105">Разрешение имени</span><span class="sxs-lookup"><span data-stu-id="1bb48-105">Resolving a name</span></span>](#resolving-a-name)
-   [<span data-ttu-id="1bb48-106">Перечисление сетевых облаков</span><span class="sxs-lookup"><span data-stu-id="1bb48-106">Enumerating network clouds</span></span>](#enumerating-network-clouds)

<span data-ttu-id="1bb48-107">Клиенты, пытающиеся выполнить одну из функций, используют функции [**всалукупсервицебегин**](winsock-nsp-reference-links.md), **всалукупсервиценекст** и **всалукупсервицеенд** .</span><span class="sxs-lookup"><span data-stu-id="1bb48-107">Clients that attempt to perform one of the functions use the [**WSALookupServiceBegin**](winsock-nsp-reference-links.md), **WSALookupServiceNext**, and **WSALookupServiceEnd** functions.</span></span>

<span data-ttu-id="1bb48-108">С помощью [**всанспиоктл**](winsock-nsp-reference-links.md)службу поиска можно использовать асинхронно.</span><span class="sxs-lookup"><span data-stu-id="1bb48-108">By using [**WSANSPIoctl**](winsock-nsp-reference-links.md), the lookup service can be used asynchronously.</span></span> <span data-ttu-id="1bb48-109">Сведения об асинхронном использовании функций службы поиска см. в разделе [PNRP and всанспиоктл](pnrp-and-wsanspioctl.md).</span><span class="sxs-lookup"><span data-stu-id="1bb48-109">For information about using the lookup service functions asynchronously, see [PNRP and WSANSPIoctl](pnrp-and-wsanspioctl.md).</span></span>

<span data-ttu-id="1bb48-110">Процесс работы с именами одноранговых узлов отличается от работы с облаками.</span><span class="sxs-lookup"><span data-stu-id="1bb48-110">The process for working with peer names is different from working with clouds.</span></span> <span data-ttu-id="1bb48-111">Каждый процесс описан отдельно в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="1bb48-111">Each process is described separately in this topic.</span></span>

## <a name="resolving-a-name"></a><span data-ttu-id="1bb48-112">Разрешение имени</span><span class="sxs-lookup"><span data-stu-id="1bb48-112">Resolving a Name</span></span>

<span data-ttu-id="1bb48-113">Приложение использует [**всалукупсервицебегин**](winsock-nsp-reference-links.md) для получения IP-адреса, порта и протокола для одноранговой службы, зарегистрированной на другом компьютере.</span><span class="sxs-lookup"><span data-stu-id="1bb48-113">An application uses [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) to obtain the IP address, port, and protocol for a peer service that is registered on another computer.</span></span> <span data-ttu-id="1bb48-114">Функция **всалукупсервицебегин** используется для запуска процесса разрешения имен и настройки параметров и ограничений.</span><span class="sxs-lookup"><span data-stu-id="1bb48-114">The **WSALookupServiceBegin** function is used to start the name resolution process, and set up the parameters and restrictions.</span></span> <span data-ttu-id="1bb48-115">Возвращается маркер, который должен использоваться при вызове **всалукупсервиценекст** и **всанспиоктл**.</span><span class="sxs-lookup"><span data-stu-id="1bb48-115">A handle is returned, and must be used when calling **WSALookupServiceNext** and **WSANSPIoctl**.</span></span>

### <a name="lpqsrestrictions"></a><span data-ttu-id="1bb48-116">лпксрестриктионс</span><span class="sxs-lookup"><span data-stu-id="1bb48-116">lpqsRestrictions</span></span>

<span data-ttu-id="1bb48-117">При разрешении имени однорангового узла Структура [**лпвсакуерисет**](pnrp-and-wsaqueryset.md) , на которую ссылается параметр *лпксрестриктионс* , должна содержать следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1bb48-117">When resolving a peer name, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure that the *lpqsRestrictions* parameter references must contain the following values:</span></span>

<dl> <dt>

<span data-ttu-id="1bb48-118"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**двсизе**</span><span class="sxs-lookup"><span data-stu-id="1bb48-118"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-119">Задает размер этой структуры.</span><span class="sxs-lookup"><span data-stu-id="1bb48-119">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-120"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**лпсзсервицеинстанценаме**</span><span class="sxs-lookup"><span data-stu-id="1bb48-120"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-121">Указывает имя однорангового узла для разрешения.</span><span class="sxs-lookup"><span data-stu-id="1bb48-121">Specifies a peer name to resolve.</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-122"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**лпсервицеклассид**</span><span class="sxs-lookup"><span data-stu-id="1bb48-122"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-123">Должен быть **свЦид \_ пнрпнаме**.</span><span class="sxs-lookup"><span data-stu-id="1bb48-123">Must be **SVCID\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-124"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**лпверсион**</span><span class="sxs-lookup"><span data-stu-id="1bb48-124"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-125">Зарезервировано, должно быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="1bb48-125">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-126"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**лпсзкоммент**</span><span class="sxs-lookup"><span data-stu-id="1bb48-126"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-127">Зарезервировано, должно быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="1bb48-127">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-128"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**двнамеспаце**</span><span class="sxs-lookup"><span data-stu-id="1bb48-128"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-129">Должен быть либо **NS \_ пнрпнаме** , либо **NS \_ ALL**.</span><span class="sxs-lookup"><span data-stu-id="1bb48-129">Must be either **NS\_PNRPNAME** or **NS\_ALL**.</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-130"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**лпнспровидерид**</span><span class="sxs-lookup"><span data-stu-id="1bb48-130"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-131">Необходимо указать либо **\_ \_ пнрпнаме Provider** , либо **null**.</span><span class="sxs-lookup"><span data-stu-id="1bb48-131">Must be either **NS\_PROVIDER\_PNRPNAME** or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-132"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**лпсзконтекст**</span><span class="sxs-lookup"><span data-stu-id="1bb48-132"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-133">Должно быть именем облака, пустой строкой или **значением NULL**.</span><span class="sxs-lookup"><span data-stu-id="1bb48-133">Must be a cloud name, an empty string, or **NULL**.</span></span> <span data-ttu-id="1bb48-134">Если это значение равно **null** или является пустой строкой, используется облако по умолчанию Global \_ .</span><span class="sxs-lookup"><span data-stu-id="1bb48-134">If this value is **NULL** or an empty string, the default cloud, "Global\_" is used.</span></span> <span data-ttu-id="1bb48-135">В противном случае он должен указывать на допустимое имя облака.</span><span class="sxs-lookup"><span data-stu-id="1bb48-135">Otherwise, it must point to a valid cloud name.</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-136"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**двнумберофпротоколс**</span><span class="sxs-lookup"><span data-stu-id="1bb48-136"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-137">Зарезервировано, должно быть равно нулю (0).</span><span class="sxs-lookup"><span data-stu-id="1bb48-137">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-138"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**лпсзкуеристринг**</span><span class="sxs-lookup"><span data-stu-id="1bb48-138"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-139">Зарезервировано, должно быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="1bb48-139">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-140"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**двнумберофксаддрс**</span><span class="sxs-lookup"><span data-stu-id="1bb48-140"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-141">Зарезервировано, должно быть равно нулю (0).</span><span class="sxs-lookup"><span data-stu-id="1bb48-141">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-142"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**лпксабуффер**</span><span class="sxs-lookup"><span data-stu-id="1bb48-142"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-143">Зарезервировано, должно быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="1bb48-143">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-144"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**дваутпутфлагс**</span><span class="sxs-lookup"><span data-stu-id="1bb48-144"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-145">Зарезервировано, должно быть равно нулю (0).</span><span class="sxs-lookup"><span data-stu-id="1bb48-145">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-146"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**лпблоб**</span><span class="sxs-lookup"><span data-stu-id="1bb48-146"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-147">Значение должно быть указателем на структуру [**больших двоичных объектов**](winsock-nsp-reference-links.md) или **null**.</span><span class="sxs-lookup"><span data-stu-id="1bb48-147">Must be either a pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure or **NULL**.</span></span> <span data-ttu-id="1bb48-148">Если он имеет **значение NULL**, используются значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1bb48-148">If it is **NULL**, default values are used.</span></span> <span data-ttu-id="1bb48-149">Если задано значение, **лпблоб** указывает на структуру [**пнрпинфо**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) , и необходимо задать определенные параметры в структуре **пнрпинфо** .</span><span class="sxs-lookup"><span data-stu-id="1bb48-149">If it is set, **lpBlob** points to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure, and specific parameters in the **PNRPINFO** structure must be set.</span></span> <span data-ttu-id="1bb48-150">Дополнительные сведения см. в следующих описаниях для структуры ПНРПИНФО.</span><span class="sxs-lookup"><span data-stu-id="1bb48-150">For more information, see the following descriptions for the PNRPINFO Structure.</span></span>

</dd> </dl>

<span data-ttu-id="1bb48-151">Структура ПНРПИНФО</span><span class="sxs-lookup"><span data-stu-id="1bb48-151">PNRPINFO Structure</span></span>

<span data-ttu-id="1bb48-152">Если задан элемент **лпблоб** структуры [**лпвсакуерисет**](pnrp-and-wsaqueryset.md) , необходимо установить следующие элементы структуры [**пнрпинфо**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) :</span><span class="sxs-lookup"><span data-stu-id="1bb48-152">If the **lpBlob** member of the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure is set, the following members of the [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure must be set:</span></span>

<dl> <dt>

<span data-ttu-id="1bb48-153"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**двсизе**</span><span class="sxs-lookup"><span data-stu-id="1bb48-153"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-154">Задает размер этой структуры.</span><span class="sxs-lookup"><span data-stu-id="1bb48-154">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-155"><span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**лпвсзидентити**</span><span class="sxs-lookup"><span data-stu-id="1bb48-155"><span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-156">Зарезервировано, должно быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="1bb48-156">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-157"><span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**нмаксресолве**</span><span class="sxs-lookup"><span data-stu-id="1bb48-157"><span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-158">Указывает запрошенное число разрешений.</span><span class="sxs-lookup"><span data-stu-id="1bb48-158">Specifies the requested number of resolutions.</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-159"><span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**двтимеаут**</span><span class="sxs-lookup"><span data-stu-id="1bb48-159"><span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-160">Указывает запрошенный период ожидания ответов.</span><span class="sxs-lookup"><span data-stu-id="1bb48-160">Specifies the requested timeout period to wait for responses.</span></span> <span data-ttu-id="1bb48-161">По умолчанию это 30 секунд.</span><span class="sxs-lookup"><span data-stu-id="1bb48-161">The default is 30 seconds.</span></span> <span data-ttu-id="1bb48-162">Максимальное значение составляет 600 секунд (10 минут).</span><span class="sxs-lookup"><span data-stu-id="1bb48-162">The maximum is 600 seconds (10 minutes).</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-163"><span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**двлифетиме**</span><span class="sxs-lookup"><span data-stu-id="1bb48-163"><span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-164">Зарезервировано, должно быть равно нулю (0).</span><span class="sxs-lookup"><span data-stu-id="1bb48-164">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-165"><span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**енресолвекритериа**</span><span class="sxs-lookup"><span data-stu-id="1bb48-165"><span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-166">Должно быть одним из допустимых значений.</span><span class="sxs-lookup"><span data-stu-id="1bb48-166">Must be one of the allowed values.</span></span> <span data-ttu-id="1bb48-167">По умолчанию **используется \_ условие разрешения PNRP, \_ \_ отличное от \_ текущего \_ \_ однорангового узла \_ процесса**.</span><span class="sxs-lookup"><span data-stu-id="1bb48-167">The default is **PNRP\_RESOLVE\_CRITERIA\_NON\_CURRENT\_PROCESS\_PEER\_NAME**.</span></span> <span data-ttu-id="1bb48-168">Допустимые значения указываются [**в \_ \_ критериях разрешения PNRP**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_resolve_criteria).</span><span class="sxs-lookup"><span data-stu-id="1bb48-168">Valid values are specified by [**PNRP\_RESOLVE\_CRITERIA**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_resolve_criteria).</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-169"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="1bb48-169"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-170">Должно быть либо нулевым (0), **либо \_ подсказкой пнрпинфо**.</span><span class="sxs-lookup"><span data-stu-id="1bb48-170">Must be either zero (0) or **PNRPINFO\_HINT**.</span></span> <span data-ttu-id="1bb48-171">Значение по умолчанию равно нулю (0).</span><span class="sxs-lookup"><span data-stu-id="1bb48-171">The default is zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-172"><span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**сахинт**</span><span class="sxs-lookup"><span data-stu-id="1bb48-172"><span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**saHint**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-173">Указывает IP-адрес для указания.</span><span class="sxs-lookup"><span data-stu-id="1bb48-173">Specifies the IP address for the hint.</span></span> <span data-ttu-id="1bb48-174">Указание используется при попытке найти ближайшее имя однорангового узла.</span><span class="sxs-lookup"><span data-stu-id="1bb48-174">The hint is used when attempting to find the nearest peer name.</span></span> <span data-ttu-id="1bb48-175">Подсказка представляет собой IPv6-адрес.</span><span class="sxs-lookup"><span data-stu-id="1bb48-175">The format of the hint is an IPv6 address.</span></span> <span data-ttu-id="1bb48-176">Если **сахинт** не указан при поиске ближайшего однорангового имени, вместо него используется IPv6-адрес локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="1bb48-176">If **saHint** is not specified when finding the closest peer name, then an IPv6 address of the local computer is used instead.</span></span> <span data-ttu-id="1bb48-177">Этот элемент игнорируется, если **dwFlags** не задан.</span><span class="sxs-lookup"><span data-stu-id="1bb48-177">This member is ignored if **dwFlags** is not set.</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-178"><span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**еннаместате**</span><span class="sxs-lookup"><span data-stu-id="1bb48-178"><span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-179">Зарезервировано, должно быть равно нулю (0).</span><span class="sxs-lookup"><span data-stu-id="1bb48-179">Reserved, must be zero (0).</span></span>

</dd> </dl>

### <a name="dwcontrolflags"></a><span data-ttu-id="1bb48-180">двконтролфлагс</span><span class="sxs-lookup"><span data-stu-id="1bb48-180">dwControlFlags</span></span>

<span data-ttu-id="1bb48-181">\_ \_ \* PNRP поддерживает следующие флаги возврата Луп:</span><span class="sxs-lookup"><span data-stu-id="1bb48-181">The following LUP\_RETURN\_\* flags are supported by PNRP:</span></span>



| <span data-ttu-id="1bb48-182">Значение</span><span class="sxs-lookup"><span data-stu-id="1bb48-182">Value</span></span>                | <span data-ttu-id="1bb48-183">Описание</span><span class="sxs-lookup"><span data-stu-id="1bb48-183">Description</span></span>                                |
|----------------------|--------------------------------------------|
| <span data-ttu-id="1bb48-184">\_имя возврата \_ Луп</span><span class="sxs-lookup"><span data-stu-id="1bb48-184">LUP\_RETURN\_NAME</span></span>    | <span data-ttu-id="1bb48-185">Возвращает имя и контекст.</span><span class="sxs-lookup"><span data-stu-id="1bb48-185">Returns a name and context.</span></span>                |
| <span data-ttu-id="1bb48-186">\_Комментарий возврата \_ Луп</span><span class="sxs-lookup"><span data-stu-id="1bb48-186">LUP\_RETURN\_COMMENT</span></span> | <span data-ttu-id="1bb48-187">Возвращает комментарий, связанный с именем.</span><span class="sxs-lookup"><span data-stu-id="1bb48-187">Returns a comment associated with a name.</span></span>  |
| <span data-ttu-id="1bb48-188">ЛУП \_ обратный \_ адрес</span><span class="sxs-lookup"><span data-stu-id="1bb48-188">LUP\_RETURN\_ADDR</span></span>    | <span data-ttu-id="1bb48-189">Возвращает адрес, связанный с именем.</span><span class="sxs-lookup"><span data-stu-id="1bb48-189">Returns an address associated with a name.</span></span> |



 

## <a name="enumerating-network-clouds"></a><span data-ttu-id="1bb48-190">Перечисление сетевых облаков</span><span class="sxs-lookup"><span data-stu-id="1bb48-190">Enumerating Network Clouds</span></span>

### <a name="lpqsrestrictions"></a><span data-ttu-id="1bb48-191">лпксрестриктионс</span><span class="sxs-lookup"><span data-stu-id="1bb48-191">lpqsRestrictions</span></span>

<span data-ttu-id="1bb48-192">При перечислении облаков структура [**лпвсакуерисет**](pnrp-and-wsaqueryset.md) , на которую ссылается параметр *лпксрестриктионс* , должна содержать следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1bb48-192">When enumerating clouds, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure that the *lpqsRestrictions* parameter references must contain the following values:</span></span>

<dl> <dt>

<span data-ttu-id="1bb48-193"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**двсизе**</span><span class="sxs-lookup"><span data-stu-id="1bb48-193"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-194">Задает размер этой структуры.</span><span class="sxs-lookup"><span data-stu-id="1bb48-194">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-195"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**лпсзсервицеинстанценаме**</span><span class="sxs-lookup"><span data-stu-id="1bb48-195"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-196">Должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="1bb48-196">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-197"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**лпсервицеклассид**</span><span class="sxs-lookup"><span data-stu-id="1bb48-197"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-198">Должен быть **свЦид \_ пнрпклауд**.</span><span class="sxs-lookup"><span data-stu-id="1bb48-198">Must be **SVCID\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-199"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**лпверсион**</span><span class="sxs-lookup"><span data-stu-id="1bb48-199"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-200">Зарезервировано, должно быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="1bb48-200">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-201"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**лпсзкоммент**</span><span class="sxs-lookup"><span data-stu-id="1bb48-201"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-202">Зарезервировано, должно быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="1bb48-202">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-203"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**двнамеспаце**</span><span class="sxs-lookup"><span data-stu-id="1bb48-203"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-204">Должен быть **\_ пнрпклауд NS**.</span><span class="sxs-lookup"><span data-stu-id="1bb48-204">Must be **NS\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-205"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**лпнспровидерид**</span><span class="sxs-lookup"><span data-stu-id="1bb48-205"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-206">Необходимо указать либо **\_ \_ пнрпклауд Provider** , либо **null**.</span><span class="sxs-lookup"><span data-stu-id="1bb48-206">Must be either **NS\_PROVIDER\_PNRPCLOUD** or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-207"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**лпсзконтекст**</span><span class="sxs-lookup"><span data-stu-id="1bb48-207"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-208">Зарезервировано, должно быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="1bb48-208">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-209"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**двнумберофпротоколс**</span><span class="sxs-lookup"><span data-stu-id="1bb48-209"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-210">Зарезервировано, должно быть равно нулю (0).</span><span class="sxs-lookup"><span data-stu-id="1bb48-210">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-211"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**лпсзкуеристринг**</span><span class="sxs-lookup"><span data-stu-id="1bb48-211"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-212">Зарезервировано, должно быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="1bb48-212">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-213"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**двнумберофксаддрс**</span><span class="sxs-lookup"><span data-stu-id="1bb48-213"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-214">Зарезервировано, должно быть равно нулю (0).</span><span class="sxs-lookup"><span data-stu-id="1bb48-214">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-215"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**лпксабуффер**</span><span class="sxs-lookup"><span data-stu-id="1bb48-215"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-216">Зарезервировано, должно быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="1bb48-216">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-217"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**дваутпутфлагс**</span><span class="sxs-lookup"><span data-stu-id="1bb48-217"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-218">Зарезервировано, должно быть равно нулю (0).</span><span class="sxs-lookup"><span data-stu-id="1bb48-218">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-219"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**лпблоб**</span><span class="sxs-lookup"><span data-stu-id="1bb48-219"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-220">Указатель на структуру [**большого двоичного объекта**](winsock-nsp-reference-links.md) , указывающую на структуру [**пнрпклаудинфо**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) .</span><span class="sxs-lookup"><span data-stu-id="1bb48-220">Pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure that points to a [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) structure.</span></span> <span data-ttu-id="1bb48-221">Если **лпблоб** имеет **значение NULL**, перечисляются все облака.</span><span class="sxs-lookup"><span data-stu-id="1bb48-221">If **lpBlob** is **NULL**, all clouds are enumerated.</span></span>

</dd> </dl>

<span data-ttu-id="1bb48-222">Структура ПНРПКЛАУДИНФО</span><span class="sxs-lookup"><span data-stu-id="1bb48-222">PNRPCLOUDINFO Structure</span></span>

<span data-ttu-id="1bb48-223">При перечислении облаков необходимо задать следующие члены структуры [**пнрпклаудинфо**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) :</span><span class="sxs-lookup"><span data-stu-id="1bb48-223">When enumerating clouds, the following members of the [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) structure must be set:</span></span>

<dl> <dt>

<span data-ttu-id="1bb48-224"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**двсизе**</span><span class="sxs-lookup"><span data-stu-id="1bb48-224"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-225">Задает размер этой структуры.</span><span class="sxs-lookup"><span data-stu-id="1bb48-225">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-226"><span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Вычислений**</span><span class="sxs-lookup"><span data-stu-id="1bb48-226"><span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Cloud**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-227">Указывает на структуру, задающую критерии, которые можно использовать для фильтрации результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="1bb48-227">Points to a structure that specifies criteria that you can use to filter search results.</span></span> <span data-ttu-id="1bb48-228">**Облако. Scope** может быть **\_ областью PNRP \_ любой**, **\_ глобальной \_ областью PNRP**, **\_ \_ локальной \_ областью сайта PNRP** или **\_ \_ локальной \_ областью связи PNRP**.</span><span class="sxs-lookup"><span data-stu-id="1bb48-228">The **Cloud.Scope** member can be **PNRP\_SCOPE\_ANY**, **PNRP\_GLOBAL\_SCOPE**, **PNRP\_SITE\_LOCAL\_SCOPE**, or **PNRP\_LINK\_LOCAL\_SCOPE**.</span></span> <span data-ttu-id="1bb48-229">Если указана **\_ область PNRP \_ ANY** , возвращаются все облака.</span><span class="sxs-lookup"><span data-stu-id="1bb48-229">If **PNRP\_SCOPE\_ANY** is specified, all clouds are returned.</span></span> <span data-ttu-id="1bb48-230">В противном случае возвращаются только облака, соответствующие **облаку. Scope** .</span><span class="sxs-lookup"><span data-stu-id="1bb48-230">Otherwise, only clouds that match the **Cloud.Scope** are returned.</span></span>

</dd> <dt>

<span data-ttu-id="1bb48-231"><span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**енклаудстате**</span><span class="sxs-lookup"><span data-stu-id="1bb48-231"><span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**</span></span>
</dt> <dd>

<span data-ttu-id="1bb48-232">Зарезервировано, должно быть равно нулю (0).</span><span class="sxs-lookup"><span data-stu-id="1bb48-232">Reserved, must be zero (0).</span></span>

</dd> </dl>

### <a name="dwcontrolflags"></a><span data-ttu-id="1bb48-233">двконтролфлагс</span><span class="sxs-lookup"><span data-stu-id="1bb48-233">dwControlFlags</span></span>

<span data-ttu-id="1bb48-234">\_ \_ \* PNRP поддерживает следующие флаги возврата Луп:</span><span class="sxs-lookup"><span data-stu-id="1bb48-234">The following LUP\_RETURN\_\* flags are supported by PNRP:</span></span>



| <span data-ttu-id="1bb48-235">Значение</span><span class="sxs-lookup"><span data-stu-id="1bb48-235">Value</span></span>             | <span data-ttu-id="1bb48-236">Описание</span><span class="sxs-lookup"><span data-stu-id="1bb48-236">Description</span></span>                                                       |
|-------------------|-------------------------------------------------------------------|
| <span data-ttu-id="1bb48-237">\_имя возврата \_ Луп</span><span class="sxs-lookup"><span data-stu-id="1bb48-237">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="1bb48-238">Возвращает имя и контекст.</span><span class="sxs-lookup"><span data-stu-id="1bb48-238">Returns a name and context.</span></span>                                       |
| <span data-ttu-id="1bb48-239">\_возвращаемый \_ BLOB-объект Луп</span><span class="sxs-lookup"><span data-stu-id="1bb48-239">LUP\_RETURN\_BLOB</span></span> | <span data-ttu-id="1bb48-240">Возвращает [большой двоичный объект](pnrp-and-blob.md) , связанный с этим облаком.</span><span class="sxs-lookup"><span data-stu-id="1bb48-240">Returns the [BLOB](pnrp-and-blob.md) associated with this cloud.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1bb48-241">См. также</span><span class="sxs-lookup"><span data-stu-id="1bb48-241">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bb48-242">PNRP и BLOB-объект</span><span class="sxs-lookup"><span data-stu-id="1bb48-242">PNRP and BLOB</span></span>](pnrp-and-blob.md)
</dt> <dt>

[<span data-ttu-id="1bb48-243">PNRP и Всалукупсервицеенд</span><span class="sxs-lookup"><span data-stu-id="1bb48-243">PNRP and WSALookupServiceEnd</span></span>](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[<span data-ttu-id="1bb48-244">PNRP и Всалукупсервиценекст</span><span class="sxs-lookup"><span data-stu-id="1bb48-244">PNRP and WSALookupServiceNext</span></span>](pnrp-and-wsalookupservicenext.md)
</dt> <dt>

[<span data-ttu-id="1bb48-245">PNRP и Всанспиоктл</span><span class="sxs-lookup"><span data-stu-id="1bb48-245">PNRP and WSANSPIoctl</span></span>](pnrp-and-wsanspioctl.md)
</dt> <dt>

[<span data-ttu-id="1bb48-246">PNRP и ВСАКУЕРИСЕТ</span><span class="sxs-lookup"><span data-stu-id="1bb48-246">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)
</dt> <dt>

[<span data-ttu-id="1bb48-247">**пнрпклаудинфо**</span><span class="sxs-lookup"><span data-stu-id="1bb48-247">**PNRPCLOUDINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)
</dt> <dt>

[<span data-ttu-id="1bb48-248">**пнрпинфо**</span><span class="sxs-lookup"><span data-stu-id="1bb48-248">**PNRPINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[<span data-ttu-id="1bb48-249">Коды ошибок PNRP NSP</span><span class="sxs-lookup"><span data-stu-id="1bb48-249">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> </dl>

 

 



