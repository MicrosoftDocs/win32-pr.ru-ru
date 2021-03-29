---
description: 'Версия метода Имфтопологиноде:: Жетинпутпрефтипе, поддерживающая удаленное взаимодействие.'
ms.assetid: b02cf739-97a9-4bb0-abb1-0da491857c50
title: Ремотежетинпутпрефтипе (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6461e804d6066b467378742ff02c8e708f5f6714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810816"
---
# <a name="remotegetinputpreftype"></a><span data-ttu-id="69e59-103">ремотежетинпутпрефтипе</span><span class="sxs-lookup"><span data-stu-id="69e59-103">RemoteGetInputPrefType</span></span>

<span data-ttu-id="69e59-104">Версия метода [**имфтопологиноде:: жетинпутпрефтипе**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype) , поддерживающая удаленное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="69e59-104">Remotable version of the [**IMFTopologyNode::GetInputPrefType**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype) method.</span></span>

``` syntax
[call_as(GetInputPrefType)] 
HRESULT RemoteGetInputPrefType(
    DWORD dwInputIndex,
    DWORD *pcbData,
    BYTE **ppbData
);
```

## <a name="remarks"></a><span data-ttu-id="69e59-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="69e59-105">Remarks</span></span>

<span data-ttu-id="69e59-106">Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод.</span><span class="sxs-lookup"><span data-stu-id="69e59-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="69e59-107">Метод не отображается в таблице vtable для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="69e59-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="69e59-108">Если [**жетинпутпрефтипе**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.</span><span class="sxs-lookup"><span data-stu-id="69e59-108">If [**GetInputPrefType**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="69e59-109">Требования</span><span class="sxs-lookup"><span data-stu-id="69e59-109">Requirements</span></span>



| <span data-ttu-id="69e59-110">Требование</span><span class="sxs-lookup"><span data-stu-id="69e59-110">Requirement</span></span> | <span data-ttu-id="69e59-111">Значение</span><span class="sxs-lookup"><span data-stu-id="69e59-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69e59-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="69e59-112">Minimum supported client</span></span><br/> | <span data-ttu-id="69e59-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="69e59-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="69e59-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="69e59-114">Minimum supported server</span></span><br/> | <span data-ttu-id="69e59-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="69e59-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="69e59-116">Header</span><span class="sxs-lookup"><span data-stu-id="69e59-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="69e59-117"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="69e59-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="69e59-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="69e59-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="69e59-119"><dt>Мфууид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69e59-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="69e59-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="69e59-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69e59-121">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="69e59-121">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 




