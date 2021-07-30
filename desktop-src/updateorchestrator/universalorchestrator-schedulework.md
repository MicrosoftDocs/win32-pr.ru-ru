---
title: IUniversalOrchestrator::ScheduleWork
description: Вызывает универсальную Orchestrator для планирования работы
ms.topic: reference
ms.date: 01/14/2021
ms.openlocfilehash: 4c49d06a28497c33e86cc1e919fdb59f2363d1f5
ms.sourcegitcommit: 3cea99a2ed9579a94236fa7924abd6149db51a58
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/30/2021
ms.locfileid: "114991821"
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



 

 



