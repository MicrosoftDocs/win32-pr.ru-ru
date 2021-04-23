---
description: Распределитель памяти
ms.assetid: 2dc055a2-b77a-443d-b602-d9636cbe4db3
title: Распределитель памяти
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2412adb78be18ac8c14eb4706624424f97ff13
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909425"
---
# <a name="memory-allocator"></a>Распределитель памяти

Объект распределителя памяти выделяет буферы для образцов мультимедиа. Фильтры могут использовать этот объект для выделения буферов общей памяти; Однако фильтр с особыми требованиями также может реализовать собственный объект распределителя памяти. Создайте этот объект, вызвав **CoCreateInstance**.



| Метка | Значение |
|------------------|----------------------------------------|
| Идентификатор класса | \_МЕМОРЯЛЛОКАТОР CLSID                 |
| Интерфейсы       | [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Объекты DirectShow](directshow-objects.md)
</dt> </dl>

 

 



