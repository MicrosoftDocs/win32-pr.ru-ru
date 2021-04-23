---
description: 'Версия Имфворккуеуесервицесекс:: Бегинрегистерплатформворккуеуевисммкссекс, поддерживающая удаленное взаимодействие.'
ms.assetid: 75af7ce6-9b74-4d61-b7f2-5d07538f91cf
title: ремотебегинрегистерплатформворккуеуевисммкссекс
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9d519d13f1e23927f1d34a18d5c5f860e007881
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272385"
---
# <a name="remotebeginregisterplatformworkqueuewithmmcssex"></a><span data-ttu-id="3c480-103">ремотебегинрегистерплатформворккуеуевисммкссекс</span><span class="sxs-lookup"><span data-stu-id="3c480-103">RemoteBeginRegisterPlatformWorkQueueWithMMCSSEx</span></span>

<span data-ttu-id="3c480-104">Версия [**имфворккуеуесервицесекс:: бегинрегистерплатформворккуеуевисммкссекс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex), поддерживающая удаленное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="3c480-104">Remotable version of [**IMFWorkQueueServicesEX::BeginRegisterPlatformWorkQueueWithMMCSSEx**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex).</span></span>

``` syntax
[call_as(BeginRegisterPlatformWorkQueueWithMMCSSEx)]
HRESULT RemoteBeginRegisterPlatformWorkQueueWithMMCSSEx(
    DWORD dwPlatformWorkQueue,
    LPCWSTR wszClass,
    DWORD dwTaskId, 
    LONG lPriority,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="3c480-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3c480-105">Remarks</span></span>

<span data-ttu-id="3c480-106">Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод.</span><span class="sxs-lookup"><span data-stu-id="3c480-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="3c480-107">Метод не отображается в таблице vtable для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3c480-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="3c480-108">Если [**бегинрегистерплатформворккуеуевисммкссекс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.</span><span class="sxs-lookup"><span data-stu-id="3c480-108">If [**BeginRegisterPlatformWorkQueueWithMMCSSEx**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c480-109">Требования</span><span class="sxs-lookup"><span data-stu-id="3c480-109">Requirements</span></span>



| <span data-ttu-id="3c480-110">Требование</span><span class="sxs-lookup"><span data-stu-id="3c480-110">Requirement</span></span> | <span data-ttu-id="3c480-111">Значение</span><span class="sxs-lookup"><span data-stu-id="3c480-111">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3c480-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c480-112">Minimum supported client</span></span><br/> | <span data-ttu-id="3c480-113">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3c480-113">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3c480-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c480-114">Minimum supported server</span></span><br/> | <span data-ttu-id="3c480-115">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3c480-115">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3c480-116">Header</span><span class="sxs-lookup"><span data-stu-id="3c480-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c480-117"><dt>Мфидл. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3c480-117"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c480-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c480-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c480-119">**имфворккуеуесервицесекс**</span><span class="sxs-lookup"><span data-stu-id="3c480-119">**IMFWorkQueueServicesEx**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservicesex)
</dt> </dl>

 

 




