---
title: Интерфейс IUniversalOrchestrator
description: COM-интерфейс, предоставляющий методы, позволяющие клиенту обмениваться данными с универсальной Orchestrator.
ms.date: 01/14/2021
ms.topic: interface
ms.openlocfilehash: 6fa5dfd9f7853159645fbe3b543c228450f4e1c4
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "105719755"
---
# <a name="iuniversalorchestrator-interface"></a>Интерфейс IUniversalOrchestrator

> [!NOTE] 
> Этот API принадлежит к универсальному API Orchestrator.

**Иуниверсалорчестратор** — это COM-интерфейс, предоставляющий следующие методы, позволяющие клиенту обмениваться данными с универсальной Orchestrator.

## <a name="methods"></a>Методы

|Метод | Описание |
|---|---|
|[:: Счедулеворк](universalorchestrator-schedulework.md) | Регистрирует ожидающие работы с универсальной Orchestrator. |
|[:: Ворккомплетед](universalorchestrator-workcompleted.md) | Информирует универсальную Orchestrator о том, что вся работа завершена. |
|[:: Хасмораториумпассед](universalorchestrator-hasmoratoriumpassed.md) | Запрашивает универсальную Orchestrator, чтобы определить, работает ли она сразу после завершения работы нового устройства. |


## <a name="requirements"></a>Требования

| Требование | Версия |
|---|---|
| Минимальная версия клиента | Windows 10 1903 |
|   |   |