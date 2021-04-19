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
ms.openlocfilehash: 00ec040a848b3103b4d5070541f025ab9cfb0cfa
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222832"
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



## <a name="remarks"></a>Примечания

Эта структура определена в ``D3DX\_DXGIFormatConvert.inl`` заголовке пакета SDK DirectX (июнь 2010) для использования из C++. Последняя версия этого заголовка в пакете NuGet [Microsoft. дкссдк. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) больше не определяет его и использует [DirectX:: XMUINT2](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmuint2) в директксмас.



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3DX \_ дксгиформатконверт. inl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры](format-conversion-structures.md)
</dt> <dt>

[Распаковка и \_ формат упаковки для редактирования образа In-Place](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>
