---
title: Интерфейс ID3DX11DataProcessor (D3DX11core. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Объект обработки данных, используемый интерфейсом ID3DX11ThreadPump для асинхронной загрузки данных.
ms.assetid: ab893879-416f-4b17-9035-a7f03a62b753
keywords:
- Интерфейс ID3DX11DataProcessor Direct3D 11
- Интерфейс ID3DX11DataProcessor Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e421a6e840665220311e5a27c0692cd7f347e7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104984148"
---
# <a name="id3dx11dataprocessor-interface"></a>Интерфейс ID3DX11DataProcessor

> [!Note]  
> Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.

 

Объект обработки данных, используемый [**интерфейсом ID3DX11ThreadPump**](id3dx11threadpump.md) для асинхронной загрузки данных.

## <a name="members"></a>Элементы

Интерфейс **ID3DX11DataProcessor** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ID3DX11DataProcessor** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DX11DataProcessor** содержит следующие методы.



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
<td style="text-align: left;"><a href="id3dx11dataprocessor-createdeviceobject.md"><strong>креатедевицеобжект</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.
</blockquote>
<br/> Создает объект устройства.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="id3dx11dataprocessor-destroy.md"><strong>Завершить</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.
</blockquote>
<br/> Уничтожает процессор после завершения рабочего элемента.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11dataprocessor-process.md"><strong>Процесс</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.
</blockquote>
<br/> Обрабатывает данные.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Примечания

Этот объект может быть унаследован и его члены переопределяются для обработки пользовательских форматов файлов.

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

 

