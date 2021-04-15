---
description: Образец фильтра области
ms.assetid: f967d4c7-94d2-440b-9e52-423feefec66d
title: Образец фильтра области
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74ba823e68da1cd1faadd3e1e3acc4e613e2f42
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494892"
---
# <a name="scope-filter-sample"></a><span data-ttu-id="9f8f1-103">Образец фильтра области</span><span class="sxs-lookup"><span data-stu-id="9f8f1-103">Scope Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="9f8f1-104">Описание</span><span class="sxs-lookup"><span data-stu-id="9f8f1-104">Description</span></span>

<span data-ttu-id="9f8f1-105">Фильтр области является фильтром модуля подготовки отчетов, который отображает звуковые данные как формы-волны.</span><span class="sxs-lookup"><span data-stu-id="9f8f1-105">The Scope filter is a renderer filter that displays sound data as wave forms.</span></span>

## <a name="usage"></a><span data-ttu-id="9f8f1-106">Использование</span><span class="sxs-lookup"><span data-stu-id="9f8f1-106">Usage</span></span>

<span data-ttu-id="9f8f1-107">Чтобы использовать этот фильтр, откройте Графедит и выводите звуковой файл (или видеофайл с аудио-потоком).</span><span class="sxs-lookup"><span data-stu-id="9f8f1-107">To use this filter, open GraphEdit and render an audio file (or a video file with an audio stream).</span></span> <span data-ttu-id="9f8f1-108">Временно отключите модуль подготовки звука и вставьте образец фильтра Infinite-Pin tee ([Пример фильтра инфти](inftee-filter-sample.md)).</span><span class="sxs-lookup"><span data-stu-id="9f8f1-108">Disconnect the audio renderer temporarily and insert the Infinite-Pin Tee ([InfTee Filter Sample](inftee-filter-sample.md)) sample filter.</span></span> <span data-ttu-id="9f8f1-109">Повторно подключите модуль подготовки звука.</span><span class="sxs-lookup"><span data-stu-id="9f8f1-109">Reconnect the audio renderer.</span></span> <span data-ttu-id="9f8f1-110">Затем подключите второй выходной закрепление фильтра tee Infinite-Pin к фильтру области.</span><span class="sxs-lookup"><span data-stu-id="9f8f1-110">Then connect the Infinite-Pin Tee filter's second output pin to the Scope filter.</span></span> <span data-ttu-id="9f8f1-111">Теперь запустите граф.</span><span class="sxs-lookup"><span data-stu-id="9f8f1-111">Now run the graph.</span></span>

<span data-ttu-id="9f8f1-112">Окно область реализуется как диалоговое окно, а не как фактическое окно.</span><span class="sxs-lookup"><span data-stu-id="9f8f1-112">The Scope window is implemented as a dialog box, not as an actual window.</span></span> <span data-ttu-id="9f8f1-113">Разработчикам, создающим панели управления для изменения параметров фильтра в режиме реального времени, может потребоваться использовать такой метод, как и страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="9f8f1-113">Developers creating control panels to alter filter parameters in real time might want to use a technique like this rather than property pages.</span></span>

<span data-ttu-id="9f8f1-114">Фильтр области показывает настройку отдельного потока для обработки данных.</span><span class="sxs-lookup"><span data-stu-id="9f8f1-114">The Scope filter demonstrates setting up a separate thread to process data.</span></span> <span data-ttu-id="9f8f1-115">В этом случае данные просто копируются в отдельный буфер метода [**имеминпутпин:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) , а затем отрисовывается в окне область в отдельном потоке.</span><span class="sxs-lookup"><span data-stu-id="9f8f1-115">In this case, the data is just copied to a separate buffer on the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method, and is then drawn on the Scope window on the separate thread.</span></span>

<span data-ttu-id="9f8f1-116">Фильтр области также позволяет отслеживать выходные данные звука, чтобы определить, обрезаются ли они, чтобы можно было скорректировать прибыль.</span><span class="sxs-lookup"><span data-stu-id="9f8f1-116">The Scope filter also enables you to monitor audio output to determine if you are clipping, so you can adjust the gain.</span></span>

<span data-ttu-id="9f8f1-117">Этот фильтр отображается в Графедит как "ОсЦиллоскопе".</span><span class="sxs-lookup"><span data-stu-id="9f8f1-117">This filter appears in GraphEdit as "Oscilloscope."</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="9f8f1-118">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="9f8f1-118">Downloading the Sample</span></span>

<span data-ttu-id="9f8f1-119">Чтобы скачать примеры пакета SDK для DirectShow, установите последнюю версию [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9f8f1-119">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="9f8f1-120">Этот пример устанавливается по следующему пути: *\[ корневой \] пример пакета SDK* \\ \\ \\ \\ . область фильтров мультимедийных файлов DirectShow \\ .</span><span class="sxs-lookup"><span data-stu-id="9f8f1-120">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\Scope.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f8f1-121">См. также</span><span class="sxs-lookup"><span data-stu-id="9f8f1-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f8f1-122">Примеры DirectShow</span><span class="sxs-lookup"><span data-stu-id="9f8f1-122">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



