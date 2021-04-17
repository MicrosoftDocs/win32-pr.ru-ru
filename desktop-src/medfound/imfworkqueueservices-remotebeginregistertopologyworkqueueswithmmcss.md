---
description: 'Версия метода Имфворккуеуесервицес:: Бегинрегистертопологиворккуеуесвисммксс, поддерживающая удаленное взаимодействие.'
ms.assetid: 1ea258c9-1f7f-4324-a17a-d044a4864ea4
title: Ремотебегинрегистертопологиворккуеуесвисммксс (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 448008c29e34574263f04ebbc7dee54d60b6f4ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693522"
---
# <a name="remotebeginregistertopologyworkqueueswithmmcss"></a><span data-ttu-id="ae71b-103">ремотебегинрегистертопологиворккуеуесвисммксс</span><span class="sxs-lookup"><span data-stu-id="ae71b-103">RemoteBeginRegisterTopologyWorkQueuesWithMMCSS</span></span>

<span data-ttu-id="ae71b-104">Версия метода [**имфворккуеуесервицес:: бегинрегистертопологиворккуеуесвисммксс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) , поддерживающая удаленное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="ae71b-104">Remotable version of the [**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) method.</span></span>

``` syntax
[call_as(BeginRegisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteBeginRegisterTopologyWorkQueuesWithMMCSS(
    IMFRemoteAsyncCallback *pCallback
); 
```

## <a name="remarks"></a><span data-ttu-id="ae71b-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ae71b-105">Remarks</span></span>

<span data-ttu-id="ae71b-106">Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод.</span><span class="sxs-lookup"><span data-stu-id="ae71b-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="ae71b-107">Метод не отображается в таблице vtable для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ae71b-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="ae71b-108">Если [**бегинрегистертопологиворккуеуесвисммксс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.</span><span class="sxs-lookup"><span data-stu-id="ae71b-108">If [**BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae71b-109">Требования</span><span class="sxs-lookup"><span data-stu-id="ae71b-109">Requirements</span></span>



| <span data-ttu-id="ae71b-110">Требование</span><span class="sxs-lookup"><span data-stu-id="ae71b-110">Requirement</span></span> | <span data-ttu-id="ae71b-111">Значение</span><span class="sxs-lookup"><span data-stu-id="ae71b-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae71b-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ae71b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ae71b-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ae71b-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ae71b-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ae71b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ae71b-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ae71b-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ae71b-116">Header</span><span class="sxs-lookup"><span data-stu-id="ae71b-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae71b-117"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae71b-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="ae71b-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ae71b-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="ae71b-119"><dt>Мфууид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae71b-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="ae71b-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ae71b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae71b-121">**имфворккуеуесервицес**</span><span class="sxs-lookup"><span data-stu-id="ae71b-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




