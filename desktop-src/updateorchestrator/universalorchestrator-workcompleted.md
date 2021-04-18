---
title: IUniversalOrchestrator::WorkCompleted
description: Вызывает универсальную Orchestrator для обозначения завершения работы
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 8d4a08e7f021811e59a182a8b726397476b78433
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "105719757"
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



 

 



