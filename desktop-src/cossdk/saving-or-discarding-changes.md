---
description: Сохранение или Отмена изменений
ms.assetid: eba4e794-0929-450c-a172-6de6c2f2f2c4
title: Сохранение или Отмена изменений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4946574facd0d41d68f4de8cf2f2f48410eb6e99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895617"
---
# <a name="saving-or-discarding-changes"></a>Сохранение или Отмена изменений

При задании свойств элемента никакие изменения фактически не записываются в каталог COM+, пока не будут явно сохранены изменения. Это делается с помощью метода [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) в объекте [**комадминкаталогколлектион**](comadmincatalogcollection.md) для коллекции, содержащей элемент.

Если вы хотите отменить изменения, которые еще не были зафиксированы, можно вызвать метод [**заполнения**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) для объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) . Это считывает все постоянные данные из каталога COM+ для всех элементов в коллекции, фактически удаляя все ожидающие изменения.

При использовании [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)все несоответствия в выбранных параметрах свойств приводят к ошибке, и **SaveChanges** не может записать объект, который вернул ошибку. Все свойства данного элемента либо записываются, либо не могут быть записаны как единое целое.

Однако при возникновении ошибок записи они могут не быть из-за несовместимых параметров. возможно, произошли другие ошибки. Необходимо проверить сведения о сбое. Дополнительные сведения см. в разделе [Обработка ошибок администрирования com+](handling-com--administration-errors.md) и [взаимозависимости между свойствами](interdependencies-between-properties.md).

Как правило, чем больше изменений вы пытаетесь сохранить одновременно, в частности, изменения в нескольких объектах, тем больше вероятность, что вы получаете сообщение об ошибке, а тем сложнее.

Кроме того, между вызовами функций [**заполнения**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) и [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)нет блокировки на элементы в коллекции; состязание возможно. Дополнительные сведения см. в разделе [Получение и Настройка свойств](getting-and-setting-properties.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Получение и задание свойств](getting-and-setting-properties.md)
</dt> <dt>

[Взаимозависимости между свойствами](interdependencies-between-properties.md)
</dt> <dt>

[Запрос доступных свойств](querying-for-available-properties.md)
</dt> </dl>

 

 



