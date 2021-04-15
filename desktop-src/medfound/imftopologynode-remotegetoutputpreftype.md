---
description: 'Версия метода Имфтопологиноде:: Жетаутпутпрефтипе, поддерживающая удаленное взаимодействие.'
ms.assetid: 56fbbf14-0c55-4f98-bcda-7f434cff803c
title: Ремотежетаутпутпрефтипе (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46069add8f9d15a2b3742a083a1cf169a46b969f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701709"
---
# <a name="remotegetoutputpreftype"></a><span data-ttu-id="cb463-103">ремотежетаутпутпрефтипе</span><span class="sxs-lookup"><span data-stu-id="cb463-103">RemoteGetOutputPrefType</span></span>

<span data-ttu-id="cb463-104">Версия метода [**имфтопологиноде:: жетаутпутпрефтипе**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getoutputpreftype) , поддерживающая удаленное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="cb463-104">Remotable version of the [**IMFTopologyNode::GetOutputPrefType**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getoutputpreftype) method.</span></span>

``` syntax
[call_as(GetOutputPrefType)] 
HRESULT RemoteGetOutputPrefType(
    DWORD dwOutputIndex,
    DWORD *pcbData,
    BYTE **ppbData
);
```

## <a name="remarks"></a><span data-ttu-id="cb463-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb463-105">Remarks</span></span>

<span data-ttu-id="cb463-106">Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод.</span><span class="sxs-lookup"><span data-stu-id="cb463-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="cb463-107">Метод не отображается в таблице vtable для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="cb463-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="cb463-108">Если **жетаутпутпрефтипе** вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.</span><span class="sxs-lookup"><span data-stu-id="cb463-108">If **GetOutputPrefType** is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb463-109">Требования</span><span class="sxs-lookup"><span data-stu-id="cb463-109">Requirements</span></span>



| <span data-ttu-id="cb463-110">Требование</span><span class="sxs-lookup"><span data-stu-id="cb463-110">Requirement</span></span> | <span data-ttu-id="cb463-111">Значение</span><span class="sxs-lookup"><span data-stu-id="cb463-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb463-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cb463-112">Minimum supported client</span></span><br/> | <span data-ttu-id="cb463-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cb463-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cb463-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cb463-114">Minimum supported server</span></span><br/> | <span data-ttu-id="cb463-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cb463-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cb463-116">Header</span><span class="sxs-lookup"><span data-stu-id="cb463-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb463-117"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb463-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="cb463-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cb463-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="cb463-119"><dt>Мфууид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb463-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="cb463-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb463-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb463-121">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="cb463-121">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 




