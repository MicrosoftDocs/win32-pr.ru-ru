---
description: Указывает, как Иинканализер выполняет анализ рукописного ввода.
ms.assetid: bc526445-0c9c-4c53-8b02-32cf758266e6
title: Перечисление Аналисисмодес (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AnalysisModes
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: b9fdebd3ef3cd505b49ff6c82f7609bc339af0a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423506"
---
# <a name="analysismodes-enumeration"></a>Перечисление Аналисисмодес

Указывает, как [**иинканализер**](iinkanalyzer.md) выполняет анализ рукописного ввода.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum AnalysisModes { 
  AnalysisModes_None                     = 0x0000,
  AnalysisModes_AutomaticReconciliation  = 0x0002,
  AnalysisModes_StrokeCacheAutoCleanup   = 0x0004,
  AnalysisModes_PersonalizationEnabled   = 0x0008,
  AnalysisModes_Default                  = 0x000d
} AnalysisModes;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="AnalysisModes_None"></span><span id="analysismodes_none"></span><span id="ANALYSISMODES_NONE"></span>**Аналисисмодес \_ None**
</dt> <dd>

Не указаны режимы.

</dd> <dt>

<span id="AnalysisModes_AutomaticReconciliation"></span><span id="analysismodes_automaticreconciliation"></span><span id="ANALYSISMODES_AUTOMATICRECONCILIATION"></span>**Аналисисмодес \_ аутоматикреконЦилиатион**
</dt> <dd>

Будет ли [**иинканализер**](iinkanalyzer.md) автоматически запускать операцию сверки, как только промежуточные или окончательные результаты будут готовы.

Если этот режим включен, событие [**\_ ианалисисевентс:: реадитореконЦиле**](-ianalysisevents-readytoreconcile.md) не возникает. Если этот режим отключен, возникает событие **\_ ианалисисевентс:: реадитореконЦиле** .

</dd> <dt>

<span id="AnalysisModes_StrokeCacheAutoCleanup"></span><span id="analysismodes_strokecacheautocleanup"></span><span id="ANALYSISMODES_STROKECACHEAUTOCLEANUP"></span>**Аналисисмодес \_ строкекачеаутоклеануп**
</dt> <dd>

Будет ли [**иинканализер**](iinkanalyzer.md) автоматически очищать ненужные росчерки из кэша штрихов перед выполнением анализа.

Если этот режим включен, [**иинканализер**](iinkanalyzer.md) очищает данные о штрихах перед выполнением анализа. Код также должен обработано событие [**\_ ианалисисевентс:: упдатестрокескаче**](-ianalysisevents-updatestrokescache.md) . Если событие **\_ ианалисисевентс:: упдатестрокескаче** не обрабатывается, возникает исключение. Эта проверка выполняется на стадиях анализа (или Баккграунданализе) и выверки.

Если этот режим отключен, [**иинканализер**](iinkanalyzer.md) не очищает данные росчерка. Чтобы очистить данные штриха, вызовите [**метод иинканализер:: клеарстрокедата**](iinkanalyzer-clearstrokedata.md). Если этот режим отключен, вызывается событие [**\_ ианалисисевентс:: упдатестрокескаче**](-ianalysisevents-updatestrokescache.md) , поэтому **иинканализер** может получить последние данные о штрихах для всех штрихов, для которых был снят свой кэш. Если кэш штрихов сброшен, но событие **\_ ианалисисевентс:: упдатестрокескаче** не обрабатывается, возникает исключение.

</dd> <dt>

<span id="AnalysisModes_PersonalizationEnabled"></span><span id="analysismodes_personalizationenabled"></span><span id="ANALYSISMODES_PERSONALIZATIONENABLED"></span>**Аналисисмодес \_ персонализатионенаблед**
</dt> <dd>

Персонализация распознавания рукописного текста включена.

</dd> <dt>

<span id="AnalysisModes_Default"></span><span id="analysismodes_default"></span><span id="ANALYSISMODES_DEFAULT"></span>**Аналисисмодес \_ по умолчанию**
</dt> <dd>

Все режимы включены.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Это перечисление позволяет побитовое сочетание значений его членов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Метод Иинканализер:: Жетаналисисмодес**](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[**Метод Иинканализер:: Сетаналисисмодес**](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[**\_Ианалисисевентс:: Интермедиатересултс**](-ianalysisevents-intermediateresults.md)
</dt> <dt>

[**\_Ианалисисевентс:: РеадитореконЦиле**](-ianalysisevents-readytoreconcile.md)
</dt> <dt>

[**\_Ианалисисевентс:: Упдатестрокескаче**](-ianalysisevents-updatestrokescache.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




