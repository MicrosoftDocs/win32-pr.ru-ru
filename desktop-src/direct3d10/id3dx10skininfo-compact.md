---
description: Ограничьте число костей, которые могут повлиять на вершину и/или ограничить объем влияния на кость на вершину.
ms.assetid: 75c4d2eb-0a43-494d-9642-4c08aa814794
title: 'Метод ID3DX10SkinInfo:: Compact (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.Compact
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3aab3534ea55d2f6675ef1e65b03d19f4c516562b242e284ee2865f98bc03f18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046912"
---
# <a name="id3dx10skininfocompact-method"></a>Метод ID3DX10SkinInfo:: Compact

Ограничьте число костей, которые могут повлиять на вершину и/или ограничить объем влияния на кость на вершину.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Compact(
  [in] UINT  MaxPerVertexInfluences,
  [in] UINT  ScaleMode,
  [in] float MinWeight
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Макспервертексинфлуенцес* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Максимальное число костей, которые могут повлиять на любую заданную вершину. Это значение пропускается, если оно больше значения, возвращенного [**ID3DX10SkinInfo:: жетмаксбонеинфлуенцес**](id3dx10skininfo-getmaxboneinfluences.md).

</dd> <dt>

*ScaleMode* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Флаг, описывающий, как масштабировать оставшиеся веса в заданной вершине после того, как некоторые из них были удалены с помощью Минвеигхт. Если D3DX10 \_ скининфо \_ не \_ указано масштабирование, весовые коэффициенты не будут масштабироваться вообще. Если \_ \_ указан параметр D3DX10 скининфо Scale \_ to \_ 1, то весовые коэффициенты, превышающие минвеигхт, будут масштабироваться до 1,0. Если указан параметр D3DX10 \_ скининфо \_ Scale for \_ \_ Total, то весовые коэффициенты, превышающие минвеигхт, будут масштабироваться, чтобы они добавлялись к исходному итогу.

</dd> <dt>

*Минвеигхт* \[ окне\]
</dt> <dd>

Тип: **float**

Минимальный процент влияния или веса, который может иметь любая кость на любой вершине. Это значение должно находиться в диапазоне от 0 до 1.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается ошибкой, возвращаемое значение может быть следующим: E \_ OUTOFMEMORY или e \_ INVALIDARG.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
