---
description: 'Версия метода Имфворккуеуесервицес:: Бегинунрегистертопологиворккуеуесвисммксс, поддерживающая удаленное взаимодействие.'
ms.assetid: 1a168462-400d-46c9-a489-7b861770469f
title: Ремотебегинунрегистертопологиворккуеуесвисммксс (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f52f82c55d692a2e1d9160c7a619338d82956ea0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910808"
---
# <a name="remotebeginunregistertopologyworkqueueswithmmcss"></a><span data-ttu-id="09456-103">ремотебегинунрегистертопологиворккуеуесвисммксс</span><span class="sxs-lookup"><span data-stu-id="09456-103">RemoteBeginUnregisterTopologyWorkQueuesWithMMCSS</span></span>

<span data-ttu-id="09456-104">Версия метода [**имфворккуеуесервицес:: бегинунрегистертопологиворккуеуесвисммксс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregistertopologyworkqueueswithmmcss) , поддерживающая удаленное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="09456-104">Remotable version of the [**IMFWorkQueueServices::BeginUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregistertopologyworkqueueswithmmcss) method.</span></span>

``` syntax
[call_as(BeginUnregisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteBeginUnregisterTopologyWorkQueuesWithMMCSS(
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="09456-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="09456-105">Remarks</span></span>

<span data-ttu-id="09456-106">Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод.</span><span class="sxs-lookup"><span data-stu-id="09456-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="09456-107">Метод не отображается в таблице vtable для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="09456-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="09456-108">Если [**бегинунрегистертопологиворккуеуесвисммксс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregistertopologyworkqueueswithmmcss) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.</span><span class="sxs-lookup"><span data-stu-id="09456-108">If [**BeginUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregistertopologyworkqueueswithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="09456-109">Требования</span><span class="sxs-lookup"><span data-stu-id="09456-109">Requirements</span></span>



| <span data-ttu-id="09456-110">Требование</span><span class="sxs-lookup"><span data-stu-id="09456-110">Requirement</span></span> | <span data-ttu-id="09456-111">Значение</span><span class="sxs-lookup"><span data-stu-id="09456-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09456-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="09456-112">Minimum supported client</span></span><br/> | <span data-ttu-id="09456-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="09456-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="09456-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="09456-114">Minimum supported server</span></span><br/> | <span data-ttu-id="09456-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="09456-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="09456-116">Header</span><span class="sxs-lookup"><span data-stu-id="09456-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="09456-117"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="09456-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="09456-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="09456-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="09456-119"><dt>Мфууид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="09456-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="09456-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="09456-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09456-121">**имфворккуеуесервицес**</span><span class="sxs-lookup"><span data-stu-id="09456-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




