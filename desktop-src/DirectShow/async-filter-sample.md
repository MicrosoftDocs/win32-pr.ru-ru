---
description: Пример асинхронного фильтра
ms.assetid: ad1f2386-6d23-4a6d-8542-bbca53df4825
title: Пример асинхронного фильтра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 099931e9a20c977da18a67f9fe232c2ec391dd4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104072308"
---
# <a name="async-filter-sample"></a><span data-ttu-id="b2132-103">Пример асинхронного фильтра</span><span class="sxs-lookup"><span data-stu-id="b2132-103">Async Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="b2132-104">Описание</span><span class="sxs-lookup"><span data-stu-id="b2132-104">Description</span></span>

<span data-ttu-id="b2132-105">Пример асинхронного фильтра — это фильтр чтения файлов, поддерживающий последовательное скачивание.</span><span class="sxs-lookup"><span data-stu-id="b2132-105">The Async Filter sample is a file reader filter that supports progressive download.</span></span> <span data-ttu-id="b2132-106">Этот образец фильтра реализует интерфейсы [**иасинкреадер**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) и [**ифилесаурцефилтер**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) .</span><span class="sxs-lookup"><span data-stu-id="b2132-106">This sample filter implements the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) and [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) interfaces.</span></span> <span data-ttu-id="b2132-107">Она поддерживает файлы MPEG, но не AVI.</span><span class="sxs-lookup"><span data-stu-id="b2132-107">It supports MPEG files, but not AVI files.</span></span>

## <a name="usage"></a><span data-ttu-id="b2132-108">Использование</span><span class="sxs-lookup"><span data-stu-id="b2132-108">Usage</span></span>

<span data-ttu-id="b2132-109">Этот пример включает небольшое приложение командной строки, Memfile.exe, которое демонстрирует фильтр.</span><span class="sxs-lookup"><span data-stu-id="b2132-109">This sample includes a small command-line application, Memfile.exe, that demonstrates the filter.</span></span> <span data-ttu-id="b2132-110">Аргументы командной строки указывают файл мультимедиа и скорость передачи в килобайтах в секунду.</span><span class="sxs-lookup"><span data-stu-id="b2132-110">The command-line arguments specify a media file and a bit rate, in kilobytes per second.</span></span> <span data-ttu-id="b2132-111">Приложение считывает файл в память с указанной частотой и воспроизводит файл.</span><span class="sxs-lookup"><span data-stu-id="b2132-111">The application reads the file into memory at the specified rate and plays the file.</span></span> <span data-ttu-id="b2132-112">Для этого создается экземпляр фильтра, добавляется фильтр к графу фильтра и подготавливается к просмотру выходной ПИН-код фильтра.</span><span class="sxs-lookup"><span data-stu-id="b2132-112">To do so, it creates an instance of the filter, adds the filter to the filter graph, and renders the filter's output pin.</span></span>

<span data-ttu-id="b2132-113">В командной строке введите:</span><span class="sxs-lookup"><span data-stu-id="b2132-113">At the command line, type:</span></span>

<span data-ttu-id="b2132-114">**Мемфиле имя файла с скоростью**</span><span class="sxs-lookup"><span data-stu-id="b2132-114">**Memfile Filename BitRate**</span></span>  

<span data-ttu-id="b2132-115">Фильтр образцов Async не поддерживает AVI-файлы, так как не может подключиться к фильтру [AVI](avi-splitter-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="b2132-115">The Async sample filter does not support AVI files, because it cannot connect to the [AVI Splitter](avi-splitter-filter.md) filter.</span></span> <span data-ttu-id="b2132-116">Закрепление выходных данных асинхронного фильтра предлагает \_ поток MEDIATYPE и медиасубтипе \_ значение NULL для типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b2132-116">The Async filter's output pin proposes MEDIATYPE\_Stream and MEDIASUBTYPE\_NULL for the media type.</span></span> <span data-ttu-id="b2132-117">Входной ПИН-код в фильтре разделителя AVI не принимает МЕДИАСУБТИПЕ \_ null и не предлагает никаких собственных типов.</span><span class="sxs-lookup"><span data-stu-id="b2132-117">The input pin on the AVI Splitter filter does not accept MEDIASUBTYPE\_NULL, and does not propose any types of its own.</span></span> <span data-ttu-id="b2132-118">Поэтому соединение с ПИН-кодом завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="b2132-118">Therefore, the pin connection fails.</span></span> <span data-ttu-id="b2132-119">Фильтр Async можно улучшить, чтобы предложить МЕДИАСУБТИПЕ \_ AVI, когда это необходимо.</span><span class="sxs-lookup"><span data-stu-id="b2132-119">The Async filter could be enhanced to offer MEDIASUBTYPE\_Avi when appropriate.</span></span> <span data-ttu-id="b2132-120">Например, он может проверить формат файла или использовать расширение файла.</span><span class="sxs-lookup"><span data-stu-id="b2132-120">For example, it could examine the file format, or use the file extension.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="b2132-121">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="b2132-121">Downloading the Sample</span></span>

<span data-ttu-id="b2132-122">Чтобы скачать примеры пакета SDK для DirectShow, установите последнюю версию [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b2132-122">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="b2132-123">Этот пример устанавливается по следующему пути: \[ *корневые примеры пакета SDK* \] \\ \\ файлы мультимедиа для \\ \\ фильтров DirectShow \\ асинхронно.</span><span class="sxs-lookup"><span data-stu-id="b2132-123">This sample is installed under the following path: \[*SDK Root*\]\\Samples\\Multimedia\\DirectShow\\Filters\\Async.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2132-124">См. также</span><span class="sxs-lookup"><span data-stu-id="b2132-124">Related topics</span></span>



[<span data-ttu-id="b2132-125">Примеры DirectShow</span><span class="sxs-lookup"><span data-stu-id="b2132-125">DirectShow Samples</span></span>](directshow-samples.md)


 

 



