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
ms.openlocfilehash: e932d2f2b60a72ca167f3f6edd7f4ddae9b68710
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805981"
---
# <a name="span-idvspixengineexperimentspanexperiment-structure"></a><span id="vspixengine.experiment"></span>Структура эксперимента

Представляет сведения о эксперименте (захвате).

## <a name="syntax"></a>Синтаксис


```C++
} Experiment;
```

## <a name="members"></a>Члены

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
Идентификатор локали, используемый для элементов наложения пользовательского интерфейса во время експериемент (записи). Это передается из узла (например, Visual Studio диагностика графики) в подсистему записи.

**регистрирут**  
Строка COM, содержащая корень реестра. Это передается из узла (например, Visual Studio диагностика графики) в подсистему записи.

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

 

 



