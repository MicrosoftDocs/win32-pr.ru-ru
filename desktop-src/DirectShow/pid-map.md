---
description: '\_Структура схемы PID содержит определение содержимого идентификатора пакета транспортного потока MPEG-2.'
ms.assetid: c247ec75-483d-4587-a82f-07bbf6d277b4
title: Структура PID_MAP (Бдатипес. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PID_MAP
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 98b238c61ccfcfb93e4ddcc0a051d9084228f604
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689276"
---
# <a name="pid_map-structure"></a>\_Структура схемы PID

`PID_MAP`Структура содержит определение содержимого идентификатора пакета транспортного потока MPEG-2.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  ULONG                ulPID;
  MEDIA_SAMPLE_CONTENT MediaSampleContent;
} PID_MAP;
```



## <a name="members"></a>Члены

<dl> <dt>

**улпид**
</dt> <dd>

Указывает идентификатор пакета (PID)

</dd> <dt>

**медиасамплеконтент**
</dt> <dd>

Задает содержимое полезных данных пакета в виде типа перечисления [**мультимедиа \_ образец \_ содержимого**](media-sample-content.md) .

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Бдатипес. h (включение Бдаифаце. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры DirectShow](directshow-structures.md)
</dt> <dt>

[**Интерфейс Иенумпидмап**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-ienumpidmap)
</dt> </dl>

 

 




