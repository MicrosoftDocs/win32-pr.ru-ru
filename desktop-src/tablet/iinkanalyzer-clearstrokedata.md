---
description: Очищает данные пакета обводки от Иинканализер.
ms.assetid: c87a1e73-5e3f-4d27-93e9-e30d9ec5d9e3
title: 'Метод Иинканализер:: Клеарстрокедата (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ClearStrokeData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3413d8d6fb322030afdcffb97e8739ae4ca5e2314fe968f366ce25e58d90351e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057874"
---
# <a name="iinkanalyzerclearstrokedata-method"></a>Метод Иинканализер:: Клеарстрокедата

Очищает данные пакета обводки от [**иинканализер**](iinkanalyzer.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ClearStrokeData(
  [in] LONG lStrokeId
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лстрокеид* \[ окне\]
</dt> <dd>

Идентификатор штриха, для которого очищаются данные пакета.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

Используйте этот метод при изменении данных пакета для штриха, например при перемещении или преобразовании штриха. [**Иинканализер**](iinkanalyzer.md) вызывает событие [**\_ ианалисисевентс:: упдатестрокескаче**](-ianalysisevents-updatestrokescache.md) , когда ему требуются данные пакета Stroke из штриха, для которого были удалены данные пакета.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также

<dl> <dt>

[**иинканализер**](iinkanalyzer.md)
</dt> <dt>

[**Метод Иинканализер:: Упдатестрокесдата**](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




