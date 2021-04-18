---
description: Сохраняет том в файл на диске.
ms.assetid: 4d33fba5-e003-4385-b683-aff6723af2a5
title: Функция D3DXSaveVolumeToFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveVolumeToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 36550cda8d9ef664f96e236d2770a82c88412772
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694130"
---
# <a name="d3dxsavevolumetofile-function"></a>Функция D3DXSaveVolumeToFile

Сохраняет том в файл на диске.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXSaveVolumeToFile(
  _In_       LPCTSTR              pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT DestFormat,
  _In_       LPDIRECT3DVOLUME9    pSrcVolume,
  _In_ const PALETTEENTRY         *pSrcPalette,
  _In_ const D3DBOX               *pSrcBox
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдестфиле* \[ окне\]
</dt> <dd>

Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Указатель на строку, указывающую имя файла конечного изображения. Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР. В противном случае строковый тип данных разрешается в LPCSTR. См. заметки.

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

## <a name="remarks"></a>Комментарии

Параметр компилятора также определяет версию функции. Если определен Юникод, вызов функции разрешается в D3DXSaveVolumeToFileW. В противном случае вызов функции разрешается в >D3DXSaveVolumeToFileA, так как используются строки ANSI.

Эта функция обрабатывает преобразование в форматы сжатой текстуры и из них.

Если том является нединамическим (из-за параметра использования, установленного в значение 0 при создании) и расположен в видеопамяти (пул памяти со значением D3DPOOL \_ по умолчанию), [**D3DXSaveTextureToFile**](d3dxsavetexturetofile.md) завершится сбоем, так как D3DX не сможет блокировать нединамические тома, расположенные в видеопамяти.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции текстуры в D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXSaveSurfaceToFile**](d3dxsavesurfacetofile.md)
</dt> <dt>

[**D3DXSaveTextureToFile**](d3dxsavetexturetofile.md)
</dt> <dt>

[**D3DXSaveVolumeToFileInMemory**](d3dxsavevolumetofileinmemory.md)
</dt> </dl>

 

 
