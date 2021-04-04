---
description: Происходит при возникновении ошибки времени выполнения в приложении.
ms.assetid: d99400a4-3661-4162-bfd6-8c2a27e0f328
title: 'Событие Ивинхттпрекуестевентс:: OnError'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8582deec90eb6bfc2985460f3127d5c7ee9c01b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999451"
---
# <a name="iwinhttprequesteventsonerror-event"></a><span data-ttu-id="70446-103">Событие Ивинхттпрекуестевентс:: OnError</span><span class="sxs-lookup"><span data-stu-id="70446-103">IWinHttpRequestEvents::OnError event</span></span>

<span data-ttu-id="70446-104">Событие **OnError** возникает при возникновении ошибки времени выполнения в приложении.</span><span class="sxs-lookup"><span data-stu-id="70446-104">The **OnError** event occurs when there is a run-time error in the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="70446-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="70446-105">Syntax</span></span>


```C++
void OnError(
  [in] long ErrorNumber,
  [in] BSTR ErrorDescription
);
```



## <a name="parameters"></a><span data-ttu-id="70446-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="70446-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70446-107">*Номер ошибки* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="70446-107">*ErrorNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70446-108">Получает числовое значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="70446-108">Receives the numerical value of the error.</span></span> <span data-ttu-id="70446-109">Младшие 16 разрядов этого номера ошибки соответствуют одной из ошибок, перечисленных в [**сообщениях об ошибках**](error-messages.md).</span><span class="sxs-lookup"><span data-stu-id="70446-109">The lower 16 bits of this error number corresponds to one of the errors listed in [**Error Messages**](error-messages.md).</span></span>

</dd> <dt>

<span data-ttu-id="70446-110">*ErrorDescription* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="70446-110">*ErrorDescription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70446-111">Указывает краткое описание возникшей ошибки.</span><span class="sxs-lookup"><span data-stu-id="70446-111">Specifies a short description of the error which occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70446-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="70446-112">Return value</span></span>

<span data-ttu-id="70446-113">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="70446-113">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="70446-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="70446-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="70446-115">Для Windows XP и Windows 2000 см. раздел [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="70446-115">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="70446-116">Требования</span><span class="sxs-lookup"><span data-stu-id="70446-116">Requirements</span></span>



| <span data-ttu-id="70446-117">Требование</span><span class="sxs-lookup"><span data-stu-id="70446-117">Requirement</span></span> | <span data-ttu-id="70446-118">Значение</span><span class="sxs-lookup"><span data-stu-id="70446-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="70446-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="70446-119">Minimum supported client</span></span><br/> | <span data-ttu-id="70446-120">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="70446-120">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="70446-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="70446-121">Minimum supported server</span></span><br/> | <span data-ttu-id="70446-122">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="70446-122">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="70446-123">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="70446-123">Redistributable</span></span><br/>          | <span data-ttu-id="70446-124">WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="70446-124">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="70446-125">IDL</span><span class="sxs-lookup"><span data-stu-id="70446-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="70446-126"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="70446-126"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70446-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="70446-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70446-128">**ивинхттпрекуестевентс**</span><span class="sxs-lookup"><span data-stu-id="70446-128">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="70446-129">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="70446-129">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="70446-130">Версии WinHTTP</span><span class="sxs-lookup"><span data-stu-id="70446-130">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




