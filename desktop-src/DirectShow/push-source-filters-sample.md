---
description: Пример фильтров источника push-уведомлений
ms.assetid: fc52f7bc-e9c7-4cd4-91e8-5c8f3450ca95
title: Пример фильтров источника push-уведомлений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce22c7c6d73f54152ce469b4b3bb40c20db6c29
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537151"
---
# <a name="push-source-filters-sample"></a><span data-ttu-id="3c80e-103">Пример фильтров источника push-уведомлений</span><span class="sxs-lookup"><span data-stu-id="3c80e-103">Push Source Filters Sample</span></span>

## <a name="description"></a><span data-ttu-id="3c80e-104">Описание</span><span class="sxs-lookup"><span data-stu-id="3c80e-104">Description</span></span>

<span data-ttu-id="3c80e-105">Этот пример состоит из трех исходных фильтров, которые предоставляют следующие исходные данные в качестве видеопотока:</span><span class="sxs-lookup"><span data-stu-id="3c80e-105">This sample consists of a set of three source filters that provide the following source data as a video stream:</span></span>

-   <span data-ttu-id="3c80e-106">Кпушсаурцебитмап: одно битовое изображение (загруженное из текущего каталога)</span><span class="sxs-lookup"><span data-stu-id="3c80e-106">CPushSourceBitmap: Single bitmap (loaded from current directory)</span></span>
-   <span data-ttu-id="3c80e-107">Кпушсаурцебитмапсет: набор точечных рисунков (загруженных из текущего каталога)</span><span class="sxs-lookup"><span data-stu-id="3c80e-107">CPushSourceBitmapSet: Set of bitmaps (loaded from current directory)</span></span>
-   <span data-ttu-id="3c80e-108">Кпушсаурцедесктоп: копия текущего образа рабочего стола (только GDI)</span><span class="sxs-lookup"><span data-stu-id="3c80e-108">CPushSourceDesktop: Copy of current desktop image (GDI only)</span></span>

## <a name="usage"></a><span data-ttu-id="3c80e-109">Использование</span><span class="sxs-lookup"><span data-stu-id="3c80e-109">Usage</span></span>

<span data-ttu-id="3c80e-110">Чтобы использовать фильтр, загрузите его в Графедит и выводите его выходной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="3c80e-110">To use a filter, load it into GraphEdit and render its output pin.</span></span> <span data-ttu-id="3c80e-111">При этом будет подключен модуль подготовки видео (и, возможно, фильтр преобразователя цветового пространства), и вы сможете отобразить выходные данные.</span><span class="sxs-lookup"><span data-stu-id="3c80e-111">This will connect a video renderer (and possibly a Color Space Converter filter) and allow you to display the output.</span></span> <span data-ttu-id="3c80e-112">Если вы хотите вывести выходные данные в AVI-файл, загрузите его, загрузите фильтр записи файлов, введите имя выходных данных в модуль записи файлов и отфильтруйте выходной код фильтра Пушсаурце.</span><span class="sxs-lookup"><span data-stu-id="3c80e-112">If you want to render the output to an AVI file, load the AVI Mux, load a File Writer Filter, provide an output name to the File Writer, and render the PushSource filter's output pin.</span></span> <span data-ttu-id="3c80e-113">Можно также загрузить и подключить видео компрессоры, видеоэффекты и т. д.</span><span class="sxs-lookup"><span data-stu-id="3c80e-113">You can also load and connect video compressors, video effects, and so on.</span></span>

> [!Note]  
> <span data-ttu-id="3c80e-114">Фильтр записи рабочего стола не поддерживает наложение оборудования, поэтому он не будет записывать видео, отображаемое в области наложения или курсоров, отображаемых через наложение оборудования.</span><span class="sxs-lookup"><span data-stu-id="3c80e-114">The desktop capture filter does not support hardware overlays, so it will not capture video rendered to an overlay surface or cursors displayed via hardware overlay.</span></span> <span data-ttu-id="3c80e-115">Он использует GDI для преобразования текущего образа рабочего стола в точечный рисунок, который передается в выходной закрепление в качестве примера носителя.</span><span class="sxs-lookup"><span data-stu-id="3c80e-115">It uses GDI to convert the current desktop image into a bitmap, which is passed to the output pin as a media sample.</span></span>

 

## <a name="downloading-the-sample"></a><span data-ttu-id="3c80e-116">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="3c80e-116">Downloading the Sample</span></span>

<span data-ttu-id="3c80e-117">Чтобы скачать примеры пакета SDK для DirectShow, установите последнюю версию [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3c80e-117">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="3c80e-118">Этот пример устанавливается по следующему пути: *\[ \] корневые примеры SDK* \\ \\ мультимедиа \\ DirectShow \\ фильтры \\ пушсаурце.</span><span class="sxs-lookup"><span data-stu-id="3c80e-118">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\PushSource.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c80e-119">См. также</span><span class="sxs-lookup"><span data-stu-id="3c80e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c80e-120">Примеры DirectShow</span><span class="sxs-lookup"><span data-stu-id="3c80e-120">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



