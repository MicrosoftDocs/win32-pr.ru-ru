---
description: Задает учетные данные для использования с HTTP-сервером, будь то прокси-сервер или исходный сервер.
ms.assetid: d96c6e76-92b8-4ad7-8ca7-a9acbed523ff
title: 'Метод Ивинхттпрекуест:: Сеткредентиалс'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetCredentials
- WinHttpRequest.SetCredentials
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 46b0dfb321763a3b3bfe622e116f2e76c5e59423
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712201"
---
# <a name="iwinhttprequestsetcredentials-method"></a><span data-ttu-id="249a8-103">Метод Ивинхттпрекуест:: Сеткредентиалс</span><span class="sxs-lookup"><span data-stu-id="249a8-103">IWinHttpRequest::SetCredentials method</span></span>

<span data-ttu-id="249a8-104">Метод **сеткредентиалс** задает учетные данные для использования с сервером HTTP, будь то прокси-сервер или исходный сервер.</span><span class="sxs-lookup"><span data-stu-id="249a8-104">The **SetCredentials** method sets credentials to be used with an HTTP server, whether it is a proxy server or an originating server.</span></span>

## <a name="syntax"></a><span data-ttu-id="249a8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="249a8-105">Syntax</span></span>


```C++
HRESULT SetCredentials(
  [in] BSTR                             UserName,
  [in] BSTR                             Password,
  [in] HTTPREQUEST_SETCREDENTIALS_FLAGS Flags
);
```



## <a name="parameters"></a><span data-ttu-id="249a8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="249a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="249a8-107">*Имя пользователя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="249a8-107">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="249a8-108">Указывает имя пользователя для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="249a8-108">Specifies the user name for authentication.</span></span>

</dd> <dt>

<span data-ttu-id="249a8-109">*Пароль* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="249a8-109">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="249a8-110">Указывает пароль для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="249a8-110">Specifies the password for authentication.</span></span> <span data-ttu-id="249a8-111">Этот параметр пропускается, если *бструсернаме* имеет **значение NULL** или отсутствует.</span><span class="sxs-lookup"><span data-stu-id="249a8-111">This parameter is ignored if *bstrUserName* is **NULL** or missing.</span></span>

</dd> <dt>

<span data-ttu-id="249a8-112">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="249a8-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="249a8-113">Указывает, когда [**ивинхттпрекуест**](iwinhttprequest-interface.md) использует учетные данные.</span><span class="sxs-lookup"><span data-stu-id="249a8-113">Specifies when [**IWinHttpRequest**](iwinhttprequest-interface.md) uses credentials.</span></span> <span data-ttu-id="249a8-114">Может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="249a8-114">Can be one of the following values.</span></span>



| <span data-ttu-id="249a8-115">Значение</span><span class="sxs-lookup"><span data-stu-id="249a8-115">Value</span></span>                                                                                                               | <span data-ttu-id="249a8-116">Значение</span><span class="sxs-lookup"><span data-stu-id="249a8-116">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="249a8-117"><dt>HTTPREQUEST \_ сеткредентиалс \_ для \_ сервера</dt></span><span class="sxs-lookup"><span data-stu-id="249a8-117"><dt>HTTPREQUEST\_SETCREDENTIALS\_FOR\_SERVER</dt></span></span> </dl> | <span data-ttu-id="249a8-118">Учетные данные передаются на сервер.</span><span class="sxs-lookup"><span data-stu-id="249a8-118">Credentials are passed to a server.</span></span><br/> |
| <dl> <span data-ttu-id="249a8-119"><dt>HTTPREQUEST \_ сеткредентиалс \_ для \_ прокси-сервера</dt></span><span class="sxs-lookup"><span data-stu-id="249a8-119"><dt>HTTPREQUEST\_SETCREDENTIALS\_FOR\_PROXY</dt></span></span> </dl>  | <span data-ttu-id="249a8-120">Учетные данные передаются прокси-серверу.</span><span class="sxs-lookup"><span data-stu-id="249a8-120">Credentials are passed to a proxy.</span></span><br/>  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="249a8-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="249a8-121">Return value</span></span>

<span data-ttu-id="249a8-122">В случае успешного выполнения возвращается значение **S \_** , а в противном случае — значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="249a8-122">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="249a8-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="249a8-123">Remarks</span></span>

<span data-ttu-id="249a8-124">Этот метод возвращает значение ошибки, если вызов метода [**Open**](iwinhttprequest-open.md) не завершился успешно.</span><span class="sxs-lookup"><span data-stu-id="249a8-124">This method returns an error value if a call to [**Open**](iwinhttprequest-open.md) has not completed successfully.</span></span> <span data-ttu-id="249a8-125">Предполагается, что некоторые меры взаимодействия с прокси-сервером или исходным сервером должны быть выполнены до того, как пользователи смогут задать учетные данные для сеанса.</span><span class="sxs-lookup"><span data-stu-id="249a8-125">It is assumed that some measure of interaction with a proxy server or origin server must occur before users can set credentials for the session.</span></span> <span data-ttu-id="249a8-126">Более того, пока пользователи не узнают, какие схемы проверки подлинности поддерживаются, они не могут отформатировать учетные данные.</span><span class="sxs-lookup"><span data-stu-id="249a8-126">Moreover, until users know which authentication scheme(s) are supported, they cannot format the credentials.</span></span>

> [!Note]  
> <span data-ttu-id="249a8-127">Для Windows XP и Windows 2000 см. раздел [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="249a8-127">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

<span data-ttu-id="249a8-128">Чтобы выполнить аутентификацию как на сервере, так и на прокси, приложение должно вызвать **сеткредентиалс** дважды. сначала с параметром *flags* , имеющим значение **HttpRequest \_ сеткредентиалс \_ для \_ Server**, и во-вторых, параметр *flags* имеет значение **HttpRequest \_ сеткредентиалс \_ для \_ proxy**.</span><span class="sxs-lookup"><span data-stu-id="249a8-128">To authenticate with both the server and the proxy, the application must call **SetCredentials** twice; first with the *Flags* parameter set to **HTTPREQUEST\_SETCREDENTIALS\_FOR\_SERVER**, and second, with the *Flags* parameter set to **HTTPREQUEST\_SETCREDENTIALS\_FOR\_PROXY**.</span></span>

## <a name="examples"></a><span data-ttu-id="249a8-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="249a8-129">Examples</span></span>

<span data-ttu-id="249a8-130">В следующем примере показано, как открыть HTTP-соединение, задать учетные данные для сервера, отправить HTTP-запрос и прочитать текст ответа.</span><span class="sxs-lookup"><span data-stu-id="249a8-130">The following example shows how to open an HTTP connection, set credentials for the server, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="249a8-131">Этот пример необходимо запустить из командной строки.</span><span class="sxs-lookup"><span data-stu-id="249a8-131">This example must be run from a command prompt.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <objbase.h>

#include "httprequest.h"

#pragma comment(lib, "ole32.lib")
#pragma comment(lib, "oleaut32.lib")

// IID for IWinHttpRequest.
const IID IID_IWinHttpRequest =
{
  0x06f29373,
  0x5c5a,
  0x4b54,
  {0xb0, 0x25, 0x6e, 0xf1, 0xbf, 0x8a, 0xbf, 0x0e}
};

int main()
{
    // Variable for return value
    HRESULT    hr;

    // Initialize COM.
    hr = CoInitialize( NULL );

    IWinHttpRequest *  pIWinHttpRequest = NULL;

    BSTR            bstrResponse = NULL;
    VARIANT         varFalse;
    VARIANT         varEmpty;

    CLSID           clsid;

    VariantInit(&varFalse);
    V_VT(&varFalse)   = VT_BOOL;
    V_BOOL(&varFalse) = VARIANT_FALSE;

    VariantInit(&varEmpty);
    V_VT(&varEmpty) = VT_ERROR;

    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IWinHttpRequest,
                              (void **)&pIWinHttpRequest);
    }
    if (SUCCEEDED(hr))
    {    // Open WinHttpRequest.
        BSTR bstrMethod = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Set Credentials.
        BSTR bstrUserName = SysAllocString(L"User Name");
        BSTR bstrPassword = SysAllocString(L"Password");
        hr = pIWinHttpRequest->SetCredentials(
                               bstrUserName,
                               bstrPassword,
                               HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);
        SysFreeString(bstrUserName);
        SysFreeString(bstrPassword);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Get Response text.
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
    }
    if (SUCCEEDED(hr))
    {    // Print response to console.
        wprintf(L"%.256s",bstrResponse);
    }

    // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
    if (bstrResponse)
        SysFreeString(bstrResponse);

    CoUninitialize();
    return 0;
}

```



<span data-ttu-id="249a8-132">В следующем примере скрипта показано, как открыть HTTP-соединение, задать учетные данные для сервера, задать учетные данные для прокси-сервера, если он используется, отправить HTTP-запрос и прочитать текст ответа.</span><span class="sxs-lookup"><span data-stu-id="249a8-132">The following scripting example shows how to open an HTTP connection, set credentials for the server, set credentials for a proxy if one is used, send an HTTP request, and read the response text.</span></span>


```JScript
// HttpRequest SetCredentials flags
HTTPREQUEST_SETCREDENTIALS_FOR_SERVER = 0;
HTTPREQUEST_SETCREDENTIALS_FOR_PROXY = 1;

// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Specify the target resource.
var targURL = "https://msdn.microsoft.com/downloads/samples/"+
              "internet/winhttp/auth/authenticate.asp";    
WinHttpReq.open("GET", targURL, false);

var Done = false;
var LastStatus=0;
do {
    // Send a request to the server and wait for a response.                               
    WinHttpReq.send(); 
    
    // Obtain the status code from the response.
    var Status = WinHttpReq.Status;

    switch (Status){
        // A 200 status indicates that the resource was retrieved.
        case 200:
            Done = true;
            break;
                
        // A 401 status indicates that the server 
        // requires authentication.    
        case 401:
            WScript.Echo("Requires Server UserName and Password.");

            // Specify the target resource.
            WinHttpReq.open("GET", targURL, false);
                            
            // Set credentials for the server.
            WinHttpReq.SetCredentials("User Name", "Password", 
                        HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);

            // If the same credentials are requested twice, abort 
            // the request.  For simplicity, this sample does not 
            // check for a repeated sequence of status codes.
            if (LastStatus==401)
                Done = true;
            break;

        // A 407 status indicates that the proxy 
        // requires authentication.    
        case 407:
            WScript.Echo("Requires Proxy UserName and Password.");
                
            // Specify the target resource.
            WinHttpReq.open("GET", targURL, false);
    
            // Set credentials for the proxy.
            WinHttpReq.SetCredentials("User Name", "Password", 
                HTTPREQUEST_SETCREDENTIALS_FOR_PROXY);

            // If the same credentials are requested twice, abort 
            // the request.  For simplicity, this sample does not 
            // check for a repeated sequence of status codes.
            if (LastStatus==407)
                Done = true;
            break;
        
        // Any other status is unexpected.
        default:
            WScript.Echo("Unexpected Status: "+Status);
            Done = true;
            break;
    }
    
    // Keep track of the last status code.
    LastStatus = Status;
    
} while (!Done);

// Display the results of the request.
WScript.Echo(WinHttpReq.Status + "   " + WinHttpReq.StatusText);
WScript.Echo(WinHttpReq.GetAllResponseHeaders());
```



## <a name="requirements"></a><span data-ttu-id="249a8-133">Требования</span><span class="sxs-lookup"><span data-stu-id="249a8-133">Requirements</span></span>



| <span data-ttu-id="249a8-134">Требование</span><span class="sxs-lookup"><span data-stu-id="249a8-134">Requirement</span></span> | <span data-ttu-id="249a8-135">Значение</span><span class="sxs-lookup"><span data-stu-id="249a8-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="249a8-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="249a8-136">Minimum supported client</span></span><br/> | <span data-ttu-id="249a8-137">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="249a8-137">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="249a8-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="249a8-138">Minimum supported server</span></span><br/> | <span data-ttu-id="249a8-139">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="249a8-139">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="249a8-140">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="249a8-140">Redistributable</span></span><br/>          | <span data-ttu-id="249a8-141">WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="249a8-141">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="249a8-142">IDL</span><span class="sxs-lookup"><span data-stu-id="249a8-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="249a8-143"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="249a8-143"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="249a8-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="249a8-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="249a8-145"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="249a8-145"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="249a8-146">DLL</span><span class="sxs-lookup"><span data-stu-id="249a8-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="249a8-147"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="249a8-147"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="249a8-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="249a8-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="249a8-149">**ивинхттпрекуест**</span><span class="sxs-lookup"><span data-stu-id="249a8-149">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="249a8-150">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="249a8-150">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="249a8-151">Версии WinHTTP</span><span class="sxs-lookup"><span data-stu-id="249a8-151">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




