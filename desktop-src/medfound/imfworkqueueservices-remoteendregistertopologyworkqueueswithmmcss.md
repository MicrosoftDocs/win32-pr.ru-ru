---
description: 'Версия метода Имфворккуеуесервицес:: Ендрегистертопологиворккуеуесвисммксс, поддерживающая удаленное взаимодействие.'
ms.assetid: 94dce412-6a72-4ddf-86a3-5176ee1eb6d2
title: Ремотиндрегистертопологиворккуеуесвисммксс (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3333becfcd7a3c5e2621b628b6435b96af017cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693614"
---
# <a name="remoteendregistertopologyworkqueueswithmmcss"></a><span data-ttu-id="90222-103">ремотиндрегистертопологиворккуеуесвисммксс</span><span class="sxs-lookup"><span data-stu-id="90222-103">RemoteEndRegisterTopologyWorkQueuesWithMMCSS</span></span>

<span data-ttu-id="90222-104">Версия метода [**имфворккуеуесервицес:: ендрегистертопологиворккуеуесвисммксс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss) , поддерживающая удаленное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="90222-104">Remotable version of the [**IMFWorkQueueServices::EndRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss) method.</span></span>

``` syntax
[call_as(EndRegisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteEndRegisterTopologyWorkQueuesWithMMCSS(
    IUnknown *pResult
);
```

## <a name="remarks"></a><span data-ttu-id="90222-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="90222-105">Remarks</span></span>

<span data-ttu-id="90222-106">Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод.</span><span class="sxs-lookup"><span data-stu-id="90222-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="90222-107">Метод не отображается в таблице vtable для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="90222-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="90222-108">Если [**ендрегистертопологиворккуеуесвисммксс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.</span><span class="sxs-lookup"><span data-stu-id="90222-108">If [**EndRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="90222-109">Требования</span><span class="sxs-lookup"><span data-stu-id="90222-109">Requirements</span></span>



| <span data-ttu-id="90222-110">Требование</span><span class="sxs-lookup"><span data-stu-id="90222-110">Requirement</span></span> | <span data-ttu-id="90222-111">Значение</span><span class="sxs-lookup"><span data-stu-id="90222-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90222-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="90222-112">Minimum supported client</span></span><br/> | <span data-ttu-id="90222-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="90222-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="90222-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="90222-114">Minimum supported server</span></span><br/> | <span data-ttu-id="90222-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="90222-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="90222-116">Header</span><span class="sxs-lookup"><span data-stu-id="90222-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="90222-117"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="90222-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="90222-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="90222-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="90222-119"><dt>Мфууид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="90222-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="90222-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90222-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90222-121">**имфворккуеуесервицес**</span><span class="sxs-lookup"><span data-stu-id="90222-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




