---
description: Метод Abort прерывает метод Send WinHTTP.
ms.assetid: 8326feef-8611-4441-b52d-74855e6acfff
title: 'Метод Ивинхттпрекуест:: Abort'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.Abort
- WinHttpRequest.Abort
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 56290dfc16f9986cb7d7596c098bb53c207efebe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999292"
---
# <a name="iwinhttprequestabort-method"></a><span data-ttu-id="00db0-103">Метод Ивинхттпрекуест:: Abort</span><span class="sxs-lookup"><span data-stu-id="00db0-103">IWinHttpRequest::Abort method</span></span>

<span data-ttu-id="00db0-104">Метод **Abort** прерывает метод [**Send**](iwinhttprequest-send.md) [WinHTTP](about-winhttp.md) .</span><span class="sxs-lookup"><span data-stu-id="00db0-104">The **Abort** method aborts a [WinHTTP](about-winhttp.md) [**Send**](iwinhttprequest-send.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="00db0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="00db0-105">Syntax</span></span>


```C++
HRESULT Abort();
```



## <a name="parameters"></a><span data-ttu-id="00db0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="00db0-106">Parameters</span></span>

<span data-ttu-id="00db0-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="00db0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="00db0-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="00db0-108">Return value</span></span>

<span data-ttu-id="00db0-109">В случае успешного выполнения возвращается значение **S \_** , а в противном случае — значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="00db0-109">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="00db0-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="00db0-110">Remarks</span></span>

<span data-ttu-id="00db0-111">Можно прерывать как асинхронные, так и синхронные методы [**отправки**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="00db0-111">You can abort both asynchronous and synchronous [**Send**](iwinhttprequest-send.md) methods.</span></span> <span data-ttu-id="00db0-112">Для прерывания синхронного метода [**отправки**](iwinhttprequest-send.md) необходимо вызвать метод **Abort** из события [**ивинхттпрекуестевентс**](iwinhttprequestevents-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="00db0-112">To abort a synchronous [**Send**](iwinhttprequest-send.md) method, you must call **Abort** from within an [**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md) event.</span></span>

> [!Note]  
> <span data-ttu-id="00db0-113">Для Windows XP и Windows 2000 см. раздел [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="00db0-113">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="00db0-114">Требования</span><span class="sxs-lookup"><span data-stu-id="00db0-114">Requirements</span></span>



| <span data-ttu-id="00db0-115">Требование</span><span class="sxs-lookup"><span data-stu-id="00db0-115">Requirement</span></span> | <span data-ttu-id="00db0-116">Значение</span><span class="sxs-lookup"><span data-stu-id="00db0-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="00db0-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="00db0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="00db0-118">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="00db0-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="00db0-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="00db0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="00db0-120">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="00db0-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="00db0-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="00db0-121">Redistributable</span></span><br/>          | <span data-ttu-id="00db0-122">WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="00db0-122">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="00db0-123">IDL</span><span class="sxs-lookup"><span data-stu-id="00db0-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="00db0-124"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="00db0-124"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="00db0-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="00db0-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="00db0-126"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00db0-126"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="00db0-127">DLL</span><span class="sxs-lookup"><span data-stu-id="00db0-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00db0-128"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00db0-128"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="00db0-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="00db0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00db0-130">**ивинхттпрекуест**</span><span class="sxs-lookup"><span data-stu-id="00db0-130">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="00db0-131">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="00db0-131">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="00db0-132">Версии WinHTTP</span><span class="sxs-lookup"><span data-stu-id="00db0-132">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




