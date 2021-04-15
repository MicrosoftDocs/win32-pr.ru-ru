---
description: 'Версия метода Имфсаурцересолвер:: Ендкреатеобжектфромурл, поддерживающая удаленное взаимодействие.'
ms.assetid: 42764869-9cbc-4f41-a3af-f2d869db9f99
title: Ремотиндкреатеобжектфромурл (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26fff650dca012b58dc6fd46b26f13b1c2ac3c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701691"
---
# <a name="remoteendcreateobjectfromurl"></a><span data-ttu-id="dadfb-103">ремотиндкреатеобжектфромурл</span><span class="sxs-lookup"><span data-stu-id="dadfb-103">RemoteEndCreateObjectFromURL</span></span>

<span data-ttu-id="dadfb-104">Версия метода [**имфсаурцересолвер:: ендкреатеобжектфромурл**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) , поддерживающая удаленное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="dadfb-104">Remotable version of the [**IMFSourceResolver::EndCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) method.</span></span>

``` syntax
[call_as(EndCreateObjectFromURL)]
HRESULT RemoteEndCreateObjectFromURL(
    IUnknown *pResult,
    MF_OBJECT_TYPE *pObjectType,
    IUnknown **ppObject
);
```

## <a name="remarks"></a><span data-ttu-id="dadfb-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dadfb-105">Remarks</span></span>

<span data-ttu-id="dadfb-106">Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод.</span><span class="sxs-lookup"><span data-stu-id="dadfb-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="dadfb-107">Метод не отображается в таблице vtable для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="dadfb-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="dadfb-108">Если [**ендкреатеобжектфромурл**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.</span><span class="sxs-lookup"><span data-stu-id="dadfb-108">If [**EndCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="dadfb-109">Требования</span><span class="sxs-lookup"><span data-stu-id="dadfb-109">Requirements</span></span>



| <span data-ttu-id="dadfb-110">Требование</span><span class="sxs-lookup"><span data-stu-id="dadfb-110">Requirement</span></span> | <span data-ttu-id="dadfb-111">Значение</span><span class="sxs-lookup"><span data-stu-id="dadfb-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dadfb-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dadfb-112">Minimum supported client</span></span><br/> | <span data-ttu-id="dadfb-113">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="dadfb-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="dadfb-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dadfb-114">Minimum supported server</span></span><br/> | <span data-ttu-id="dadfb-115">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="dadfb-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="dadfb-116">Header</span><span class="sxs-lookup"><span data-stu-id="dadfb-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="dadfb-117"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dadfb-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="dadfb-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dadfb-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="dadfb-119"><dt>Мфууид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dadfb-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="dadfb-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dadfb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dadfb-121">**имфсаурцересолвер**</span><span class="sxs-lookup"><span data-stu-id="dadfb-121">**IMFSourceResolver**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




