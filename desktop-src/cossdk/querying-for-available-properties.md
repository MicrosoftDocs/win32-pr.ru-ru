---
description: Запрос доступных свойств
ms.assetid: 9acf10cd-19a8-4542-8078-3e4ee275d4d5
title: Запрос доступных свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22238e04404d2b88efa81ce98d0b0fb0e09d245f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142379"
---
# <a name="querying-for-available-properties"></a>Запрос доступных свойств

При написании средства администрирования общего назначения вам, скорее всего, придется написать подпрограммы для настройки свойств в полной общей настройке. Для этого существует средство, которое позволяет динамически запрашивать свойства, доступные для элементов в любой заданной коллекции.

Коллекция [**PropertyInfo**](propertyinfo.md) доступна из любой коллекции, которую вы можете удерживать. Коллекция **PropertyInfo** содержит элемент для каждого доступного свойства. Можно перечислить эти элементы, чтобы определить, доступно ли данное свойство.

Коллекцию [**PropertyInfo**](propertyinfo.md) можно получить из любой коллекции, которую вы удерживаете, используя метод [**IsCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) для объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) , и оставить второй параметр пустым, где обычно указывается свойство ключа родительского элемента.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Получение и задание свойств](getting-and-setting-properties.md)
</dt> <dt>

[Взаимозависимости между свойствами](interdependencies-between-properties.md)
</dt> <dt>

[Сохранение или Отмена изменений](saving-or-discarding-changes.md)
</dt> </dl>

 

 



