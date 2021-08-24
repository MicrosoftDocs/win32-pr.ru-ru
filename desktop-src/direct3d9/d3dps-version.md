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
ms.openlocfilehash: a3958cfaa3afe06e22015a28e8e1ebfd8799c01e89772eb9794dd1249cc0df9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750904"
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

*\_Значительно* 
</dt> <dd>

Версия основного шейдера пикселей.

</dd> <dt>

*\_Дополнительный номер* 
</dt> <dd>

Версия незначительного шейдера пикселей.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение типа DWORD, которое является версией шейдера пикселей.

## <a name="remarks"></a>Remarks

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
| Заголовок<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Макросы](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[D3DCAPS9](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> </dl>

 

 




