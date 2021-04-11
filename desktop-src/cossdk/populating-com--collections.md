---
description: Заполнение коллекций COM+
ms.assetid: df86cbab-dcb8-46ac-aebf-8516276b6e81
title: Заполнение коллекций COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 521d85521eb7e3750d06920a570ddeaf4d7e9b20
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342252"
---
# <a name="populating-com-collections"></a>Заполнение коллекций COM+

После получения коллекции и перед непосредственной работой с элементами, которые она содержит, необходимо заполнить коллекцию с помощью метода [**заполнения**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) . Это приведет к получению данных для содержимого коллекции из каталога COM+.

Важно понимать, что при использовании объектов Комадмин для управления элементами или данными в коллекциях вы фактически работаете с временными кэшированными данными. Вы не работаете непосредственно с сохраненным каталогом. Действия, выполняемые с коллекцией или любыми ее элементами, отражаются в каталоге до тех пор, пока не будет вызван метод [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) в коллекции. Дополнительные сведения см. в разделе [Сохранение или удаление изменений](saving-or-discarding-changes.md).

Все последующие вызовы, которые необходимо [**заполнить**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate)до вызова команды [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), влияют на отмену ожидающих изменений для всех элементов в коллекции. **Заполнение** всегда заполняет кэш, с которым вы работаете, независимо от того, какие данные сохраняются в базовом хранилище данных каталога.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Навигация по иерархии коллекции COM+](navigating-the-com--collection-hierarchy.md)
</dt> <dt>

[Запросы к доступным связанным коллекциям](querying-for-available-related-collections.md)
</dt> <dt>

[Получение коллекций в каталоге COM+](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



