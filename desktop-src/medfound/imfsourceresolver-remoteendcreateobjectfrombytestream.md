---
description: 'Версия метода Имфсаурцересолвер:: Ендкреатеобжектфромбитестреам, поддерживающая удаленное взаимодействие.'
ms.assetid: 6e4e9ace-e18a-45df-b20c-28e352fcdee7
title: Ремотиндкреатеобжектфромбитестреам (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba53b7d22ed79cb97edba034dc4c61d9aa27fa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154995"
---
# <a name="remoteendcreateobjectfrombytestream"></a><span data-ttu-id="c2ddd-103">ремотиндкреатеобжектфромбитестреам</span><span class="sxs-lookup"><span data-stu-id="c2ddd-103">RemoteEndCreateObjectFromByteStream</span></span>

<span data-ttu-id="c2ddd-104">Версия метода [**имфсаурцересолвер:: ендкреатеобжектфромбитестреам**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfrombytestream) , поддерживающая удаленное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="c2ddd-104">Remotable version of the [**IMFSourceResolver::EndCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfrombytestream) method.</span></span>

``` syntax
[call_as(EndCreateObjectFromByteStream)]
HRESULT RemoteEndCreateObjectFromByteStream(
    IUnknown *pResult,
    MF_OBJECT_TYPE *pObjectType,
    IUnknown **ppObject
);
```

## <a name="remarks"></a><span data-ttu-id="c2ddd-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c2ddd-105">Remarks</span></span>

<span data-ttu-id="c2ddd-106">Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод.</span><span class="sxs-lookup"><span data-stu-id="c2ddd-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="c2ddd-107">Метод не отображается в таблице vtable для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c2ddd-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="c2ddd-108">Если [**ендкреатеобжектфромбитестреам**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfrombytestream) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.</span><span class="sxs-lookup"><span data-stu-id="c2ddd-108">If [**EndCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfrombytestream) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2ddd-109">Требования</span><span class="sxs-lookup"><span data-stu-id="c2ddd-109">Requirements</span></span>



| <span data-ttu-id="c2ddd-110">Требование</span><span class="sxs-lookup"><span data-stu-id="c2ddd-110">Requirement</span></span> | <span data-ttu-id="c2ddd-111">Значение</span><span class="sxs-lookup"><span data-stu-id="c2ddd-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2ddd-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c2ddd-112">Minimum supported client</span></span><br/> | <span data-ttu-id="c2ddd-113">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="c2ddd-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="c2ddd-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c2ddd-114">Minimum supported server</span></span><br/> | <span data-ttu-id="c2ddd-115">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="c2ddd-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="c2ddd-116">Header</span><span class="sxs-lookup"><span data-stu-id="c2ddd-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2ddd-117"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2ddd-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="c2ddd-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c2ddd-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="c2ddd-119"><dt>Мфууид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2ddd-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="c2ddd-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c2ddd-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2ddd-121">**имфсаурцересолвер**</span><span class="sxs-lookup"><span data-stu-id="c2ddd-121">**IMFSourceResolver**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




