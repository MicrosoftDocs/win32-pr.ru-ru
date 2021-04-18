---
description: Распределитель памяти
ms.assetid: 2dc055a2-b77a-443d-b602-d9636cbe4db3
title: Распределитель памяти
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be12e25886eda968a00b10386a6eac3fd36e7279
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537805"
---
# <a name="memory-allocator"></a>Распределитель памяти

Объект распределителя памяти выделяет буферы для образцов мультимедиа. Фильтры могут использовать этот объект для выделения буферов общей памяти; Однако фильтр с особыми требованиями также может реализовать собственный объект распределителя памяти. Создайте этот объект, вызвав **CoCreateInstance**.



|                  |                                        |
|------------------|----------------------------------------|
| Идентификатор класса | \_МЕМОРЯЛЛОКАТОР CLSID                 |
| Интерфейсы       | [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Объекты DirectShow](directshow-objects.md)
</dt> </dl>

 

 



