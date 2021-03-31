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
ms.openlocfilehash: a231dde453467ad2973d729fa068cedcc35151c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810001"
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

## <a name="remarks"></a>Комментарии

Язык штриха задается при добавлении штриха путем вызова метода [**иинканализер:: аддстроке**](iinkanalyzer-addstroke.md), метода [**Иинканализер:: аддстрокефорлангуаже**](iinkanalyzer-addstrokeforlanguage.md), [**Иинканализер:: аддстрокес**](iinkanalyzer-addstrokes.md)или [**метода IInkAnalyzer:: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md). Чтобы изменить языковой стандарт обводки, используйте [**метод иинканализер:: сетстрокелангуажеид**](iinkanalyzer-setstrokelanguageid.md) или [**метод Иинканализер:: сетстрокеслангуажеид**](iinkanalyzer-setstrokeslanguageid.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
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

 

 




