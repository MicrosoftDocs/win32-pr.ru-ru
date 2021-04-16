---
description: Задает текущую политику автоматического входа в систему.
ms.assetid: bc8e8c9c-574e-4392-b336-2c06947022ee
title: 'Метод Ивинхттпрекуест:: Сетаутологонполици'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetAutoLogonPolicy
- WinHttpRequest.SetAutoLogonPolicy
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: cad8bd0080d10a1395a0a9d275951ff961a60bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712549"
---
# <a name="iwinhttprequestsetautologonpolicy-method"></a><span data-ttu-id="0712f-103">Метод Ивинхттпрекуест:: Сетаутологонполици</span><span class="sxs-lookup"><span data-stu-id="0712f-103">IWinHttpRequest::SetAutoLogonPolicy method</span></span>

<span data-ttu-id="0712f-104">Метод **сетаутологонполици** задает текущую [политику автоматического входа в систему](authentication-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="0712f-104">The **SetAutoLogonPolicy** method sets the current [Automatic Logon Policy](authentication-in-winhttp.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0712f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0712f-105">Syntax</span></span>


```C++
HRESULT SetAutoLogonPolicy(
  [in] WinHttpRequestAutoLogonPolicy AutoLogonPolicy
);
```



## <a name="parameters"></a><span data-ttu-id="0712f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0712f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0712f-107">*Аутологонполици* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0712f-107">*AutoLogonPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0712f-108">Указывает текущую политику автоматического входа в систему.</span><span class="sxs-lookup"><span data-stu-id="0712f-108">Specifies the current automatic logon policy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0712f-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0712f-109">Return value</span></span>

<span data-ttu-id="0712f-110">В случае успешного выполнения возвращается значение **S \_** , а в противном случае — значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="0712f-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0712f-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0712f-111">Remarks</span></span>

<span data-ttu-id="0712f-112">Политика по умолчанию — [**аутологонполици \_ онлифбипасспрокси**](winhttprequestautologonpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="0712f-112">The default policy is [**AutoLogonPolicy\_OnlyIfBypassProxy**](winhttprequestautologonpolicy.md).</span></span>

<span data-ttu-id="0712f-113">Вызовите **сетаутологонполици** , чтобы задать политику автоматического входа перед вызовом [**Send**](iwinhttprequest-send.md) для отправки запроса.</span><span class="sxs-lookup"><span data-stu-id="0712f-113">Call **SetAutoLogonPolicy** to set the automatic logon policy before calling [**Send**](iwinhttprequest-send.md) to send the request.</span></span>

> [!Note]  
> <span data-ttu-id="0712f-114">Для Windows XP и Windows 2000 см. раздел [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="0712f-114">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="0712f-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="0712f-115">Examples</span></span>

<span data-ttu-id="0712f-116">В следующем примере скрипта показано, как настроить автоматическую проверку подлинности для автоматического использования NTLM или согласования аутентификации.</span><span class="sxs-lookup"><span data-stu-id="0712f-116">The following scripting example shows how to set the automatic logon policy to never use NTLM or Negotiate authentication automatically.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var HttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
    
// Open an HTTP connection.
HttpReq.Open("GET", "https://www.fabrikam.com/", false);
    
// Do not automatically send user credentials.
HttpReq.SetAutoLogonPolicy(2);

// Send the HTTP Request.
HttpReq.Send();
```



## <a name="requirements"></a><span data-ttu-id="0712f-117">Требования</span><span class="sxs-lookup"><span data-stu-id="0712f-117">Requirements</span></span>



| <span data-ttu-id="0712f-118">Требование</span><span class="sxs-lookup"><span data-stu-id="0712f-118">Requirement</span></span> | <span data-ttu-id="0712f-119">Значение</span><span class="sxs-lookup"><span data-stu-id="0712f-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="0712f-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0712f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0712f-121">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0712f-121">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="0712f-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0712f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0712f-123">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0712f-123">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="0712f-124">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="0712f-124">Redistributable</span></span><br/>          | <span data-ttu-id="0712f-125">WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="0712f-125">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="0712f-126">IDL</span><span class="sxs-lookup"><span data-stu-id="0712f-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0712f-127"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0712f-127"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="0712f-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0712f-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="0712f-129"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0712f-129"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="0712f-130">DLL</span><span class="sxs-lookup"><span data-stu-id="0712f-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0712f-131"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0712f-131"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0712f-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0712f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0712f-133">**ивинхттпрекуест**</span><span class="sxs-lookup"><span data-stu-id="0712f-133">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="0712f-134">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="0712f-134">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="0712f-135">Проверка подлинности в WinHTTP</span><span class="sxs-lookup"><span data-stu-id="0712f-135">Authentication in WinHTTP</span></span>](authentication-in-winhttp.md)
</dt> <dt>

[<span data-ttu-id="0712f-136">Версии WinHTTP</span><span class="sxs-lookup"><span data-stu-id="0712f-136">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




