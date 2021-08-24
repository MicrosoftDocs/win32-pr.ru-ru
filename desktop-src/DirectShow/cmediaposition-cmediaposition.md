---
description: Сведения о методе конструктора Кмедиапоситион. Кмедиапоситион (Ктлутил. h). Этот метод использует параметры "pName" и "pUnk".
ms.assetid: 18a7785c-30c6-43b8-9a41-542a8424522c
title: Конструктор Кмедиапоситион. Кмедиапоситион (Ктлутил. h) — pName, параметры pUnk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.CMediaPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0df3337c07ed678354515bdf0c665a5d6157f158ac6c2370a8981d8e5028b27e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634803"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-parameters"></a>Конструктор Кмедиапоситион. Кмедиапоситион (Ктлутил. h) — pName, параметры pUnk

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CMediaPosition(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pName* 
</dt> <dd>

Указатель на имя объекта для целей отладки. Выделите этот параметр в статической памяти.

</dd> <dt>

*pUnk* 
</dt> <dd>

Указатель на владельца этого объекта или **значение NULL** , если объект не является агрегированным.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|-|-|
| Заголовок | ктлутил. h (включает Потоки. h) |
| Библиотека| Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки) |

## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кмедиапоситион**](cmediaposition.md)
</dt> </dl>

 

 




