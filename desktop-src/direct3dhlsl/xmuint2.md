---
title: Структура XMUINT2
description: Описывает двумерный вектор целых чисел без знака.
ms.assetid: 8622eca1-fc8f-4129-a375-142b4f4018b0
keywords:
- HLSL структура XMUINT2
topic_type:
- apiref
api_name:
- XMUINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39ec30fd4966e46bd511729671c39653640fe3f8f858d74db96e59fa1f09d242
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067274"
---
# <a name="xmuint2-structure"></a>Структура XMUINT2

Описывает двумерный вектор целых чисел без знака.

## <a name="syntax"></a>Синтаксис


``` syntax
typedef struct _XMUINT2 {
  UINT x;
  UINT y;
} XMUINT2;
```



## <a name="members"></a>Члены

<dl> <dt>

**x**
</dt> <dd>

компонент x вектора.

</dd> <dt>

**y**
</dt> <dd>

y-компонент вектора.

</dd> </dl>



## <a name="remarks"></a>Remarks

Эта структура определена в ``D3DX\_DXGIFormatConvert.inl`` заголовке пакета SDK DirectX (июнь 2010) для использования из C++. последняя версия этого заголовка в пакете [Microsoft. дкссдк. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet больше не определяет его и использует [DirectX:: XMUINT2](/windows/win32/api/directxmath/ns-directxmath-xmuint2) в директксмас.



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3DX \_ дксгиформатконверт. inl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Структуры](format-conversion-structures.md)
</dt> <dt>

[Распаковка и \_ формат упаковки для редактирования образа In-Place](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>