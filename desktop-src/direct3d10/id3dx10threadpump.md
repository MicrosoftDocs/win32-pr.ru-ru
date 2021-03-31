---
description: Используется для асинхронного выполнения задач и создания с помощью D3DX10CreateThreadPump.
ms.assetid: 8d03c94a-9b64-464c-b0f4-4e5f5a00503f
title: Интерфейс ID3DX10ThreadPump (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9fe3f0ca5955963864ef18de5d86fe03083d3f3b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157259"
---
# <a name="id3dx10threadpump-interface"></a>Интерфейс ID3DX10ThreadPump

Используется для асинхронного выполнения задач и создания с помощью [**D3DX10CreateThreadPump**](d3dx10createthreadpump.md). Существует несколько D3DX10 интерфейсов API, которые при необходимости могут принимать конвейер потока в качестве параметра, например [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) и [**D3DX10CompileFromFile**](d3dx10compilefromfile.md) (см. раздел Примечания для полного списка). Если конвейер потока передается в эти API, они будут выполняться асинхронно в отдельном потоке конвейера потока. Преимущество этого подхода заключается в том, что она может затруднить загрузку и обработку больших объемов данных, не оказывая заметного снижения производительности на экране.

## <a name="members"></a>Элементы

Интерфейс **ID3DX10ThreadPump** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10ThreadPump** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DX10ThreadPump** содержит следующие методы.



| Метод                                                                     | Описание                                                                                                                                                                                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**аддворкитем**](id3dx10threadpump-addworkitem.md)                       | Добавьте рабочий элемент в конвейер потоков.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| [**жеткуеуестатус**](id3dx10threadpump-getqueuestatus.md)                 | Возвращает количество элементов в каждой из трех очередей в конвейере потока.<br/>                                                                                                                                                                                                                                                                                                                                           |
| [**жетворкитемкаунт**](id3dx10threadpump-getworkitemcount.md)             | Получение количества рабочих элементов, находящихся в настоящий момент в конвейере потоков.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| [**процессдевицеворкитемс**](id3dx10threadpump-processdeviceworkitems.md) | Задание рабочих элементов для устройства после завершения загрузки и обработки. Когда конвейер потока закончит загрузку и обработку ресурса или шейдера, он будет хранить его в очереди до вызова этого API, после чего обработанные элементы будут установлены на устройство. Это полезно для управления объемом обработки, который тратится на привязку ресурсов к устройству для каждого кадра. См. примечания.<br/> |
| [**пуржеаллитемс**](id3dx10threadpump-purgeallitems.md)                   | Очистка всех рабочих элементов из конвейера потоков.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| [**ваитфораллитемс**](id3dx10threadpump-waitforallitems.md)               | Дождитесь завершения обработки всех рабочих элементов в конвейере потока.<br/>                                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Комментарии

Конвейер потоков загружает и обрабатывает данные в 3-этапном процессе. Он выглядит так:

1.  Загрузка и распаковка данных с помощью загрузчика данных. У объекта загрузчика данных есть три метода, которые будут вызываться конвейером потоков во внутреннем процессе загрузки и распаковки данных: [**ID3DX10DataLoader:: Load**](id3dx10dataloader-load.md), [**ID3DX10DataLoader::D екомпресс**](id3dx10dataloader-decompress.md)и [**ID3DX10DataLoader::D естрой**](id3dx10dataloader-destroy.md). Конкретные функциональные возможности этих трех интерфейсов API различаются в зависимости от типа загружаемых и распакованных данных. Интерфейс загрузчика данных также может быть унаследован, и его API-интерфейсы можно изменить, если он загружает файл данных, определенный в собственном пользовательском формате.
2.  Обработка данных с помощью обработчика данных. Объект обработчика данных имеет три метода, которые конвейер потока будет вызывать внутренне при обработке данных: [**ID3DX10DataProcessor::P шаблоны**](id3dx10dataprocessor-process.md), [**ID3DX10DataProcessor:: креатедевицеобжект**](id3dx10dataprocessor-createdeviceobject.md)и [**ID3DX10DataProcessor::D естрой**](id3dx10dataprocessor-destroy.md). Способ обработки данных будет отличаться в зависимости от типа данных. Например, если данные являются текстурой, хранящейся в формате JPEG, **ID3DX10DataProcessor::P шаблоны** выполняет распаковку JPEG, чтобы получить необработанные биты изображения изображения. Если данные являются шейдером, то **ID3DX10DataProcessor::P шаблоны** будет компилировать HLSL в байт-код. После обработки данных объект устройства будет создан для этих данных (с помощью **ID3DX10DataProcessor:: креатедевицеобжект**), а объект будет добавлен в очередь объектов устройств. Интерфейс обработчика данных также может быть унаследован и его API-интерфейсы могут быть изменены, если один из них обрабатывает файл данных, определенный в собственном пользовательском формате.
3.  Привяжите объект устройства к устройству. Это делается, когда одно приложение вызывает [**ID3DX10ThreadPump::P роцессдевицеворкитемс**](id3dx10threadpump-processdeviceworkitems.md), которое привязывает указанное число объектов в очереди объектов устройств к устройству.

Конвейер потока можно использовать для загрузки данных одним из двух способов: путем вызова API, который принимает потоковый цикл в качестве параметра, например [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) и [**D3DX10CompileFromFile**](d3dx10compilefromfile.md), или путем вызова [**ID3DX10ThreadPump:: аддворкитем**](id3dx10threadpump-addworkitem.md). В случае с интерфейсами API, которые принимают потоковый цикл, загрузчик данных и обработчик данных создаются внутренним образом. В случае с **аддворкитем** загрузчик данных и обработчик данных должны быть созданы заранее, а затем передаваться в аддворкитем. D3DX10 предоставляет набор API-интерфейсов для создания загрузчиков данных и обработчиков данных, которые имеют функциональные возможности для загрузки и обработки общих форматов данных (см. примечания по полному списку интерфейсов API). Для пользовательских форматов данных интерфейсы загрузчика данных и обработчика данных должны быть унаследованы, а их методы должны быть переопределены.

Объект насоса потока занимает значительный объем ресурсов, поэтому обычно для каждого приложения необходимо создать только один ресурс.

Встроенные загрузчики данных D3DX10



|                                                                            |                                          |
|----------------------------------------------------------------------------|------------------------------------------|
| [**D3DX10CreateAsyncFileLoader**](d3dx10createasyncfileloader.md)         | Асинхронно Создайте файловый загрузчик.     |
| [**D3DX10CreateAsyncMemoryLoader**](d3dx10createasyncmemoryloader.md)     | Асинхронное создание загрузчика данных.     |
| [**D3DX10CreateAsyncResourceLoader**](d3dx10createasyncresourceloader.md) | Асинхронное создание загрузчика ресурсов. |



 

Встроенные обработчики данных D3DX10



|                                                                                                  |                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3DX10CreateAsyncTextureProcessor**](d3dx10createasynctextureprocessor.md)                   | Создайте обработчик данных, который будет использоваться в конвейере потоков. Этот API похож на D3DX10CreateAsyncTextureInfoProcessor, но он также загружает текстуру. |
| [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md)           | Создайте обработчик данных, который будет использоваться в конвейере потоков.                                                                                             |
| [**D3DX10CreateAsyncShaderCompilerProcessor**](d3dx10createasyncshadercompilerprocessor.md)     | Скомпилируйте шейдер и создайте обработчик данных в асинхронном режиме.                                                                                       |
| [**D3DX10CreateAsyncEffectCompilerProcessor**](d3dx10createasynceffectcompilerprocessor.md)     | Асинхронное создание влияния на обработчик данных.                                                                                             |
| [**D3DX10CreateAsyncEffectCreateProcessor**](d3dx10createasynceffectcreateprocessor.md)         | Асинхронное создание пула эффектов.                                                                                                              |
| [**D3DX10CreateAsyncEffectPoolCreateProcessor**](d3dx10createasynceffectpoolcreateprocessor.md) | Создание обработчика данных в асинхронном режиме.                                                                                                            |
| [**D3DX10CreateAsyncShaderPreprocessProcessor**](d3dx10createasyncshaderpreprocessprocessor.md) | Асинхронно Создайте обработчик данных для шейдера.                                                                                               |



 

Интерфейсы API, принимающие потоковый насос в качестве параметра.



|                                                                                                  |                                                                  |
|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**D3DX10CompileFromFile**](d3dx10compilefromfile.md)                                           | Скомпилируйте шейдер из файла.                                    |
| [**D3DX10CompileFromMemory**](d3dx10compilefrommemory.md)                                       | Скомпилируйте шейдер, находящийся в памяти.                             |
| [**D3DX10CompileFromResource**](d3dx10compilefromresource.md)                                   | Скомпилируйте шейдер из ресурса.                                |
| [**D3DX10CreateEffectFromFile**](d3dx10createeffectfromfile.md)                                 | Создание результата из файла.                                    |
| [**D3DX10CreateEffectFromMemory**](d3dx10createeffectfrommemory.md)                             | Создание воздействия из памяти.                                    |
| [**D3DX10CreateEffectFromResource**](d3dx10createeffectfromresource.md)                         | Создание воздействия на ресурс.                                |
| [**D3DX10CreateEffectPoolFromFile**](d3dx10createeffectpoolfromfile.md)                         | Создайте пул эффектов из файла.                               |
| [**D3DX10CreateEffectPoolFromMemory**](d3dx10createeffectpoolfrommemory.md)                     | Создайте пул эффектов из файла, находящегося в памяти.            |
| [**D3DX10CreateEffectPoolFromResource**](d3dx10createeffectpoolfromresource.md)                 | Создание пула эффектов на основе ресурса.                           |
| [**D3DX10PreprocessShaderFromFile**](d3dx10preprocessshaderfromfile.md)                         | Создание шейдера из файла без его компиляции.                |
| [**D3DX10PreprocessShaderFromMemory**](d3dx10preprocessshaderfrommemory.md)                     | Создание шейдера из памяти без его компиляции.                |
| [**D3DX10PreprocessShaderFromResource**](d3dx10preprocessshaderfromresource.md)                 | Создание шейдера из ресурса без его компиляции.            |
| [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md)         | Создание представления "шейдер — представление ресурсов" из файла.                       |
| [**D3DX10CreateShaderResourceViewFromMemory**](d3dx10createshaderresourceviewfrommemory.md)     | Создание представления "шейдер — представление ресурсов" из файла в памяти.             |
| [**D3DX10CreateShaderResourceViewFromResource**](d3dx10createshaderresourceviewfromresource.md) | Создание представления "шейдер — представление ресурсов" из ресурса.                   |
| [**D3DX10GetImageInfoFromFile**](d3dx10getimageinfofromfile.md)                                 | Извлекает сведения о заданном файле изображения.                  |
| [**D3DX10GetImageInfoFromMemory**](d3dx10getimageinfofrommemory.md)                             | Получение сведений о изображении, которое уже загружено в память.       |
| [**D3DX10GetImageInfoFromResource**](d3dx10getimageinfofromresource.md)                         | Извлекает сведения об определенном изображении в ресурсе.         |
| [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md)                               | Создание ресурса текстуры из файла.                           |
| [**D3DX10CreateTextureFromMemory**](d3dx10createtexturefrommemory.md)                           | Создайте ресурс текстуры из файла, находящегося в системной памяти. |
| [**D3DX10CreateTextureFromResource**](d3dx10createtexturefromresource.md)                       | Создайте ресурс текстуры из другого ресурса.                 |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
