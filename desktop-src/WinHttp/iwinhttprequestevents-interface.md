---
description: Предоставляет события служб Microsoft Windows HTTP (WinHTTP).
ms.assetid: 0721d7f9-2e84-41a9-be52-89c8d638eb90
title: Интерфейс Ивинхттпрекуестевентс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequestEvents
api_type:
- COM
api_location:
- HttpRequest.idl
ms.openlocfilehash: 3cdd0bf10c0d4bd75351ddaab6e88ce7182850fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674199"
---
# <a name="iwinhttprequestevents-interface"></a><span data-ttu-id="26120-103">Интерфейс Ивинхттпрекуестевентс</span><span class="sxs-lookup"><span data-stu-id="26120-103">IWinHttpRequestEvents interface</span></span>

<span data-ttu-id="26120-104">Интерфейс **ивинхттпрекуестевентс** предоставляет события для [служб Microsoft Windows HTTP (WinHTTP)](about-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="26120-104">The **IWinHttpRequestEvents** interface provides events for [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md).</span></span> <span data-ttu-id="26120-105">В нем используются только методы событий.</span><span class="sxs-lookup"><span data-stu-id="26120-105">It uses only event methods.</span></span>

## <a name="members"></a><span data-ttu-id="26120-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="26120-106">Members</span></span>

<span data-ttu-id="26120-107">Интерфейс **ивинхттпрекуестевентс** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="26120-107">The **IWinHttpRequestEvents** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="26120-108">**Ивинхттпрекуестевентс** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="26120-108">**IWinHttpRequestEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="26120-109">Методы</span><span class="sxs-lookup"><span data-stu-id="26120-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="26120-110">Методы</span><span class="sxs-lookup"><span data-stu-id="26120-110">Methods</span></span>

<span data-ttu-id="26120-111">Интерфейс **ивинхттпрекуестевентс** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="26120-111">The **IWinHttpRequestEvents** interface has these methods.</span></span>



| <span data-ttu-id="26120-112">Метод</span><span class="sxs-lookup"><span data-stu-id="26120-112">Method</span></span>                                                                           | <span data-ttu-id="26120-113">Описание</span><span class="sxs-lookup"><span data-stu-id="26120-113">Description</span></span>                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="26120-114">**OnError**</span><span class="sxs-lookup"><span data-stu-id="26120-114">**OnError**</span></span>](iwinhttprequestevents-onerror.md)                                 | <span data-ttu-id="26120-115">Происходит при возникновении ошибки времени выполнения в приложении.</span><span class="sxs-lookup"><span data-stu-id="26120-115">Occurs when there is a run-time error in the application.</span></span><br/> |
| [<span data-ttu-id="26120-116">**онреспонседатааваилабле**</span><span class="sxs-lookup"><span data-stu-id="26120-116">**OnResponseDataAvailable**</span></span>](iwinhttprequestevents-onresponsedataavailable.md) | <span data-ttu-id="26120-117">Происходит при доступе к данным из ответа.</span><span class="sxs-lookup"><span data-stu-id="26120-117">Occurs when data is available from the response.</span></span><br/>          |
| [<span data-ttu-id="26120-118">**онреспонсефинишед**</span><span class="sxs-lookup"><span data-stu-id="26120-118">**OnResponseFinished**</span></span>](iwinhttprequestevents-onresponsefinished.md)           | <span data-ttu-id="26120-119">Происходит при завершении данных ответа.</span><span class="sxs-lookup"><span data-stu-id="26120-119">Occurs when the response data is complete.</span></span><br/>                |
| [<span data-ttu-id="26120-120">**онреспонсестарт**</span><span class="sxs-lookup"><span data-stu-id="26120-120">**OnResponseStart**</span></span>](iwinhttprequestevents-onresponsestart.md)                 | <span data-ttu-id="26120-121">Происходит при начале получения данных ответа.</span><span class="sxs-lookup"><span data-stu-id="26120-121">Occurs when the response data starts to be received.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="26120-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="26120-122">Remarks</span></span>

<span data-ttu-id="26120-123">В следующей процедуре описывается регистрация для получения уведомлений.</span><span class="sxs-lookup"><span data-stu-id="26120-123">The following procedure describes how to register for notifications.</span></span>

1.  <span data-ttu-id="26120-124">Получите интерфейс [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) путем вызова **QueryInterface** для объекта [**ивинхттпрекуест**](iwinhttprequest-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="26120-124">Get an [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) interface by calling **QueryInterface** on an [**IWinHttpRequest**](iwinhttprequest-interface.md) object.</span></span>
2.  <span data-ttu-id="26120-125">Вызовите [финдконнектионпоинт](/windows/win32/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) в возвращенном интерфейсе и передайте **IID \_ ивинхттпрекуестевентс** в *riid*.</span><span class="sxs-lookup"><span data-stu-id="26120-125">Call [FindConnectionPoint](/windows/win32/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) on the returned interface and pass **IID\_IWinHttpRequestEvents** to *riid*.</span></span>
3.  <span data-ttu-id="26120-126">Вызовите [advise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) в возвращенной точке соединения и передайте указатель на интерфейс **IUnknown** для объекта, который реализует **ивинхттпрекуестевентс** для *Punk*.</span><span class="sxs-lookup"><span data-stu-id="26120-126">Call [Advise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) on the returned connection point and pass a pointer to an **IUnknown** interface on an object that implements **IWinHttpRequestEvents** to *pUnk*.</span></span>

<span data-ttu-id="26120-127">Уведомления могут быть завершены путем вызова команды [unadvise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-unadvise) на точке соединения, возвращенной на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="26120-127">Notifications can be terminated by calling [Unadvise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-unadvise) on the connection point returned in step 2.</span></span>

<span data-ttu-id="26120-128">Чтобы просмотреть код, регистрирующий для COM-уведомлений, см. раздел клиент в статье [точки подключения COM](/archive/msdn-magazine/2007/september/clr-inside-out-com-connection-points) .</span><span class="sxs-lookup"><span data-stu-id="26120-128">To view some code that registers for COM notifications, see the Client section of the [COM Connection Points](/archive/msdn-magazine/2007/september/clr-inside-out-com-connection-points) article.</span></span>

> [!Note]  
> <span data-ttu-id="26120-129">Для Windows XP и Windows 2000 см. раздел [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="26120-129">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="26120-130">Требования</span><span class="sxs-lookup"><span data-stu-id="26120-130">Requirements</span></span>



| <span data-ttu-id="26120-131">Требование</span><span class="sxs-lookup"><span data-stu-id="26120-131">Requirement</span></span> | <span data-ttu-id="26120-132">Значение</span><span class="sxs-lookup"><span data-stu-id="26120-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="26120-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="26120-133">Minimum supported client</span></span><br/> | <span data-ttu-id="26120-134">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="26120-134">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="26120-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="26120-135">Minimum supported server</span></span><br/> | <span data-ttu-id="26120-136">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="26120-136">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="26120-137">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="26120-137">Redistributable</span></span><br/>          | <span data-ttu-id="26120-138">WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="26120-138">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="26120-139">IDL</span><span class="sxs-lookup"><span data-stu-id="26120-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="26120-140"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="26120-140"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26120-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26120-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26120-142">**ивинхттпрекуест**</span><span class="sxs-lookup"><span data-stu-id="26120-142">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="26120-143">Версии WinHTTP</span><span class="sxs-lookup"><span data-stu-id="26120-143">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

