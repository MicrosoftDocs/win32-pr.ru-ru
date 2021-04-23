---
description: Происходит при начале получения данных ответа.
ms.assetid: 7245725b-40dd-4282-b681-f0b2c191db94
title: 'Событие Ивинхттпрекуестевентс:: Онреспонсестарт'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a299c535dd854bff07f2c24989096f7b9e49fc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702513"
---
# <a name="iwinhttprequesteventsonresponsestart-event"></a><span data-ttu-id="e8c17-103">Событие Ивинхттпрекуестевентс:: Онреспонсестарт</span><span class="sxs-lookup"><span data-stu-id="e8c17-103">IWinHttpRequestEvents::OnResponseStart event</span></span>

<span data-ttu-id="e8c17-104">Событие **онреспонсестарт** возникает при начале получения данных ответа.</span><span class="sxs-lookup"><span data-stu-id="e8c17-104">The **OnResponseStart** event occurs when the response data starts to be received.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8c17-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8c17-105">Syntax</span></span>


```C++
void OnResponseStart(
  [in] long Status,
  [in] BSTR ContentType
);
```



## <a name="parameters"></a><span data-ttu-id="e8c17-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8c17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8c17-107">*Состояние* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8c17-107">*Status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c17-108">Получает стандартный код состояния, возвращенный с данными ответа.</span><span class="sxs-lookup"><span data-stu-id="e8c17-108">Receives the standard status code returned with the response data.</span></span> <span data-ttu-id="e8c17-109">Коды состояния определяются в [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="e8c17-109">Status codes are defined in [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>

</dd> <dt>

<span data-ttu-id="e8c17-110">*ContentType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8c17-110">*ContentType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c17-111">Указывает тип получаемого содержимого, например "text/html" или "image/gif".</span><span class="sxs-lookup"><span data-stu-id="e8c17-111">Specifies the type of content received, such as "text/html" or "image/gif".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8c17-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e8c17-112">Return value</span></span>

<span data-ttu-id="e8c17-113">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e8c17-113">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8c17-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e8c17-114">Remarks</span></span>

<span data-ttu-id="e8c17-115">Чтобы это событие произошло, используйте [**Open**](iwinhttprequest-open.md) для отправки HTTP-соединения в асинхронном режиме и используйте [**Send**](iwinhttprequest-send.md) для отправки запроса данных на Интернет-сервер.</span><span class="sxs-lookup"><span data-stu-id="e8c17-115">For this event to occur, use [**Open**](iwinhttprequest-open.md) to send an HTTP connection in asynchronous mode and use [**Send**](iwinhttprequest-send.md) to send a data request to an Internet server.</span></span>

<span data-ttu-id="e8c17-116">Это первое событие WinHTTP, возникающее после [**отправки**](iwinhttprequest-send.md).</span><span class="sxs-lookup"><span data-stu-id="e8c17-116">This is the first WinHTTP event to occur after the [**Send**](iwinhttprequest-send.md).</span></span>

> [!Note]  
> <span data-ttu-id="e8c17-117">Для Windows XP и Windows 2000 см. раздел [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="e8c17-117">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e8c17-118">Требования</span><span class="sxs-lookup"><span data-stu-id="e8c17-118">Requirements</span></span>



| <span data-ttu-id="e8c17-119">Требование</span><span class="sxs-lookup"><span data-stu-id="e8c17-119">Requirement</span></span> | <span data-ttu-id="e8c17-120">Значение</span><span class="sxs-lookup"><span data-stu-id="e8c17-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8c17-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8c17-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e8c17-122">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e8c17-122">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="e8c17-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8c17-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e8c17-124">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e8c17-124">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="e8c17-125">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="e8c17-125">Redistributable</span></span><br/>          | <span data-ttu-id="e8c17-126">WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="e8c17-126">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="e8c17-127">IDL</span><span class="sxs-lookup"><span data-stu-id="e8c17-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e8c17-128"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e8c17-128"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8c17-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8c17-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8c17-130">**ивинхттпрекуестевентс**</span><span class="sxs-lookup"><span data-stu-id="e8c17-130">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="e8c17-131">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="e8c17-131">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="e8c17-132">Версии WinHTTP</span><span class="sxs-lookup"><span data-stu-id="e8c17-132">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




