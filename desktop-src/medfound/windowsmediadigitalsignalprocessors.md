---
description: Обработчики цифровых сигналов
ms.assetid: cd3952ca-3958-4944-8fde-f0163a47bff9
title: Обработчики цифровых сигналов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0961554d9c9902e68f74c6b2b57662b23846614f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105693824"
---
# <a name="digital-signal-processors"></a><span data-ttu-id="6871b-103">Обработчики цифровых сигналов</span><span class="sxs-lookup"><span data-stu-id="6871b-103">Digital Signal Processors</span></span>

<span data-ttu-id="6871b-104">В этом разделе описываются объекты обработчика цифровых сигналов (DSP), предоставляемые Windows.</span><span class="sxs-lookup"><span data-stu-id="6871b-104">This section describes the digital signal processor (DSP) objects provided by Windows.</span></span>

<span data-ttu-id="6871b-105">Корпорация Майкрософт использует термин " *обработчик цифровых сигналов* " для обозначения набора COM-объектов, выполняющих преобразования для несжатых аудио-и видеоданных.</span><span class="sxs-lookup"><span data-stu-id="6871b-105">Microsoft uses the term *digital signal processor* to designate a set of COM objects that perform transformations on uncompressed audio and video data.</span></span> <span data-ttu-id="6871b-106">Поставщики DSP, описанные в этом пакете SDK, преобразуют аудио и видео в различных форматах без сжатия.</span><span class="sxs-lookup"><span data-stu-id="6871b-106">The DSPs described in this SDK transform audio and video in a variety of uncompressed formats.</span></span>

<span data-ttu-id="6871b-107">Поставщики DSP могут использоваться самостоятельно или в сочетании с аудиокодеками и видеокодеками.</span><span class="sxs-lookup"><span data-stu-id="6871b-107">The DSPs can be used by themselves, or in combination with audio and video codecs.</span></span> <span data-ttu-id="6871b-108">За исключением схемы DSP для записи речи, каждый из перечисленных здесь DSP реализует два отдельных, но схожих интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6871b-108">With the exception of the Voice Capture DSP, each DSP listed here implements two separate but similar interfaces.</span></span>



| <span data-ttu-id="6871b-109">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="6871b-109">Interface</span></span>                              | <span data-ttu-id="6871b-110">Описание</span><span class="sxs-lookup"><span data-stu-id="6871b-110">Description</span></span>                                 |
|----------------------------------------|---------------------------------------------|
| [<span data-ttu-id="6871b-111">**имфтрансформ**</span><span class="sxs-lookup"><span data-stu-id="6871b-111">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | <span data-ttu-id="6871b-112">Совместимо с Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="6871b-112">Compatible with Microsoft Media Foundation.</span></span> |
| [<span data-ttu-id="6871b-113">**имедиаобжект**</span><span class="sxs-lookup"><span data-stu-id="6871b-113">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | <span data-ttu-id="6871b-114">Совместимо с DirectShow.</span><span class="sxs-lookup"><span data-stu-id="6871b-114">Compatible with DirectShow.</span></span>                 |



 

<span data-ttu-id="6871b-115">Поставщики DSP можно настроить с помощью интерфейса [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) , чтобы задать свойства.</span><span class="sxs-lookup"><span data-stu-id="6871b-115">You can configure the DSPs by using the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface to set properties.</span></span> <span data-ttu-id="6871b-116">Некоторые поставщики DSP имеют дополнительные интерфейсы, устанавливающие свойства.</span><span class="sxs-lookup"><span data-stu-id="6871b-116">Some of the DSPs have additional interfaces that set properties.</span></span> <span data-ttu-id="6871b-117">Чтобы использовать эти интерфейсы, вызовите метод [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) любого другого интерфейса DSP.</span><span class="sxs-lookup"><span data-stu-id="6871b-117">To use these interfaces, call the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method of any other interface of the DSP.</span></span> <span data-ttu-id="6871b-118">В справочной статье по каждому DSP содержится список поддерживаемых свойств, интерфейсов и других функций.</span><span class="sxs-lookup"><span data-stu-id="6871b-118">The reference topic for each DSP lists the supported properties, interfaces, and other features.</span></span>

<span data-ttu-id="6871b-119">Этот раздел содержит следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="6871b-119">This section contains the following topics.</span></span>



| <span data-ttu-id="6871b-120">DSP</span><span class="sxs-lookup"><span data-stu-id="6871b-120">DSP</span></span>                                                      | <span data-ttu-id="6871b-121">Описание</span><span class="sxs-lookup"><span data-stu-id="6871b-121">Description</span></span>                                          |
|----------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="6871b-122">DSP по интерполяции аудио</span><span class="sxs-lookup"><span data-stu-id="6871b-122">Audio Resampler DSP</span></span>](audioresampler.md)                | <span data-ttu-id="6871b-123">Преобразует частоту выборки звукового потока.</span><span class="sxs-lookup"><span data-stu-id="6871b-123">Converts the sampling rate of an audio stream.</span></span>       |
| [<span data-ttu-id="6871b-124">Преобразование элемента управления цветом DSP</span><span class="sxs-lookup"><span data-stu-id="6871b-124">Color Control Transform DSP</span></span>](colorcontroltransform.md) | <span data-ttu-id="6871b-125">Регулирует цветовые характеристики потока видео.</span><span class="sxs-lookup"><span data-stu-id="6871b-125">Adjusts the color characteristics of a video stream.</span></span> |
| [<span data-ttu-id="6871b-126">DSP цветового преобразователя</span><span class="sxs-lookup"><span data-stu-id="6871b-126">Color Converter DSP</span></span>](colorconverter.md)                | <span data-ttu-id="6871b-127">Преобразует видеопоток между цветовыми форматами.</span><span class="sxs-lookup"><span data-stu-id="6871b-127">Converts a video stream between color formats.</span></span>       |
| [<span data-ttu-id="6871b-128">Средство преобразования частоты кадров DSP</span><span class="sxs-lookup"><span data-stu-id="6871b-128">Frame Rate Converter DSP</span></span>](framerateconverter.md)       | <span data-ttu-id="6871b-129">Изменяет частоту кадров потока видео.</span><span class="sxs-lookup"><span data-stu-id="6871b-129">Changes the frame rate of a video stream.</span></span>            |
| [<span data-ttu-id="6871b-130">DSP изменения видеоконтроллеров</span><span class="sxs-lookup"><span data-stu-id="6871b-130">Video Resizer DSP</span></span>](videoresizer.md)                    | <span data-ttu-id="6871b-131">Изменяет размер видеопотока.</span><span class="sxs-lookup"><span data-stu-id="6871b-131">Resizes a video stream.</span></span>                              |
| [<span data-ttu-id="6871b-132">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="6871b-132">Voice Capture DSP</span></span>](voicecapturedmo.md)                 | <span data-ttu-id="6871b-133">Инкапсулирует несколько DSP, связанных с захватом голоса.</span><span class="sxs-lookup"><span data-stu-id="6871b-133">Encapsulates several DSPs related to voice capture.</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="6871b-134">См. также</span><span class="sxs-lookup"><span data-stu-id="6871b-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6871b-135">Справочник по программированию в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6871b-135">Media Foundation Programming Reference</span></span>](media-foundation-programming-reference.md)
</dt> </dl>

 

 
