---
description: Удаляет указанные штрихи из Иинканализер.
ms.assetid: ea7c8a9f-a427-4781-b5ba-97ffd983dbe5
title: 'Метод Иинканализер:: Ремовестрокес (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.RemoveStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e6d53d21df9734ee43cdda618c5221fd83300598d46b51bd366c50fedf5cec45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092024"
---
# <a name="iinkanalyzerremovestrokes-method"></a>Метод Иинканализер:: Ремовестрокес

Удаляет указанные штрихи из [**иинканализер**](iinkanalyzer.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RemoveStrokes(
  [in] ULONG ulStrokeIdCount,
  [in] LONG  *plStrokes
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*улстрокеидкаунт* \[ окне\]
</dt> <dd>

Число идентификаторов Stroke в *плстрокес*.

</dd> <dt>

*плстрокес* \[ окне\]
</dt> <dd>

Идентификаторы для удаляемых штрихов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

Этот метод удаляет данные пакета для и ссылается на указанные штрихи из [**иинканализер**](iinkanalyzer.md).

Этот метод удаляет штрихи из конечного узла контекста, который ссылается на штрихи. Если любые [**иконтекстноде**](icontextnode.md) больше не ссылаются на штрихи, этот метод удаляет **иконтекстноде** и все объекты предка **иконтекстноде** , которые больше не имеют дочерних узлов.

После того как этот метод удаляет штрихи из [**иконтекстноде**](icontextnode.md), он обновляет "грязную" область объекта [**иинканализер**](iinkanalyzer.md) (см. [**метод иинканализер:: жетдиртирегион**](iinkanalyzer-getdirtyregion.md)) для включения ограничивающего прямоугольника удаленных штрихов.

Если штрих, определенный в *плстрокес* , не связан с [**иинканализер**](iinkanalyzer.md), этот метод игнорирует идентификатор.

Если ни один из штрихов, указанных в *плстрокес* , не связан с анализатором рукописного ввода, этот метод возвращает значение без обновления [**иинканализер**](iinkanalyzer.md).

Этот метод возвращает код ошибки, если *плстрокес* имеет значение null.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иинканализер**](iinkanalyzer.md)
</dt> <dt>

[**Метод Иинканализер:: Аддстроке**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**Метод Иинканализер:: Аддстрокефорлангуаже**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**Метод Иинканализер:: Аддстрокес**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**Метод Иинканализер:: Аддстрокесфорлангуаже**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**Метод Иинканализер:: Ремовестроке**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**Метод Иинканализер:: Жетдиртирегион**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




