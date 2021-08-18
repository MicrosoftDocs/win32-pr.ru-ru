---
description: Удаляет указанный росчерк из Иинканализер.
ms.assetid: e182ae35-854e-401d-8e26-aee645c05430
title: 'Метод Иинканализер:: Ремовестроке (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.RemoveStroke
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: dd0a972ed776c40fc42d695df2058c62f9af84f8fc09155758d197772e9abfc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092014"
---
# <a name="iinkanalyzerremovestroke-method"></a>Метод Иинканализер:: Ремовестроке

Удаляет указанный росчерк из [**иинканализер**](iinkanalyzer.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RemoveStroke(
  [in] LONG *plStrokeId
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*плстрокеид* \[ окне\]
</dt> <dd>

Идентификатор штриха.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

Этот метод удаляет данные пакета для и ссылается на указанный росчерк из [**иинканализер**](iinkanalyzer.md).

Этот метод удаляет штрих из узла конечного контекста, который ссылается на штрих. Если [**иконтекстноде**](icontextnode.md) больше не ссылается на штрихи, этот метод удаляет **иконтекстноде** и все объекты предка **иконтекстноде** , которые больше не имеют дочерних узлов.

После того как этот метод удаляет штрих из [**иконтекстноде**](icontextnode.md), он обновляет "грязную" область объекта [**иинканализер**](iinkanalyzer.md) (см. [**метод иинканализер:: жетдиртирегион**](iinkanalyzer-getdirtyregion.md)) для включения ограничивающего прямоугольника удаленного росчерка.

Если *плстрокеид* не определяет штрих, связанный с [**иинканализер**](iinkanalyzer.md), этот метод возвращает данные без обновления анализатора рукописного ввода.

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

[**Метод Иинканализер:: Ремовестрокес**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[**Метод Иинканализер:: Жетдиртирегион**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




