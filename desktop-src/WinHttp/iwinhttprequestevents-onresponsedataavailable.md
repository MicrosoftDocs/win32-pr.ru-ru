---
description: Происходит при доступе к данным из ответа.
ms.assetid: 62d02e3b-466a-4d3d-994b-0a1ae12049e1
title: 'Событие Ивинхттпрекуестевентс:: Онреспонседатааваилабле'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41cb2fbc680b1f6739a66bb68565188c8a5d78b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673957"
---
# <a name="iwinhttprequesteventsonresponsedataavailable-event"></a><span data-ttu-id="b05a3-103">Событие Ивинхттпрекуестевентс:: Онреспонседатааваилабле</span><span class="sxs-lookup"><span data-stu-id="b05a3-103">IWinHttpRequestEvents::OnResponseDataAvailable event</span></span>

<span data-ttu-id="b05a3-104">Событие **онреспонседатааваилабле** возникает при доступе к данным из ответа.</span><span class="sxs-lookup"><span data-stu-id="b05a3-104">The **OnResponseDataAvailable** event occurs when data is available from the response.</span></span>

## <a name="syntax"></a><span data-ttu-id="b05a3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b05a3-105">Syntax</span></span>


```C++
void OnResponseDataAvailable(
  [in] SAFEARRAY(unsigned char) *Data
);
```



## <a name="parameters"></a><span data-ttu-id="b05a3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b05a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b05a3-107">*Данные* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b05a3-107">*Data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b05a3-108">Отсчитываемый от нуля массив байтов, который получает данные ответа, полученные службами Microsoft Windows HTTP (WinHTTP) вплоть до момента возникновения этого события.</span><span class="sxs-lookup"><span data-stu-id="b05a3-108">A zero-based array of bytes that receives the response data received by Microsoft Windows HTTP Services (WinHTTP) up to the point that this event occurs.</span></span> <span data-ttu-id="b05a3-109">Это **вариант** типа VT \_ array \| VT \_ UI1.</span><span class="sxs-lookup"><span data-stu-id="b05a3-109">This is a **VARIANT** of type VT\_ARRAY \| VT\_UI1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b05a3-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b05a3-110">Return value</span></span>

<span data-ttu-id="b05a3-111">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b05a3-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b05a3-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b05a3-112">Remarks</span></span>

<span data-ttu-id="b05a3-113">Поскольку данные находятся в байтах, их необходимо преобразовать в широкие символы при помещении в строку расширенных символов (Юникод).</span><span class="sxs-lookup"><span data-stu-id="b05a3-113">Because data is in bytes, it must be converted to wide characters when placed in a wide character (Unicode) string.</span></span>

> [!Note]  
> <span data-ttu-id="b05a3-114">Для Windows XP и Windows 2000 см. раздел [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="b05a3-114">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b05a3-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b05a3-115">Requirements</span></span>



| <span data-ttu-id="b05a3-116">Требование</span><span class="sxs-lookup"><span data-stu-id="b05a3-116">Requirement</span></span> | <span data-ttu-id="b05a3-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b05a3-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b05a3-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b05a3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b05a3-119">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b05a3-119">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="b05a3-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b05a3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b05a3-121">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b05a3-121">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="b05a3-122">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="b05a3-122">Redistributable</span></span><br/>          | <span data-ttu-id="b05a3-123">WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="b05a3-123">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="b05a3-124">IDL</span><span class="sxs-lookup"><span data-stu-id="b05a3-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b05a3-125"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b05a3-125"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b05a3-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b05a3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b05a3-127">**ивинхттпрекуестевентс**</span><span class="sxs-lookup"><span data-stu-id="b05a3-127">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="b05a3-128">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="b05a3-128">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="b05a3-129">Версии WinHTTP</span><span class="sxs-lookup"><span data-stu-id="b05a3-129">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




