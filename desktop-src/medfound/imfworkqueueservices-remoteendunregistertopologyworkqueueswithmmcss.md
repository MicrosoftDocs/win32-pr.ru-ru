---
description: 'Версия метода Имфворккуеуесервицес:: Ендунрегистертопологиворккуеуесвисммксс, поддерживающая удаленное взаимодействие.'
ms.assetid: 8767a145-07b9-4427-9446-cee25e9074fa
title: Ремотиндунрегистертопологиворккуеуесвисммксс (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd1131fcd920e306bc6d5f2954c283d41d61310f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712262"
---
# <a name="remoteendunregistertopologyworkqueueswithmmcss"></a><span data-ttu-id="123d0-103">ремотиндунрегистертопологиворккуеуесвисммксс</span><span class="sxs-lookup"><span data-stu-id="123d0-103">RemoteEndUnregisterTopologyWorkQueuesWithMMCSS</span></span>

<span data-ttu-id="123d0-104">Версия метода [**имфворккуеуесервицес:: ендунрегистертопологиворккуеуесвисммксс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss) , поддерживающая удаленное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="123d0-104">Remotable version of the [**IMFWorkQueueServices::EndUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss) method.</span></span>

``` syntax
[call_as(EndUnregisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteEndUnregisterTopologyWorkQueuesWithMMCSS(
    IUnknown *pResult
);
```

## <a name="remarks"></a><span data-ttu-id="123d0-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="123d0-105">Remarks</span></span>

<span data-ttu-id="123d0-106">Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод.</span><span class="sxs-lookup"><span data-stu-id="123d0-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="123d0-107">Метод не отображается в таблице vtable для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="123d0-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="123d0-108">Если [**ендунрегистертопологиворккуеуесвисммксс**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.</span><span class="sxs-lookup"><span data-stu-id="123d0-108">If [**EndUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="123d0-109">Требования</span><span class="sxs-lookup"><span data-stu-id="123d0-109">Requirements</span></span>



| <span data-ttu-id="123d0-110">Требование</span><span class="sxs-lookup"><span data-stu-id="123d0-110">Requirement</span></span> | <span data-ttu-id="123d0-111">Значение</span><span class="sxs-lookup"><span data-stu-id="123d0-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="123d0-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="123d0-112">Minimum supported client</span></span><br/> | <span data-ttu-id="123d0-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="123d0-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="123d0-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="123d0-114">Minimum supported server</span></span><br/> | <span data-ttu-id="123d0-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="123d0-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="123d0-116">Header</span><span class="sxs-lookup"><span data-stu-id="123d0-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="123d0-117"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="123d0-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="123d0-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="123d0-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="123d0-119"><dt>Мфууид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="123d0-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="123d0-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="123d0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="123d0-121">**имфворккуеуесервицес**</span><span class="sxs-lookup"><span data-stu-id="123d0-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




