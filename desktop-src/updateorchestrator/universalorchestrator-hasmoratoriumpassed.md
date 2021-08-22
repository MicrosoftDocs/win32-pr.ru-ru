---
title: IUniversalOrchestrator::HasMoratoriumPassed
description: Запрашивает универсальную Orchestrator, чтобы определить, был ли превышен период после OOBE.
ms.topic: reference
ms.date: 01/14/2021
ms.openlocfilehash: 61870e1bd57f54afded3f905da34ddc9198bcdb555c42adc4c799e08f2acf392
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966131"
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



 

 



