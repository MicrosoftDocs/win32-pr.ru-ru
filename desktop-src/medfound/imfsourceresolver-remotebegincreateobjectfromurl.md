---
description: 'Версия метода Имфсаурцересолвер:: Бегинкреатеобжектфромурл, поддерживающая удаленное взаимодействие.'
ms.assetid: 3c0b0aaf-832b-4708-bed9-6f448770ee77
title: Ремотебегинкреатеобжектфромурл (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9d9a72ab5522b56fc0b78238f6a1dbc9aae0c6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701745"
---
# <a name="remotebegincreateobjectfromurl"></a><span data-ttu-id="83348-103">ремотебегинкреатеобжектфромурл</span><span class="sxs-lookup"><span data-stu-id="83348-103">RemoteBeginCreateObjectFromURL</span></span>

<span data-ttu-id="83348-104">Версия метода [**имфсаурцересолвер:: бегинкреатеобжектфромурл**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) , поддерживающая удаленное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="83348-104">Remotable version of the [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) method.</span></span>

``` syntax
[call_as(BeginCreateObjectFromURL)]
HRESULT RemoteBeginCreateObjectFromURL(
    LPCWSTR pwszURL,
    DWORD dwFlags,
    IPropertyStore *pProps,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="83348-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="83348-105">Remarks</span></span>

<span data-ttu-id="83348-106">Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод.</span><span class="sxs-lookup"><span data-stu-id="83348-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="83348-107">Метод не отображается в таблице vtable для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="83348-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="83348-108">Если [**бегинкреатеобжектфромурл**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.</span><span class="sxs-lookup"><span data-stu-id="83348-108">If [**BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="83348-109">Требования</span><span class="sxs-lookup"><span data-stu-id="83348-109">Requirements</span></span>



| <span data-ttu-id="83348-110">Требование</span><span class="sxs-lookup"><span data-stu-id="83348-110">Requirement</span></span> | <span data-ttu-id="83348-111">Значение</span><span class="sxs-lookup"><span data-stu-id="83348-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83348-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="83348-112">Minimum supported client</span></span><br/> | <span data-ttu-id="83348-113">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="83348-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="83348-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="83348-114">Minimum supported server</span></span><br/> | <span data-ttu-id="83348-115">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="83348-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="83348-116">Header</span><span class="sxs-lookup"><span data-stu-id="83348-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="83348-117"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="83348-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="83348-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="83348-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="83348-119"><dt>Мфууид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83348-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="83348-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="83348-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83348-121">**имфсаурцересолвер**</span><span class="sxs-lookup"><span data-stu-id="83348-121">**IMFSourceResolver**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




