---
description: Создайте маркер номера версии шейдера вершин.
ms.assetid: c3aa6b01-7949-4171-a8b5-2f453fd7a422
title: Макрос D3DVS_VERSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVS_VERSION
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 915d5b843287602c80572d739d8b369d8c301770
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713791"
---
# <a name="d3dvs_version-macro"></a>\_Макрос версии D3DVS

Создайте маркер номера версии шейдера вершин.

## <a name="syntax"></a>Синтаксис


```C++
DWORD D3DVS_VERSION(
   int _Major,
   int _Minor
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*\_Большой* 
</dt> <dd>

Версия основного шейдера вершин. Соответствующие значения см. в разделе Примечания.

</dd> <dt>

*\_Дополнительный номер* 
</dt> <dd>

Младшая версия шейдера вершин. Соответствующие значения см. в разделе Примечания.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение типа DWORD, которое является версией шейдера вершин.

## <a name="remarks"></a>Комментарии

Номера версий

Номер версии — это сочетание основной версии и дополнительных номеров версий шейдера вершин. Допустимые числа показаны в таблице.



| Значительно | Дополнительный номер | Пример             |
|-------|-------|---------------------|
| 1     | 1     | \_Версия D3DVS (1, 1) |
| 2     | 0     | \_Версия D3DVS (2, 0) |
| 3     | 0     | \_Версия D3DVS (3, 0) |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Макросы](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




