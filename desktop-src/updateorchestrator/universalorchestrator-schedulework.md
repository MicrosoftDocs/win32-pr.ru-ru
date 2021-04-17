---
title: IUniversalOrchestrator::ScheduleWork
description: Вызывает универсальную Orchestrator для планирования работы
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 456df8f975114f7bdf750a0449f3bd98efcc3b2e
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "105719756"
---
# <a name="iuniversalorchestratorschedulework-method"></a>Метод Иуниверсалорчестратор:: Счедулеворк

> [!NOTE] 
> Этот API принадлежит к универсальному API Orchestrator.

Позволяет клиентам сообщать о неработающем универсальном Orchestrator Management и предоставить двоичный файл, который будет вызываться универсальной Orchestrator для выполнения обновления позже.

Двоичный ответ обратного вызова должен быть подписан действительным сертификатом Майкрософт, а вызывающий должен вызывать вызов Счедулеворк из контекста системы.

## <a name="syntax"></a>Синтаксис

```C++
HRESULT ScheduleWork(
  LPCWSTR callerIdentifier,
  LPCWSTR cmdLine
  LPCWSTR startArg,
  LPCWSTR pauseArg);
```

## <a name="parameters"></a>Параметры

`callerIdentifier`

Уникальная строка, идентифицирующая все вызовы от этого конкретного клиента.

`cmdLine`

Полный путь к двоичному файлу обратного вызова, который будет вызываться универсальной Orchestrator для выполнения работы.

`startArg`

Параметры для передачи в двоичный файл обратного вызова, указывающие на запрос Start.

`pauseArg`

*(необязательно)* Параметры для передачи в двоичный файл обратного вызова для указания запрошения приостановки.

## <a name="return-value"></a>Возвращаемое значение
Если этот метод завершается с ошибкой, возвращается **S_OK**.  В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

| Требование | Версия |
|---|---|
| Минимальная версия клиента | Windows 10 1903 |
|   |   |



 

 



