---
title: IUniversalOrchestrator::HasMoratoriumPassed
description: Запрашивает универсальную Orchestrator, чтобы определить, был ли превышен период после OOBE.
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 2ed354d365b795a0c959396e6b26d6bc73baad97
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "105719754"
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



 

 



