---
title: Ввод и вывод данных
description: Ввод и вывод данных
ms.assetid: a03b5327-65df-4cb9-a639-1e943ac28bfc
keywords:
- Подключаемые модули проигрывателя Windows Media, ввод и вывод данных
- подключаемые модули, входные и выходные данные
- подключаемые модули обработки цифровых сигналов, ввод и вывод данных
- Подключаемые модули DSP, входные и выходные данные
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39f66946dc796337d1f1e638cfe3828b3cbfbb6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104132954"
---
# <a name="data-input-and-output"></a><span data-ttu-id="85e7d-107">Ввод и вывод данных</span><span class="sxs-lookup"><span data-stu-id="85e7d-107">Data Input and Output</span></span>

<span data-ttu-id="85e7d-108">Проигрыватель Windows Media обеспечивает воспроизведение аудио-или видео-данных в подключаемые модули DSP через входной буфер, выделенный проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="85e7d-108">Windows Media Player provides audio or video data to DSP plug-ins through an input buffer allocated by Windows Media Player.</span></span> <span data-ttu-id="85e7d-109">Подключаемые модули DSP возвращают обработанные данные в проигрыватель Windows Media через выходной буфер, который также выделяется проигрывателем Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="85e7d-109">DSP plug-ins return processed data to Windows Media Player through an output buffer that is also allocated by Windows Media Player.</span></span> <span data-ttu-id="85e7d-110">Проигрыватель Windows Media управляет процессом передачи данных между собой и подключаемым модулем DSP путем вызова методов, реализованных подключаемым модулем.</span><span class="sxs-lookup"><span data-stu-id="85e7d-110">Windows Media Player manages the process of passing data between itself and the DSP plug-in by calling methods implemented by the plug-in.</span></span> <span data-ttu-id="85e7d-111">Для подключаемого модуля, который выступает в качестве объекта мультимедиа DirectX (DMO), этот процесс работает следующим образом:</span><span class="sxs-lookup"><span data-stu-id="85e7d-111">For a plug-in acting as a DirectX Media Object (DMO), the process works as follows:</span></span>

1.  <span data-ttu-id="85e7d-112">Проигрыватель Windows Media вызывает **имедиаобжект::P роцессинпут**, передавая указатель на объект **имедиабуффер** подключаемому модулю DSP.</span><span class="sxs-lookup"><span data-stu-id="85e7d-112">Windows Media Player calls **IMediaObject::ProcessInput**, passing a pointer to an **IMediaBuffer** object to the DSP plug-in.</span></span>
2.  <span data-ttu-id="85e7d-113">Подключаемый модуль DSP хранит счетчик ссылок на объект входного буфера.</span><span class="sxs-lookup"><span data-stu-id="85e7d-113">The DSP plug-in keeps a reference count on the input buffer object.</span></span> <span data-ttu-id="85e7d-114">Подключаемый модуль DSP возвращает соответствующее **значение HRESULT** успешного или неуспешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="85e7d-114">The DSP plug-in returns an appropriate success or failure **HRESULT**.</span></span>
3.  <span data-ttu-id="85e7d-115">Проигрыватель Windows Media вызывает **имедиаобжект::P роцессаутпут**, передавая указатель на массив **\_ выходных \_ данных структур \_ буферов объектов DMO** (которые содержат буферы вывода) в подключаемый модуль DSP.</span><span class="sxs-lookup"><span data-stu-id="85e7d-115">Windows Media Player calls **IMediaObject::ProcessOutput**, passing a pointer to an array of **DMO\_OUTPUT\_DATA\_BUFFER** structures (which contain output buffers) to the DSP plug-in.</span></span>
4.  <span data-ttu-id="85e7d-116">Подключаемый модуль DSP обрабатывает данные во входном буфере, а затем копирует их в соответствующий выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="85e7d-116">The DSP plug-in processes the data in the input buffer and then copies the data to the appropriate output buffer.</span></span> <span data-ttu-id="85e7d-117">Подключаемый модуль DSP освобождает счетчик ссылок на объект входного буфера, когда все данные в буфере обрабатывались.</span><span class="sxs-lookup"><span data-stu-id="85e7d-117">The DSP plug-in releases the reference count on the input buffer object when all the data in the buffer has been processed.</span></span> <span data-ttu-id="85e7d-118">Затем подключаемый модуль DSP возвращает соответствующее **значение HRESULT** Success или failure.</span><span class="sxs-lookup"><span data-stu-id="85e7d-118">The DSP plug-in then returns an appropriate success or failure **HRESULT**.</span></span>
5.  <span data-ttu-id="85e7d-119">Проигрыватель Windows Media визуализирует содержимое в выходном буфере.</span><span class="sxs-lookup"><span data-stu-id="85e7d-119">Windows Media Player renders the content in the output buffer.</span></span>

<span data-ttu-id="85e7d-120">Для подключаемого модуля, выполняющего функции преобразования Media Foundation (MFT), процесс работает следующим образом:</span><span class="sxs-lookup"><span data-stu-id="85e7d-120">For a plug-in acting as a Media Foundation Transform (MFT), the process works as follows:</span></span>

-   <span data-ttu-id="85e7d-121">Проигрыватель Windows Media вызывает **имфтрансформ::P роцессинпут**, передавая указатель на объект интерфейса **имфсампле** подключаемому модулю DSP.</span><span class="sxs-lookup"><span data-stu-id="85e7d-121">Windows Media Player calls **IMFTransform::ProcessInput**, passing a pointer to an **IMFSample** interface object to the DSP plug-in.</span></span>
    1.  <span data-ttu-id="85e7d-122">Подключаемый модуль DSP хранит счетчик ссылок в интерфейсе **имфсампле** .</span><span class="sxs-lookup"><span data-stu-id="85e7d-122">The DSP plug-in keeps a reference count on the **IMFSample** interface.</span></span> <span data-ttu-id="85e7d-123">Подключаемый модуль DSP возвращает соответствующее **значение HRESULT** успешного или неуспешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="85e7d-123">The DSP plug-in returns an appropriate success or failure **HRESULT**.</span></span>
    2.  <span data-ttu-id="85e7d-124">Проигрыватель Windows Media вызывает **имфтрансформ::P роцессаутпут**, передавая указатель на массив **\_ \_ \_ буферов выходных данных MFT** (которые содержат буферы вывода) в подключаемый модуль DSP.</span><span class="sxs-lookup"><span data-stu-id="85e7d-124">Windows Media Player calls **IMFTransform::ProcessOutput**, passing a pointer to an array of **MFT\_OUTPUT\_DATA\_BUFFER** structures (which contain output buffers) to the DSP plug-in.</span></span>
    3.  <span data-ttu-id="85e7d-125">Подключаемый модуль DSP обрабатывает данные во входном буфере, а затем копирует их в соответствующий выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="85e7d-125">The DSP plug-in processes the data in the input buffer and then copies the data to the appropriate output buffer.</span></span> <span data-ttu-id="85e7d-126">Подключаемый модуль DSP освобождает счетчик ссылок на объект входного буфера, когда все данные в буфере обрабатывались.</span><span class="sxs-lookup"><span data-stu-id="85e7d-126">The DSP plug-in releases the reference count on the input buffer object when all the data in the buffer has been processed.</span></span> <span data-ttu-id="85e7d-127">Затем подключаемый модуль DSP возвращает соответствующее **значение HRESULT** Success или failure.</span><span class="sxs-lookup"><span data-stu-id="85e7d-127">The DSP plug-in then returns an appropriate success or failure **HRESULT**.</span></span>
    4.  <span data-ttu-id="85e7d-128">Проигрыватель Windows Media визуализирует содержимое в выходном буфере.</span><span class="sxs-lookup"><span data-stu-id="85e7d-128">Windows Media Player renders the content in the output buffer.</span></span>

<span data-ttu-id="85e7d-129">Этот процесс повторяется постоянно, пока подключаемый модуль включен и проигрыватель Windows Media имеет содержимое для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="85e7d-129">This process repeats continuously while the plug-in is enabled and Windows Media Player has content to render.</span></span>

> [!Note]  
> <span data-ttu-id="85e7d-130">Не записывайте код, который записывает данные во входной буфер или считывает данные из выходного буфера.</span><span class="sxs-lookup"><span data-stu-id="85e7d-130">Do not write code that writes data to the input buffer or reads data from the output buffer.</span></span> <span data-ttu-id="85e7d-131">Неправильное обращение к буферам данных может привести к непредвиденным результатам.</span><span class="sxs-lookup"><span data-stu-id="85e7d-131">Incorrectly accessing data buffers may yield unexpected results.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="85e7d-132">См. также</span><span class="sxs-lookup"><span data-stu-id="85e7d-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85e7d-133">**Обзор подключаемого модуля DSP**</span><span class="sxs-lookup"><span data-stu-id="85e7d-133">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




