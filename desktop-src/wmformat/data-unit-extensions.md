---
title: Расширения модулей данных
description: Расширения модулей данных
ms.assetid: f95de189-0449-4b88-aba3-7b19f385c8fe
keywords:
- Windows Media Format SDK, расширения модулей данных
- Расширенный системный формат (ASF), расширения модулей данных
- ASF (Расширенный системный формат), расширения модулей данных
- Windows Media Format SDK, системы расширений полезных данных
- Расширенные системные форматы (ASF), системы расширения полезных данных
- ASF (Расширенный системный формат), системы расширения полезных данных
- расширения модулей данных, сведения
- расширения модулей полезных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c8ed5c9db82d0002648148ca14bd7f94baa9029
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788761"
---
# <a name="data-unit-extensions"></a><span data-ttu-id="52adf-111">Расширения модулей данных</span><span class="sxs-lookup"><span data-stu-id="52adf-111">Data Unit Extensions</span></span>

<span data-ttu-id="52adf-112">Пакет SDK для формата Windows Media позволяет дополнять данные в образцах с помощью *модулей обработки данных*, также называемых системами расширения полезной нагрузки.</span><span class="sxs-lookup"><span data-stu-id="52adf-112">The Windows Media Format SDK enables you to supplement data in samples with *data unit extensions*, also called payload extension systems.</span></span> <span data-ttu-id="52adf-113">В этой документации используется термин "расширения модулей данных", чтобы обеспечить соответствие именам методов, таким как [**адддатаунитекстенсион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension).</span><span class="sxs-lookup"><span data-stu-id="52adf-113">This documentation uses the term "data unit extensions" in order to remain consistent with method names such as [**AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension).</span></span> <span data-ttu-id="52adf-114">Модуль обработки данных — это пара "имя-значение", которая прикрепляется к образцу в разделе данных файла.</span><span class="sxs-lookup"><span data-stu-id="52adf-114">A data unit extension is a name/value pair that is attached to the sample in the data section of the file.</span></span> <span data-ttu-id="52adf-115">Доступ к расширенным данным можно получить с помощью методов объекта buffer, когда образец извлекается модулем чтения.</span><span class="sxs-lookup"><span data-stu-id="52adf-115">You can access the extended data using methods of the buffer object when the sample is retrieved by the reader.</span></span>

<span data-ttu-id="52adf-116">Вы можете создавать расширения единиц данных для собственных спецификаций, но несколько типов являются предопределенными и поддерживаются объектами этого пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="52adf-116">You can create data unit extensions to your own specifications, but several types are predefined and supported by the objects of this SDK.</span></span> <span data-ttu-id="52adf-117">Эти стандартные расширения используются для предоставления дополнительных данных для имен файлов (в скриптах и веб-потоках), SMPTE данных кода времени, неквадратных пропорций, длительности и типа чередования.</span><span class="sxs-lookup"><span data-stu-id="52adf-117">These standard extensions are used to provide additional data for file names (in script and Web streams), SMPTE time code data, non-square pixel aspect ratio, duration, and type of interlacing.</span></span>

<span data-ttu-id="52adf-118">Чтобы использовать расширения единиц данных, необходимо настроить поток для их приема, а затем добавить расширения в каждый пример для этого потока.</span><span class="sxs-lookup"><span data-stu-id="52adf-118">To use data unit extensions, you must configure the stream to accept them, and then add extensions to each sample for that stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52adf-119">См. также</span><span class="sxs-lookup"><span data-stu-id="52adf-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52adf-120">**Функции файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="52adf-120">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="52adf-121">**Настройка расширений модуля данных**</span><span class="sxs-lookup"><span data-stu-id="52adf-121">**Configuring Data Unit Extensions**</span></span>](configuring-data-unit-extensions.md)
</dt> <dt>

[<span data-ttu-id="52adf-122">**Настройка модулей обработки данных**</span><span class="sxs-lookup"><span data-stu-id="52adf-122">**Setting Data Unit Extensions**</span></span>](setting-data-unit-extensions.md)
</dt> </dl>

 

 




