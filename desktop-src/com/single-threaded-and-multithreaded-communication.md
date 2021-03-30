---
title: Single-Threaded и многопоточное взаимодействие
description: Single-Threaded и многопоточное взаимодействие
ms.assetid: 8d3a855c-b52d-48bb-9fdf-efbf8005c374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6470ac398e6ae1c8a645fb076fbbf509d58b579
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329304"
---
# <a name="single-threaded-and-multithreaded-communication"></a>Single-Threaded и многопоточное взаимодействие

Клиент или сервер, поддерживающий как однопотоковые, так и многопоточные подразделения, будут иметь один многопоточный апартамент, содержащий все потоки, инициализированные в качестве свободных потоков, и один или несколько однопотоковых апартаментов. Указатели интерфейса должны быть упакованы между апартаментами, но их можно использовать без маршалирования в апартамент. Вызовы объектов в однопотоковом апартаменте будут синхронизированы COM. Вызовы объектов в многопоточном апартаменте не будут синхронизированы COM.

Вся информация о однопотоковых апартаментах применяется к потокам, помеченным как модель подразделения, и вся информация о многопоточных подразделениях применяется ко всем потокам, помеченным как свободные потоки. Правила потоков подразделений применяются к взаимодействию между апартаментами. при этом указатели интерфейса должны быть упакованы между апартаментами с вызовами [**комаршалинтерсреадинтерфацеинстреам**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) и [**кожетинтерфацеандрелеасестреам**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream), как описано в [однопотоковых апартаментах](single-threaded-apartments.md).

> [!Note]  
> При работе с внутрипроцессного серверами применяются некоторые особенности. Дополнительные сведения см. [в разделе проблемы потоковой обработки на сервере](in-process-server-threading-issues.md).

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Доступ к интерфейсам в разных апартаментах](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Выбор потоковой модели](choosing-the-threading-model.md)
</dt> <dt>

[Многопоточные подразделения](multithreaded-apartments.md)
</dt> <dt>

[Проблемы потоковой обработки в процессе сервера](in-process-server-threading-issues.md)
</dt> <dt>

[Процессы, потоки и подразделения](processes--threads--and-apartments.md)
</dt> <dt>

[Подразделения с одним потоком](single-threaded-apartments.md)
</dt> </dl>

 

 




