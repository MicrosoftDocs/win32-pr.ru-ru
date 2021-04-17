---
title: Объект buffer
description: Объект buffer
ms.assetid: 0812261c-698c-4071-929c-4363a16dd5a8
keywords:
- Windows Media Format SDK, буферные объекты
- Расширенный системный формат (ASF), буферные объекты
- ASF (Расширенный системный формат), объекты buffer
- объекты, объекты buffer
- Объекты буфера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8a9a3c6acfa0b0780b07f2853f60fdd68d0eaf
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/21/2020
ms.locfileid: "105700817"
---
# <a name="buffer-object"></a><span data-ttu-id="03827-108">Объект buffer</span><span class="sxs-lookup"><span data-stu-id="03827-108">Buffer Object</span></span>

<span data-ttu-id="03827-109">Объект buffer используется для хранения образцов и их доставки между объектами пакета SDK Windows Media Format и приложением.</span><span class="sxs-lookup"><span data-stu-id="03827-109">A buffer object is used to hold samples and deliver them between the objects of the Windows Media Format SDK and your application.</span></span> <span data-ttu-id="03827-110">При написании файла входные образцы передаются в модуль записи с помощью объектов buffer.</span><span class="sxs-lookup"><span data-stu-id="03827-110">When you write a file, you pass your input samples to the writer using buffer objects.</span></span> <span data-ttu-id="03827-111">При чтении файла объект Reader или синхронный объект Reader предоставляет примеры для приложения в объектах буфера.</span><span class="sxs-lookup"><span data-stu-id="03827-111">When you read a file, the reader object or synchronous reader object provides samples to your application in buffer objects.</span></span>

<span data-ttu-id="03827-112">Для записи образцов в файл можно создать объект buffer с помощью метода [**ивмвритер:: аллокатесампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample) .</span><span class="sxs-lookup"><span data-stu-id="03827-112">For writing samples to a file, you can create a buffer object using the [**IWMWriter::AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample) method.</span></span> <span data-ttu-id="03827-113">Для чтения образцов объект Reader и синхронный объект Reader создают объекты буфера внутренним образом.</span><span class="sxs-lookup"><span data-stu-id="03827-113">For reading samples, the reader object and synchronous reader object both create buffer objects internally.</span></span> <span data-ttu-id="03827-114">При выборе вы можете выделить собственные объекты буфера для чтения файлов с помощью [**ивмреадераллокаторекс:: аллокатефораутпутекс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex) или [**Ивмреадераллокаторекс:: аллокатефорстреамекс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex).</span><span class="sxs-lookup"><span data-stu-id="03827-114">If you choose to, you can allocate your own buffer objects for file reading by using [**IWMReaderAllocatorEx::AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex) or [**IWMReaderAllocatorEx::AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex).</span></span>

<span data-ttu-id="03827-115">Каждый объект buffer поддерживает следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="03827-115">The following interfaces are supported by every buffer object.</span></span>



| <span data-ttu-id="03827-116">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="03827-116">Interface</span></span>                          | <span data-ttu-id="03827-117">Описание</span><span class="sxs-lookup"><span data-stu-id="03827-117">Description</span></span>                                                          |
|------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="03827-118">**инссбуффер**</span><span class="sxs-lookup"><span data-stu-id="03827-118">**INSSBuffer**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)   | <span data-ttu-id="03827-119">Элементы управления и предоставляют доступ к буферу.</span><span class="sxs-lookup"><span data-stu-id="03827-119">Controls and provides access to the buffer.</span></span>                          |
| [<span data-ttu-id="03827-120">**INSSBuffer2**</span><span class="sxs-lookup"><span data-stu-id="03827-120">**INSSBuffer2**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer2) | <span data-ttu-id="03827-121">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="03827-121">Not implemented.</span></span>                                                     |
| [<span data-ttu-id="03827-122">**INSSBuffer3**</span><span class="sxs-lookup"><span data-stu-id="03827-122">**INSSBuffer3**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) | <span data-ttu-id="03827-123">Поддерживает свойства буфера, используемые для расширений модулей данных.</span><span class="sxs-lookup"><span data-stu-id="03827-123">Supports buffer properties, which are used for data unit extensions.</span></span> |
| [<span data-ttu-id="03827-124">**INSSBuffer4**</span><span class="sxs-lookup"><span data-stu-id="03827-124">**INSSBuffer4**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) | <span data-ttu-id="03827-125">Перечисляет свойства буфера.</span><span class="sxs-lookup"><span data-stu-id="03827-125">Enumerates buffer properties.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="03827-126">См. также</span><span class="sxs-lookup"><span data-stu-id="03827-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03827-127">**Объекты**</span><span class="sxs-lookup"><span data-stu-id="03827-127">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




