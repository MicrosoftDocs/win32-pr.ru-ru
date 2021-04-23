---
description: 'Версия метода Имфмедиасаурце:: Креатепресентатиондескриптор, поддерживающая удаленное взаимодействие.'
ms.assetid: 9ad6793e-32ca-471b-8639-41098b3e8216
title: Ремотекреатепресентатиондескриптор (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c02d78c1febe8c1a82ae3e91c50e06c750bcfef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155327"
---
# <a name="remotecreatepresentationdescriptor"></a><span data-ttu-id="3e147-103">ремотекреатепресентатиондескриптор</span><span class="sxs-lookup"><span data-stu-id="3e147-103">RemoteCreatePresentationDescriptor</span></span>

<span data-ttu-id="3e147-104">Версия метода [**имфмедиасаурце:: креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) , поддерживающая удаленное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="3e147-104">Remotable version of the [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) method.</span></span>

``` syntax
[call_as(CreatePresentationDescriptor)]
HRESULT RemoteCreatePresentationDescriptor(
    DWORD *pcbPD,
    BYTE **pbPD,
    IMFPresentationDescriptor **ppRemotePD
);
```

## <a name="remarks"></a><span data-ttu-id="3e147-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3e147-105">Remarks</span></span>

<span data-ttu-id="3e147-106">Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод.</span><span class="sxs-lookup"><span data-stu-id="3e147-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="3e147-107">Метод не отображается в таблице vtable для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3e147-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="3e147-108">Если [**креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.</span><span class="sxs-lookup"><span data-stu-id="3e147-108">If [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e147-109">Требования</span><span class="sxs-lookup"><span data-stu-id="3e147-109">Requirements</span></span>



| <span data-ttu-id="3e147-110">Требование</span><span class="sxs-lookup"><span data-stu-id="3e147-110">Requirement</span></span> | <span data-ttu-id="3e147-111">Значение</span><span class="sxs-lookup"><span data-stu-id="3e147-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e147-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3e147-112">Minimum supported client</span></span><br/> | <span data-ttu-id="3e147-113">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="3e147-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="3e147-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3e147-114">Minimum supported server</span></span><br/> | <span data-ttu-id="3e147-115">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="3e147-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="3e147-116">Header</span><span class="sxs-lookup"><span data-stu-id="3e147-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e147-117"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e147-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="3e147-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3e147-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="3e147-119"><dt>Мфууид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e147-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="3e147-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e147-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e147-121">**имфмедиасаурце**</span><span class="sxs-lookup"><span data-stu-id="3e147-121">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> </dl>

 

 




