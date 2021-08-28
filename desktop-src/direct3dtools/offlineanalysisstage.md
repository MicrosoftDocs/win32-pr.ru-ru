---
description: Перечисление, используемое для обозначения этапов хода выполнения анализа кадров.
MS-HAID: vspixengine.OFFLINEANALYSISSTAGE
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Перечисление ОФФЛИНЕАНАЛИСИССТАЖЕ
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 85D0288C-113A-4ABE-8EDB-ABB8F009956A
api_name:
- OFFLINEANALYSISSTAGE
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: da78be36b9999d6c082b3c683dfd7e0e5ae18ef5
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627990"
---
# <a name="span-idvspixengineofflineanalysisstagespanofflineanalysisstage-enumeration"></a><span id="vspixengine.offlineanalysisstage"></span>Перечисление ОФФЛИНЕАНАЛИСИССТАЖЕ

Перечисление, используемое для обозначения этапов хода выполнения анализа кадров.

## <a name="syntax"></a>Синтаксис


```C++
};
```

## <a name="constants"></a>Константы

<span id="OfflineAnalysisStage_NotStarted"></span><span id="offlineanalysisstage_notstarted"></span><span id="OFFLINEANALYSISSTAGE_NOTSTARTED"></span>**Оффлинеаналисисстаже \_ NotStarted**  
Анализ кадров еще не запущен.

<span id="OfflineAnalysisStage_Initializing"></span><span id="offlineanalysisstage_initializing"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING"></span>**\_Инициализация оффлинеаналисисстаже**  
Инициализация анализа кадров (запрос выдан).

<span id="OfflineAnalysisStage_Initializing_LinkOk"></span><span id="offlineanalysisstage_initializing_linkok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_LINKOK"></span>**Оффлинеаналисисстаже \_ инициализация \_ линкок**  
Инициализация анализа кадров (связь установлена).

<span id="OfflineAnalysisStage_Initializing_ManifestOk"></span><span id="offlineanalysisstage_initializing_manifestok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_MANIFESTOK"></span>**Оффлинеаналисисстаже \_ инициализация \_ манифесток**  
Инициализация анализа кадров (манифест успешно проанализирован).

<span id="OfflineAnalysisStage_Initializing_ToolOk"></span><span id="offlineanalysisstage_initializing_toolok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_TOOLOK"></span>**Оффлинеаналисисстаже \_ инициализация \_ тулок**  
Инициализация анализа кадров (Загрузка анализатора).

<span id="OfflineAnalysisStage_Analyzing"></span><span id="offlineanalysisstage_analyzing"></span><span id="OFFLINEANALYSISSTAGE_ANALYZING"></span>**\_Анализ оффлинеаналисисстаже**  
Анализ кадров работает.

<span id="OfflineAnalysisStage_AnalysisCompleted"></span><span id="offlineanalysisstage_analysiscompleted"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED"></span>**Оффлинеаналисисстаже \_ аналисискомплетед**  
Анализ кадров завершен (отправлено событие "завершено").

<span id="OfflineAnalysisStage_AnalysisCompleted_Successful"></span><span id="offlineanalysisstage_analysiscompleted_successful"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_SUCCESSFUL"></span>**Оффлинеаналисисстаже \_ аналисискомплетед \_ успешно**  
Анализ кадров успешно выполнен.

<span id="OfflineAnalysisStage_AnalysisCompleted_OutputFileExists"></span><span id="offlineanalysisstage_analysiscompleted_outputfileexists"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_OUTPUTFILEEXISTS"></span>**Оффлинеаналисисстаже \_ аналисискомплетед \_ аутпутфиликсистс**  
Анализ кадра завершен, и выходной файл существует.

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

 

 



