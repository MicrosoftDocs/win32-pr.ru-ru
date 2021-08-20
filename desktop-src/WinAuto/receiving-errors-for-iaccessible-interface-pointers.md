---
title: Получение ошибок для указателей интерфейса IAccessible
description: В этом разделе описываются ситуации, в которых может возникнуть ошибка для указателя на интерфейс IAccessible.
ms.assetid: 408bfa47-fda0-4a25-89c1-da41d967ad61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d36a29c688966526d5431e1fe2f643e39b378779d122d22f38dea2089a5191c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115145"
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

 

 




