---
description: Ожидание завершения работы указанного обработчика (вызов блокировки).
MS-HAID: vspixengine.IServerConnectionCallback\_WaitForShutdown\_IPixEngine\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Исерверконнектионкаллбакк:: Ваитфоршутдовн'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B70229D5-3C41-4B50-8336-A1271A9EBE81
api_name:
- IServerConnectionCallback.WaitForShutdown
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d98bd5f398748e6e62a099bcc2be94b5e5f27bc8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140555"
---
# <a name="span-idvspixengineiserverconnectioncallback_waitforshutdown_ipixengine_ptrspaniserverconnectioncallbackwaitforshutdown-method"></a><span data-ttu-id="f3f48-103"><span id="vspixengine.iserverconnectioncallback_waitforshutdown_ipixengine_ptr"></span>Метод Исерверконнектионкаллбакк:: Ваитфоршутдовн</span><span class="sxs-lookup"><span data-stu-id="f3f48-103"><span id="vspixengine.iserverconnectioncallback_waitforshutdown_ipixengine_ptr"></span>IServerConnectionCallback::WaitForShutdown method</span></span>

<span data-ttu-id="f3f48-104">Ожидание завершения работы указанного обработчика (вызов блокировки).</span><span class="sxs-lookup"><span data-stu-id="f3f48-104">Wait for shutdown of the specified engine (Blocking call).</span></span>

## <a name="syntax"></a><span data-ttu-id="f3f48-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3f48-105">Syntax</span></span>


```C++
HRESULT WaitForShutdown(
   IPixEngine * pEngine
);
```

## <a name="parameters"></a><span data-ttu-id="f3f48-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f3f48-106">Parameters</span></span>

<span data-ttu-id="f3f48-107">*пенгине* </span><span class="sxs-lookup"><span data-stu-id="f3f48-107">*pEngine* </span></span>  
<span data-ttu-id="f3f48-108">Подсистема для завершения работы.</span><span class="sxs-lookup"><span data-stu-id="f3f48-108">The engine to shut down.</span></span>

## <a name="return-value"></a><span data-ttu-id="f3f48-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f3f48-109">Return value</span></span>

<span data-ttu-id="f3f48-110">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="f3f48-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f3f48-111">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f3f48-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3f48-112">Требования</span><span class="sxs-lookup"><span data-stu-id="f3f48-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f3f48-113">Header</span><span class="sxs-lookup"><span data-stu-id="f3f48-113">Header</span></span></p></td><td><span data-ttu-id="f3f48-114">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="f3f48-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="f3f48-115"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="f3f48-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="f3f48-116">**исерверконнектионкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="f3f48-116">**IServerConnectionCallback**</span></span>](/windows/desktop/direct3dtools/iserverconnectioncallback)

 

 
