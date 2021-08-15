---
title: Функция D3DX11CreateAsyncFileLoader (D3DX11async. h)
description: обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений магазина Windows. См. заметки. Создание загрузчика асинхронных файлов.
ms.assetid: ee24ac00-3636-4900-9b8a-27778c9a2152
keywords:
- D3DX11CreateAsyncFileLoader функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncFileLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc5997d31765df1de78ed6323a0176be024a5e26bb2eb81a0556f2abedbf2e5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124869"
---
# <a name="d3dx11createasyncfileloader-function"></a>Функция D3DX11CreateAsyncFileLoader

> [!Note]  
> библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений магазина Windows. См. заметки.

 

Создание загрузчика асинхронных файлов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX11CreateAsyncFileLoader(
  _In_  LPCTSTR           pFileName,
  _Out_ ID3DX11DataLoader **ppDataLoader
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфиленаме* \[ окне\]
</dt> <dd>

Тип: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Имя загружаемого файла. Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР. В противном случае тип данных разрешается в LPCSTR.

</dd> <dt>

*ппдаталоадер* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\*\***

Адрес указателя на загрузчик асинхронных данных (см. [**интерфейс ID3DX11DataLoader**](id3dx11dataloader.md)).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarks

Нет реализации асинхронного загрузчика за пределами D3DX 10 и D3DX 11.

для приложений магазина Windows, примеры DirectX (например, [пример учебника по Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) включают модуль **басиклоадер** , использующий среда выполнения Windows асинхронной модели программирования ([**метод asyncbase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).

для классических приложений Win32 можно использовать [среда выполнения с параллелизмом](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) для реализации чего-то, что аналогично среда выполнения Windows асинхронной модели программирования.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX11async. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX11. lib</dt> </dl>    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

