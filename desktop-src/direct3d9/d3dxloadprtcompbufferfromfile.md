---
description: Загружает в память сжатый предварительно вычисленный буфер радианценой пересылки (PRT), сохраненный на диске.
ms.assetid: ea8bb0d6-f3ed-4ba0-ac87-02e9ac3ae15f
title: Функция D3DXLoadPRTCompBufferFromFile (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPRTCompBufferFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a05a5712961e8bf72f4eb67f7e644d0f41150b812800fc1c0bd9bca464e3f54f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027384"
---
# <a name="d3dxloadprtcompbufferfromfile-function"></a>Функция D3DXLoadPRTCompBufferFromFile

Загружает в память сжатый предварительно вычисленный буфер радианценой пересылки (PRT), сохраненный на диске.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXLoadPRTCompBufferFromFile(
  _In_    LPCSTR              pFileName,
  _Inout_ LPD3DXPRTCOMPBUFFER *ppBuffer
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфиленаме* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Имя файла, из которого загружаются данные сжатого буфера.

</dd> <dt>

*ппбуффер* \[ в, out\]
</dt> <dd>

Тип: **[ **LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***

Адрес указателя на выходной объект [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Параметр компилятора также определяет версию функции. Если определен Юникод, вызов функции разрешается в D3DXLoadPRTCompBufferFromFileW. В противном случае вызов функции разрешается в D3DXLoadPRTCompBufferFromFileA.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Предварительно вычисленные функции пересылки Радианце](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
