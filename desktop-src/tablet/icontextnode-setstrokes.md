---
description: Связывает указанные штрихи с этим Иконтекстноде.
ms.assetid: 5ce8893a-da59-4cec-a349-d5ffc4f43905
title: 'Метод Иконтекстноде:: Сетстрокес (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 67834a10e5e08070c991af76fe19b720853789a9f5e2c771f5c1ed0dc4fc9754
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119552604"
---
# <a name="icontextnodesetstrokes-method"></a>Метод Иконтекстноде:: Сетстрокес

Связывает указанные штрихи с этим [**иконтекстноде**](icontextnode.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetStrokes(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*улстрокеидскаунт* \[ окне\]
</dt> <dd>

Число идентификаторов Stroke в *плстрокеидс*.

</dd> <dt>

*плстрокеидс* \[ окне\]
</dt> <dd>

Идентификаторы штрихов, связываемых с этим [**иконтекстноде**](icontextnode.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

Этот метод не обновляет «грязную» область анализатора рукописного ввода (см. раздел [**метод иинканализер:: жетдиртирегион**](iinkanalyzer-getdirtyregion.md)).

Используйте этот метод, если приложение поддерживает собственную структуру данных, которая синхронизируется с [**иинканализер**](iinkanalyzer.md). Используйте этот метод для назначения данных Stroke определенному контекстному узлу. Дополнительные сведения о синхронизации данных приложения с помощью **иинканализер** см. в разделе [учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).

Если любой из указанных штрихов уже связан с [**иинканализер**](iinkanalyzer.md), этот метод возвращает **E \_ INVALIDARG**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также

<dl> <dt>

[**иконтекстноде**](icontextnode.md)
</dt> <dt>

[**Метод Иинканализер:: Аддстроке**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**Метод Иинканализер:: Аддстрокефорлангуаже**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**Метод Иинканализер:: Аддстрокес**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**Метод Иинканализер:: Аддстрокесфорлангуаже**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**Метод Иинканализер:: Аддстрокестокустомрекогнизер**](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[**Метод Иинканализер:: Аддстрокетокустомрекогнизер**](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[**Метод Иинканализер:: Ремовестроке**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**Метод Иинканализер:: Ремовестрокес**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[**Иконтекстноде:: Жетстрокеид**](icontextnode-getstrokeid.md)
</dt> <dt>

[**Иконтекстноде:: Жетстрокеидс**](icontextnode-getstrokeids.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




