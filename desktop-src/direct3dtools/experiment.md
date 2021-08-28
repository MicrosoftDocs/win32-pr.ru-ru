---
description: Представляет сведения о эксперименте (захвате).
MS-HAID: vspixengine.Experiment
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Структура эксперимента
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 632F1F92-3E32-4B0A-8E38-2613694C267F
api_name:
- Experiment
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 90e60f3f197db78a3ec399c2f8ffe7144901b097
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625370"
---
# <a name="span-idvspixengineexperimentspanexperiment-structure"></a><span id="vspixengine.experiment"></span>Структура эксперимента

Представляет сведения о эксперименте (захвате).

## <a name="syntax"></a>Синтаксис


```C++
} Experiment;
```

## <a name="members"></a>Участники

**Идентификатор**  
Идентификатор связанного процесса.

**applicationName**  
Строка COM, содержащая имя приложения для запуска эксперимента.

**коммандлинеаргументс**  
Строка COM, содержащая аргументы командной строки.

**workingDirectory**  
Строка COM, содержащая путь к рабочему каталогу.

**темппиксрунфиле**  
Строка COM, содержащая путь к временному файлу, используемому для выполнения эксперимента.

**стартоптион**  
Параметр запуска, связанный с экспериментом.

**експерименттипе**  
Тип эксперимента (захват).

**уилокале**  
Идентификатор локали, используемый для элементов наложения пользовательского интерфейса во время експериемент (записи). он передается из узла (например, Visual Studio диагностика графики) в подсистему записи.

**регистрирут**  
Строка COM, содержащая корень реестра. он передается из узла (например, Visual Studio диагностика графики) в подсистему записи.

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

 

 



