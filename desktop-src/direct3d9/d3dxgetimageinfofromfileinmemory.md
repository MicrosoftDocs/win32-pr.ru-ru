---
description: Извлекает сведения о заданном файле изображения в памяти.
ms.assetid: 6363aaf1-abfc-49df-9b99-be8a1c3540e1
title: Функция D3DXGetImageInfoFromFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetImageInfoFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c292c7969e9ebcaa565c3bc3c28bff93a075f5fffb0ad0672e45ead1458d26c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857035"
---
# <a name="d3dxgetimageinfofromfileinmemory-function"></a>Функция D3DXGetImageInfoFromFileInMemory

Извлекает сведения о заданном файле изображения в памяти.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXGetImageInfoFromFileInMemory(
  _In_ LPCVOID        pSrcData,
  _In_ UINT           SrcDataSize,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псркдата* \[ окне\]
</dt> <dd>

Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**

ПУСТОЙ указатель на исходный файл в памяти.

</dd> <dt>

*Сркдатасизе* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Размер файла в памяти, в байтах. .

</dd> <dt>

*псрЦинфо* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXIMAGE \_ info** .](d3dximage-info.md)\***

Указатель на структуру [**\_ сведений о D3DXIMAGE**](d3dximage-info.md) , которая будет заполнена описанием данных в исходном файле.

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

[**D3DXGetImageInfoFromFile**](d3dxgetimageinfofromfile.md)
</dt> <dt>

[**D3DXGetImageInfoFromResource**](d3dxgetimageinfofromresource.md)
</dt> </dl>

 

 
