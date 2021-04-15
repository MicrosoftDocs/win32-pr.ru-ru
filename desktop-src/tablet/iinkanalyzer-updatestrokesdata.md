---
description: Обновляет данные пакета для указанных штрихов.
ms.assetid: 7fca4c39-eef2-4019-86a0-27cd0e4e7510
title: 'Метод Иинканализер:: Упдатестрокесдата (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.UpdateStrokesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 151403a7114bca2644d0425fdba0155135ac9ed8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701599"
---
# <a name="iinkanalyzerupdatestrokesdata-method"></a>Метод Иинканализер:: Упдатестрокесдата

Обновляет данные пакета для указанных штрихов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT UpdateStrokesData(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds,
  [in] ULONG ulStrokePacketDescriptionCount,
  [in] GUID  *pStrokePacketDescriptionGuids,
  [in] ULONG *pulPacketDataCountPerStroke,
  [in] LONG  *plStrokePacketData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*улстрокеидскаунт* \[ окне\]
</dt> <dd>

Число штрихов для обновления.

</dd> <dt>

*плстрокеидс* \[ окне\]
</dt> <dd>

Массив, содержащий идентификаторы штрихов.

</dd> <dt>

*улстрокепаккетдескриптионкаунт* \[ окне\]
</dt> <dd>

Число свойств в каждом пакете.

</dd> <dt>

*пстрокепаккетдескриптионгуидс* \[ окне\]
</dt> <dd>

Массив, содержащий идентификаторы свойств пакета.

</dd> <dt>

*пулпаккетдатакаунтперстроке* \[ окне\]
</dt> <dd>

Массив, содержащий количество пакетов в каждом штрихе.

</dd> <dt>

*плстрокепаккетдата* \[ окне\]
</dt> <dd>

Массив, содержащий данные пакета для штрихов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

параметр *плстрокепаккетдата* содержит данные пакетов для всех штрихов. Параметр *пстрокепаккетдескриптионгуидс* содержит глобальные уникальные идентификаторы (GUID), которые описывают типы данных пакетов, включаемые для каждой точки в каждом штрихе. Полный список доступных свойств пакетов см. в разделе [константы паккетпропертигуидс](packetpropertyguids-constants.md).

Только штрихи с одинаковыми описаниями пакетов могут быть обновлены в одном вызове **метода иинканализер:: упдатестрокесдата**.

Этот метод не обновляет «грязную» область анализатора рукописного ввода (см. раздел [**метод иинканализер:: жетдиртирегион**](iinkanalyzer-getdirtyregion.md)).

Если указанный штрих не связан с [**иинканализер**](iinkanalyzer.md), этот метод игнорирует идентификатор.

Если ни один из указанных штрихов не определяет штрих, связанный с [**иинканализер**](iinkanalyzer.md), этот метод возвращает значение без обновления **иинканализер**.

Этот метод возвращает код ошибки, если *плстрокеидс* имеет **значение NULL**.

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

[**Метод Иинканализер:: Аддстроке**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**Метод Иинканализер:: Аддстрокефорлангуаже**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**Метод Иинканализер:: Аддстрокетокустомрекогнизер**](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[**Метод Иинканализер:: Аддстрокес**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**Метод Иинканализер:: Аддстрокесфорлангуаже**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**Метод Иинканализер:: Аддстрокестокустомрекогнизер**](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[**Метод Иинканализер:: Клеарстрокедата**](iinkanalyzer-clearstrokedata.md)
</dt> <dt>

[**\_Ианалисисевентс:: Упдатестрокескаче**](-ianalysisevents-updatestrokescache.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




