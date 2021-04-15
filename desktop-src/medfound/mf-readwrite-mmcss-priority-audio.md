---
description: Задает базовый приоритет для потоков обработки звука, созданных модулем чтения источника или модулем записи приемника.
ms.assetid: C0E3A472-959F-4F74-8906-03630DE4CB8C
title: Атрибут MF_READWRITE_MMCSS_PRIORITY_AUDIO (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c33f3e4cab26a448c3b5a28c6f3cfe631a7c1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701704"
---
# <a name="mf_readwrite_mmcss_priority_audio-attribute"></a><span data-ttu-id="a76f8-103">\_ \_ \_ Звуковой атрибут MMCSS с приоритетом MF ReadWrite \_</span><span class="sxs-lookup"><span data-stu-id="a76f8-103">MF\_READWRITE\_MMCSS\_PRIORITY\_AUDIO attribute</span></span>

<span data-ttu-id="a76f8-104">Задает базовый приоритет для потоков обработки звука, созданных модулем чтения источника или модулем записи приемника.</span><span class="sxs-lookup"><span data-stu-id="a76f8-104">Sets the base priority for audio-processing threads created by the Source Reader or Sink Writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="a76f8-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a76f8-105">Data type</span></span>

<span data-ttu-id="a76f8-106">**Int32** хранится как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="a76f8-106">**INT32** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="a76f8-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="a76f8-107">Get/set</span></span>

<span data-ttu-id="a76f8-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="a76f8-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="a76f8-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="a76f8-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="a76f8-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a76f8-110">Remarks</span></span>

<span data-ttu-id="a76f8-111">При необходимости задайте этот атрибут при создании экземпляра модуля [чтения источника](source-reader.md) или [средства записи приемника](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="a76f8-111">Optionally set this attribute when you create an instance of the [Source Reader](source-reader.md) or [Sink Writer](sink-writer.md).</span></span> <span data-ttu-id="a76f8-112">Если этот атрибут задан, также следует установить атрибут [ \_ \_ \_ Audio класса MMCSS для \_ записи на MF](mf-readwrite-mmcss-class-audio.md) .</span><span class="sxs-lookup"><span data-stu-id="a76f8-112">If you set this attribute, also set the [MF\_READWRITE\_MMCSS\_CLASS\_AUDIO](mf-readwrite-mmcss-class-audio.md) attribute.</span></span> <span data-ttu-id="a76f8-113">В противном случае этот атрибут игнорируется.</span><span class="sxs-lookup"><span data-stu-id="a76f8-113">Otherwise, this attribute is ignored.</span></span>

<span data-ttu-id="a76f8-114">Когда модуль чтения исходного кода или модуль записи приемника регистрирует потоки обработки звука с помощью [службы планировщика классов мультимедиа](../procthread/multimedia-class-scheduler-service.md), значение этого атрибута указывает базовый приоритет потока.</span><span class="sxs-lookup"><span data-stu-id="a76f8-114">When the Source Reader or Sink Writer registers audio-processing threads with the [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md), the value of this attribute specifies the base thread priority.</span></span> <span data-ttu-id="a76f8-115">Если этот атрибут не задан, значение по умолчанию равно нулю.</span><span class="sxs-lookup"><span data-stu-id="a76f8-115">If this attribute is not set, the default value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="a76f8-116">Требования</span><span class="sxs-lookup"><span data-stu-id="a76f8-116">Requirements</span></span>



| <span data-ttu-id="a76f8-117">Требование</span><span class="sxs-lookup"><span data-stu-id="a76f8-117">Requirement</span></span> | <span data-ttu-id="a76f8-118">Значение</span><span class="sxs-lookup"><span data-stu-id="a76f8-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a76f8-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a76f8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a76f8-120">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="a76f8-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="a76f8-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a76f8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a76f8-122">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="a76f8-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="a76f8-123">Header</span><span class="sxs-lookup"><span data-stu-id="a76f8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a76f8-124"><dt>Мфреадврите. h</dt></span><span class="sxs-lookup"><span data-stu-id="a76f8-124"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a76f8-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a76f8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a76f8-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a76f8-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
