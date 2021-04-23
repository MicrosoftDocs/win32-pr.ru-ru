---
description: 'Версия метода Имфворккуеуесервицес:: Бегинрегистерплатформворккуеуевисммксс, поддерживающая удаленное взаимодействие.'
ms.assetid: 158497a9-9d66-4e58-919d-e35765fd29e4
title: Ремотебегинрегистерплатформворккуеуевисммксс (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c7009def4e86a97720bc4b94eb2c9edb477afe0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912652"
---
# <a name="remotebeginregisterplatformworkqueuewithmmcss"></a><span data-ttu-id="5efca-103">ремотебегинрегистерплатформворккуеуевисммксс</span><span class="sxs-lookup"><span data-stu-id="5efca-103">RemoteBeginRegisterPlatformWorkQueueWithMMCSS</span></span>

<span data-ttu-id="5efca-104">Версия метода [**имфворккуеуесервицес:: бегинрегистерплатформворккуеуевисммксс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss) , поддерживающая удаленное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="5efca-104">Remotable version of the [**IMFWorkQueueServices::BeginRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss) method.</span></span>

``` syntax
[call_as(BeginRegisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteBeginRegisterPlatformWorkQueueWithMMCSS(
    DWORD dwPlatformWorkQueue,
    LPCWSTR wszClass,
    DWORD dwTaskId,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="5efca-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5efca-105">Remarks</span></span>

<span data-ttu-id="5efca-106">Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод.</span><span class="sxs-lookup"><span data-stu-id="5efca-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="5efca-107">Метод не отображается в таблице vtable для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5efca-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="5efca-108">Если [**бегинрегистерплатформворккуеуевисммксс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.</span><span class="sxs-lookup"><span data-stu-id="5efca-108">If [**BeginRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="5efca-109">Требования</span><span class="sxs-lookup"><span data-stu-id="5efca-109">Requirements</span></span>



| <span data-ttu-id="5efca-110">Требование</span><span class="sxs-lookup"><span data-stu-id="5efca-110">Requirement</span></span> | <span data-ttu-id="5efca-111">Значение</span><span class="sxs-lookup"><span data-stu-id="5efca-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5efca-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5efca-112">Minimum supported client</span></span><br/> | <span data-ttu-id="5efca-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5efca-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5efca-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5efca-114">Minimum supported server</span></span><br/> | <span data-ttu-id="5efca-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5efca-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5efca-116">Header</span><span class="sxs-lookup"><span data-stu-id="5efca-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="5efca-117"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5efca-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="5efca-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5efca-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="5efca-119"><dt>Мфууид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5efca-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="5efca-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5efca-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5efca-121">**имфворккуеуесервицес**</span><span class="sxs-lookup"><span data-stu-id="5efca-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




