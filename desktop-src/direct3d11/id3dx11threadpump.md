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
# <a name="id3dx11threadpump-interface"></a>Интерфейс ID3DX11ThreadPump

> [!Note]  
> Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.

 

Конвейер потока выполняет задачи асинхронно. Он создается путем вызова [**D3DX11CreateThreadPump**](d3dx11createthreadpump.md). Существует несколько интерфейсов API, принимающих дополнительный потоковый конвейер в качестве параметра, например [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) и [**D3DX11CompileFromFile**](d3dx11compilefromfile.md). Если передать в эти API интерфейс конвейера потока, функции будут выполняться асинхронно в отдельном потоке. В частности, на многопроцессорных компьютерах конвейер потоков может загружать ресурсы и обрабатывать данные без заметного снижения производительности.

## <a name="members"></a>Элементы

Интерфейс **ID3DX11ThreadPump** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ID3DX11ThreadPump** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DX11ThreadPump** содержит следующие методы.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Метод</th>
<th style="text-align: left;">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11threadpump-addworkitem.md"><strong>аддворкитем</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.
</blockquote>
<br/> Добавляет рабочий элемент в конвейер потока.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="id3dx11threadpump-getqueuestatus.md"><strong>жеткуеуестатус</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.
</blockquote>
<br/> Возвращает количество элементов в каждой из трех очередей в конвейере потока.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11threadpump-getworkitemcount.md"><strong>жетворкитемкаунт</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.
</blockquote>
<br/> Возвращает количество рабочих элементов в конвейере потока.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="id3dx11threadpump-processdeviceworkitems.md"><strong>процессдевицеворкитемс</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.
</blockquote>
<br/> Задает рабочие элементы для устройства после завершения загрузки и обработки.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11threadpump-purgeallitems.md"><strong>пуржеаллитемс</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.
</blockquote>
<br/> Удаляет все рабочие элементы из конвейера потоков.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="id3dx11threadpump-waitforallitems.md"><strong>ваитфораллитемс</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.
</blockquote>
<br/> Ожидает завершения всех рабочих элементов в конвейере потока.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Примечания

### <a name="using-a-thread-pump"></a>Использование конвейера потоков

Конвейер потоков загружает и обрабатывает данные с помощью следующего процесса в три этапа:

1.  Загрузка и распаковка данных с помощью [**загрузчика данных**](id3dx11dataloader.md). У объекта загрузчика данных есть три метода, которые будут вызываться конвейером потоков во внутреннем процессе загрузки и распаковки данных: [**ID3DX11DataLoader:: Load**](id3dx11dataloader-load.md), [**ID3DX11DataLoader::D екомпресс**](id3dx11dataloader-decompress.md)и [**ID3DX11DataLoader::D естрой**](id3dx11dataloader-destroy.md). Конкретные функциональные возможности этих трех интерфейсов API различаются в зависимости от типа загружаемых и распакованных данных. Интерфейс загрузчика данных также может быть унаследован, и его API-интерфейсы можно изменить, если он загружает файл данных, определенный в собственном пользовательском формате.
2.  Обработка данных с помощью [**обработчика данных**](id3dx11dataprocessor.md). Объект обработчика данных имеет три метода, которые конвейер потока будет вызывать внутренне при обработке данных: [**ID3DX11DataProcessor::P шаблоны**](id3dx11dataprocessor-process.md), [**ID3DX11DataProcessor:: креатедевицеобжект**](id3dx11dataprocessor-createdeviceobject.md)и [**ID3DX11DataProcessor::D естрой**](id3dx11dataprocessor-destroy.md). Способ обработки данных будет отличаться в зависимости от типа данных. Например, если данные являются текстурой, хранящейся в формате JPEG, [**ID3DX11DataProcessor::P шаблоны**](id3dx11dataprocessor-process.md) выполняет распаковку JPEG, чтобы получить необработанные биты изображения изображения. Если данные являются шейдером, то [**ID3DX11DataProcessor::P шаблоны**](id3dx11dataprocessor-process.md) будет компилировать HLSL в байт-код. После обработки данных объект устройства будет создан для этих данных (с помощью [**ID3DX11DataProcessor:: креатедевицеобжект**](id3dx11dataprocessor-createdeviceobject.md)), а объект будет добавлен в очередь объектов устройств. Интерфейс обработчика данных также может быть унаследован и его API-интерфейсы могут быть изменены, если один из них обрабатывает файл данных, определенный в собственном пользовательском формате.
3.  Привяжите объект устройства к устройству. Это делается, когда одно приложение вызывает [**ID3DX11ThreadPump::P роцессдевицеворкитемс**](id3dx11threadpump-processdeviceworkitems.md), которое привязывает указанное число объектов в очереди объектов устройств к устройству.

Конвейер потока можно использовать для загрузки данных одним из двух способов: путем вызова API, который принимает потоковый цикл в качестве параметра, например [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) и [**D3DX11CompileFromFile**](d3dx11compilefromfile.md), или путем вызова [**ID3DX11ThreadPump:: аддворкитем**](id3dx11threadpump-addworkitem.md). В случае с интерфейсами API, которые принимают потоковый цикл, загрузчик данных и обработчик данных создаются внутренним образом. В случае с Аддворкитем загрузчик данных и обработчик данных должны быть созданы заранее, а затем передаваться в Аддворкитем. D3DX11 предоставляет набор интерфейсов API для создания загрузчиков данных и обработчиков данных, которые обладают функциональными возможностями для загрузки и обработки общих форматов данных. Для пользовательских форматов данных интерфейсы загрузчика данных и обработчика данных должны быть унаследованы, а их методы должны быть переопределены.

Объект насоса потока занимает значительный объем ресурсов, поэтому обычно для каждого приложения необходимо создать только один ресурс.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                 |
| Header<br/>                   | <dl> <dt>D3DX11core. h</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

