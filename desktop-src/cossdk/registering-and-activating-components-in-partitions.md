---
description: Регистрация и Активация компонентов в секциях
ms.assetid: 2cca71da-c7f7-4997-b63a-74ba266e9e95
title: Регистрация и Активация компонентов в секциях
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31790bc9a3df12d961a4b16271937ae22f963c38
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538801"
---
# <a name="registering-and-activating-components-in-partitions"></a>Регистрация и Активация компонентов в секциях

После создания раздела на следующем шаге выполняется регистрация компонентов COM+ в этом разделе. Компонент регистрируется в разделе при создании нового приложения COM+ или при установке существующего приложения COM+ в раздел. Чтобы упростить администрирование регистрации, когда несколько секций содержат одинаковые компоненты COM+, служба partitions позволяет администратору копировать приложения или компоненты из одной секции в другую. При копировании приложения или компонента COM+ все связанные с ним свойства разделов копируются вместе с удостоверением приложения или любым из членов роли.

Когда клиентская программа вызывает функцию [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) или [**кожетобжект**](/windows/desktop/api/objbase/nf-objbase-cogetobject) для создания экземпляра объекта, com+ выполняет два отдельных шага, как показано ниже.

1.  Находит секцию, в которой находится компонент
2.  Находит нужный компонент в этой секции

Эти действия подробно описаны в следующих подразделах этого раздела:

-   [Поиск секций во время активации](locating-partitions-during-activation.md)
-   [Поиск компонента для активации](locating-a-component-for-activation.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Ограничения разработки приложений](application-design-restrictions.md)
</dt> <dt>

[Компоненты и разделы, помещенные в очередь COM+](com--queued-components-and-partitions.md)
</dt> <dt>

[Реализация секционирования](partition-implementation.md)
</dt> <dt>

[Что такое разделы COM+?](what-are-com--partitions-.md)
</dt> </dl>

 

 
