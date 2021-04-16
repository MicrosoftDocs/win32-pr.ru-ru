---
description: Эта структура содержит данные для отчетов о нехватке памяти.
ms.assetid: 42cf0922-53cc-48b9-8359-b88583ef5f1c
title: Структура D3DMEMORYPRESSURE (D3d9types. h) для Microsoft Media Foundation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMEMORYPRESSURE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7400c4822b61a84ab288f0424cfa84e825e69dc9
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2021
ms.locfileid: "106188029"
---
# <a name="d3dmemorypressure-structure-d3d9typesh-for-microsoft-media-foundation"></a>Структура D3DMEMORYPRESSURE (D3d9types. h) для Microsoft Media Foundation

Содержит данные для отчетов о нехватке памяти.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _D3DMEMORYPRESSURE {
  UINT64 BytesEvictedFromProcess;
  UINT64 SizeOfInefficientAllocation;
  DWORD  LevelOfEfficiency;
} D3DMEMORYPRESSURE;
```



## <a name="members"></a>Члены

<dl> <dt>

**битесевиктедфромпроцесс**
</dt> <dd>

Число байтов, которые были исключены процессом во время выполнения запроса.

</dd> <dt>

**сизеофинеффиЦиенталлокатион**
</dt> <dd>

Общее число байтов, помещенных в неоптимальные сегменты памяти из-за недостаточного места в предпочтительных сегментах памяти.

</dd> <dt>

**левелофеффиЦиенци**
</dt> <dd>

Общая эффективность выделения памяти, помещенных в неоптимальную память. Значение выражается в процентах. Например, значение 95 указывает, что выделения, помещаемые в непредпочтительные сегменты памяти, имеют эффективность 95%. Это число не должно считаться точным измерением.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента | \[Только классические приложения Windows 7\]                                                              |
| Минимальная версия сервера | Только классические приложения Windows Server 2008 R2 \[\]                                                 |
| Заголовок                  | D3d9types. h (включение D3d9. h) |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Видеоструктуры Direct3D](direct3d-video-structures.md)
</dt> <dt>

[Отчеты о нехватке памяти](memory-pressure-reporting.md)
</dt> </dl>

 

 




