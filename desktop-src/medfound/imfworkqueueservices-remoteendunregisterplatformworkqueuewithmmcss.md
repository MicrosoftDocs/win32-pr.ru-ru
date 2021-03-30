---
description: 'Версия метода Имфворккуеуесервицес:: Ендунрегистерплатформворккуеуевисммксс, поддерживающая удаленное взаимодействие.'
ms.assetid: 92eef511-0af0-4146-ac81-7dfa4a649016
title: Ремотиндунрегистерплатформворккуеуевисммксс (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a03f8cdc1bfdded539c8143c3fa50c6bafb54de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912648"
---
# <a name="remoteendunregisterplatformworkqueuewithmmcss"></a><span data-ttu-id="cb73e-103">ремотиндунрегистерплатформворккуеуевисммксс</span><span class="sxs-lookup"><span data-stu-id="cb73e-103">RemoteEndUnregisterPlatformWorkQueueWithMMCSS</span></span>

<span data-ttu-id="cb73e-104">Версия метода [**имфворккуеуесервицес:: ендунрегистерплатформворккуеуевисммксс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss) , поддерживающая удаленное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="cb73e-104">Remotable version of the [**IMFWorkQueueServices::EndUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss) method.</span></span>

``` syntax
[call_as(EndUnregisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteEndUnregisterPlatformWorkQueueWithMMCSS(
    IUnknown *pResult
);
```

## <a name="remarks"></a><span data-ttu-id="cb73e-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb73e-105">Remarks</span></span>

<span data-ttu-id="cb73e-106">Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод.</span><span class="sxs-lookup"><span data-stu-id="cb73e-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="cb73e-107">Метод не отображается в таблице vtable для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="cb73e-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="cb73e-108">Если [**ендунрегистерплатформворккуеуевисммксс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.</span><span class="sxs-lookup"><span data-stu-id="cb73e-108">If [**EndUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb73e-109">Требования</span><span class="sxs-lookup"><span data-stu-id="cb73e-109">Requirements</span></span>



| <span data-ttu-id="cb73e-110">Требование</span><span class="sxs-lookup"><span data-stu-id="cb73e-110">Requirement</span></span> | <span data-ttu-id="cb73e-111">Значение</span><span class="sxs-lookup"><span data-stu-id="cb73e-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb73e-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cb73e-112">Minimum supported client</span></span><br/> | <span data-ttu-id="cb73e-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cb73e-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cb73e-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cb73e-114">Minimum supported server</span></span><br/> | <span data-ttu-id="cb73e-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cb73e-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cb73e-116">Header</span><span class="sxs-lookup"><span data-stu-id="cb73e-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb73e-117"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb73e-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="cb73e-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cb73e-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="cb73e-119"><dt>Мфууид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb73e-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="cb73e-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb73e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb73e-121">**имфворккуеуесервицес**</span><span class="sxs-lookup"><span data-stu-id="cb73e-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




