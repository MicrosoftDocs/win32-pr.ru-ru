---
title: Преобразование данных из одного формата в другой
description: Преобразование данных из одного формата в другой
ms.assetid: df995b7d-ac45-4964-a1b0-efd079c0c010
keywords:
- Диспетчер аудиосжатия (ACM), преобразование данных
- ACM (диспетчер аудиосжатия), преобразование данных
- Примеры ACM, преобразование данных
- преобразование данных
- Функция Акмстреамопен
- Функция Акмстреамсизе
- Функция Акмстреампрепарехеадер
- Функция Акмстреамконверт
- Функция Акмстреамунпрепарехеадер
- Функция Акмстреамклосе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9645342aa9f19b2c31de77dc9d1031122ed0b2ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329755"
---
# <a name="converting-data-from-one-format-to-another"></a><span data-ttu-id="fb68b-113">Преобразование данных из одного формата в другой</span><span class="sxs-lookup"><span data-stu-id="fb68b-113">Converting Data from One Format to Another</span></span>

<span data-ttu-id="fb68b-114">ACM использует функции потока для поддержки преобразования формата данных.</span><span class="sxs-lookup"><span data-stu-id="fb68b-114">The ACM uses stream functions to support data format conversion.</span></span> <span data-ttu-id="fb68b-115">Преобразователи в ACM изменяют формат, но не тип данных.</span><span class="sxs-lookup"><span data-stu-id="fb68b-115">Converters in the ACM change the format, but not the data type.</span></span> <span data-ttu-id="fb68b-116">Например, модуль преобразователя может заменить 16-битные данные 44 кГц на 44-кГц, 8-разрядные данные.</span><span class="sxs-lookup"><span data-stu-id="fb68b-116">For example, a converter module can change 44-kHz, 16-bit data to 44-kHz, 8-bit data.</span></span>

<span data-ttu-id="fb68b-117">Следующие функции ACM поддерживают преобразование формата данных.</span><span class="sxs-lookup"><span data-stu-id="fb68b-117">The following ACM functions support data format conversion.</span></span> <span data-ttu-id="fb68b-118">Они перечислены в том порядке, в котором они обычно используются.</span><span class="sxs-lookup"><span data-stu-id="fb68b-118">They are listed in the order in which you would typically use them.</span></span>

-   <span data-ttu-id="fb68b-119">Функция [**акмстреамопен**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) открывает поток преобразования.</span><span class="sxs-lookup"><span data-stu-id="fb68b-119">The [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) function opens a conversion stream.</span></span>
-   <span data-ttu-id="fb68b-120">Функция [**акмстреамсизе**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) вычисляет соответствующий размер исходного или целевого буфера.</span><span class="sxs-lookup"><span data-stu-id="fb68b-120">The [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) function calculates the appropriate size of the source or destination buffer.</span></span>
-   <span data-ttu-id="fb68b-121">Функция [**акмстреампрепарехеадер**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader) готовит буферы источника и назначения для использования при преобразовании.</span><span class="sxs-lookup"><span data-stu-id="fb68b-121">The [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader) function prepares source and destination buffers to be used in a conversion.</span></span>
-   <span data-ttu-id="fb68b-122">Функция [**акмстреамконверт**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) преобразует данные из исходного буфера в формат назначения, записывая преобразованные данные в целевой буфер.</span><span class="sxs-lookup"><span data-stu-id="fb68b-122">The [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) function converts data in a source buffer into the destination format, writing the converted data into the destination buffer.</span></span>
-   <span data-ttu-id="fb68b-123">Функция [**акмстреамунпрепарехеадер**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) очищает исходный и целевой буферы, подготовленные **акмстреампрепарехеадер**.</span><span class="sxs-lookup"><span data-stu-id="fb68b-123">The [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) function cleans up the source and destination buffers prepared by **acmStreamPrepareHeader**.</span></span> <span data-ttu-id="fb68b-124">Необходимо вызвать эту функцию перед освобождением исходного и целевого буферов.</span><span class="sxs-lookup"><span data-stu-id="fb68b-124">You must call this function before freeing the source and destination buffers.</span></span>
-   <span data-ttu-id="fb68b-125">Функция [**акмстреамклосе**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) закрывает поток преобразования.</span><span class="sxs-lookup"><span data-stu-id="fb68b-125">The [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) function closes a conversion stream.</span></span>

<span data-ttu-id="fb68b-126">При преобразовании данных сначала укажите формат источника, а затем выберите формат назначения.</span><span class="sxs-lookup"><span data-stu-id="fb68b-126">When converting data, first identify the source format, then choose the destination format.</span></span> <span data-ttu-id="fb68b-127">Проще всего это сделать с помощью функции [**акмформатчусе**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , которая отображает диалоговое окно выбора формата и возвращает выбор формата пользователя.</span><span class="sxs-lookup"><span data-stu-id="fb68b-127">The easiest way to do this is by using the [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) function, which displays a format-selection dialog box and returns the user's format choice.</span></span>

<span data-ttu-id="fb68b-128">Если вы узнаете форматы источника и назначения, можно использовать [**акмстреамопен**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) для открытия потока преобразования.</span><span class="sxs-lookup"><span data-stu-id="fb68b-128">When you know the source and destination formats, you can use [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) to open a conversion stream.</span></span> <span data-ttu-id="fb68b-129">Затем можно использовать функцию [**акмстреамсизе**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) , чтобы определить соответствующие размеры буфера.</span><span class="sxs-lookup"><span data-stu-id="fb68b-129">Then you can use the [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) function to determine the appropriate buffer sizes.</span></span>

<span data-ttu-id="fb68b-130">Следующим шагом является подготовка буферов для использования в преобразовании с помощью [**акмстреампрепарехеадер**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader).</span><span class="sxs-lookup"><span data-stu-id="fb68b-130">The next step is to prepare the buffers to be used in the conversion by using [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader).</span></span>

<span data-ttu-id="fb68b-131">Чтобы выполнить преобразование, используйте [**акмстреамконверт**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) , пока не будут обработаны все буферы.</span><span class="sxs-lookup"><span data-stu-id="fb68b-131">To perform the conversion, use [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) until all the buffers have been processed.</span></span> <span data-ttu-id="fb68b-132">По завершении преобразования используйте [**акмстреамунпрепарехеадер**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) для очистки буферов, а затем используйте [**акмстреамклосе**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) для закрытия потока преобразования.</span><span class="sxs-lookup"><span data-stu-id="fb68b-132">When the conversion is complete, use [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) to clean up the buffers and then use [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) to close the conversion stream.</span></span>

 

 




