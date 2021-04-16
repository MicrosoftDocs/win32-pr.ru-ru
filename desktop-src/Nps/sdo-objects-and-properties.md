---
title: Объекты и свойства
description: Характеристики объекта в SDO определяются свойствами объекта и значениями, связанными с этими свойствами.
ms.assetid: 9faa7759-cad5-4429-94b0-6cba145cfadb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efed7720388e61b9d6131acafd4b9bda17694d29
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672335"
---
# <a name="objects-and-properties"></a>Объекты и свойства

Характеристики объекта в SDO определяются свойствами объекта и значениями, связанными с этими свойствами. В отличие от других объектных моделей, объекты SDO сами по себе не имеют методов. Однако объекты SDO предоставляют интерфейсы COM, предоставляющие методы.

Объекты SDO предоставляют интерфейс [**исдо**](/windows/desktop/api/sdoias/nn-sdoias-isdo) , предоставляющий методы для управления свойствами объектов. Чтобы получить доступ к свойствам объекта, получите интерфейс **исдо** для объекта и используйте методы интерфейса GetObject [**и**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) [**putproperty изменил**](/windows/desktop/api/sdoias/nf-sdoias-isdo-putproperty) для получения и установки значений свойств. В разделе [Получение ПОЛЬЗОВАТЕЛЬСКОГО SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) содержится пример кода, демонстрирующий получение интерфейса **Исдо** для объекта пользователя.

После внесения изменений в свойства объекта используйте метод [**исдо:: Apply**](/windows/desktop/api/sdoias/nf-sdoias-isdo-apply) , чтобы записать изменения в постоянное хранилище для объекта. Вы можете отменить изменения, внесенные в свойства объекта перед вызовом **исдо:: Apply** путем вызова метода [**исдо:: Restore**](/windows/desktop/api/sdoias/nf-sdoias-isdo-restore) . Этот метод восстанавливает значения свойств объекта из постоянного хранилища.

В следующей таблице показаны типы перечислений, которые перечисляют свойства некоторых объектов в SDO.



| Объект                                 | Тип перечисления                                       |
|----------------------------------------|--------------------------------------------------------|
| Все объекты SDO                        | [**иаскоммонпропертиес**](/windows/desktop/api/sdoias/ne-sdoias-iascommonproperties) |
| Объект User                            | [**усерпропертиес**](/windows/desktop/api/sdoias/ne-sdoias-userproperties)           |
| Объект службы (сервер политики сети) | [**иаспропертиес**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)             |
| Объект протокола Microsoft RADIUS       | [**радиуспропертиес**](/windows/desktop/api/sdoias/ne-sdoias-radiusproperties)       |



 

> [!Note]  
> Служба проверки подлинности в Интернете (IAS) переименовала сервер политики сети (NPS), начиная с Windows Server 2008.

 

## <a name="collections"></a>Коллекции

Объекты часто группируются в коллекции. API SDO предоставляет функциональные возможности через интерфейс [**сбора исдо**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) для перечисления объектов в коллекции и добавления и удаления объектов из коллекции.

Доступ к коллекции получается путем получения свойства коллекции для объекта, содержащего коллекцию. Дополнительные сведения см. в разделе [Иерархия объектной модели](/windows/desktop/Nps/sdo-object-model-hierarchy).

Тип данных для всех свойств, соответствующих коллекциям, — это VT \_ Dispatch.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Иерархия объектной модели SDO](/windows/desktop/Nps/sdo-object-model-hierarchy)
</dt> <dt>

[Поддерживаемые в SDO атрибуты](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> </dl>

 

 