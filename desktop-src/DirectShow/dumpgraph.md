---
description: Функция Думпграф отправляет сведения о графе фильтра в расположение выходных данных отладки. Игнорируется в розничных сборках.
ms.assetid: c78f86bb-44d0-4904-b7f8-e756bda0151d
title: Функция Думпграф (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DumpGraph
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55c3adf793982b7b00ab44e26e7c34e08a1ac42b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652018"
---
# <a name="dumpgraph-function"></a>Функция Думпграф

`DumpGraph`Функция отправляет сведения о графе фильтра в расположение выходных данных отладки. Игнорируется в розничных сборках.

## <a name="syntax"></a>Синтаксис


```C++
void DumpGraph(
   IFilterGraph *pGraph,
   DWORD        dwLevel
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пграф* 
</dt> <dd>

Указатель на интерфейс [**ифилтерграф**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) в диспетчере графов фильтров.

</dd> <dt>

*двлевел* 
</dt> <dd>

Уровень ведения журнала. Функция создает \_ сообщение трассировки журнала с указанным уровнем ведения журнала.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксдебуг. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Выходные функции отладки](debug-output-functions.md)
</dt> </dl>

 

 




