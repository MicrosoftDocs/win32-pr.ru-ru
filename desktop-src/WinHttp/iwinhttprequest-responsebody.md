---
description: Извлекает тело объекта ответа в виде массива байтов без знака.
ms.assetid: 557913e0-9f19-42fc-bfca-9ed248972b4b
title: 'Свойство Ивинхттпрекуест:: Респонсебоди'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.ResponseBody
- IWinHttpRequest.get_ResponseBody
- WinHttpRequest.ResponseBody
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 5a608f2744ad2880ecf7c4862b03821afcef9630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703126"
---
# <a name="iwinhttprequestresponsebody-property"></a><span data-ttu-id="dd510-103">Свойство Ивинхттпрекуест:: Респонсебоди</span><span class="sxs-lookup"><span data-stu-id="dd510-103">IWinHttpRequest::ResponseBody property</span></span>

<span data-ttu-id="dd510-104">Свойство **респонсебоди** извлекает тело объекта ответа в виде массива байтов без знака.</span><span class="sxs-lookup"><span data-stu-id="dd510-104">The **ResponseBody** property retrieves the response entity body as an array of unsigned bytes.</span></span>

<span data-ttu-id="dd510-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dd510-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd510-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd510-106">Syntax</span></span>


```C++
HRESULT get_ResponseBody(
  [out, retval] VARIANT *Body
);
```


```JScript

vtResponseBody = WinHttpRequest.ResponseBody
```





## <a name="property-value"></a><span data-ttu-id="dd510-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="dd510-107">Property value</span></span>

<span data-ttu-id="dd510-108">Значение **типа Variant** , которое получает тело сущности ответа в виде массива беззнаковых байтов.</span><span class="sxs-lookup"><span data-stu-id="dd510-108">A **Variant** value that receives the response entity body as an array of unsigned bytes.</span></span> <span data-ttu-id="dd510-109">Этот массив содержит необработанные данные, полученные непосредственно с сервера.</span><span class="sxs-lookup"><span data-stu-id="dd510-109">This array contains the raw data as received directly from the server.</span></span>

## <a name="error-codes"></a><span data-ttu-id="dd510-110">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="dd510-110">Error codes</span></span>

<span data-ttu-id="dd510-111">В случае успешного выполнения возвращается значение **S \_** , а в противном случае — значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="dd510-111">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd510-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dd510-112">Remarks</span></span>

<span data-ttu-id="dd510-113">Это свойство возвращает данные ответа в массиве беззнаковых байтов.</span><span class="sxs-lookup"><span data-stu-id="dd510-113">This property returns the response data in an array of unsigned bytes.</span></span> <span data-ttu-id="dd510-114">Если ответ не имеет текста ответа, возвращается пустой вариант.</span><span class="sxs-lookup"><span data-stu-id="dd510-114">If the response does not have a response body, an empty variant is returned.</span></span> <span data-ttu-id="dd510-115">Это свойство может быть вызвано только после вызова метода [**Send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="dd510-115">This property can only be invoked after the [**Send**](iwinhttprequest-send.md) method has been called.</span></span>

> [!Note]  
> <span data-ttu-id="dd510-116">Дополнительные сведения о реализации для Windows XP и Windows 2000 см. в разделе [требования к времени выполнения](winhttp-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="dd510-116">For more information about implementation for Windows XP and Windows 2000, see [Run-Time Requirements](winhttp-start-page.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dd510-117">Требования</span><span class="sxs-lookup"><span data-stu-id="dd510-117">Requirements</span></span>



| <span data-ttu-id="dd510-118">Требование</span><span class="sxs-lookup"><span data-stu-id="dd510-118">Requirement</span></span> | <span data-ttu-id="dd510-119">Значение</span><span class="sxs-lookup"><span data-stu-id="dd510-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd510-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd510-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dd510-121">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dd510-121">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="dd510-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd510-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dd510-123">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dd510-123">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="dd510-124">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="dd510-124">Redistributable</span></span><br/>          | <span data-ttu-id="dd510-125">WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="dd510-125">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="dd510-126">IDL</span><span class="sxs-lookup"><span data-stu-id="dd510-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dd510-127"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dd510-127"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="dd510-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dd510-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="dd510-129"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd510-129"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="dd510-130">DLL</span><span class="sxs-lookup"><span data-stu-id="dd510-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd510-131"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd510-131"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="dd510-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd510-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd510-133">**ивинхттпрекуест**</span><span class="sxs-lookup"><span data-stu-id="dd510-133">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="dd510-134">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="dd510-134">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="dd510-135">**ResponseStream**</span><span class="sxs-lookup"><span data-stu-id="dd510-135">**ResponseStream**</span></span>](iwinhttprequest-responsestream.md)
</dt> <dt>

[<span data-ttu-id="dd510-136">**респонсетекст**</span><span class="sxs-lookup"><span data-stu-id="dd510-136">**ResponseText**</span></span>](iwinhttprequest-responsetext.md)
</dt> <dt>

[<span data-ttu-id="dd510-137">Версии WinHTTP</span><span class="sxs-lookup"><span data-stu-id="dd510-137">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




