---
title: IUniversalOrchestrator::ScheduleWork
description: Вызывает универсальную Orchestrator для планирования работы
ms.topic: reference
ms.date: 01/14/2021
ms.openlocfilehash: bb2ecc67167e0651663856354a07ec86f985c664f1d2bccff98917adf72f054d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966094"
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



 

 



