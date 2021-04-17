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
ms.openlocfilehash: cb9d86a2403cd0e2e71130b51cdb87bad15c4e95
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "105665009"
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
| Header | Ктлутил. h (включение Streams. h) |
| Библиотека| Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки) |

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиапоситион**](cmediaposition.md)
</dt> </dl>

 

 




