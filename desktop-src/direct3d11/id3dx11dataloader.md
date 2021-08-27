---
title: Интерфейс ID3DX11DataLoader (D3DX11core. h)
description: обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений магазина Windows. Объект загрузки данных, используемый интерфейсом ID3DX11ThreadPump для асинхронной загрузки данных.
ms.assetid: 878929ea-0228-4650-9ca0-f83d60d9f915
keywords:
- Интерфейс ID3DX11DataLoader Direct3D 11
- Интерфейс ID3DX11DataLoader Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11DataLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92b688fcbeff21edf23f6a3be1b39be5a9cf0000
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471650"
---
# <a name="id3dx11dataloader-interface"></a>Интерфейс ID3DX11DataLoader

> [!Note]  
> библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений магазина Windows.

 

Объект загрузки данных, используемый [**интерфейсом ID3DX11ThreadPump**](id3dx11threadpump.md) для асинхронной загрузки данных.

## <a name="members"></a>Элементы

Интерфейс **ID3DX11DataLoader** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ID3DX11DataLoader** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DX11DataLoader** содержит следующие методы.




| Метод | Описание | 
|--------|-------------|
| <a href="id3dx11dataloader-decompress.md"><strong>Распаковки</strong></a> | <blockquote>[!Note]<br />библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений магазина Windows.</blockquote><br /> Распаковывает закодированные данные.<br /> | 
| <a href="id3dx11dataloader-destroy.md"><strong>Завершить</strong></a> | <blockquote>[!Note]<br />библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений магазина Windows.</blockquote><br /> Уничтожает загрузчик после завершения рабочего элемента.<br /> | 
| <a href="id3dx11dataloader-load.md"><strong>Загрузить</strong></a> | <blockquote>[!Note]<br />библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений магазина Windows.</blockquote><br /> Загружает данные с диска.<br /> | 




 

## <a name="remarks"></a>Комментарии

Этот объект может быть унаследован и его члены переопределены. Это позволит вам настроить API для загрузки и распаковки собственных пользовательских форматов файлов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                              |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>D3DX11core. h</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Интерфейсы D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

