---
description: Задает обратный вызов, который создает сеанс мультимедиа PMP во время разрешения источника.
ms.assetid: 7277C5E0-BB91-4EEA-9529-64E66D179CDC
title: Свойство MFPKEY_PMP_Creation_Callback (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2b18e04a15e035a9e4dc04a4039ce230342031a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263981"
---
# <a name="mfpkey_pmp_creation_callback-property"></a><span data-ttu-id="c8278-103">\_ \_ \_ Свойство обратного вызова создания PMP мфпкэй</span><span class="sxs-lookup"><span data-stu-id="c8278-103">MFPKEY\_PMP\_Creation\_Callback property</span></span>

<span data-ttu-id="c8278-104">Задает обратный вызов, который создает [сеанс мультимедиа PMP](pmp-media-session.md) во время разрешения источника.</span><span class="sxs-lookup"><span data-stu-id="c8278-104">Sets a callback that creates the [PMP Media Session](pmp-media-session.md) during source resolution.</span></span>



<span data-ttu-id="c8278-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c8278-105">Data type</span></span>

<span data-ttu-id="c8278-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="c8278-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="c8278-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="c8278-107">PROPVARIANT member</span></span>

<span data-ttu-id="c8278-108">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="c8278-108">\**IUnknown\** _</span></span>

<span data-ttu-id="c8278-109">VT \_ Unknown</span><span class="sxs-lookup"><span data-stu-id="c8278-109">VT\_UNKNOWN</span></span>

<span data-ttu-id="c8278-110">_ *пунквал*\*</span><span class="sxs-lookup"><span data-stu-id="c8278-110">_ *punkVal*\*</span></span>



## <a name="remarks"></a><span data-ttu-id="c8278-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c8278-111">Remarks</span></span>

<span data-ttu-id="c8278-112">Для некоторых защищенных содержимого может потребоваться использование этого свойства.</span><span class="sxs-lookup"><span data-stu-id="c8278-112">Some protected content might require the use of this property.</span></span> <span data-ttu-id="c8278-113">Если это так, то процесс разрешения источника завершается ошибкой с кодом ошибки **MF \_ E, \_ \_ требующего \_ \_ \_ обратного вызова при создании PMP**.</span><span class="sxs-lookup"><span data-stu-id="c8278-113">If so, the source resolution process fails with the error code **MF\_E\_RESOLUTION\_REQUIRES\_PMP\_CREATION\_CALLBACK**.</span></span>

<span data-ttu-id="c8278-114">Чтобы использовать это свойство, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c8278-114">To use this property, do the following.</span></span>

1.  <span data-ttu-id="c8278-115">Вызовите [**пскреатемеморипропертисторе**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) , чтобы создать хранилище свойств.</span><span class="sxs-lookup"><span data-stu-id="c8278-115">Call [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) to create a property store.</span></span>
2.  <span data-ttu-id="c8278-116">Реализуйте интерфейс обратного вызова [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="c8278-116">Implement the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) callback interface.</span></span>
3.  <span data-ttu-id="c8278-117">Задайте \_ \_ \_ свойство обратного вызова создания PMP мфпкэй для хранилища свойств.</span><span class="sxs-lookup"><span data-stu-id="c8278-117">Set the MFPKEY\_PMP\_Creation\_Callback property on the property store.</span></span> <span data-ttu-id="c8278-118">Значение является указателем на реализацию [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="c8278-118">The value is a pointer to the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) implementation.</span></span>
4.  <span data-ttu-id="c8278-119">Вызовите [**имфсаурцересолвер:: бегинкреатеобжектфромурл**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span><span class="sxs-lookup"><span data-stu-id="c8278-119">Call [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span></span> <span data-ttu-id="c8278-120">Передайте указатель на хранилище свойств в параметре *ппропс* .</span><span class="sxs-lookup"><span data-stu-id="c8278-120">Pass in a pointer to the property store in the *pProps* parameter.</span></span>

<span data-ttu-id="c8278-121">В методе [**имфасинккаллбакк:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) интерфейса ответного вызова выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c8278-121">In the [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method of your callback interface, do the following.</span></span>

1.  <span data-ttu-id="c8278-122">Вызовите [**мфкреатепмпмедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) , чтобы создать [сеанс PMP мультимедиа](pmp-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="c8278-122">Call [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) to create the [PMP Media Session](pmp-media-session.md).</span></span>
2.  <span data-ttu-id="c8278-123">Вызовите [**имфжетсервице::-Service**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) в сеансе PMP Media, чтобы указатель на интерфейс [**имфпмфост**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) .</span><span class="sxs-lookup"><span data-stu-id="c8278-123">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the PMP Media Session to a pointer to the [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) interface.</span></span>
3.  <span data-ttu-id="c8278-124">Вызовите [**имфасинкресулт::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate) GetObject для результирующего объекта, который передается в параметре *пасинкресулт* метода [**имфасинккаллбакк:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span><span class="sxs-lookup"><span data-stu-id="c8278-124">Call [**IMFAsyncResult::GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate) on the result object that is passed in the *pAsyncResult* parameter of [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span></span> <span data-ttu-id="c8278-125">Запросите возвращенный указатель [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) для интерфейса [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="c8278-125">Query the returned [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer for the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
4.  <span data-ttu-id="c8278-126">Вызовите [**мфпутворкитем**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="c8278-126">Call [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) with the following parameters:</span></span>
    -   <span data-ttu-id="c8278-127">*dwQueue*: **\_ \_ \_ стандартная очередь обратного вызова мфасинк**</span><span class="sxs-lookup"><span data-stu-id="c8278-127">*dwQueue*: **MFASYNC\_CALLBACK\_QUEUE\_STANDARD**</span></span>
    -   <span data-ttu-id="c8278-128">*пкаллбакк*: указатель [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , полученный на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="c8278-128">*pCallback*: The [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) pointer obtained in step 3.</span></span>
    -   <span data-ttu-id="c8278-129">*пстате*: указатель [**имфпмфост**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) , полученный на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="c8278-129">*pState*: The [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) pointer obtained in step 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8278-130">Требования</span><span class="sxs-lookup"><span data-stu-id="c8278-130">Requirements</span></span>



| <span data-ttu-id="c8278-131">Требование</span><span class="sxs-lookup"><span data-stu-id="c8278-131">Requirement</span></span> | <span data-ttu-id="c8278-132">Значение</span><span class="sxs-lookup"><span data-stu-id="c8278-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c8278-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c8278-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c8278-134">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="c8278-134">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="c8278-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c8278-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c8278-136">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="c8278-136">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="c8278-137">Header</span><span class="sxs-lookup"><span data-stu-id="c8278-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8278-138"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8278-138"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8278-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c8278-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8278-140">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c8278-140">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="c8278-141">Сеанс PMP мультимедиа</span><span class="sxs-lookup"><span data-stu-id="c8278-141">PMP Media Session</span></span>](pmp-media-session.md)
</dt> <dt>

[<span data-ttu-id="c8278-142">Путь к защищенному носителю</span><span class="sxs-lookup"><span data-stu-id="c8278-142">Protected Media Path</span></span>](protected-media-path.md)
</dt> <dt>

[<span data-ttu-id="c8278-143">Сопоставитель источников</span><span class="sxs-lookup"><span data-stu-id="c8278-143">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 
