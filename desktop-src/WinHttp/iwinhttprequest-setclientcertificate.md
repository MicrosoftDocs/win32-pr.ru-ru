---
description: Выбирает сертификат клиента для отправки на HTTPS-сервер.
ms.assetid: e76f1e76-5efe-46f2-9a21-064aa06fb3a8
title: 'Метод Ивинхттпрекуест:: Сетклиентцертификате'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetClientCertificate
- WinHttpRequest.SetClientCertificate
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 0b346451e87b62116d7202b476e554c84604ea48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347205"
---
# <a name="iwinhttprequestsetclientcertificate-method"></a><span data-ttu-id="55a50-103">Метод Ивинхттпрекуест:: Сетклиентцертификате</span><span class="sxs-lookup"><span data-stu-id="55a50-103">IWinHttpRequest::SetClientCertificate method</span></span>

<span data-ttu-id="55a50-104">Метод **сетклиентцертификате** выбирает сертификат клиента для отправки на HTTPS-сервер.</span><span class="sxs-lookup"><span data-stu-id="55a50-104">The **SetClientCertificate** method selects a client certificate to send to a Secure Hypertext Transfer Protocol (HTTPS) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="55a50-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55a50-105">Syntax</span></span>


```C++
HRESULT SetClientCertificate(
  [in] BSTR ClientCertificate
);
```



## <a name="parameters"></a><span data-ttu-id="55a50-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="55a50-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55a50-107">*Clientcertificate* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="55a50-107">*ClientCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55a50-108">Указывает расположение, [*хранилище сертификатов*](glossary.md)и субъект сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="55a50-108">Specifies the location, [*certificate store*](glossary.md), and subject of a client certificate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55a50-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="55a50-109">Return value</span></span>

<span data-ttu-id="55a50-110">В случае успешного выполнения возвращается значение **S \_** , а в противном случае — значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="55a50-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="55a50-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55a50-111">Remarks</span></span>

<span data-ttu-id="55a50-112">Строка, указанная в параметре *clientcertificate* , состоит из расположения сертификата, хранилища сертификатов и имени субъекта, разделенных символами обратной косой черты.</span><span class="sxs-lookup"><span data-stu-id="55a50-112">The string specified in the *ClientCertificate* parameter consists of the certificate location, certificate store, and subject name delimited by backslashes.</span></span> <span data-ttu-id="55a50-113">Дополнительные сведения о компонентах строки сертификата см. в разделе [Client Certificates](ssl-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="55a50-113">For more information about the components of the certificate string, see [Client Certificates](ssl-in-winhttp.md).</span></span>

<span data-ttu-id="55a50-114">Имя и расположение хранилища сертификатов являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="55a50-114">The certificate store name and location are optional.</span></span> <span data-ttu-id="55a50-115">Однако если указать хранилище сертификатов, необходимо также указать расположение этого хранилища сертификатов.</span><span class="sxs-lookup"><span data-stu-id="55a50-115">However, if you specify a certificate store, you must also specify the location of that certificate store.</span></span> <span data-ttu-id="55a50-116">Расположение по умолчанию — текущий \_ пользователь, а хранилище сертификатов по умолчанию — "My".</span><span class="sxs-lookup"><span data-stu-id="55a50-116">The default location is CURRENT\_USER and the default certificate store is "MY".</span></span> <span data-ttu-id="55a50-117">Пустой субъект указывает, что следует использовать первый сертификат в хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="55a50-117">A blank subject indicates that the first certificate in the certificate store should be used.</span></span>

<span data-ttu-id="55a50-118">Вызовите **сетклиентцертификате** , чтобы выбрать сертификат перед вызовом [**Send**](iwinhttprequest-send.md) для отправки запроса.</span><span class="sxs-lookup"><span data-stu-id="55a50-118">Call **SetClientCertificate** to select a certificate before calling [**Send**](iwinhttprequest-send.md) to send the request.</span></span>

<span data-ttu-id="55a50-119">Службы Microsoft Windows HTTP Services (WinHTTP) не предоставляют сертификаты клиента прокси-серверам, запрашивающим сертификаты для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="55a50-119">Microsoft Windows HTTP Services (WinHTTP) does not provide client certificates to proxy servers that request certificates for authentication.</span></span>

> [!Note]  
> <span data-ttu-id="55a50-120">Для Windows XP и Windows 2000 см. раздел [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="55a50-120">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="55a50-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="55a50-121">Examples</span></span>

<span data-ttu-id="55a50-122">В следующем примере скрипта показано, как выбрать сертификат клиента для отправки с запросом.</span><span class="sxs-lookup"><span data-stu-id="55a50-122">The following scripting example shows how to select a client certificate to send with a request.</span></span> <span data-ttu-id="55a50-123">Сертификат с темой "мой Middle-Tier сертификат" выбирается из хранилища сертификатов "Личное" в реестре в разделе **hKey \_ локальный \_ компьютер**.</span><span class="sxs-lookup"><span data-stu-id="55a50-123">A certificate with the subject "My Middle-Tier Certificate" is chosen from the "Personal" certificate store in the registry under **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="55a50-124">Поскольку этот пример кода характерен для Microsoft JScript, который использует обратную косую черту в качестве escape-символа, для разделения компонентов строки сертификата должны использоваться две смежные обратные косые черты.</span><span class="sxs-lookup"><span data-stu-id="55a50-124">Because this code example is specific to Microsoft JScript, which uses the backslash as an escape character, two adjacent backslashes are required to delimit components of the certificate string.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var HttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
    
// Open an HTTP connection.
HttpReq.Open("GET", "https://www.fabrikam.com/", false);
    
// Select a client certificate.
HttpReq.SetClientCertificate(
            "LOCAL_MACHINE\\Personal\\My Middle-Tier Certificate");

// Send the HTTP Request.
HttpReq.Send();
```



## <a name="requirements"></a><span data-ttu-id="55a50-125">Требования</span><span class="sxs-lookup"><span data-stu-id="55a50-125">Requirements</span></span>



| <span data-ttu-id="55a50-126">Требование</span><span class="sxs-lookup"><span data-stu-id="55a50-126">Requirement</span></span> | <span data-ttu-id="55a50-127">Значение</span><span class="sxs-lookup"><span data-stu-id="55a50-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="55a50-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55a50-128">Minimum supported client</span></span><br/> | <span data-ttu-id="55a50-129">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="55a50-129">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="55a50-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55a50-130">Minimum supported server</span></span><br/> | <span data-ttu-id="55a50-131">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="55a50-131">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="55a50-132">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="55a50-132">Redistributable</span></span><br/>          | <span data-ttu-id="55a50-133">WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="55a50-133">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="55a50-134">IDL</span><span class="sxs-lookup"><span data-stu-id="55a50-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="55a50-135"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="55a50-135"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="55a50-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="55a50-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="55a50-137"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55a50-137"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="55a50-138">DLL</span><span class="sxs-lookup"><span data-stu-id="55a50-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55a50-139"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55a50-139"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="55a50-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55a50-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55a50-141">**ивинхттпрекуест**</span><span class="sxs-lookup"><span data-stu-id="55a50-141">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="55a50-142">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="55a50-142">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="55a50-143">SSL в WinHTTP</span><span class="sxs-lookup"><span data-stu-id="55a50-143">SSL in WinHTTP</span></span>](ssl-in-winhttp.md)
</dt> <dt>

[<span data-ttu-id="55a50-144">Версии WinHTTP</span><span class="sxs-lookup"><span data-stu-id="55a50-144">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




