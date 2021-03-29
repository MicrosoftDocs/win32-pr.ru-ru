---
description: 'Версия метода Имфмедиаевентженератор:: Бегинжетевент, поддерживающая удаленное взаимодействие.'
ms.assetid: 96a16fd3-10bc-4cd9-967a-ceb92e26ccc8
title: Ремотебегинжетевент (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d728653df99baf0e816c53d8d22d7720c9aefac9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898185"
---
# <a name="remotebegingetevent"></a><span data-ttu-id="61ee2-103">ремотебегинжетевент</span><span class="sxs-lookup"><span data-stu-id="61ee2-103">RemoteBeginGetEvent</span></span>

<span data-ttu-id="61ee2-104">Версия метода [**имфмедиаевентженератор:: бегинжетевент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) , поддерживающая удаленное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="61ee2-104">Remotable version of the [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) method.</span></span>

``` syntax
[call_as(BeginGetEvent)]
HRESULT RemoteBeginGetEvent(
    IMFRemoteAsyncCallback* pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="61ee2-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="61ee2-105">Remarks</span></span>

<span data-ttu-id="61ee2-106">Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод.</span><span class="sxs-lookup"><span data-stu-id="61ee2-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="61ee2-107">Метод не отображается в таблице vtable для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="61ee2-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="61ee2-108">Если [**бегинжетевент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.</span><span class="sxs-lookup"><span data-stu-id="61ee2-108">If [**BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="61ee2-109">Требования</span><span class="sxs-lookup"><span data-stu-id="61ee2-109">Requirements</span></span>



| <span data-ttu-id="61ee2-110">Требование</span><span class="sxs-lookup"><span data-stu-id="61ee2-110">Requirement</span></span> | <span data-ttu-id="61ee2-111">Значение</span><span class="sxs-lookup"><span data-stu-id="61ee2-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61ee2-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="61ee2-112">Minimum supported client</span></span><br/> | <span data-ttu-id="61ee2-113">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="61ee2-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="61ee2-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="61ee2-114">Minimum supported server</span></span><br/> | <span data-ttu-id="61ee2-115">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="61ee2-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="61ee2-116">Header</span><span class="sxs-lookup"><span data-stu-id="61ee2-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="61ee2-117"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="61ee2-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="61ee2-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="61ee2-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="61ee2-119"><dt>Мфууид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="61ee2-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="61ee2-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61ee2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61ee2-121">**имфмедиаевентженератор**</span><span class="sxs-lookup"><span data-stu-id="61ee2-121">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
</dt> </dl>

 

 




