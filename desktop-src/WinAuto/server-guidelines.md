---
title: Рекомендации по серверам
description: Чтобы обеспечить работу Microsoft Active Accessibility, серверы должны предоставить клиентам сведения о специальных возможностях.
ms.assetid: 88be4bae-fdeb-467c-b5b1-19f2adc0575d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 344721428c94e2ea3d9e9ff78e194851ba9304db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410713"
---
# <a name="server-guidelines"></a>Рекомендации по серверам

Чтобы обеспечить работу Microsoft Active Accessibility, серверы должны предоставить клиентам сведения о специальных возможностях.

Для реализации [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)разработчики сервера должны следовать этому базовому процессу.

1.  Создайте объекты со специальными возможностями, реализовав свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) и методы для пользовательских элементов пользовательского интерфейса и для клиента приложения. Не забудьте предоставить сдвоенный интерфейс, поддерживающий и **IAccessible** , и [**IDispatch**](idispatch-interface.md) , чтобы клиенты, написанные на Visual Basic Майкрософт и различные языки сценариев, могли получить сведения об этих объектах.
2.  Вызовите [**нотифивиневент**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) , чтобы уведомить клиентов об изменениях в пользовательских элементах пользовательского интерфейса.
3.  Обработайте [**WM \_ GetObject**](wm-getobject.md) для предоставления доступа к доступным объектам.

Рекомендации и рекомендации по проектированию объектов со специальными возможностями см. в [Руководстве разработчика для Active Accessibility серверов](developer-s-guide-for-active-accessibility-servers.md).

## <a name="in-this-section"></a>Содержание раздела

-   [Как серверы реализуют дочерние идентификаторы](how-servers-implement-child-ids.md)

 

 




