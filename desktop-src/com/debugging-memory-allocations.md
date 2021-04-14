---
title: Отладка выделения памяти
description: Отладка выделения памяти
ms.assetid: 522adb1f-0e3e-4dfb-8836-f539a79a3d9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb6a7dbe313cfe571fa6b4d244df35407fa331e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339329"
---
# <a name="debugging-memory-allocations"></a>Отладка выделения памяти

COM предоставляет разработчикам интерфейс [**IMallocSpy**](/windows/desktop/api/ObjIdl/nn-objidl-imallocspy) для отладки выделения памяти. Для каждого метода нахождения [**в**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc)интерфейсе **IMallocSpy** есть два метода: «Pre» и «POST». После того, как разработчик реализовал его и опубликует в системе, система вызывает метод **IMallocSpy** "Pre" непосредственно **перед соответствующим методом** освобождения, фактически позволяя коду отладки "Spy" в операции выделения памяти и вызову метода POST для освобождения Spy.

Например, когда COM обнаруживает, что следующий вызов является вызовом метода [**unalloc:: Alloc**](/windows/desktop/api/ObjIdl/nf-objidl-imalloc-alloc), он вызывает метод [**IMallocSpy::P перераспределения**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-prealloc), выполняя все операции отладки, необходимые разработчику во время выполнения **выделения** , а затем, когда вызывается метод **выделения** , вызывает интерфейс [**IMallocSpy::P осталлок**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-postalloc) для освобождения Spy и возврата управления в код.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Управление выделением памяти](managing-memory-allocation.md)
</dt> </dl>

 

 