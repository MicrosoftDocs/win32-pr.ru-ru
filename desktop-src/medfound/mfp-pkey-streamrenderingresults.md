---
description: Указывает, какие потоки были успешно подключены к приемнику мультимедиа.
ms.assetid: b5e45bfc-d91d-41b8-aaa4-72b3a23d869e
title: Свойство MFP_PKEY_StreamRenderingResults (Мфплай. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6acf04f751e8611f3add3a62fc7b4406d757999e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343925"
---
# <a name="mfp_pkey_streamrenderingresults-property"></a><span data-ttu-id="6a706-103">МФП \_ PKEY \_ стреамрендерингресултс, свойство</span><span class="sxs-lookup"><span data-stu-id="6a706-103">MFP\_PKEY\_StreamRenderingResults property</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6a706-104">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="6a706-104">Deprecated.</span></span> <span data-ttu-id="6a706-105">Этот API может быть удален из будущих выпусков Windows.</span><span class="sxs-lookup"><span data-stu-id="6a706-105">This API may be removed from future releases of Windows.</span></span> <span data-ttu-id="6a706-106">Приложения должны использовать [сеанс мультимедиа](media-session.md) для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="6a706-106">Applications should use the [Media Session](media-session.md) for playback.</span></span>

 

<span data-ttu-id="6a706-107">Указывает, какие потоки были успешно подключены к приемнику мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="6a706-107">Specifies which streams were connected successfully to a media sink.</span></span>



<span data-ttu-id="6a706-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6a706-108">Data type</span></span>

<span data-ttu-id="6a706-109">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="6a706-109">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="6a706-110">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="6a706-110">PROPVARIANT member</span></span>

<span data-ttu-id="6a706-111">Массив значений **типа DWORD** (**Каул**)</span><span class="sxs-lookup"><span data-stu-id="6a706-111">Array of **DWORD** values (**CAUL**)</span></span>

<span data-ttu-id="6a706-112">VT \_ вектор \| VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="6a706-112">VT\_VECTOR \| VT\_UI4</span></span>

<span data-ttu-id="6a706-113">**каул**</span><span class="sxs-lookup"><span data-stu-id="6a706-113">**caul**</span></span>



## <a name="remarks"></a><span data-ttu-id="6a706-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6a706-114">Remarks</span></span>

<span data-ttu-id="6a706-115">Это свойство может быть отправлено с событием **МФП \_ \_ типа события \_ MEDIAITEM \_ Set** .</span><span class="sxs-lookup"><span data-stu-id="6a706-115">This property can be sent with the **MFP\_EVENT\_TYPE\_MEDIAITEM\_SET** event.</span></span>

<span data-ttu-id="6a706-116">Значением свойства является массив **HRESULT** s.</span><span class="sxs-lookup"><span data-stu-id="6a706-116">The value of the property is an array of **HRESULT** s.</span></span> <span data-ttu-id="6a706-117">Записи массива соответствуют потокам на текущем элементе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="6a706-117">The array entries correspond to streams on the current media item.</span></span> <span data-ttu-id="6a706-118">Каждая запись в массиве указывает, был ли соответствующий поток подключен к приемнику мультимедиа следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6a706-118">Each entry in the array indicates whether the corresponding stream was connected to a media sink, as follows:</span></span>

-   <span data-ttu-id="6a706-119">Если поток подключен к приемнику мультимедиа, значение равно **S \_**.</span><span class="sxs-lookup"><span data-stu-id="6a706-119">If the stream is connected to a media sink, the value is **S\_OK**.</span></span>
-   <span data-ttu-id="6a706-120">Если поток не выбран, значение равно **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="6a706-120">If the stream is not selected, the value is **S\_FALSE**.</span></span>
-   <span data-ttu-id="6a706-121">Если при попытке подключения к потоку произошла ошибка, значением будет код ошибки.</span><span class="sxs-lookup"><span data-stu-id="6a706-121">If an error occurred while attempting to connect the stream, the value is an error code.</span></span>

<span data-ttu-id="6a706-122">Если по крайней мере один поток был успешно подключен, воспроизведение возможно.</span><span class="sxs-lookup"><span data-stu-id="6a706-122">If at least one stream was connected successfully, playback is possible.</span></span> <span data-ttu-id="6a706-123">Например, у пользователя может быть кодек, необходимый для воспроизведения аудиопотока, но не воспроизведение видеопотока.</span><span class="sxs-lookup"><span data-stu-id="6a706-123">For example, the user might have the codec needed to play the audio stream but not to play the video stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a706-124">Требования</span><span class="sxs-lookup"><span data-stu-id="6a706-124">Requirements</span></span>



| <span data-ttu-id="6a706-125">Требование</span><span class="sxs-lookup"><span data-stu-id="6a706-125">Requirement</span></span> | <span data-ttu-id="6a706-126">Значение</span><span class="sxs-lookup"><span data-stu-id="6a706-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6a706-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6a706-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6a706-128">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6a706-128">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6a706-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6a706-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6a706-130">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6a706-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6a706-131">Header</span><span class="sxs-lookup"><span data-stu-id="6a706-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a706-132"><dt>Мфплай. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a706-132"><dt>Mfplay.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a706-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6a706-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a706-134">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6a706-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="6a706-135">**МФП \_ MEDIAITEM \_ Set, \_ событие**</span><span class="sxs-lookup"><span data-stu-id="6a706-135">**MFP\_MEDIAITEM\_SET\_EVENT**</span></span>](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_set_event)
</dt> </dl>

 

 




