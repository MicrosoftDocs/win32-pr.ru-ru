---
description: Работа с типами файлов MFT
ms.assetid: 16c270ee-f246-4222-97e9-d8d0fe009155
title: Работа с типами файлов MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98bfc996704f6069ca1d16570b33f456ea1cc115
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104273242"
---
# <a name="working-with-mft-media-types"></a><span data-ttu-id="ae71e-103">Работа с типами файлов MFT</span><span class="sxs-lookup"><span data-stu-id="ae71e-103">Working with MFT Media Types</span></span>

<span data-ttu-id="ae71e-104">Тип мультимедиа — это способ описания формата потока мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ae71e-104">A media type is a way to describe the format of a media stream.</span></span> <span data-ttu-id="ae71e-105">В Media Foundation типы мультимедиа представлены интерфейсом **имфмедиатипе** .</span><span class="sxs-lookup"><span data-stu-id="ae71e-105">In Media Foundation, media types are represented by the **IMFMediaType** interface.</span></span> <span data-ttu-id="ae71e-106">Этот интерфейс наследует интерфейс **имфаттрибутес** .</span><span class="sxs-lookup"><span data-stu-id="ae71e-106">This interface inherits the **IMFAttributes** interface.</span></span> <span data-ttu-id="ae71e-107">Сведения о типе мультимедиа указываются в виде атрибутов.</span><span class="sxs-lookup"><span data-stu-id="ae71e-107">The details of a media type are specified as attributes.</span></span>

<span data-ttu-id="ae71e-108">Чтобы создать новый тип мультимедиа, вызовите функцию **мфкреатемедиатипе** .</span><span class="sxs-lookup"><span data-stu-id="ae71e-108">To create a new media type, call the **MFCreateMediaType** function.</span></span> <span data-ttu-id="ae71e-109">Эта функция возвращает указатель на интерфейс **имфмедиатипе** .</span><span class="sxs-lookup"><span data-stu-id="ae71e-109">This function returns a pointer to the **IMFMediaType** interface.</span></span> <span data-ttu-id="ae71e-110">Тип носителя изначально не имеет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="ae71e-110">The media type initially has no attributes.</span></span>

<span data-ttu-id="ae71e-111">Пакет SDK для Media Foundation предоставляет несколько вспомогательных функций для инициализации типов мультимедиа из структур форматов.</span><span class="sxs-lookup"><span data-stu-id="ae71e-111">The Media Foundation SDK provides several helper functions for initializing Media Types from format structures.</span></span> <span data-ttu-id="ae71e-112">Например, функция **мфинитмедиатипефромвидеоинфохеадер** инициализирует тип видео из структуры **видеоинфохеадер** , а функция **мфинитмедиатипефромвавеформатекс** инициализирует тип видео из структуры **WAVEFORMATEX** или **WAVEFORMATEXTENSIBLE** .</span><span class="sxs-lookup"><span data-stu-id="ae71e-112">For example the function **MFInitMediaTypeFromVideoInfoHeader** initializes a video type from a **VIDEOINFOHEADER** structure, and the function **MFInitMediaTypeFromWaveFormatEx** initializes a video type from a **WAVEFORMATEX** or **WAVEFORMATEXTENSIBLE** structure.</span></span>

<span data-ttu-id="ae71e-113">Типы форматов, используемые кодеками, обычно ограничиваются теми, которые описаны структурами **видеоинфохеадер** и **вавеформатекс** .</span><span class="sxs-lookup"><span data-stu-id="ae71e-113">The format types that are used by the codecs are generally limited to those described by the **VIDEOINFOHEADER** and **WAVEFORMATEX** structures.</span></span>

<span data-ttu-id="ae71e-114">Дополнительные сведения о создании Media Foundation типов носителей и доступе к ним можно найти в документации по Media Foundation SDK.</span><span class="sxs-lookup"><span data-stu-id="ae71e-114">More information on creating and accessing Media Foundation media types is available in the Media Foundation SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae71e-115">См. также</span><span class="sxs-lookup"><span data-stu-id="ae71e-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae71e-116">Работа с кодеками МФТС</span><span class="sxs-lookup"><span data-stu-id="ae71e-116">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 



