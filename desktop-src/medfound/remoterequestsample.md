---
description: 'Версия метода Имфмедиастреам:: Рекуестсампле, поддерживающая удаленное взаимодействие.'
ms.assetid: 05ed4de0-fe5c-4183-8f1d-55d5a27e436a
title: Ремотерекуестсампле (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c8b06f0501de9cc041bf5776adb5e17e59a8c17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701795"
---
# <a name="remoterequestsample"></a><span data-ttu-id="a9fde-103">ремотерекуестсампле</span><span class="sxs-lookup"><span data-stu-id="a9fde-103">RemoteRequestSample</span></span>

<span data-ttu-id="a9fde-104">Версия метода [**имфмедиастреам:: рекуестсампле**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) , поддерживающая удаленное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="a9fde-104">Remotable version of the [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method.</span></span>

``` syntax
[call_as(RequestSample)]
HRESULT RemoteRequestSample();
```

## <a name="remarks"></a><span data-ttu-id="a9fde-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a9fde-105">Remarks</span></span>

<span data-ttu-id="a9fde-106">Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод.</span><span class="sxs-lookup"><span data-stu-id="a9fde-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="a9fde-107">Метод не отображается в таблице vtable для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a9fde-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="a9fde-108">Если [**рекуестсампле**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.</span><span class="sxs-lookup"><span data-stu-id="a9fde-108">If [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9fde-109">Требования</span><span class="sxs-lookup"><span data-stu-id="a9fde-109">Requirements</span></span>



| <span data-ttu-id="a9fde-110">Требование</span><span class="sxs-lookup"><span data-stu-id="a9fde-110">Requirement</span></span> | <span data-ttu-id="a9fde-111">Значение</span><span class="sxs-lookup"><span data-stu-id="a9fde-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9fde-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a9fde-112">Minimum supported client</span></span><br/> | <span data-ttu-id="a9fde-113">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="a9fde-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="a9fde-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a9fde-114">Minimum supported server</span></span><br/> | <span data-ttu-id="a9fde-115">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="a9fde-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="a9fde-116">Header</span><span class="sxs-lookup"><span data-stu-id="a9fde-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9fde-117"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9fde-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="a9fde-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a9fde-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="a9fde-119"><dt>Мфууид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9fde-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="a9fde-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a9fde-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9fde-121">**имфмедиастреам**</span><span class="sxs-lookup"><span data-stu-id="a9fde-121">**IMFMediaStream**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)
</dt> </dl>

 

 




