---
description: 'Версия метода Имфворккуеуесервицес:: Бегинунрегистерплатформворккуеуевисммксс, поддерживающая удаленное взаимодействие.'
ms.assetid: c3117086-268e-4e52-acfb-2c8167adaa07
title: Ремотебегинунрегистерплатформворккуеуевисммксс (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ab364f041d6bc8d0f6275879c82a937e98f463b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693667"
---
# <a name="remotebeginunregisterplatformworkqueuewithmmcss"></a><span data-ttu-id="d39e0-103">ремотебегинунрегистерплатформворккуеуевисммксс</span><span class="sxs-lookup"><span data-stu-id="d39e0-103">RemoteBeginUnregisterPlatformWorkQueueWithMMCSS</span></span>

<span data-ttu-id="d39e0-104">Версия метода [**имфворккуеуесервицес:: бегинунрегистерплатформворккуеуевисммксс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregisterplatformworkqueuewithmmcss) , поддерживающая удаленное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="d39e0-104">Remotable version of the [**IMFWorkQueueServices::BeginUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregisterplatformworkqueuewithmmcss) method.</span></span>

``` syntax
[call_as(BeginUnregisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteBeginUnregisterPlatformWorkQueueWithMMCSS(
    DWORD dwPlatformWorkQueue,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="d39e0-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d39e0-105">Remarks</span></span>

<span data-ttu-id="d39e0-106">Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод.</span><span class="sxs-lookup"><span data-stu-id="d39e0-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="d39e0-107">Метод не отображается в таблице vtable для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d39e0-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="d39e0-108">Если [**бегинунрегистерплатформворккуеуевисммксс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregisterplatformworkqueuewithmmcss) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.</span><span class="sxs-lookup"><span data-stu-id="d39e0-108">If [**BeginUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregisterplatformworkqueuewithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="d39e0-109">Требования</span><span class="sxs-lookup"><span data-stu-id="d39e0-109">Requirements</span></span>



| <span data-ttu-id="d39e0-110">Требование</span><span class="sxs-lookup"><span data-stu-id="d39e0-110">Requirement</span></span> | <span data-ttu-id="d39e0-111">Значение</span><span class="sxs-lookup"><span data-stu-id="d39e0-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d39e0-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d39e0-112">Minimum supported client</span></span><br/> | <span data-ttu-id="d39e0-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d39e0-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d39e0-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d39e0-114">Minimum supported server</span></span><br/> | <span data-ttu-id="d39e0-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d39e0-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d39e0-116">Header</span><span class="sxs-lookup"><span data-stu-id="d39e0-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="d39e0-117"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d39e0-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="d39e0-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d39e0-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="d39e0-119"><dt>Мфууид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d39e0-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="d39e0-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d39e0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d39e0-121">**имфворккуеуесервицес**</span><span class="sxs-lookup"><span data-stu-id="d39e0-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




