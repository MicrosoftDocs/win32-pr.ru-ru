---
description: Происходит при завершении данных ответа.
ms.assetid: 0df2031e-826f-436e-a689-201fa8b5c38f
title: 'Событие Ивинхттпрекуестевентс:: Онреспонсефинишед'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d3a596e23028cec0401a21a1ee866ef6e51d9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702515"
---
# <a name="iwinhttprequesteventsonresponsefinished-event"></a><span data-ttu-id="1c0be-103">Событие Ивинхттпрекуестевентс:: Онреспонсефинишед</span><span class="sxs-lookup"><span data-stu-id="1c0be-103">IWinHttpRequestEvents::OnResponseFinished event</span></span>

<span data-ttu-id="1c0be-104">Событие **онреспонсефинишед** возникает при завершении данных ответа.</span><span class="sxs-lookup"><span data-stu-id="1c0be-104">The **OnResponseFinished** event occurs when the response data is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c0be-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c0be-105">Syntax</span></span>


```C++
void OnResponseFinished();
```



## <a name="parameters"></a><span data-ttu-id="1c0be-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1c0be-106">Parameters</span></span>

<span data-ttu-id="1c0be-107">У этого события нет параметров.</span><span class="sxs-lookup"><span data-stu-id="1c0be-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1c0be-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1c0be-108">Return value</span></span>

<span data-ttu-id="1c0be-109">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1c0be-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c0be-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c0be-110">Remarks</span></span>

<span data-ttu-id="1c0be-111">Это событие сигнализирует о получении всех данных ответа, относящихся к последнему запросу.</span><span class="sxs-lookup"><span data-stu-id="1c0be-111">This event signals that all of the response data that pertains to the most recent request has been received.</span></span> <span data-ttu-id="1c0be-112">[**Онреспонседатааваилабле**](iwinhttprequestevents-onresponsedataavailable.md) не повторяется до следующего запроса.</span><span class="sxs-lookup"><span data-stu-id="1c0be-112">[**OnResponseDataAvailable**](iwinhttprequestevents-onresponsedataavailable.md) does not occur again until the next request.</span></span>

> [!Note]  
> <span data-ttu-id="1c0be-113">Для Windows XP и Windows 2000 см. раздел [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="1c0be-113">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1c0be-114">Требования</span><span class="sxs-lookup"><span data-stu-id="1c0be-114">Requirements</span></span>



| <span data-ttu-id="1c0be-115">Требование</span><span class="sxs-lookup"><span data-stu-id="1c0be-115">Requirement</span></span> | <span data-ttu-id="1c0be-116">Значение</span><span class="sxs-lookup"><span data-stu-id="1c0be-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c0be-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1c0be-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1c0be-118">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1c0be-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="1c0be-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1c0be-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1c0be-120">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1c0be-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="1c0be-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="1c0be-121">Redistributable</span></span><br/>          | <span data-ttu-id="1c0be-122">WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="1c0be-122">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="1c0be-123">IDL</span><span class="sxs-lookup"><span data-stu-id="1c0be-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1c0be-124"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1c0be-124"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c0be-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c0be-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c0be-126">**ивинхттпрекуестевентс**</span><span class="sxs-lookup"><span data-stu-id="1c0be-126">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="1c0be-127">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="1c0be-127">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="1c0be-128">Версии WinHTTP</span><span class="sxs-lookup"><span data-stu-id="1c0be-128">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




