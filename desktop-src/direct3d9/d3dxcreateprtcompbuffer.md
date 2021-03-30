---
description: Создает сжатый предварительно вычисленный буфер радианценой пересылки (PRT) из несжатого объекта ID3DXPRTBuffer. Эта функция должна использоваться с буферами на уровне вершины или тома.
ms.assetid: 1464d2dd-05db-4d9a-84ac-39d57b6fff4f
title: Функция D3DXCreatePRTCompBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTCompBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6906067c8f2b412b58c728756ecaa6415168f05a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354920"
---
# <a name="d3dxcreateprtcompbuffer-function"></a>Функция D3DXCreatePRTCompBuffer

Создает сжатый предварительно вычисленный буфер радианценой пересылки (PRT) из несжатого объекта [**ID3DXPRTBuffer**](id3dxprtbuffer.md) . Эта функция должна использоваться с буферами на уровне вершины или тома.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXCreatePRTCompBuffer(
  _In_    D3DXSHCOMPRESSQUALITYTYPE Quality,
  _In_    UINT                      NumClusters,
  _In_    UINT                      NumPCA,
  _In_    LPD3DXSHPRTSIMCB          pCB,
  _In_    LPVOID                    lpUserContext,
  _In_    LPD3DXPRTBUFFER           pBuffer,
  _Inout_ LPD3DXPRTCOMPBUFFER       *ppBuffer
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Качество* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md)**

Качество сжатия сферических гармонических излучений (SH). См. [**D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md).

</dd> <dt>

*Нумклустерс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Количество кластеров, используемых для сжатия.

</dd> <dt>

*Нумпка* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Количество отдельных векторов анализа основных компонентов (PCA) для использования в каждом кластере.

</dd> <dt>

*ПКБ* \[ окне\]
</dt> <dd>

Тип: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**

Необязательный указатель на функцию обратного вызова [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) , используемый для вычисления процента завершенных вычислений сжатия PRT. Функция обратного вызова должна быть реализована, чтобы вернуть значение S \_ ОК для сохранения выполнения программы сжатия. Любое другое значение приведет к прерыванию сжатия. Может иметь **значение NULL**.

</dd> <dt>

*лпусерконтекст* \[ окне\]
</dt> <dd>

Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**

Необязательный указатель на определяемое пользователем значение, передаваемое функции обратного вызова [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) . Обычно используется приложением для передачи указателя на структуру данных, которая предоставляет сведения о контексте для функции обратного вызова. Может иметь **значение NULL**.

</dd> <dt>

*pBuffer* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Адрес указателя на несжатый объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , который будет сжат.

</dd> <dt>

*ппбуффер* \[ в, out\]
</dt> <dd>

Тип: **[ **LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***

Адрес указателя на выходной объект [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Предварительно вычисленные функции пересылки Радианце](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md)
</dt> <dt>

[**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)
</dt> </dl>

 

 
