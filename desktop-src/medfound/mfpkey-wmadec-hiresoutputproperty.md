---
description: Указывает, должен ли декодер звука предоставлять выходные данные высокого разрешения.
ms.assetid: a96bd78f-982c-43fa-b2d3-8caba4aa84b6
title: Свойство MFPKEY_WMADEC_HIRESOUTPUT (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd59bc6b8b0e74be1daaea4a61ca82c810a0ca79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702037"
---
# <a name="mfpkey_wmadec_hiresoutput-property"></a><span data-ttu-id="7c02d-103">МФПКЭЙ \_ вмадек \_ Хиресаутпут, свойство</span><span class="sxs-lookup"><span data-stu-id="7c02d-103">MFPKEY\_WMADEC\_HIRESOUTPUT Property</span></span>

<span data-ttu-id="7c02d-104">Указывает, должен ли декодер звука предоставлять выходные данные высокого разрешения.</span><span class="sxs-lookup"><span data-stu-id="7c02d-104">Specifies whether the audio decoder should deliver high-resolution output.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="7c02d-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="7c02d-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="7c02d-106">g \_ всзвмачиресаутпут</span><span class="sxs-lookup"><span data-stu-id="7c02d-106">g\_wszWMACHiResOutput</span></span>

## <a name="data-type"></a><span data-ttu-id="7c02d-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7c02d-107">Data Type</span></span>

<span data-ttu-id="7c02d-108">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="7c02d-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="7c02d-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="7c02d-109">Default Value</span></span>

<span data-ttu-id="7c02d-110">**ВАРИАНТ \_ false**</span><span class="sxs-lookup"><span data-stu-id="7c02d-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="7c02d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7c02d-111">Remarks</span></span>

<span data-ttu-id="7c02d-112">Присвойте этому свойству значение VARIANT \_ true, чтобы декодировать многоканальное или 24-битовое звуковое содержимое, или звук с частотой выборки выше 48 000 Гц.</span><span class="sxs-lookup"><span data-stu-id="7c02d-112">Set this property to VARIANT\_TRUE to decode multichannel or 24-bit audio content, or audio with a sample rate greater than 48,000 Hz.</span></span> <span data-ttu-id="7c02d-113">Если содержимое кодируется в высоком разрешении, но это свойство имеет значение VARIANT \_ false, применяются следующие правила поведения.</span><span class="sxs-lookup"><span data-stu-id="7c02d-113">If the content is encoded in high resolution, but this property is VARIANT\_FALSE, the following behaviors apply:</span></span>

-   <span data-ttu-id="7c02d-114">Выходные данные DMO будут ограничены 16-битным стерео, 48-кГц.</span><span class="sxs-lookup"><span data-stu-id="7c02d-114">The DMO output will be limited to 16-bit, 48-KHz stereo.</span></span>
-   <span data-ttu-id="7c02d-115">В MFT будут перечислены режимы вывода, которые ограничены 16 битами и не затрагивают изменения в количестве каналов или частоте выборки.</span><span class="sxs-lookup"><span data-stu-id="7c02d-115">The MFT will enumerate output modes that are limited to 16 bits and do not involve changes in channel count or sampling rate.</span></span>

<span data-ttu-id="7c02d-116">Свойства звука с высоким разрешением передаются в виде структуры [**вавеформатекстенсибле**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) , а не [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7c02d-116">The properties of high-resolution audio are passed in a [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure, not [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)).</span></span>

<span data-ttu-id="7c02d-117">Выходные данные высокого разрешения доступны только в том случае, если декодер работает под управлением Windows XP или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="7c02d-117">High-resolution output is available only if the decoder is running on Windows XP or later.</span></span> <span data-ttu-id="7c02d-118">Это свойство можно задать независимо от операционной системы, в которой выполняется приложение.</span><span class="sxs-lookup"><span data-stu-id="7c02d-118">You can set this property regardless of the operating system on which your application is running.</span></span> <span data-ttu-id="7c02d-119">В версиях Windows, предшествующих Windows XP, декодер игнорирует этот параметр и выдает стандартные выходные данные.</span><span class="sxs-lookup"><span data-stu-id="7c02d-119">On versions of Windows earlier than Windows XP, the decoder will ignore this setting and deliver standard output.</span></span>

<span data-ttu-id="7c02d-120">Многие игроки (включая проигрыватель Windows Media 9 Series и более поздние версии) задают это значение для всего содержимого.</span><span class="sxs-lookup"><span data-stu-id="7c02d-120">Many players (including Windows Media Player 9 Series and later) set this value for all content.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c02d-121">Требования</span><span class="sxs-lookup"><span data-stu-id="7c02d-121">Requirements</span></span>



| <span data-ttu-id="7c02d-122">Требование</span><span class="sxs-lookup"><span data-stu-id="7c02d-122">Requirement</span></span> | <span data-ttu-id="7c02d-123">Значение</span><span class="sxs-lookup"><span data-stu-id="7c02d-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c02d-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7c02d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7c02d-125">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7c02d-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7c02d-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7c02d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7c02d-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7c02d-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7c02d-128">Header</span><span class="sxs-lookup"><span data-stu-id="7c02d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c02d-129"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c02d-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c02d-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c02d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c02d-131">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7c02d-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
