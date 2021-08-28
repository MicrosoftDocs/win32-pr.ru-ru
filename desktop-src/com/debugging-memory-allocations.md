---
title: Отладка выделения памяти
description: Отладка выделения памяти
ms.assetid: 522adb1f-0e3e-4dfb-8836-f539a79a3d9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae81b3376b2ffee17ce747197eb57fecbdae18e086d5252dd5f4721975181885
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993454"
---
# <a name="debugging-memory-allocations"></a>Отладка выделения памяти

COM предоставляет разработчикам интерфейс [**IMallocSpy**](/windows/desktop/api/ObjIdl/nn-objidl-imallocspy) для отладки выделения памяти. Для каждого метода нахождения [**в**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc)интерфейсе **IMallocSpy** есть два метода: «Pre» и «POST». После того, как разработчик реализовал его и опубликует в системе, система вызывает метод **IMallocSpy** "Pre" непосредственно **перед соответствующим методом** освобождения, фактически позволяя коду отладки "Spy" в операции выделения памяти и вызову метода POST для освобождения Spy.

Например, когда COM обнаруживает, что следующий вызов является вызовом метода [**unalloc:: Alloc**](/windows/desktop/api/ObjIdl/nf-objidl-imalloc-alloc), он вызывает метод [**IMallocSpy::P перераспределения**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-prealloc), выполняя все операции отладки, необходимые разработчику во время выполнения **выделения** , а затем, когда вызывается метод **выделения** , вызывает интерфейс [**IMallocSpy::P осталлок**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-postalloc) для освобождения Spy и возврата управления в код.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Управление выделением памяти](managing-memory-allocation.md)
</dt> </dl>

 

 