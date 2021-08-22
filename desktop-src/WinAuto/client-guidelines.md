---
title: Рекомендации для клиентов
description: Разработчики клиентов должны использовать следующие функциональные возможности для получения сведений об элементах пользовательского интерфейса.
ms.assetid: 0e102e60-4d11-490e-88d5-dfadba620781
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d3cfa9a269d796d7071b2107bba2fde6717f42928b9c9dc8074f94afbdbe15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133947"
---
# <a name="client-guidelines"></a>Рекомендации для клиентов

Разработчики клиентов должны использовать следующие функциональные возможности для получения сведений о элементах пользовательского интерфейса:

-   Чтобы получить интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) для объектов, вызовите [**акцессиблеобжектфромвиндов**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), [**акцессиблеобжектфромпоинт**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)или [**акцессиблеобжектфромевент**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).
-   Для проверки доступных объектов и управления ими используйте свойства и методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .
-   Чтобы получить [виневентс](winevents-overview.md), вызовите [**сетвиневенсук**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) , чтобы зарегистрировать функцию обратного вызова WinEvent для событий, относящихся к клиентскому приложению.

## <a name="in-this-section"></a>Содержание раздела

-   [Получение идентификаторов дочерних объектов клиентами](how-clients-obtain-child-ids.md)

 

 




