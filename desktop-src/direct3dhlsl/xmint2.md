---
title: Структура XMINT2
description: Описывает двухмерный целочисленный вектор.
ms.assetid: 651f62f8-577d-4356-9bbc-0d4a9ca8fb01
keywords:
- HLSL структура XMINT2
topic_type:
- apiref
api_name:
- XMINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e93e26933ad6b3829848e7e826d8d9685e9f141
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222862"
---
# <a name="xmint2-structure"></a>Структура XMINT2

Описывает двухмерный целочисленный вектор.

## <a name="syntax"></a>Синтаксис


``` syntax
typedef struct _XMINT2 {
  INT x;
  INT y;
} XMINT2;
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

Эта структура определена в ``D3DX\_DXGIFormatConvert.inl`` заголовке пакета SDK DirectX (июнь 2010) для использования из C++. Последняя версия этого заголовка в пакете NuGet [Microsoft. дкссдк. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) больше не определяет его и использует [DirectX:: XMINT2](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmint2) в директксмас.



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
