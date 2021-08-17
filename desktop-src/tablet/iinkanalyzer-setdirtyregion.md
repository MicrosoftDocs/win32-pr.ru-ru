---
description: Изменяет область, которая изменилась со времени последнего выполнения операции анализа.
ms.assetid: 1484fd96-2791-4583-b13b-e5a8275ecb0e
title: 'Метод Иинканализер:: Сетдиртирегион (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetDirtyRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a39fc420b368911788efcb9462c9c4be5b4828c82906ef2c94bb5be99ca17568
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091474"
---
# <a name="iinkanalyzersetdirtyregion-method"></a>Метод Иинканализер:: Сетдиртирегион

Изменяет область, которая изменилась со времени последнего выполнения операции анализа.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetDirtyRegion(
  [in] IAnalysisRegion *pDirtyRegion
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдиртирегион* \[ окне\]
</dt> <dd>

Объект [**ианалисисрегион**](ianalysisregion.md) , описывающий область, измененную с момента последнего выполнения операции анализа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

Этот метод определяет области, которые необходимо проанализировать или повторно проанализировать. Все методы [**иинканализер**](iinkanalyzer.md) , которые добавляют, обновляют или удаляют данные обводки, обновляют «грязную» область. Чтобы вручную пометить область для переанализа:

1.  Получите "грязную" область с помощью [**метода иинканализер:: жетдиртирегион**](iinkanalyzer-getdirtyregion.md).
2.  Используйте [**метод ианалисисрегион:: унионрегион**](ianalysisregion-unionregion.md) или [**метод Ианалисисрегион:: унионректангле**](ianalysisregion-unionrectangle.md) для добавления области в регион из шага 1.
3.  Чтобы обновить "грязную" область, используйте **метод иинканализер:: сетдиртирегион** .

[**Иинканализер**](iinkanalyzer.md) анализирует рукописный ввод в своей «грязной» области во время вызова метода [**Иинканализер:: Analyze**](iinkanalyzer-analyze.md) или [**иинканализер:: баккграунданализе**](iinkanalyzer-backgroundanalyze.md). Однако **иинканализер** может расширить операцию анализа, включив в нее соседние регионы.

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

[**Метод Иинканализер:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Метод Иинканализер:: Баккграунданализе**](iinkanalyzer-backgroundanalyze.md)
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

[**Метод Иинканализер:: Ремовестрокес**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[**Метод Иинканализер:: Упдатестрокесдата**](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




