---
title: IUniversalOrchestrator::WorkCompleted
description: Вызывает универсальную Orchestrator для обозначения завершения работы
ms.topic: reference
ms.date: 01/14/2021
ms.openlocfilehash: e36a3ba744df807abbebc6332ac8433010afd667
ms.sourcegitcommit: 3cea99a2ed9579a94236fa7924abd6149db51a58
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/30/2021
ms.locfileid: "114991831"
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

## <a name="requirements"></a>Требования

| Требование | Версия |
|---|---|
| Минимальная версия клиента | Windows 10 1903 |
|   |   |



 

 



