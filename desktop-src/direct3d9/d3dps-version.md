---
description: Создайте маркер версии построителя текстуры.
ms.assetid: 70089a93-83df-4ac4-8d98-4e1bb6ad2581
title: Макрос D3DPS_VERSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPS_VERSION
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: c3f30d673145ec9dfe38bd8e2a636ac04c9a195a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355050"
---
# <a name="d3dps_version-macro"></a>\_Макрос версии D3DPS

Создайте маркер версии построителя текстуры.

## <a name="syntax"></a>Синтаксис


```C++
DWORD D3DPS_VERSION(
   int _Major,
   int _Minor
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*\_Большой* 
</dt> <dd>

Версия основного шейдера пикселей.

</dd> <dt>

*\_Дополнительный номер* 
</dt> <dd>

Версия незначительного шейдера пикселей.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение типа DWORD, которое является версией шейдера пикселей.

## <a name="remarks"></a>Комментарии

Номера версий

Номер версии — это сочетание основной версии и дополнительных номеров версий шейдера вершин. Допустимые числа показаны в таблице.



| Значительно | Дополнительный номер | Пример             |
|-------|-------|---------------------|
| 1     | 1     | \_Версия D3DPS (1, 1) |
| 1     | 2     | \_Версия D3DPS (1, 2) |
| 1     | 3     | \_Версия D3DPS (1, 3) |
| 1     | 4     | \_Версия D3DPS (1, 4) |
| 2     | 0     | \_Версия D3DPS (2, 0) |
| 3     | 0     | \_Версия D3DPS (3, 0) |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Макросы](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[D3DCAPS9](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> </dl>

 

 




