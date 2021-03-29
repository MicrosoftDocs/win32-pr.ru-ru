---
description: 'Версия метода Имфворккуеуесервицес:: Ендрегистерплатформворккуеуевисммксс, поддерживающая удаленное взаимодействие.'
ms.assetid: cb15129e-a3ad-4351-a7d6-dd4b883437bd
title: Ремотиндрегистерплатформворккуеуевисммксс (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 673281a8ed4e4c4174ecd2d874e7032776ea44c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808050"
---
# <a name="remoteendregisterplatformworkqueuewithmmcss"></a><span data-ttu-id="0ca1e-103">ремотиндрегистерплатформворккуеуевисммксс</span><span class="sxs-lookup"><span data-stu-id="0ca1e-103">RemoteEndRegisterPlatformWorkQueueWithMMCSS</span></span>

<span data-ttu-id="0ca1e-104">Версия метода [**имфворккуеуесервицес:: ендрегистерплатформворккуеуевисммксс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss) , поддерживающая удаленное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-104">Remotable version of the [**IMFWorkQueueServices::EndRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss) method.</span></span>

``` syntax
[call_as(EndRegisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteEndRegisterPlatformWorkQueueWithMMCSS(
    IUnknown *pResult,
    DWORD *pdwTaskId
);
```

## <a name="remarks"></a><span data-ttu-id="0ca1e-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0ca1e-105">Remarks</span></span>

<span data-ttu-id="0ca1e-106">Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="0ca1e-107">Метод не отображается в таблице vtable для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="0ca1e-108">Если [**ендрегистерплатформворккуеуевисммксс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.</span><span class="sxs-lookup"><span data-stu-id="0ca1e-108">If [**EndRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ca1e-109">Требования</span><span class="sxs-lookup"><span data-stu-id="0ca1e-109">Requirements</span></span>



| <span data-ttu-id="0ca1e-110">Требование</span><span class="sxs-lookup"><span data-stu-id="0ca1e-110">Requirement</span></span> | <span data-ttu-id="0ca1e-111">Значение</span><span class="sxs-lookup"><span data-stu-id="0ca1e-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ca1e-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0ca1e-112">Minimum supported client</span></span><br/> | <span data-ttu-id="0ca1e-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0ca1e-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0ca1e-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0ca1e-114">Minimum supported server</span></span><br/> | <span data-ttu-id="0ca1e-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0ca1e-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0ca1e-116">Header</span><span class="sxs-lookup"><span data-stu-id="0ca1e-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ca1e-117"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ca1e-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="0ca1e-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0ca1e-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="0ca1e-119"><dt>Мфууид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ca1e-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="0ca1e-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ca1e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ca1e-121">**имфворккуеуесервицес**</span><span class="sxs-lookup"><span data-stu-id="0ca1e-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




