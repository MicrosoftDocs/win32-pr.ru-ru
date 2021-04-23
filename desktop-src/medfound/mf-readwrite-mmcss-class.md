---
description: Указывает класс мультимедиа класса службы планировщика классов (MMCSS) для модуля чтения источника или приемника.
ms.assetid: A3A295E8-AC9C-4641-ADDA-B97D5AB13A9A
title: Атрибут MF_READWRITE_MMCSS_CLASS (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d2088ba09bf4f8ad9516d9b2117ab54161d7ac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817128"
---
# <a name="mf_readwrite_mmcss_class-attribute"></a><span data-ttu-id="9815f-103">\_ \_ Атрибут класса MMCSS MF ReadWrite \_</span><span class="sxs-lookup"><span data-stu-id="9815f-103">MF\_READWRITE\_MMCSS\_CLASS attribute</span></span>

<span data-ttu-id="9815f-104">Указывает класс [мультимедиа класса службы планировщика классов](../procthread/multimedia-class-scheduler-service.md) (MMCSS) для модуля чтения источника или приемника.</span><span class="sxs-lookup"><span data-stu-id="9815f-104">Specifies a [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) (MMCSS) class for the Source Reader or Sink Writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="9815f-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9815f-105">Data type</span></span>

<span data-ttu-id="9815f-106">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="9815f-106">**LPWSTR**</span></span>

## <a name="getset"></a><span data-ttu-id="9815f-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="9815f-107">Get/set</span></span>

<span data-ttu-id="9815f-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="9815f-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="9815f-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="9815f-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="9815f-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9815f-110">Remarks</span></span>

<span data-ttu-id="9815f-111">При необходимости задайте этот атрибут при создании экземпляра модуля [чтения источника](source-reader.md) или [средства записи приемника](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="9815f-111">Optionally set this attribute when you create an instance of the [Source Reader](source-reader.md) or [Sink Writer](sink-writer.md).</span></span> <span data-ttu-id="9815f-112">Значение атрибута должно быть допустимым именем класса MMCSS.</span><span class="sxs-lookup"><span data-stu-id="9815f-112">The value of the attribute must be a valid MMCSS class name.</span></span>

<span data-ttu-id="9815f-113">Если этот атрибут задан, модуль чтения источника или модуль записи приемника регистрирует все свои потоки с помощью указанного класса MMCSS.</span><span class="sxs-lookup"><span data-stu-id="9815f-113">If this attribute is set, the Source Reader or Sink Writer registers all of its threads with the specified MMCSS class.</span></span> <span data-ttu-id="9815f-114">Служба MMCSS гарантирует, что обработка данных в модуле чтения источника или в модуле записи приемника имеет приоритет над другими системными задачами.</span><span class="sxs-lookup"><span data-stu-id="9815f-114">The MMCSS ensures that data processing in the Source Reader or Sink Writer has priority over other system tasks.</span></span>

<span data-ttu-id="9815f-115">Чтобы указать базовый приоритет, установите атрибут [ \_ \_ \_ приоритета MMCSS в MF ReadWrite](mf-readwrite-mmcss-priority.md) .</span><span class="sxs-lookup"><span data-stu-id="9815f-115">To specify the base priority, set the [MF\_READWRITE\_MMCSS\_PRIORITY](mf-readwrite-mmcss-priority.md) attribute.</span></span> <span data-ttu-id="9815f-116">Если этот атрибут не задан, базовый приоритет равен нулю.</span><span class="sxs-lookup"><span data-stu-id="9815f-116">If that attribute is not set, the base priority is zero.</span></span>

<span data-ttu-id="9815f-117">Для потоков обработки звука атрибут [ \_ \_ \_ \_ Audio класса MMCSS ReadWrite](mf-readwrite-mmcss-class-audio.md) (если он задан) переопределяет этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="9815f-117">For audio-processing threads, the [MF\_READWRITE\_MMCSS\_CLASS\_AUDIO](mf-readwrite-mmcss-class-audio.md) attribute (if set) overrides this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="9815f-118">Требования</span><span class="sxs-lookup"><span data-stu-id="9815f-118">Requirements</span></span>



| <span data-ttu-id="9815f-119">Требование</span><span class="sxs-lookup"><span data-stu-id="9815f-119">Requirement</span></span> | <span data-ttu-id="9815f-120">Значение</span><span class="sxs-lookup"><span data-stu-id="9815f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9815f-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9815f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9815f-122">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="9815f-122">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="9815f-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9815f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9815f-124">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="9815f-124">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="9815f-125">Header</span><span class="sxs-lookup"><span data-stu-id="9815f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9815f-126"><dt>Мфреадврите. h</dt></span><span class="sxs-lookup"><span data-stu-id="9815f-126"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9815f-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9815f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9815f-128">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9815f-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
