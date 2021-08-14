---
description: Сохраняет том в буфере. Метод создает буфер ID3DXBuffer для хранения данных и возвращает этот объект.
ms.assetid: 4887ff1f-7904-4764-b284-b2c8e037f806
title: Функция D3DXSaveVolumeToFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveVolumeToFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f7c7326609d6d3c006f3c97aeff18de425a27569db63378864fc34335558117e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118298407"
---
# <a name="d3dxsavevolumetofileinmemory-function"></a>Функция D3DXSaveVolumeToFileInMemory

Сохраняет том в буфере. Метод создает буфер [**ID3DXBuffer**](id3dxbuffer.md) для хранения данных и возвращает этот объект.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXSaveVolumeToFileInMemory(
  _Out_       LPD3DXBUFFER         *ppDestBuf,
  _In_        D3DXIMAGE_FILEFORMAT DestFormat,
  _In_        LPDIRECT3DVOLUME9    pSrcVolume,
  _In_  const PALETTEENTRY         *pSrcPalette,
  _In_  const D3DBOX               *pSrcBox
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппдестбуф* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Адрес указателя на буфер [**ID3DXBuffer**](id3dxbuffer.md) , в котором будет храниться изображение.

</dd> <dt>

*Дестформат* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**

[**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md) , указывающий формат файла, используемый при сохранении. Эта функция поддерживает сохранение во всех форматах **\_ FILEFORMAT D3DXIMAGE** , кроме переносимых пиксмап (. ppm) и Targa/формат графического адаптера (. TGA).

</dd> <dt>

*псркволуме* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**

Указатель на интерфейс [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) , содержащий изображение для сохранения.

</dd> <dt>

*псркпалетте* \[ окне\]
</dt> <dd>

Тип: **const [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , содержащую палитру цветов 256. Этот параметр может принимать значение **NULL**.

</dd> <dt>

*псркбокс* \[ окне\]
</dt> <dd>

Тип: **const [**D3DBOX**](d3dbox.md) \***

Указатель на структуру [**D3DBOX**](d3dbox.md) . Указывает поле источника. Присвойте этому параметру **значение NULL** , чтобы указать весь том.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть следующим: D3DERR \_ инвалидкалл

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции текстуры в D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXSaveVolumeToFile**](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
