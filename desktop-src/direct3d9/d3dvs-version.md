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
ms.openlocfilehash: 861295c9068bee9e40174d877a78628aa405b9cfa5d46414190fbb7b37904e89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527260"
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

*\_Значительно* 
</dt> <dd>

Версия основного шейдера вершин. Соответствующие значения см. в разделе Примечания.

</dd> <dt>

*\_Дополнительный номер* 
</dt> <dd>

Младшая версия шейдера вершин. Соответствующие значения см. в разделе Примечания.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение типа DWORD, которое является версией шейдера вершин.

## <a name="remarks"></a>Remarks

Номера версий

Номер версии — это сочетание основной версии и дополнительных номеров версий шейдера вершин. Допустимые числа показаны в таблице.



| Значительно | Дополнительный номер | Пример             |
|-------|-------|---------------------|
| 1     | 1     | \_Версия D3DVS (1, 1) |
| 2     | 0     | \_Версия D3DVS (2, 0) |
| 3     | 0     | \_Версия D3DVS (3, 0) |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Макросы](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




