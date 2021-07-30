---
title: IUniversalOrchestrator::HasMoratoriumPassed
description: Запрашивает универсальную Orchestrator, чтобы определить, был ли превышен период после OOBE.
ms.topic: reference
ms.date: 01/14/2021
ms.openlocfilehash: 3ccbf673b8fe22fabe7001112e04e87bd45eeaa4
ms.sourcegitcommit: 3cea99a2ed9579a94236fa7924abd6149db51a58
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/30/2021
ms.locfileid: "114991801"
---
# <a name="iuniversalorchestratorhasmoratoriumpassed-method"></a>Метод Иуниверсалорчестратор:: Хасмораториумпассед

> [!NOTE] 
> Этот API принадлежит к универсальному API Orchestrator.

Позволяет клиентам определить, работает ли Универсальная схема Orchestrator сразу же после завершения работы нового устройства, что ограничивает количество попыток, позволяющих уменьшить число прерываний работы пользователей. 

## <a name="syntax"></a>Синтаксис

```C++
HRESULT HasMoratoriumPassed(
  LPCWSTR callerIdentifier,
  BOOL*   moratoriumPassed);
```

## <a name="parameters"></a>Параметры

`callerIdentifier`

Уникальная строка, идентифицирующая все вызовы от этого конкретного клиента.

`hasMoratoriumPassed`

Выходной параметр, хранящий результат запроса.

## <a name="return-value"></a>Возвращаемое значение
Если этот метод завершается с ошибкой, возвращается **S_OK**.  В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

| Требование | Версия |
|---|---|
| Минимальная версия клиента | Windows 10 1903 |
|   |   |



 

 



