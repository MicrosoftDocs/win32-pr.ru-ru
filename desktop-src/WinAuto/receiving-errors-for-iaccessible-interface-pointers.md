---
title: Получение ошибок для указателей интерфейса IAccessible
description: В этом разделе описываются ситуации, в которых может возникнуть ошибка для указателя на интерфейс IAccessible.
ms.assetid: 408bfa47-fda0-4a25-89c1-da41d967ad61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e54d3bd9e39dae9c5de9ad1644e5955bd5fb90d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888783"
---
# <a name="receiving-errors-for-iaccessible-interface-pointers"></a>Получение ошибок для указателей интерфейса IAccessible

В этом разделе описываются ситуации, в которых может возникнуть ошибка для указателя на интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Функции **IAccessible** могут возвращать ошибки для указателей на интерфейсы **IAccessible** , когда пользователь закрывает приложение, которому принадлежит объект, или если пользователь откроет элемент управления через пользовательский интерфейс.

## <a name="user-closes-an-application"></a>Пользователь закрывает приложение

Если пользователь закрывает приложение, содержащее объект, указывающий на указатель интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , все будущие вызовы этого объекта будут возвращать код ошибки. Ошибка, например **CO \_ E \_ обжнотконнектед**, указывает, что объект больше не существует. Это относится ко всем указателям интерфейса **IAccessible** .

## <a name="user-dismisses-a-control"></a>Пользователь закрывает элемент управления

Если пользователь закрывает элемент управления (например, нажав кнопку "Отправить"), клиенты по-прежнему могут вызывать методы и свойства метода [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) для этого объекта, так как объект не был освобожден. Однако будущие вызовы будут поступать с сообщениями об ошибках.

Эта ситуация относится к следующим функциям и методам:

-   [**акцессиблеобжектфромевент**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)
-   [**акцессиблеобжектфромпоинт**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [**акцессиблеобжектфромвиндов**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   [**IAccessible:: Акчиттест**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**IAccessible:: Аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**IAccessible:: Get \_ аккфокус**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)
-   [**IAccessible:: Get \_ аккселектион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)

 

 




