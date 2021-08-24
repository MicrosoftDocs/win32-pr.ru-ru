---
description: Создание топологий
ms.assetid: afd1e646-9bb6-4265-a225-6aaaf1a7bb2a
title: Создание топологий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4048200055066a601f9044ff109f173cb00fc4449a71ea1331b29c8be1a59b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777624"
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

5.  Подключение узлы. Чтобы подключить узел, вызовите [**имфтопологиноде:: коннектаутпут**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) на вышестоящем узле и передайте указатель на подчиненный узел.

Следующие разделы содержат конкретные шаги для каждого типа узла.



| Раздел                                                    | Описание                     |
|----------------------------------------------------------|---------------------------------|
| [Создание исходных узлов](creating-source-nodes.md)       | Создание исходного узла.    |
| [Создание узлов преобразования](creating-transform-nodes.md) | Создание узла преобразования. |
| [Создание выходных узлов](creating-output-nodes.md)       | Создание выходного узла.   |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Топологий](topologies.md)
</dt> </dl>

 

 



