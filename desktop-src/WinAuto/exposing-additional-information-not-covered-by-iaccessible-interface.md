---
title: Предоставление дополнительных сведений, не охваченных интерфейсом IAccessible
description: В зависимости от своих продуктов разработчикам серверов может потребоваться предоставить сведения или функции в дополнение к поддержке Microsoft Active Accessibility.
ms.assetid: c45009ca-6be3-4645-9097-36671a41dfce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3834c60de8f18fd5ec0719919a1cd79e22f451e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338665"
---
# <a name="exposing-additional-information-not-covered-by-iaccessible-interface"></a>Предоставление дополнительных сведений, не охваченных интерфейсом IAccessible

В зависимости от своих продуктов разработчикам серверов может потребоваться предоставить сведения или функции в дополнение к поддержке Microsoft Active Accessibility. Если это так, обратитесь к разработчикам вспомогательных технологий (клиенты), чтобы убедиться, что они добавляют поддержку функций.

Не пытайтесь расширить интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . После публикации интерфейсы не могут быть изменены. Чтобы предоставить дополнительные сведения, используйте пользовательский интерфейс и предоставьте его с помощью одного из следующих методов:

-   [Использование OBJID \_ нативеом для предоставления собственного интерфейса объектной модели для окна](using-objid-nativeom-to-expose-a-native-object-model-interface-for-a-window.md)
-   [Использование QueryService для предоставления собственного интерфейса объектной модели для объекта IAccessible](using-queryservice-to-expose-a-native-object-model-interface-for-an-iaccessible-object.md)

Обратите внимание, что целью интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) является наличие четко определенного интерфейса, используемого серверами и клиентами. Прежде чем предоставлять доступ к пользовательским интерфейсам, не забудьте предоставить как можно больше информации через **IAccessible**.

Нельзя использовать [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для предоставления настраиваемых интерфейсов. Используйте **IServiceProvider:: QueryService** , как описано в следующих процедурах.

 

 