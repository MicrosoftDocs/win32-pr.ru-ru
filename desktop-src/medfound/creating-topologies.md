---
description: Создание топологий
ms.assetid: afd1e646-9bb6-4265-a225-6aaaf1a7bb2a
title: Создание топологий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a9ec738c82ea2b85bcae7d4c05627b81ad939db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423562"
---
# <a name="creating-topologies"></a>Создание топологий

В этом разделе описаны некоторые общие процедуры создания топологии.

Ниже приведены общие действия по созданию топологии.

1.  Создайте новый объект Topology, вызвав [**мфкреатетопологи**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology). Эта функция возвращает указатель на интерфейс [**имфтопологи**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) топологии.

2.  Изначально топология не содержит узлов. Чтобы создать узлы для топологии, вызовите [**мфкреатетопологиноде**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode). Эта функция возвращает указатель на интерфейс [**имфтопологиноде**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) узла. При создании узла необходимо указать тип узла:

    -   Исходный узел.

    -   Узел преобразования.

    -   Выходной узел.

    -   Узел Tee.

3.  Инициализируйте каждый узел. Процесс инициализации зависит от типа узла, как описано в следующих разделах.

4.  Добавьте каждый узел в топологию, вызвав [**имфтопологи:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode).

5.  Подключите узлы. Чтобы подключить узел, вызовите [**имфтопологиноде:: коннектаутпут**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) на вышестоящем узле и передайте указатель на подчиненный узел.

Следующие разделы содержат конкретные шаги для каждого типа узла.



| Раздел                                                    | Описание                     |
|----------------------------------------------------------|---------------------------------|
| [Создание исходных узлов](creating-source-nodes.md)       | Создание исходного узла.    |
| [Создание узлов преобразования](creating-transform-nodes.md) | Создание узла преобразования. |
| [Создание выходных узлов](creating-output-nodes.md)       | Создание выходного узла.   |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Топологии](topologies.md)
</dt> </dl>

 

 



