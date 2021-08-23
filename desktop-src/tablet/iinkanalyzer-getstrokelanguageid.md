---
description: Возвращает идентификатор локали указанного штриха.
ms.assetid: a5fb9b7a-ed3e-4552-9412-39529203bd81
title: 'Метод Иинканализер:: Жетстрокелангуажеид (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetStrokeLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8b61bfa61b4e4aa2c8415c9596cb97a3b0c1313cf3a080d065a7c82e4d69b84d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713394"
---
# <a name="iinkanalyzergetstrokelanguageid-method"></a>Метод Иинканализер:: Жетстрокелангуажеид

Возвращает идентификатор локали указанного штриха.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetStrokeLanguageId(
  [in]  LONG lStrokeId,
  [out] LONG *lStrokeLCID
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лстрокеид* \[ окне\]
</dt> <dd>

Идентификатор штриха.

</dd> <dt>

*лстрокелЦид* \[ заполняет\]
</dt> <dd>

Идентификатор локали для указанного штриха.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

Язык штриха задается при добавлении штриха путем вызова метода [**иинканализер:: аддстроке**](iinkanalyzer-addstroke.md), метода [**Иинканализер:: аддстрокефорлангуаже**](iinkanalyzer-addstrokeforlanguage.md), [**Иинканализер:: аддстрокес**](iinkanalyzer-addstrokes.md)или [**метода IInkAnalyzer:: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md). Чтобы изменить языковой стандарт обводки, используйте [**метод иинканализер:: сетстрокелангуажеид**](iinkanalyzer-setstrokelanguageid.md) или [**метод Иинканализер:: сетстрокеслангуажеид**](iinkanalyzer-setstrokeslanguageid.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иинканализер**](iinkanalyzer.md)
</dt> <dt>

[**Метод Иинканализер:: Сетстрокелангуажеид**](iinkanalyzer-setstrokelanguageid.md)
</dt> <dt>

[**Метод Иинканализер:: Сетстрокеслангуажеид**](iinkanalyzer-setstrokeslanguageid.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




