---
description: Возвращает максимальное количество влияния на любую вершину в сетке.
ms.assetid: 012168e8-30e5-4571-b793-647ab23df068
title: 'Метод ID3DXSkinInfo:: Жетмаксвертексинфлуенцес (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetMaxVertexInfluences
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5cd33155ba5b306fc24e345f535a083c78031da243b291f2c36c5894561e270d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095714"
---
# <a name="id3dxskininfogetmaxvertexinfluences-method"></a>Метод ID3DXSkinInfo:: Жетмаксвертексинфлуенцес

Возвращает максимальное количество влияния на любую вершину в сетке.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetMaxVertexInfluences(
  [in] DWORD *maxVertexInfluences
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*максвертексинфлуенцес* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Указатель на максимальную влияние на вершину.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
