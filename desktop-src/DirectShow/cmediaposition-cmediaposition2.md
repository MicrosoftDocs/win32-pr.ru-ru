---
description: Сведения о методе конструктора Кмедиапоситион. Кмедиапоситион (Ктлутил. h). В этом методе используются параметры "pName", "pUnk" и "фр".
ms.assetid: 4074f513-d1e7-4311-8732-4d755e621e55
title: Конструктор Кмедиапоситион. Кмедиапоситион (Ктлутил. h)
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
ms.openlocfilehash: 101678ebcb851ef0fcdc8eeaa202435ca80eb796555c81e5e5d95eb4998131c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655265"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-phr-parameters"></a>Кмедиапоситион. Кмедиапоситион-конструктор (Ктлутил. h) — pName, pUnk, параметры фр

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CMediaPosition(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr
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

</dd> <dt>

*фр* 
</dt> <dd>

Указатель на значение **HRESULT** .

</dd> </dl>

## <a name="requirements"></a>Требования

| Требование | Значение |
|-|-|
| Заголовок | ктлутил. h (включает Потоки. h) |
| Библиотека| Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки) |

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиапоситион**](cmediaposition.md)
</dt> </dl>

 

 




