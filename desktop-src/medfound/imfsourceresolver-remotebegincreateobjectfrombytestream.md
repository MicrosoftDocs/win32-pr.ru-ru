---
description: 'Версия метода Имфсаурцересолвер:: Бегинкреатеобжектфромбитестреам, поддерживающая удаленное взаимодействие.'
ms.assetid: 960b5c51-b9b1-4956-a270-abfb7eedd482
title: Ремотебегинкреатеобжектфромбитестреам (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2cf089f0b80e83373c36731de4bd9a36d8835b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701710"
---
# <a name="remotebegincreateobjectfrombytestream"></a><span data-ttu-id="1243e-103">ремотебегинкреатеобжектфромбитестреам</span><span class="sxs-lookup"><span data-stu-id="1243e-103">RemoteBeginCreateObjectFromByteStream</span></span>

<span data-ttu-id="1243e-104">Версия метода [**имфсаурцересолвер:: бегинкреатеобжектфромбитестреам**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) , поддерживающая удаленное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="1243e-104">Remotable version of the [**IMFSourceResolver::BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) method.</span></span>

``` syntax
[call_as(BeginCreateObjectFromByteStream)]
HRESULT RemoteBeginCreateObjectFromByteStream(
    IMFByteStream* pByteStream,
    LPCWSTR pwszURL,
    IPropertyStore *pProps,
    DWORD dwFlags,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="1243e-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1243e-105">Remarks</span></span>

<span data-ttu-id="1243e-106">Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод.</span><span class="sxs-lookup"><span data-stu-id="1243e-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="1243e-107">Метод не отображается в таблице vtable для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="1243e-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="1243e-108">Если [**бегинкреатеобжектфромбитестреам**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.</span><span class="sxs-lookup"><span data-stu-id="1243e-108">If [**BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="1243e-109">Требования</span><span class="sxs-lookup"><span data-stu-id="1243e-109">Requirements</span></span>



| <span data-ttu-id="1243e-110">Требование</span><span class="sxs-lookup"><span data-stu-id="1243e-110">Requirement</span></span> | <span data-ttu-id="1243e-111">Значение</span><span class="sxs-lookup"><span data-stu-id="1243e-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1243e-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1243e-112">Minimum supported client</span></span><br/> | <span data-ttu-id="1243e-113">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="1243e-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="1243e-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1243e-114">Minimum supported server</span></span><br/> | <span data-ttu-id="1243e-115">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="1243e-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="1243e-116">Header</span><span class="sxs-lookup"><span data-stu-id="1243e-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="1243e-117"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1243e-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="1243e-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1243e-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="1243e-119"><dt>Мфууид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1243e-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="1243e-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1243e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1243e-121">**имфсаурцересолвер**</span><span class="sxs-lookup"><span data-stu-id="1243e-121">**IMFSourceResolver**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




