---
description: Возвращает идентификаторы Stroke, связанные с этим Ианалисисалтернате.
ms.assetid: 495d485f-0d16-4085-9213-cc55f3f259f0
title: 'Метод Ианалисисалтернате:: Жетстрокеидс (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetStrokeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2682107a58f126011c4d80a02a119219ccea0976408937e19eb7b511eb82cff9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967503"
---
# <a name="ianalysisalternategetstrokeids-method"></a>Метод Ианалисисалтернате:: Жетстрокеидс

Возвращает идентификаторы Stroke, связанные с этим [**ианалисисалтернате**](ianalysisalternate.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetStrokeIds(
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     LONG  **pplStrokeIds
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пулстрокеидскаунт* \[ в, out\]
</dt> <dd>

Указатель на **ulong** , для которой задано число идентификаторов Stroke, связанных с этим [**ианалисисалтернате**](ianalysisalternate.md).

</dd> <dt>

*пплстрокеидс* \[ заполняет\]
</dt> <dd>

\[out, размер \_ ( \* *ПУЛСТРОКЕИДСКАУНТ* \* sizeof (Long))\]

Массив **длинной** длины *пулстрокеидскаунт* , для которой заданы идентификаторы штриха, связанные с этим [**ианалисисалтернате**](ianalysisalternate.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

> [!Caution]  
> Чтобы избежать утечки памяти, используйте [CoTaskMemFree](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить память от \* *пплстрокеидс* , если эта информация больше не нужна.

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ианалисисалтернате**](ianalysisalternate.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

