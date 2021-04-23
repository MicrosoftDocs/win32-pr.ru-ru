---
title: Интерфейс ID3DX11ThreadPump (D3DX11core. h)
description: Конвейер потока выполняет задачи асинхронно.
ms.assetid: 1a99f728-149d-4800-a6e4-e3a00cf8cf4f
keywords:
- Интерфейс ID3DX11ThreadPump Direct3D 11
- Интерфейс ID3DX11ThreadPump Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b60cedaa4ef84cb9f3ea31cd619d7335cc09324e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135303"
---
# <a name="id3dx11threadpump-interface"></a><span data-ttu-id="f2fd3-105">Интерфейс ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="f2fd3-105">ID3DX11ThreadPump interface</span></span>

> [!Note]  
> <span data-ttu-id="f2fd3-106">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="f2fd3-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="f2fd3-107">Конвейер потока выполняет задачи асинхронно.</span><span class="sxs-lookup"><span data-stu-id="f2fd3-107">A thread pump executes tasks asynchronously.</span></span> <span data-ttu-id="f2fd3-108">Он создается путем вызова [**D3DX11CreateThreadPump**](d3dx11createthreadpump.md).</span><span class="sxs-lookup"><span data-stu-id="f2fd3-108">It is created by calling [**D3DX11CreateThreadPump**](d3dx11createthreadpump.md).</span></span> <span data-ttu-id="f2fd3-109">Существует несколько интерфейсов API, принимающих дополнительный потоковый конвейер в качестве параметра, например [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) и [**D3DX11CompileFromFile**](d3dx11compilefromfile.md). Если передать в эти API интерфейс конвейера потока, функции будут выполняться асинхронно в отдельном потоке.</span><span class="sxs-lookup"><span data-stu-id="f2fd3-109">There are several APIs that take an optional thread pump as a parameter, such as [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) and [**D3DX11CompileFromFile**](d3dx11compilefromfile.md); if you pass a thread pump interface into these APIs, the functions will execute asynchronously on a separate thread.</span></span> <span data-ttu-id="f2fd3-110">В частности, на многопроцессорных компьютерах конвейер потоков может загружать ресурсы и обрабатывать данные без заметного снижения производительности.</span><span class="sxs-lookup"><span data-stu-id="f2fd3-110">Particularly on multiprocessor machines, a thread pump can load resources and process data without a noticeable decrease in performance.</span></span>

## <a name="members"></a><span data-ttu-id="f2fd3-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="f2fd3-111">Members</span></span>

<span data-ttu-id="f2fd3-112">Интерфейс **ID3DX11ThreadPump** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f2fd3-112">The **ID3DX11ThreadPump** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f2fd3-113">**ID3DX11ThreadPump** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f2fd3-113">**ID3DX11ThreadPump** also has these types of members:</span></span>

-   [<span data-ttu-id="f2fd3-114">Методы</span><span class="sxs-lookup"><span data-stu-id="f2fd3-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f2fd3-115">Методы</span><span class="sxs-lookup"><span data-stu-id="f2fd3-115">Methods</span></span>

<span data-ttu-id="f2fd3-116">Интерфейс **ID3DX11ThreadPump** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="f2fd3-116">The **ID3DX11ThreadPump** interface has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="f2fd3-117">Метод</span><span class="sxs-lookup"><span data-stu-id="f2fd3-117">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="f2fd3-118">Описание</span><span class="sxs-lookup"><span data-stu-id="f2fd3-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="f2fd3-119"><a href="id3dx11threadpump-addworkitem.md"><strong>аддворкитем</strong></a></span><span class="sxs-lookup"><span data-stu-id="f2fd3-119"><a href="id3dx11threadpump-addworkitem.md"><strong>AddWorkItem</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="f2fd3-120">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="f2fd3-120">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="f2fd3-121">Добавляет рабочий элемент в конвейер потока.</span><span class="sxs-lookup"><span data-stu-id="f2fd3-121">Adds a work item to the thread pump.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="f2fd3-122"><a href="id3dx11threadpump-getqueuestatus.md"><strong>жеткуеуестатус</strong></a></span><span class="sxs-lookup"><span data-stu-id="f2fd3-122"><a href="id3dx11threadpump-getqueuestatus.md"><strong>GetQueueStatus</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="f2fd3-123">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="f2fd3-123">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="f2fd3-124">Возвращает количество элементов в каждой из трех очередей в конвейере потока.</span><span class="sxs-lookup"><span data-stu-id="f2fd3-124">Gets the number of items in each of the three queues inside the thread pump.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="f2fd3-125"><a href="id3dx11threadpump-getworkitemcount.md"><strong>жетворкитемкаунт</strong></a></span><span class="sxs-lookup"><span data-stu-id="f2fd3-125"><a href="id3dx11threadpump-getworkitemcount.md"><strong>GetWorkItemCount</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="f2fd3-126">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="f2fd3-126">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="f2fd3-127">Возвращает количество рабочих элементов в конвейере потока.</span><span class="sxs-lookup"><span data-stu-id="f2fd3-127">Gets the number of work items in the thread pump.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="f2fd3-128"><a href="id3dx11threadpump-processdeviceworkitems.md"><strong>процессдевицеворкитемс</strong></a></span><span class="sxs-lookup"><span data-stu-id="f2fd3-128"><a href="id3dx11threadpump-processdeviceworkitems.md"><strong>ProcessDeviceWorkItems</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="f2fd3-129">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="f2fd3-129">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="f2fd3-130">Задает рабочие элементы для устройства после завершения загрузки и обработки.</span><span class="sxs-lookup"><span data-stu-id="f2fd3-130">Sets work items to the device after they have finished loading and processing.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="f2fd3-131"><a href="id3dx11threadpump-purgeallitems.md"><strong>пуржеаллитемс</strong></a></span><span class="sxs-lookup"><span data-stu-id="f2fd3-131"><a href="id3dx11threadpump-purgeallitems.md"><strong>PurgeAllItems</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="f2fd3-132">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="f2fd3-132">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="f2fd3-133">Удаляет все рабочие элементы из конвейера потоков.</span><span class="sxs-lookup"><span data-stu-id="f2fd3-133">Clears all work items from the thread pump.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="f2fd3-134"><a href="id3dx11threadpump-waitforallitems.md"><strong>ваитфораллитемс</strong></a></span><span class="sxs-lookup"><span data-stu-id="f2fd3-134"><a href="id3dx11threadpump-waitforallitems.md"><strong>WaitForAllItems</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="f2fd3-135">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="f2fd3-135">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="f2fd3-136">Ожидает завершения всех рабочих элементов в конвейере потока.</span><span class="sxs-lookup"><span data-stu-id="f2fd3-136">Waits for all work items in the thread pump to finish.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="f2fd3-137">Примечания</span><span class="sxs-lookup"><span data-stu-id="f2fd3-137">Remarks</span></span>

### <a name="using-a-thread-pump"></a><span data-ttu-id="f2fd3-138">Использование конвейера потоков</span><span class="sxs-lookup"><span data-stu-id="f2fd3-138">Using a Thread Pump</span></span>

<span data-ttu-id="f2fd3-139">Конвейер потоков загружает и обрабатывает данные с помощью следующего процесса в три этапа:</span><span class="sxs-lookup"><span data-stu-id="f2fd3-139">The thread pump loads and processes data using the following three-step process:</span></span>

1.  <span data-ttu-id="f2fd3-140">Загрузка и распаковка данных с помощью [**загрузчика данных**](id3dx11dataloader.md).</span><span class="sxs-lookup"><span data-stu-id="f2fd3-140">Load and decompress the data with a [**Data Loader**](id3dx11dataloader.md).</span></span> <span data-ttu-id="f2fd3-141">У объекта загрузчика данных есть три метода, которые будут вызываться конвейером потоков во внутреннем процессе загрузки и распаковки данных: [**ID3DX11DataLoader:: Load**](id3dx11dataloader-load.md), [**ID3DX11DataLoader::D екомпресс**](id3dx11dataloader-decompress.md)и [**ID3DX11DataLoader::D естрой**](id3dx11dataloader-destroy.md).</span><span class="sxs-lookup"><span data-stu-id="f2fd3-141">The data loader object has three methods that the thread pump will call internally as it is loading and decompressing the data: [**ID3DX11DataLoader::Load**](id3dx11dataloader-load.md), [**ID3DX11DataLoader::Decompress**](id3dx11dataloader-decompress.md), and [**ID3DX11DataLoader::Destroy**](id3dx11dataloader-destroy.md).</span></span> <span data-ttu-id="f2fd3-142">Конкретные функциональные возможности этих трех интерфейсов API различаются в зависимости от типа загружаемых и распакованных данных.</span><span class="sxs-lookup"><span data-stu-id="f2fd3-142">The specific functionality of these three APIs differs depending on the type of data being loaded and decompressed.</span></span> <span data-ttu-id="f2fd3-143">Интерфейс загрузчика данных также может быть унаследован, и его API-интерфейсы можно изменить, если он загружает файл данных, определенный в собственном пользовательском формате.</span><span class="sxs-lookup"><span data-stu-id="f2fd3-143">The data loader interface can also be inherited and its APIs can be changed if one is loading a data file defined in one's own custom format.</span></span>
2.  <span data-ttu-id="f2fd3-144">Обработка данных с помощью [**обработчика данных**](id3dx11dataprocessor.md).</span><span class="sxs-lookup"><span data-stu-id="f2fd3-144">Process the data with a [**Data Processor**](id3dx11dataprocessor.md).</span></span> <span data-ttu-id="f2fd3-145">Объект обработчика данных имеет три метода, которые конвейер потока будет вызывать внутренне при обработке данных: [**ID3DX11DataProcessor::P шаблоны**](id3dx11dataprocessor-process.md), [**ID3DX11DataProcessor:: креатедевицеобжект**](id3dx11dataprocessor-createdeviceobject.md)и [**ID3DX11DataProcessor::D естрой**](id3dx11dataprocessor-destroy.md).</span><span class="sxs-lookup"><span data-stu-id="f2fd3-145">The data processor object has three methods that the thread pump will call internally as it is processing the data: [**ID3DX11DataProcessor::Process**](id3dx11dataprocessor-process.md), [**ID3DX11DataProcessor::CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md), and [**ID3DX11DataProcessor::Destroy**](id3dx11dataprocessor-destroy.md).</span></span> <span data-ttu-id="f2fd3-146">Способ обработки данных будет отличаться в зависимости от типа данных.</span><span class="sxs-lookup"><span data-stu-id="f2fd3-146">The way it processes the data will be different depending on the type of data.</span></span> <span data-ttu-id="f2fd3-147">Например, если данные являются текстурой, хранящейся в формате JPEG, [**ID3DX11DataProcessor::P шаблоны**](id3dx11dataprocessor-process.md) выполняет распаковку JPEG, чтобы получить необработанные биты изображения изображения.</span><span class="sxs-lookup"><span data-stu-id="f2fd3-147">For example, if the data is a texture stored as a JPEG, then [**ID3DX11DataProcessor::Process**](id3dx11dataprocessor-process.md) will do JPEG decompression to get the image's raw image bits.</span></span> <span data-ttu-id="f2fd3-148">Если данные являются шейдером, то [**ID3DX11DataProcessor::P шаблоны**](id3dx11dataprocessor-process.md) будет компилировать HLSL в байт-код.</span><span class="sxs-lookup"><span data-stu-id="f2fd3-148">If the data is a shader, then [**ID3DX11DataProcessor::Process**](id3dx11dataprocessor-process.md) will compile the HLSL into bytecode.</span></span> <span data-ttu-id="f2fd3-149">После обработки данных объект устройства будет создан для этих данных (с помощью [**ID3DX11DataProcessor:: креатедевицеобжект**](id3dx11dataprocessor-createdeviceobject.md)), а объект будет добавлен в очередь объектов устройств.</span><span class="sxs-lookup"><span data-stu-id="f2fd3-149">After the data has been processed a device object will be created for that data (with [**ID3DX11DataProcessor::CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md)) and the object will be added to a queue of device objects.</span></span> <span data-ttu-id="f2fd3-150">Интерфейс обработчика данных также может быть унаследован и его API-интерфейсы могут быть изменены, если один из них обрабатывает файл данных, определенный в собственном пользовательском формате.</span><span class="sxs-lookup"><span data-stu-id="f2fd3-150">The data processor interface can also be inherited and its APIs can be changed if one is processing a data file defined in one's own custom format.</span></span>
3.  <span data-ttu-id="f2fd3-151">Привяжите объект устройства к устройству.</span><span class="sxs-lookup"><span data-stu-id="f2fd3-151">Bind the device object to the device.</span></span> <span data-ttu-id="f2fd3-152">Это делается, когда одно приложение вызывает [**ID3DX11ThreadPump::P роцессдевицеворкитемс**](id3dx11threadpump-processdeviceworkitems.md), которое привязывает указанное число объектов в очереди объектов устройств к устройству.</span><span class="sxs-lookup"><span data-stu-id="f2fd3-152">This is done when one's application calls [**ID3DX11ThreadPump::ProcessDeviceWorkItems**](id3dx11threadpump-processdeviceworkitems.md), which will bind a specified number of objects in the queue of device objects to the device.</span></span>

<span data-ttu-id="f2fd3-153">Конвейер потока можно использовать для загрузки данных одним из двух способов: путем вызова API, который принимает потоковый цикл в качестве параметра, например [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) и [**D3DX11CompileFromFile**](d3dx11compilefromfile.md), или путем вызова [**ID3DX11ThreadPump:: аддворкитем**](id3dx11threadpump-addworkitem.md).</span><span class="sxs-lookup"><span data-stu-id="f2fd3-153">The thread pump can be used to load data in one of two ways: by calling an API that takes a thread pump as a parameter, such as [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) and [**D3DX11CompileFromFile**](d3dx11compilefromfile.md), or by calling [**ID3DX11ThreadPump::AddWorkItem**](id3dx11threadpump-addworkitem.md).</span></span> <span data-ttu-id="f2fd3-154">В случае с интерфейсами API, которые принимают потоковый цикл, загрузчик данных и обработчик данных создаются внутренним образом.</span><span class="sxs-lookup"><span data-stu-id="f2fd3-154">In the case of the APIs that take a thread pump, the data loader and data processor are created internally.</span></span> <span data-ttu-id="f2fd3-155">В случае с Аддворкитем загрузчик данных и обработчик данных должны быть созданы заранее, а затем передаваться в Аддворкитем.</span><span class="sxs-lookup"><span data-stu-id="f2fd3-155">In the case of AddWorkItem, the data loader and data processor must be created beforehand and are then passed into AddWorkItem.</span></span> <span data-ttu-id="f2fd3-156">D3DX11 предоставляет набор интерфейсов API для создания загрузчиков данных и обработчиков данных, которые обладают функциональными возможностями для загрузки и обработки общих форматов данных.</span><span class="sxs-lookup"><span data-stu-id="f2fd3-156">D3DX11 provides a set of APIs for creating data loaders and data processors that have functionality for loading and processing common data formats.</span></span> <span data-ttu-id="f2fd3-157">Для пользовательских форматов данных интерфейсы загрузчика данных и обработчика данных должны быть унаследованы, а их методы должны быть переопределены.</span><span class="sxs-lookup"><span data-stu-id="f2fd3-157">For custom data formats, the data loader and data processor interfaces must be inherited and their methods must be redefined.</span></span>

<span data-ttu-id="f2fd3-158">Объект насоса потока занимает значительный объем ресурсов, поэтому обычно для каждого приложения необходимо создать только один ресурс.</span><span class="sxs-lookup"><span data-stu-id="f2fd3-158">The thread pump object takes up a substantial amount of resources, so generally only one should be created per application.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2fd3-159">Требования</span><span class="sxs-lookup"><span data-stu-id="f2fd3-159">Requirements</span></span>



| <span data-ttu-id="f2fd3-160">Требование</span><span class="sxs-lookup"><span data-stu-id="f2fd3-160">Requirement</span></span> | <span data-ttu-id="f2fd3-161">Значение</span><span class="sxs-lookup"><span data-stu-id="f2fd3-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2fd3-162">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2fd3-162">Minimum supported client</span></span><br/> | <span data-ttu-id="f2fd3-163">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f2fd3-163">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="f2fd3-164">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2fd3-164">Minimum supported server</span></span><br/> | <span data-ttu-id="f2fd3-165">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f2fd3-165">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f2fd3-166">Header</span><span class="sxs-lookup"><span data-stu-id="f2fd3-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2fd3-167"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2fd3-167"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="f2fd3-168">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f2fd3-168">Library</span></span><br/>                  | <dl> <span data-ttu-id="f2fd3-169"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2fd3-169"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f2fd3-170">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2fd3-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2fd3-171">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="f2fd3-171">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

