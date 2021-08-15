---
description: Заполнение коллекций COM+
ms.assetid: df86cbab-dcb8-46ac-aebf-8516276b6e81
title: Заполнение коллекций COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 256c246a4f5d176e6b706515d02c0dd5cf68f7ae5a9aff7f89949da14510636b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990674"
---
# <a name="populating-com-collections"></a>Заполнение коллекций COM+

После получения коллекции и перед непосредственной работой с элементами, которые она содержит, необходимо заполнить коллекцию с помощью метода [**заполнения**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) . Это приведет к получению данных для содержимого коллекции из каталога COM+.

Важно понимать, что при использовании объектов Комадмин для управления элементами или данными в коллекциях вы фактически работаете с временными кэшированными данными. Вы не работаете непосредственно с сохраненным каталогом. Действия, выполняемые с коллекцией или любыми ее элементами, отражаются в каталоге до тех пор, пока не будет вызван метод [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) в коллекции. Дополнительные сведения см. в разделе [Сохранение или удаление изменений](saving-or-discarding-changes.md).

Все последующие вызовы, которые необходимо [**заполнить**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate)до вызова команды [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), влияют на отмену ожидающих изменений для всех элементов в коллекции. **Заполнение** всегда заполняет кэш, с которым вы работаете, независимо от того, какие данные сохраняются в базовом хранилище данных каталога.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Навигация по иерархии коллекции COM+](navigating-the-com--collection-hierarchy.md)
</dt> <dt>

[Запросы к доступным связанным коллекциям](querying-for-available-related-collections.md)
</dt> <dt>

[Получение коллекций в каталоге COM+](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



