---
description: Запрашивает конечную точку, используемую для подключения к службе.
ms.assetid: 4C02EA78-AD77-42CD-B94F-C8C3ED26CB4C
title: 'Метод Иупдатиндпоинтпровидер:: Жетсервицеендпоинт (Упдатиндпоинтаус. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointProvider.GetServiceEndpoint
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: bddb77237d6d5edabab41eefe1931514fd6aed42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682762"
---
# <a name="iupdateendpointprovidergetserviceendpoint-method"></a><span data-ttu-id="caf3c-103">Метод Иупдатиндпоинтпровидер:: Жетсервицеендпоинт</span><span class="sxs-lookup"><span data-stu-id="caf3c-103">IUpdateEndpointProvider::GetServiceEndpoint method</span></span>

<span data-ttu-id="caf3c-104">Запрашивает конечную точку, используемую для подключения к службе.</span><span class="sxs-lookup"><span data-stu-id="caf3c-104">Requests an endpoint that is used to connect to a service.</span></span>

## <a name="syntax"></a><span data-ttu-id="caf3c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="caf3c-105">Syntax</span></span>


```C++
HRESULT GetServiceEndpoint(
  [in]  GUID                        ServiceId,
  [in]  UpdateEndpointType          endpointType,
  [in]  UpdateEndpointProxySettings proxySettings,
  [in]  HANDLE_PTR                  hUserToken,
  [in]  BOOL                        fRefreshOnline,
  [out] BSTR                        *pbstrEndpointLoc
);
```



## <a name="parameters"></a><span data-ttu-id="caf3c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="caf3c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="caf3c-107">*ServiceId* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="caf3c-107">*ServiceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="caf3c-108">Определяет обновляемую службу.</span><span class="sxs-lookup"><span data-stu-id="caf3c-108">Identifies the service to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="caf3c-109">*endpointType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="caf3c-109">*endpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="caf3c-110">Определяет тип конечной точки, реализуемой службой.</span><span class="sxs-lookup"><span data-stu-id="caf3c-110">Identifies the type of endpoint implemented by the service.</span></span>

<span data-ttu-id="caf3c-111">Перечисление [**упдатиндпоинттипе**](updateendpointtype.md) определяет следующие константы.</span><span class="sxs-lookup"><span data-stu-id="caf3c-111">The [**UpdateEndpointType**](updateendpointtype.md) enumeration defines the following constants.</span></span>

<dt>

<span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>

<span data-ttu-id="caf3c-112"><span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**уетклиентсервер**</span><span class="sxs-lookup"><span data-stu-id="caf3c-112"><span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**</span></span>


</dt> <dd>

<span data-ttu-id="caf3c-113">Конечная точка клиент-сервер, которая используется для подключения к службе обновления.</span><span class="sxs-lookup"><span data-stu-id="caf3c-113">A client-server endpoint that is used to connect to the update service.</span></span>

</dd> <dt>

<span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>

<span data-ttu-id="caf3c-114"><span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**уетрепортинг**</span><span class="sxs-lookup"><span data-stu-id="caf3c-114"><span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**</span></span>


</dt> <dd>

<span data-ttu-id="caf3c-115">Конечная точка отчетов, используемая, когда клиент сообщает о результатах проверок, скачивается и устанавливается обратно в службу обновления.</span><span class="sxs-lookup"><span data-stu-id="caf3c-115">A Reporting endpoint that is used used when the client reports the results of scans, downloads, and installs back to the update service</span></span>

</dd> <dt>

<span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>

<span data-ttu-id="caf3c-116"><span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**уетвуаселфупдате**</span><span class="sxs-lookup"><span data-stu-id="caf3c-116"><span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**</span></span>


</dt> <dd>

<span data-ttu-id="caf3c-117">Self-Updateая конечная точка, используемая, когда клиентский компьютер обращается к службе обновления, чтобы узнать, существует ли новая версия клиентского программного обеспечения агента Центр обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="caf3c-117">A Self-Update endpoint that is used when the client computer contacts an update service to see whether there is a new version of the Windows Update Agent client software.</span></span>

</dd> <dt>

<span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>

<span data-ttu-id="caf3c-118"><span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**уетрегулатион**</span><span class="sxs-lookup"><span data-stu-id="caf3c-118"><span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**</span></span>


</dt> <dd>

<span data-ttu-id="caf3c-119">Регулируемая конечная точка, используемая, когда клиентский компьютер обращается к регламентированной службе для работы с определенным обновлением, применимым к целевому компьютеру.</span><span class="sxs-lookup"><span data-stu-id="caf3c-119">A Regulation endpoint that is used when the client computer contacts the regulation service to act on a particular update that is applicable to the target computer.</span></span>

</dd> <dt>

<span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>

<span data-ttu-id="caf3c-120"><span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**уетсимплетаржетинг**</span><span class="sxs-lookup"><span data-stu-id="caf3c-120"><span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**</span></span>


</dt> <dd>

<span data-ttu-id="caf3c-121">Simple-Targeting ендоинт, используемый только с частными службами (WSUS-серверы в корпоративных средах).</span><span class="sxs-lookup"><span data-stu-id="caf3c-121">A Simple-Targeting endoint that is used only with private services (WSUS servers in corporate environments).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="caf3c-122">*проксисеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="caf3c-122">*proxySettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="caf3c-123">Определяет параметры, используемые при соединении с прокси-сервером.</span><span class="sxs-lookup"><span data-stu-id="caf3c-123">Identifies the settings that are used when connecting to a proxy server.</span></span>

</dd> <dt>

<span data-ttu-id="caf3c-124">*хусертокен* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="caf3c-124">*hUserToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="caf3c-125">Содержит объект обработчика маркера, который представляет пользователя.</span><span class="sxs-lookup"><span data-stu-id="caf3c-125">Contains a token handle object that represents the user.</span></span> <span data-ttu-id="caf3c-126">Поставщик конечной точки использует этот токен для определения параметров прокси-сервера и учетных данных для использования.</span><span class="sxs-lookup"><span data-stu-id="caf3c-126">The endpoint provider uses this token to determine which proxy settings and credentials to use.</span></span>

</dd> <dt>

<span data-ttu-id="caf3c-127">*фрефрешонлине* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="caf3c-127">*fRefreshOnline* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="caf3c-128">Указывает, что погода WUA запрашивает новый маркер.</span><span class="sxs-lookup"><span data-stu-id="caf3c-128">Indicates weather WUA requests a new token.</span></span> <span data-ttu-id="caf3c-129">Значение true указывает, что запрашивается новый маркер.</span><span class="sxs-lookup"><span data-stu-id="caf3c-129">True indicates that a new token is requested.</span></span> <span data-ttu-id="caf3c-130">Значение false указывает, что запрошен новый или кэшированный токен.</span><span class="sxs-lookup"><span data-stu-id="caf3c-130">False indicates that a new or cached token is requested.</span></span> <span data-ttu-id="caf3c-131">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="caf3c-131">See Remarks for more information.</span></span>

</dd> <dt>

<span data-ttu-id="caf3c-132">*пбстрендпоинтлок* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="caf3c-132">*pbstrEndpointLoc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="caf3c-133">Укажите URL-адрес, используемый для взаимодействия со службой.</span><span class="sxs-lookup"><span data-stu-id="caf3c-133">Specify the URL used to communicate with the service.</span></span> <span data-ttu-id="caf3c-134">Например, для конечной точки клеинт-Server это будет URL-адрес службы клиентского сервера.</span><span class="sxs-lookup"><span data-stu-id="caf3c-134">For example, for a cleint-server endpoint this would be the URL to the client server service.</span></span> <span data-ttu-id="caf3c-135">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="caf3c-135">See Remarks for more information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="caf3c-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="caf3c-136">Return value</span></span>

<span data-ttu-id="caf3c-137">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="caf3c-137">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="caf3c-138">В противном случае возвращает код ошибки COM или Windows.</span><span class="sxs-lookup"><span data-stu-id="caf3c-138">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="caf3c-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="caf3c-139">Remarks</span></span>

<span data-ttu-id="caf3c-140">WUA обычно задает для параметра *фрефрешонлине* значение false при первом вызове этого метода, а затем при возникновении ошибки подключения WUA устанавливает для параметра значение true при повторном вызове метода.</span><span class="sxs-lookup"><span data-stu-id="caf3c-140">WUA typically sets the *fRefreshOnline* parameter to false when this method is first called, then if a connection error occures WUA sets that parameter to true when the method is called again.</span></span> <span data-ttu-id="caf3c-141">Однако реализация этого метода может запросить новый маркер из службы маркеров безопасности (STS) или предоставить кэшированный маркер в любое время.</span><span class="sxs-lookup"><span data-stu-id="caf3c-141">However, the implementation of this method can request a new token from a Security Token Service (STS) or provide a cached token at any time.</span></span>

<span data-ttu-id="caf3c-142">Если для конечной точки не требуется проверка подлинности, вызывающий объект может подключиться к службе, используя только URL-адрес, указанный параметром *пбстрендпоинтлок* .</span><span class="sxs-lookup"><span data-stu-id="caf3c-142">If the endpoint does not need authentication, then the caller can connect to the service using only the URL specified by the *pbstrEndpointLoc* parameter.</span></span>

<span data-ttu-id="caf3c-143">Если для конечной точки требуется проверка подлинности, вызывающий объект может использовать URL-адрес, заданный параметром *пбстрендпоинтлок* , и данные, предоставленные другими параметрами.</span><span class="sxs-lookup"><span data-stu-id="caf3c-143">If the endpoint does need authentication, then the caller can use the URL specified by the *pbstrEndpointLoc* parameter and the data provided by the other parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="caf3c-144">Требования</span><span class="sxs-lookup"><span data-stu-id="caf3c-144">Requirements</span></span>



| <span data-ttu-id="caf3c-145">Требование</span><span class="sxs-lookup"><span data-stu-id="caf3c-145">Requirement</span></span> | <span data-ttu-id="caf3c-146">Значение</span><span class="sxs-lookup"><span data-stu-id="caf3c-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caf3c-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="caf3c-147">Minimum supported client</span></span><br/> | <span data-ttu-id="caf3c-148">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="caf3c-148">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="caf3c-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="caf3c-149">Minimum supported server</span></span><br/> | <span data-ttu-id="caf3c-150">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="caf3c-150">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="caf3c-151">Header</span><span class="sxs-lookup"><span data-stu-id="caf3c-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="caf3c-152"><dt>Упдатиндпоинтаус. h</dt></span><span class="sxs-lookup"><span data-stu-id="caf3c-152"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="caf3c-153">IDL</span><span class="sxs-lookup"><span data-stu-id="caf3c-153">IDL</span></span><br/>                      | <dl> <span data-ttu-id="caf3c-154"><dt>Упдатиндпоинтаус. idl</dt></span><span class="sxs-lookup"><span data-stu-id="caf3c-154"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="caf3c-155">Библиотека</span><span class="sxs-lookup"><span data-stu-id="caf3c-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="caf3c-156"><dt>Упдатиндпоинтаус. lib</dt></span><span class="sxs-lookup"><span data-stu-id="caf3c-156"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="caf3c-157">DLL</span><span class="sxs-lookup"><span data-stu-id="caf3c-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="caf3c-158"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="caf3c-158"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="caf3c-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="caf3c-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caf3c-160">**иупдатиндпоинтпровидер**</span><span class="sxs-lookup"><span data-stu-id="caf3c-160">**IUpdateEndpointProvider**</span></span>](iupdateendpointprovider.md)
</dt> </dl>

 

 




