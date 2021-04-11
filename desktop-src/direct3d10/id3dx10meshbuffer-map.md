---
description: Получите указатель на память буфера сетки, чтобы изменить ее содержимое.
ms.assetid: d15ed47a-450e-404a-bcc2-a641abc2d02e
title: 'Метод ID3DX10MeshBuffer:: Map (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer.Map
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1b8cb03e128a6673963ce2d3cde993babb03da5c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354943"
---
# <a name="id3dx10meshbuffermap-method"></a>Метод ID3DX10MeshBuffer:: Map

Получите указатель на память буфера сетки, чтобы изменить ее содержимое.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Map(
  [out] void   **ppData,
  [out] SIZE_T *pSize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппдата* \[ заполняет\]
</dt> <dd>

Тип: **void \* \***

Указатель на данные буфера.

</dd> <dt>

*псизе* \[ заполняет\]
</dt> <dd>

Type: **[ **size \_ T**](../winprog/windows-data-types.md)\***

Размер буфера в байтах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Комментарии



|                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|
| Различия между Direct3D 9 и Direct3D 10:<br/> Map () в Direct3D 10 аналогичен карте ресурсов () в Direct3D 9.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX10MeshBuffer](id3dx10meshbuffer.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
