---
description: 'Метод ID3DXBaseMesh:: Жетаттрибутетабле — извлекает либо таблицу атрибутов для сетки, либо число записей, хранящихся в таблице атрибутов сетки.'
ms.assetid: 15b24137-0ff9-4299-971b-90fa4ef2686d
title: 'Метод ID3DXBaseMesh:: Жетаттрибутетабле (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetAttributeTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4933c3e15faee28448a653c5479be0d976abfd7bd913a7b50ef34acf4b52f6f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026504"
---
# <a name="id3dxbasemeshgetattributetable-method"></a>Метод ID3DXBaseMesh:: Жетаттрибутетабле

Извлекает либо таблицу атрибутов для сетки, либо число записей, хранящихся в таблице атрибутов сетки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetAttributeTable(
  [in, out] D3DXATTRIBUTERANGE *pAttribTable,
  [in, out] DWORD              *pAttribTableSize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*паттрибтабле* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***

Указатель на массив структур [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) , представляющий записи в таблице атрибутов сетки. Чтобы получить значение для Паттрибтаблесизе, укажите значение **null** .

</dd> <dt>

*паттрибтаблесизе* \[ в, out\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Указатель на количество записей, хранящихся в Паттрибтабле, или значение, которое должно быть заполнено количеством записей, хранящихся в таблице атрибутов сетки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Remarks

Таблица атрибутов создается с помощью [**ID3DXMesh:: optimize**](id3dxmesh--optimize.md) и передает D3DXMESHOPT \_ Аттрсорт для параметра flags.

Таблица атрибутов используется для поиска областей сетки, которые должны рисоваться с разными текстурами, состояниями рендеринга, материалами и т. д. Кроме того, приложение может использовать таблицу атрибутов для скрытия частей сетки, не рисуя заданный идентификатор атрибута при рисовании рамки.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
