---
title: IUniversalOrchestrator::WorkCompleted
description: Вызывает универсальную Orchestrator для обозначения завершения работы
ms.topic: reference
ms.date: 01/14/2021
ms.openlocfilehash: 5094ae864b4df9a3dd53b90c3b7d099a206a0ad8db1d1176b603b5ba45ca8194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966085"
---
# <a name="iuniversalorchestratorworkcompleted-method"></a>Метод Иуниверсалорчестратор:: Ворккомплетед

> [!NOTE] 
> Этот API принадлежит к универсальному API Orchestrator.

Позволяет клиентам информировать универсальную Orchestrator о том, что ранее запланированная работа была выполнена, и закончить обратные вызовы, чтобы выполнить работу до следующего успешного вызова Счедулеворк.

## <a name="syntax"></a>Синтаксис

```C++
HRESULT WorkCompleted(
  LPCWSTR callerIdentifier,
  BOOL    workCompleted);
```

## <a name="parameters"></a>Параметры

`callerIdentifier`

Уникальная строка, идентифицирующая все вызовы от этого конкретного клиента.

`workCompleted`

**Значение true** , если работа успешно завершена. В противном случае **значение false** , если попытка работы завершилась неудачей, и ее следует повторить в будущем. 

## <a name="return-value"></a>Возвращаемое значение
Если этот метод завершается с ошибкой, возвращается **S_OK**.  В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)

| Требование | Версия |
|---|---|
| Минимальная версия клиента | Windows 10 1903 |
|   |   |



 

 



