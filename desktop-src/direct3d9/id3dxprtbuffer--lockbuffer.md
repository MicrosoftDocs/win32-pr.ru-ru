---
description: Блокирует диапазон демонстрационных данных вершин или шаг текселя и получает указатель на расположение в буферной памяти.
ms.assetid: 8de2725f-507e-41ee-828d-2fb19cc2252c
title: 'Метод ID3DXPRTBuffer:: Локкбуффер (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.LockBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5d8e3b6310951a5784af99b913298c20d5556baa10b012926f3b68e44d402dbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606894"
---
# <a name="id3dxprtbufferlockbuffer-method"></a>Метод ID3DXPRTBuffer:: Локкбуффер

Блокирует диапазон демонстрационных данных вершин или шаг текселя и получает указатель на расположение в буферной памяти.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT LockBuffer(
  [in]  UINT  Start,
  [in]  UINT  NumSamples,
  [out] FLOAT **ppData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Запуск* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Индекс образца данных вершины или шаг текселя.

</dd> <dt>

*Нумсамплес* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Количество вершин (или пикселей текстуры) с выборкой.

</dd> <dt>

*ппдата* \[ заполняет\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)\*\***

Указатель на расположение в памяти, где начинается начальная выборка. Макет памяти данных буфера:


```
float fData[NumberSamples][NumberChannels][NumberCoefficients]      
```



</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение:

## <a name="remarks"></a>Remarks

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> <dt>

[**ID3DXPRTBuffer:: Жетнумчаннелс**](id3dxprtbuffer--getnumchannels.md)
</dt> <dt>

[**ID3DXPRTBuffer:: Жетнумкоеффс**](id3dxprtbuffer--getnumcoeffs.md)
</dt> <dt>

[**ID3DXPRTBuffer:: Жетнумсамплес**](id3dxprtbuffer--getnumsamples.md)
</dt> </dl>

 

 
