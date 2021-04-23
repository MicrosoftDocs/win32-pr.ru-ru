---
description: Для регистрации или удаления одноранговых имен в PNRP используется функция Всасетсервице.
ms.assetid: ea7941cd-2b3c-42d1-a291-759cbc32db0c
title: PNRP и Всасетсервице
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 005a04251a8b038c5895ae5dfafd65be9263edfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663295"
---
# <a name="pnrp-and-wsasetservice"></a><span data-ttu-id="527d9-103">PNRP и Всасетсервице</span><span class="sxs-lookup"><span data-stu-id="527d9-103">PNRP and WSASetService</span></span>

<span data-ttu-id="527d9-104">Для регистрации или удаления [одноранговых имен](peer-names.md)в PNRP используется функция [**всасетсервице**](winsock-nsp-reference-links.md) .</span><span class="sxs-lookup"><span data-stu-id="527d9-104">PNRP uses the [**WSASetService**](winsock-nsp-reference-links.md) function to register or remove [peer names](peer-names.md).</span></span>

## <a name="registering-a-name"></a><span data-ttu-id="527d9-105">Регистрация имени</span><span class="sxs-lookup"><span data-stu-id="527d9-105">Registering a Name</span></span>

<span data-ttu-id="527d9-106">Регистрация включает имя однорангового узла и набор конечных точек, с которыми можно связаться со службой.</span><span class="sxs-lookup"><span data-stu-id="527d9-106">Registration includes a peer name and set of endpoints where a service can be contacted.</span></span> <span data-ttu-id="527d9-107">Регистрация зависит от облака PNRP.</span><span class="sxs-lookup"><span data-stu-id="527d9-107">A registration is specific to a PNRP cloud.</span></span> <span data-ttu-id="527d9-108">После регистрации однорангового узла между регистрацией и распространением сведений о регистрации на другие узлы возникает задержка.</span><span class="sxs-lookup"><span data-stu-id="527d9-108">After a peer is registered, there is a delay between the registration and the propagation of the registration information to other nodes.</span></span> <span data-ttu-id="527d9-109">В течение этого времени другие узлы, возможно, не смогут разрешить только что зарегистрированный одноранговый узел.</span><span class="sxs-lookup"><span data-stu-id="527d9-109">During this time, other nodes may not be able to resolve a newly registered peer.</span></span>

<span data-ttu-id="527d9-110">Регистрация службы не является постоянной.</span><span class="sxs-lookup"><span data-stu-id="527d9-110">Service registration is not persistent.</span></span>

-   <span data-ttu-id="527d9-111">Если клиентский процесс, регистрирующий имя однорангового узла, завершает работу или вызывает [**всаклеануп**](winsock-nsp-reference-links.md), то имя однорангового узла отменяется.</span><span class="sxs-lookup"><span data-stu-id="527d9-111">If a client process that registers a peer name exits or calls [**WSACleanup**](winsock-nsp-reference-links.md), then the peer name is unregistered.</span></span>
-   <span data-ttu-id="527d9-112">Если указанное имя однорангового узла уже зарегистрировано в том же облаке текущим процессом, оно заменяется новыми значениями регистрации.</span><span class="sxs-lookup"><span data-stu-id="527d9-112">If a specified peer name is already registered in the same cloud by the current process, it is replaced with new registration values.</span></span>

<span data-ttu-id="527d9-113">При регистрации имени однорангового узла должны быть указаны следующие значения параметров:</span><span class="sxs-lookup"><span data-stu-id="527d9-113">When registering a peer name, the following parameter values must be indicated:</span></span>

-   <span data-ttu-id="527d9-114">параметр *ессоператион* должен иметь значение **рнрсервице \_ Register**.</span><span class="sxs-lookup"><span data-stu-id="527d9-114">*essOperation* parameter must have a value of **RNRSERVICE\_REGISTER**.</span></span>
-   <span data-ttu-id="527d9-115">параметр *двконтролфлагс* должен быть равен нулю (0).</span><span class="sxs-lookup"><span data-stu-id="527d9-115">*dwControlFlags* parameter must be zero (0).</span></span>

<span data-ttu-id="527d9-116">При регистрации имени однорангового узла Структура [**лпвсакуерисет**](pnrp-and-wsaqueryset.md) , на которую ссылается параметр *лпксрегинфо* , должна содержать следующие значения:</span><span class="sxs-lookup"><span data-stu-id="527d9-116">When registering a peer name, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure referenced by the *lpqsRegInfo* parameter must contain the following values:</span></span>

<dl> <dt>

<span data-ttu-id="527d9-117"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**двсизе**</span><span class="sxs-lookup"><span data-stu-id="527d9-117"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-118">Задает размер этой структуры.</span><span class="sxs-lookup"><span data-stu-id="527d9-118">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="527d9-119"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**лпсзсервицеинстанценаме**</span><span class="sxs-lookup"><span data-stu-id="527d9-119"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-120">Указывает имя однорангового узла для регистрации.</span><span class="sxs-lookup"><span data-stu-id="527d9-120">Specifies a peer name to register.</span></span> <span data-ttu-id="527d9-121">Если [имя однорангового узла](peer-names.md) не защищено, то удостоверение является необязательным.</span><span class="sxs-lookup"><span data-stu-id="527d9-121">If the [peer name](peer-names.md) is unsecured, then the identity is optional.</span></span> <span data-ttu-id="527d9-122">Если удостоверение указано как **null**, по умолчанию PNRP использует локальное удостоверение компьютера.</span><span class="sxs-lookup"><span data-stu-id="527d9-122">If the identity is specified as **NULL**, PNRP uses the machine local identity—by default.</span></span>

</dd> <dt>

<span data-ttu-id="527d9-123"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**лпсервицеклассид**</span><span class="sxs-lookup"><span data-stu-id="527d9-123"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-124">Должен быть СВЦИД \_ пнрпнаме.</span><span class="sxs-lookup"><span data-stu-id="527d9-124">Must be SVCID\_PNRPNAME.</span></span>

</dd> <dt>

<span data-ttu-id="527d9-125"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**лпверсион**</span><span class="sxs-lookup"><span data-stu-id="527d9-125"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-126">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="527d9-126">Ignored.</span></span> <span data-ttu-id="527d9-127">Задайте **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="527d9-127">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="527d9-128"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**лпсзкоммент**</span><span class="sxs-lookup"><span data-stu-id="527d9-128"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-129">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="527d9-129">Ignored.</span></span> <span data-ttu-id="527d9-130">Однако строка по-прежнему должна содержать менее 40 символов, включая знак завершения **null** .</span><span class="sxs-lookup"><span data-stu-id="527d9-130">However, the string is still required to be fewer than 40 characters, including the **NULL** terminator.</span></span>

</dd> <dt>

<span data-ttu-id="527d9-131"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**двнамеспаце**</span><span class="sxs-lookup"><span data-stu-id="527d9-131"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-132">Должен быть либо **NS \_ пнрпнаме** , либо **NS \_ ALL**.</span><span class="sxs-lookup"><span data-stu-id="527d9-132">Must be either **NS\_PNRPNAME** or **NS\_ALL**.</span></span>

</dd> <dt>

<span data-ttu-id="527d9-133"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**лпнспровидерид**</span><span class="sxs-lookup"><span data-stu-id="527d9-133"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-134">Необходимо указать либо **\_ \_ пнрпнаме Provider** , либо **null**.</span><span class="sxs-lookup"><span data-stu-id="527d9-134">Must be either **NS\_PROVIDER\_PNRPNAME** or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="527d9-135"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**лпсзконтекст**</span><span class="sxs-lookup"><span data-stu-id="527d9-135"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-136">Должно быть именем облака, пустой строкой или **значением NULL**.</span><span class="sxs-lookup"><span data-stu-id="527d9-136">Must be a cloud name, an empty string, or **NULL**.</span></span> <span data-ttu-id="527d9-137">Если это значение равно **null** или является пустой строкой, используется облако по умолчанию Global.</span><span class="sxs-lookup"><span data-stu-id="527d9-137">If this value is **NULL** or an empty string, the default cloud, "Global", is used.</span></span> <span data-ttu-id="527d9-138">В противном случае он должен указывать на допустимое имя облака.</span><span class="sxs-lookup"><span data-stu-id="527d9-138">Otherwise, it must point to a valid cloud name.</span></span>

</dd> <dt>

<span data-ttu-id="527d9-139"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**двнумберофпротоколс**</span><span class="sxs-lookup"><span data-stu-id="527d9-139"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-140">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="527d9-140">Ignored.</span></span> <span data-ttu-id="527d9-141">Установите нулевое значение (0).</span><span class="sxs-lookup"><span data-stu-id="527d9-141">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="527d9-142"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**лпсзкуеристринг**</span><span class="sxs-lookup"><span data-stu-id="527d9-142"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-143">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="527d9-143">Ignored.</span></span> <span data-ttu-id="527d9-144">Задайте **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="527d9-144">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="527d9-145"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**двнумберофксаддрс**</span><span class="sxs-lookup"><span data-stu-id="527d9-145"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-146">Указывает количество адресов, зарегистрированных службой.</span><span class="sxs-lookup"><span data-stu-id="527d9-146">Specifies the number of addresses registered by a service.</span></span> <span data-ttu-id="527d9-147">Максимальное число адресов, которое можно зарегистрировать для одного имени, равно 10.</span><span class="sxs-lookup"><span data-stu-id="527d9-147">The maximum number of addresses that can be registered for a single name is 10.</span></span>

</dd> <dt>

<span data-ttu-id="527d9-148"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**лпксабуффер**</span><span class="sxs-lookup"><span data-stu-id="527d9-148"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-149">Указатель на список адресов для регистрации.</span><span class="sxs-lookup"><span data-stu-id="527d9-149">Pointer to a list of addresses to register.</span></span>

</dd> <dt>

<span data-ttu-id="527d9-150"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**дваутпутфлагс**</span><span class="sxs-lookup"><span data-stu-id="527d9-150"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-151">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="527d9-151">Ignored.</span></span> <span data-ttu-id="527d9-152">Установите нулевое значение (0).</span><span class="sxs-lookup"><span data-stu-id="527d9-152">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="527d9-153"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**лпблоб**</span><span class="sxs-lookup"><span data-stu-id="527d9-153"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-154">Указатель на структуру [**большого двоичного объекта**](winsock-nsp-reference-links.md) , указывающую на структуру [**пнрпинфо**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) .</span><span class="sxs-lookup"><span data-stu-id="527d9-154">Pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure that points to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure.</span></span> <span data-ttu-id="527d9-155">Необходимо задать определенные параметры в структуре **пнрпинфо** .</span><span class="sxs-lookup"><span data-stu-id="527d9-155">Specific parameters in the **PNRPINFO** structure must be set.</span></span> <span data-ttu-id="527d9-156">Дополнительные сведения см. в следующем разделе структуры **пнрпинфо** .</span><span class="sxs-lookup"><span data-stu-id="527d9-156">For more information, see the following **PNRPINFO** structure section.</span></span>

</dd> </dl>

## <a name="pnrpinfo-structure"></a><span data-ttu-id="527d9-157">Структура ПНРПИНФО</span><span class="sxs-lookup"><span data-stu-id="527d9-157">PNRPINFO Structure</span></span>

<span data-ttu-id="527d9-158">Если задан элемент **лпблоб** структуры [**лпвсакуерисет**](pnrp-and-wsaqueryset.md) , необходимо установить следующие элементы структуры [**пнрпинфо**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) :</span><span class="sxs-lookup"><span data-stu-id="527d9-158">If the **lpBlob** member of the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure is set, the following members of the [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure must be set:</span></span>

<dl> <dt>

<span data-ttu-id="527d9-159"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**двсизе**</span><span class="sxs-lookup"><span data-stu-id="527d9-159"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-160">Задает размер этой структуры.</span><span class="sxs-lookup"><span data-stu-id="527d9-160">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="527d9-161"><span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**лпвсзидентити**</span><span class="sxs-lookup"><span data-stu-id="527d9-161"><span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-162">Указывает идентификатор имени однорангового узла, созданного с помощью [**пиридентитикреате**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).</span><span class="sxs-lookup"><span data-stu-id="527d9-162">Specifies the identity of the peer name that is created by using [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).</span></span> <span data-ttu-id="527d9-163">Если имя однорангового узла не защищено, то удостоверение является необязательным.</span><span class="sxs-lookup"><span data-stu-id="527d9-163">If a peer name is unsecured, then the identity is optional.</span></span> <span data-ttu-id="527d9-164">Если удостоверение указано как **null**, по умолчанию PNRP использует локальное удостоверение компьютера.</span><span class="sxs-lookup"><span data-stu-id="527d9-164">If the identity is specified as **NULL**, PNRP uses the computer local identity—by default.</span></span>

</dd> <dt>

<span data-ttu-id="527d9-165"><span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**нмаксресолве**</span><span class="sxs-lookup"><span data-stu-id="527d9-165"><span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-166">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="527d9-166">Ignored.</span></span> <span data-ttu-id="527d9-167">Установите нулевое значение (0).</span><span class="sxs-lookup"><span data-stu-id="527d9-167">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="527d9-168"><span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**двтимеаут**</span><span class="sxs-lookup"><span data-stu-id="527d9-168"><span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-169">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="527d9-169">Ignored.</span></span> <span data-ttu-id="527d9-170">Установите нулевое значение (0).</span><span class="sxs-lookup"><span data-stu-id="527d9-170">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="527d9-171"><span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**двлифетиме**</span><span class="sxs-lookup"><span data-stu-id="527d9-171"><span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-172">Указывает количество секунд между операциями обновления.</span><span class="sxs-lookup"><span data-stu-id="527d9-172">Specifies the number of seconds between refresh operations.</span></span>

</dd> <dt>

<span data-ttu-id="527d9-173"><span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**енресолвекритериа**</span><span class="sxs-lookup"><span data-stu-id="527d9-173"><span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-174">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="527d9-174">Ignored.</span></span> <span data-ttu-id="527d9-175">Установите нулевое значение (0).</span><span class="sxs-lookup"><span data-stu-id="527d9-175">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="527d9-176"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="527d9-176"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-177">Должно быть либо нулевым (0), **либо \_ подсказкой пнрпинфо**.</span><span class="sxs-lookup"><span data-stu-id="527d9-177">Must be either zero (0) or **PNRPINFO\_HINT**.</span></span> <span data-ttu-id="527d9-178">Значение по умолчанию равно нулю (0).</span><span class="sxs-lookup"><span data-stu-id="527d9-178">The default is zero (0).</span></span> <span data-ttu-id="527d9-179">Это означает, что часть расположения службы в ИДЕНТИФИКАТОРе PNRP строится с помощью IP-адреса в **сахинт**.</span><span class="sxs-lookup"><span data-stu-id="527d9-179">This means that the service location portion of the PNRP ID is built by using the IP address in **saHint**.</span></span> <span data-ttu-id="527d9-180">В противном случае расположение службы строится с помощью первого IP-адреса в первой записи IPv6 члена **лпксабуффер** .</span><span class="sxs-lookup"><span data-stu-id="527d9-180">Otherwise, the service location is built by using the first IP address in the first IPv6 entry of the **lpcsaBuffer** member.</span></span>

</dd> <dt>

<span data-ttu-id="527d9-181"><span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**сахинт**</span><span class="sxs-lookup"><span data-stu-id="527d9-181"><span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**saHint**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-182">Указывает IPv6-адрес для указания.</span><span class="sxs-lookup"><span data-stu-id="527d9-182">Specifies the IPv6 address for the hint.</span></span>

</dd> <dt>

<span data-ttu-id="527d9-183"><span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**еннаместате**</span><span class="sxs-lookup"><span data-stu-id="527d9-183"><span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-184">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="527d9-184">Ignored.</span></span> <span data-ttu-id="527d9-185">Установите нулевое значение (0).</span><span class="sxs-lookup"><span data-stu-id="527d9-185">Set to zero (0).</span></span>

</dd> </dl>

## <a name="unregistering-a-peer-name"></a><span data-ttu-id="527d9-186">Отмена регистрации имени однорангового узла</span><span class="sxs-lookup"><span data-stu-id="527d9-186">Unregistering a Peer Name</span></span>

<span data-ttu-id="527d9-187">В следующем списке приведены важные сведения об отмене регистрации имени однорангового узла.</span><span class="sxs-lookup"><span data-stu-id="527d9-187">The following list identifies the important information about unregistering a peer name.</span></span>

-   <span data-ttu-id="527d9-188">Только приложение, которое регистрирует одноранговое имя, может отменить его регистрацию.</span><span class="sxs-lookup"><span data-stu-id="527d9-188">Only an application that registers a peer name can unregister it.</span></span>
-   <span data-ttu-id="527d9-189">Отмена регистрации имени однорангового узла выполняется автоматически при вызове [**всаклеануп**](winsock-nsp-reference-links.md) .</span><span class="sxs-lookup"><span data-stu-id="527d9-189">A peer name is unregistered automatically if [**WSACleanup**](winsock-nsp-reference-links.md) is called.</span></span>
-   <span data-ttu-id="527d9-190">Протокол PNRP всегда удаляет всю регистрацию имени службы.</span><span class="sxs-lookup"><span data-stu-id="527d9-190">PNRP always removes the entire service name registration.</span></span> <span data-ttu-id="527d9-191">Удаление отдельных адресов не допускается.</span><span class="sxs-lookup"><span data-stu-id="527d9-191">It does not allow removal of individual addresses.</span></span>
-   <span data-ttu-id="527d9-192">При отмене регистрации имени параметр *ессоператион* должен иметь значение **рнрсервице \_ Delete**.</span><span class="sxs-lookup"><span data-stu-id="527d9-192">When unregistering a name, the *essOperation* parameter must have a value of **RNRSERVICE\_DELETE**.</span></span>
-   <span data-ttu-id="527d9-193">PNRP не поддерживает значение **рнрсервице \_ Unregister**.</span><span class="sxs-lookup"><span data-stu-id="527d9-193">PNRP does not support the value **RNRSERVICE\_DEREGISTER**.</span></span>
-   <span data-ttu-id="527d9-194">Параметр *двконтролфлагс* должен быть равен нулю (0).</span><span class="sxs-lookup"><span data-stu-id="527d9-194">The *dwControlFlags* parameter must be zero (0).</span></span>

<span data-ttu-id="527d9-195">При отмене регистрации имени структура [**лпвсакуерисет**](pnrp-and-wsaqueryset.md) , на которую ссылается параметр *лпксрегинфо* , должна содержать следующие значения:</span><span class="sxs-lookup"><span data-stu-id="527d9-195">When unregistering a name, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure that the *lpqsRegInfo* parameter references must contain the following values:</span></span>

<dl> <dt>

<span data-ttu-id="527d9-196"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**двсизе**</span><span class="sxs-lookup"><span data-stu-id="527d9-196"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-197">Задает размер этой структуры.</span><span class="sxs-lookup"><span data-stu-id="527d9-197">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="527d9-198"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**лпсзсервицеинстанценаме**</span><span class="sxs-lookup"><span data-stu-id="527d9-198"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-199">Указывает имя однорангового узла для отмены регистрации.</span><span class="sxs-lookup"><span data-stu-id="527d9-199">Specifies a peer name to unregister.</span></span>

</dd> <dt>

<span data-ttu-id="527d9-200"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**лпсервицеклассид**</span><span class="sxs-lookup"><span data-stu-id="527d9-200"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-201">Должен быть **свЦид \_ пнрпнаме**.</span><span class="sxs-lookup"><span data-stu-id="527d9-201">Must be **SVCID\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="527d9-202"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**лпверсион**</span><span class="sxs-lookup"><span data-stu-id="527d9-202"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-203">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="527d9-203">Ignored.</span></span> <span data-ttu-id="527d9-204">Задайте **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="527d9-204">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="527d9-205"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**лпсзкоммент**</span><span class="sxs-lookup"><span data-stu-id="527d9-205"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-206">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="527d9-206">Ignored.</span></span> <span data-ttu-id="527d9-207">Задайте **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="527d9-207">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="527d9-208"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**двнамеспаце**</span><span class="sxs-lookup"><span data-stu-id="527d9-208"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-209">Должен быть либо **NS \_ пнрпнаме** , либо **NS \_ ALL**.</span><span class="sxs-lookup"><span data-stu-id="527d9-209">Must be either **NS\_PNRPNAME** or **NS\_ALL**.</span></span>

</dd> <dt>

<span data-ttu-id="527d9-210"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**лпнспровидерид**</span><span class="sxs-lookup"><span data-stu-id="527d9-210"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-211">Необходимо указать либо **\_ \_ пнрпнаме Provider** , либо **null**.</span><span class="sxs-lookup"><span data-stu-id="527d9-211">Must be either **NS\_PROVIDER\_PNRPNAME** or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="527d9-212"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**лпсзконтекст**</span><span class="sxs-lookup"><span data-stu-id="527d9-212"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-213">Должно быть именем облака, пустой строкой или **значением NULL**.</span><span class="sxs-lookup"><span data-stu-id="527d9-213">Must be a cloud name, an empty string, or **NULL**.</span></span> <span data-ttu-id="527d9-214">Если это значение равно **null** или является пустой строкой, используется облако по умолчанию Global.</span><span class="sxs-lookup"><span data-stu-id="527d9-214">If this value is **NULL** or an empty string, the default cloud, "Global" is used.</span></span> <span data-ttu-id="527d9-215">В противном случае он должен указывать на допустимое имя облака.</span><span class="sxs-lookup"><span data-stu-id="527d9-215">Otherwise, it must point to a valid cloud name.</span></span>

</dd> <dt>

<span data-ttu-id="527d9-216"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**двнумберофпротоколс**</span><span class="sxs-lookup"><span data-stu-id="527d9-216"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-217">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="527d9-217">Ignored.</span></span> <span data-ttu-id="527d9-218">Установите нулевое значение (0).</span><span class="sxs-lookup"><span data-stu-id="527d9-218">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="527d9-219"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**лпсзкуеристринг**</span><span class="sxs-lookup"><span data-stu-id="527d9-219"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-220">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="527d9-220">Ignored.</span></span> <span data-ttu-id="527d9-221">Задайте **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="527d9-221">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="527d9-222"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**двнумберофксаддрс**</span><span class="sxs-lookup"><span data-stu-id="527d9-222"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-223">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="527d9-223">Ignored.</span></span> <span data-ttu-id="527d9-224">Задайте **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="527d9-224">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="527d9-225"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**лпксабуффер**</span><span class="sxs-lookup"><span data-stu-id="527d9-225"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-226">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="527d9-226">Ignored.</span></span> <span data-ttu-id="527d9-227">Задайте **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="527d9-227">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="527d9-228"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**дваутпутфлагс**</span><span class="sxs-lookup"><span data-stu-id="527d9-228"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-229">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="527d9-229">Ignored.</span></span> <span data-ttu-id="527d9-230">Установите нулевое значение (0).</span><span class="sxs-lookup"><span data-stu-id="527d9-230">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="527d9-231"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**лпблоб**</span><span class="sxs-lookup"><span data-stu-id="527d9-231"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="527d9-232">Указатель на структуру [**большого двоичного объекта**](winsock-nsp-reference-links.md) , указывающую на структуру [**пнрпинфо**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) .</span><span class="sxs-lookup"><span data-stu-id="527d9-232">Pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure that points to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure.</span></span> <span data-ttu-id="527d9-233">Элемент **лпсзидентити** структуры **лпблоб** определяет имя удостоверения, которое используется для регистрации имени однорангового узла.</span><span class="sxs-lookup"><span data-stu-id="527d9-233">The **lpszIdentity** member of the **lpBlob** structure identifies the name of the identity that is used to register a peer name.</span></span> <span data-ttu-id="527d9-234">Остальные элементы должны иметь те же значения, которые используются при регистрации имени.</span><span class="sxs-lookup"><span data-stu-id="527d9-234">The remaining members must be set to the same values that are used when registering a name.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="527d9-235">См. также</span><span class="sxs-lookup"><span data-stu-id="527d9-235">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="527d9-236">PNRP и BLOB-объект</span><span class="sxs-lookup"><span data-stu-id="527d9-236">PNRP and BLOB</span></span>](pnrp-and-blob.md)
</dt> <dt>

[<span data-ttu-id="527d9-237">PNRP и ВСАКУЕРИСЕТ</span><span class="sxs-lookup"><span data-stu-id="527d9-237">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)
</dt> <dt>

[<span data-ttu-id="527d9-238">**пнрпинфо**</span><span class="sxs-lookup"><span data-stu-id="527d9-238">**PNRPINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[<span data-ttu-id="527d9-239">Коды ошибок PNRP NSP</span><span class="sxs-lookup"><span data-stu-id="527d9-239">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> <dt>

[<span data-ttu-id="527d9-240">**всаклеануп**</span><span class="sxs-lookup"><span data-stu-id="527d9-240">**WSACleanup**</span></span>](winsock-nsp-reference-links.md)
</dt> <dt>

<span data-ttu-id="527d9-241">**всасетсервице**</span><span class="sxs-lookup"><span data-stu-id="527d9-241">**WSASetService**</span></span>
</dt> </dl>

 

 



