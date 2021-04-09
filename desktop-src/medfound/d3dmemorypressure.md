---
description: Содержит данные для отчетов о нехватке памяти.
ms.assetid: 42cf0922-53cc-48b9-8359-b88583ef5f1c
title: Структура D3DMEMORYPRESSURE (D3d9types. h)
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
ms.openlocfilehash: 6d92cad29bda795a9589dbe0c94863bd743505bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143150"
---
# <a name="d3dmemorypressure-structure-d3d9typesh"></a>Структура D3DMEMORYPRESSURE (D3d9types. h)

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
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>D3d9types. h (включение D3d9. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Видеоструктуры Direct3D](direct3d-video-structures.md)
</dt> <dt>

[Отчеты о нехватке памяти](memory-pressure-reporting.md)
</dt> </dl>

 

 




