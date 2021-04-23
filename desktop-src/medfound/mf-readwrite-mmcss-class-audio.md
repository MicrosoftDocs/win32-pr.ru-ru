---
description: Указывает класс мультимедиа класса службы планировщика мультимедийных данных для потоков обработки звука в модуле чтения источника или в модуле записи приемника.
ms.assetid: F1B8A8C8-2E41-4321-A94D-C50447C69941
title: Атрибут MF_READWRITE_MMCSS_CLASS_AUDIO (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa35db710c6b72c103855fa2c0a9f169f49c4511
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701705"
---
# <a name="mf_readwrite_mmcss_class_audio-attribute"></a><span data-ttu-id="be19b-103">\_ \_ \_ Аудио атрибут класса MMCSS MF ReadWrite \_</span><span class="sxs-lookup"><span data-stu-id="be19b-103">MF\_READWRITE\_MMCSS\_CLASS\_AUDIO attribute</span></span>

<span data-ttu-id="be19b-104">Указывает класс [мультимедиа класса службы планировщика мультимедийных](../procthread/multimedia-class-scheduler-service.md) данных для потоков обработки звука в модуле чтения источника или в модуле записи приемника.</span><span class="sxs-lookup"><span data-stu-id="be19b-104">Specifies a [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) (MMCSS) class for audio-processing threads in the Source Reader or Sink Writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="be19b-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="be19b-105">Data type</span></span>

<span data-ttu-id="be19b-106">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="be19b-106">**LPWSTR**</span></span>

## <a name="getset"></a><span data-ttu-id="be19b-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="be19b-107">Get/set</span></span>

<span data-ttu-id="be19b-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="be19b-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="be19b-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="be19b-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="be19b-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be19b-110">Remarks</span></span>

<span data-ttu-id="be19b-111">При необходимости задайте этот атрибут при создании экземпляра модуля [чтения источника](source-reader.md) или [средства записи приемника](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="be19b-111">Optionally set this attribute when you create an instance of the [Source Reader](source-reader.md) or [Sink Writer](sink-writer.md).</span></span> <span data-ttu-id="be19b-112">Значение атрибута должно быть допустимым именем класса MMCSS.</span><span class="sxs-lookup"><span data-stu-id="be19b-112">The value of the attribute must be a valid MMCSS class name.</span></span>

<span data-ttu-id="be19b-113">Если этот атрибут задан, модуль чтения и записи приемника регистрирует свои потоки обработки звука с помощью указанного класса MMCSS.</span><span class="sxs-lookup"><span data-stu-id="be19b-113">If this attribute is set, the Source Reader or Sink Writer registers its audio-processing threads with the specified MMCSS class.</span></span> <span data-ttu-id="be19b-114">Служба MMCSS гарантирует, что обработка данных в модуле чтения источника или в модуле записи приемника имеет приоритет над другими системными задачами.</span><span class="sxs-lookup"><span data-stu-id="be19b-114">The MMCSS ensures that data processing in the Source Reader or Sink Writer has priority over other system tasks.</span></span>

<span data-ttu-id="be19b-115">Чтобы указать базовый приоритет для потоковой передачи, задайте атрибут [ \_ \_ \_ \_ Audio Priority с приоритетом MF](mf-readwrite-mmcss-priority-audio.md) .</span><span class="sxs-lookup"><span data-stu-id="be19b-115">To specify the base priority for audio threads, set the [MF\_READWRITE\_MMCSS\_PRIORITY\_AUDIO](mf-readwrite-mmcss-priority-audio.md) attribute.</span></span> <span data-ttu-id="be19b-116">Если этот атрибут не задан, базовый приоритет для звуковых потоков равен нулю.</span><span class="sxs-lookup"><span data-stu-id="be19b-116">If that attribute is not set, the base priority for audio threads is zero.</span></span>

<span data-ttu-id="be19b-117">Этот атрибут переопределяет [атрибут \_ \_ \_ класса MMCSS MF ReadWrite](mf-readwrite-mmcss-class.md) для потоков обработки звука.</span><span class="sxs-lookup"><span data-stu-id="be19b-117">This attribute overrides the [MF\_READWRITE\_MMCSS\_CLASS](mf-readwrite-mmcss-class.md) attribute for audio-processing threads.</span></span> <span data-ttu-id="be19b-118">Если ни один из атрибутов не задан, то звуковые потоки не регистрируются в МКСС.</span><span class="sxs-lookup"><span data-stu-id="be19b-118">If neither attribute is set, audio threads are not registered with MCSS.</span></span>

<span data-ttu-id="be19b-119">Для большинства приложений сбой звука гораздо более заметен для пользователя, чем сбой видео, и, следовательно, менее приемлемый.</span><span class="sxs-lookup"><span data-stu-id="be19b-119">For most applications, audio glitching is much more noticeable to the user than video glitching, and therefore less acceptable.</span></span> <span data-ttu-id="be19b-120">По этой причине приложение обычно должно устанавливать для класса MMCSS \_ типа MMCSS с \_ \_ более высоким приоритетом, чем MF, в классе MMCSS с \_ более высокой важностью. [ \_ \_ \_ ](mf-readwrite-mmcss-class.md)</span><span class="sxs-lookup"><span data-stu-id="be19b-120">For this reason, an application should typically set MF\_READWRITE\_MMCSS\_CLASS\_AUDIO to a higher-priority MMCSS class than [MF\_READWRITE\_MMCSS\_CLASS](mf-readwrite-mmcss-class.md).</span></span> <span data-ttu-id="be19b-121">Это гарантирует, что для обработки звука будет задан более высокий приоритет, чем для других задач.</span><span class="sxs-lookup"><span data-stu-id="be19b-121">This ensures that audio processing is given higher priority than other tasks.</span></span>

## <a name="requirements"></a><span data-ttu-id="be19b-122">Требования</span><span class="sxs-lookup"><span data-stu-id="be19b-122">Requirements</span></span>



| <span data-ttu-id="be19b-123">Требование</span><span class="sxs-lookup"><span data-stu-id="be19b-123">Requirement</span></span> | <span data-ttu-id="be19b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="be19b-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="be19b-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be19b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="be19b-126">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="be19b-126">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="be19b-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be19b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="be19b-128">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="be19b-128">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="be19b-129">Header</span><span class="sxs-lookup"><span data-stu-id="be19b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="be19b-130"><dt>Мфреадврите. h</dt></span><span class="sxs-lookup"><span data-stu-id="be19b-130"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be19b-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be19b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be19b-132">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="be19b-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
