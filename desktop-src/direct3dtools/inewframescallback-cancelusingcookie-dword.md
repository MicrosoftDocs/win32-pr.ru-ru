---
description: Обратный вызов, уведомляющий узел об отмене запроса с помощью файла cookie, уникально идентифицирующего запрос.
MS-HAID: vspixengine.INewFramesCallback\_CancelUsingCookie\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Иневфрамескаллбакк:: Канцелусингкукие'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 36176554-BB4F-40CB-AB7B-4957DA84BAA8
api_name:
- INewFramesCallback.CancelUsingCookie
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: dfbbbda1a11244088dccad640be348da1e4d8313
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494715"
---
# <a name="span-idvspixengineinewframescallback_cancelusingcookie_dwordspaninewframescallbackcancelusingcookie-method"></a><span data-ttu-id="7ec52-103"><span id="vspixengine.inewframescallback_cancelusingcookie_dword"></span>Метод Иневфрамескаллбакк:: Канцелусингкукие</span><span class="sxs-lookup"><span data-stu-id="7ec52-103"><span id="vspixengine.inewframescallback_cancelusingcookie_dword"></span>INewFramesCallback::CancelUsingCookie method</span></span>

<span data-ttu-id="7ec52-104">Обратный вызов, уведомляющий узел об отмене запроса с помощью файла cookie, уникально идентифицирующего запрос.</span><span class="sxs-lookup"><span data-stu-id="7ec52-104">A callback that notifies the host of a canceled request by using a cookie that uniquely identifies the request.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ec52-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ec52-105">Syntax</span></span>


```C++
HRESULT CancelUsingCallback(
   IUnknown * requestCallback
);
```

## <a name="parameters"></a><span data-ttu-id="7ec52-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ec52-106">Parameters</span></span>

<span data-ttu-id="7ec52-107">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="7ec52-107">*requestCookie* </span></span>  
<span data-ttu-id="7ec52-108">Файл cookie, который уникальным образом иденфиес отмененный запрос.</span><span class="sxs-lookup"><span data-stu-id="7ec52-108">The cookie which uniquely idenfies the cancelled request.</span></span>

## <a name="return-value"></a><span data-ttu-id="7ec52-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ec52-109">Return value</span></span>

<span data-ttu-id="7ec52-110">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="7ec52-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7ec52-111">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7ec52-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ec52-112">Требования</span><span class="sxs-lookup"><span data-stu-id="7ec52-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="7ec52-113">Header</span><span class="sxs-lookup"><span data-stu-id="7ec52-113">Header</span></span></p></td><td><span data-ttu-id="7ec52-114">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="7ec52-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="7ec52-115"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="7ec52-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="7ec52-116">**иневфрамескаллбакк**</span><span class="sxs-lookup"><span data-stu-id="7ec52-116">**INewFramesCallback**</span></span>](/windows/desktop/direct3dtools/inewframescallback)

 

 
