---
title: Рекомендации по серверам
description: Чтобы обеспечить работу Microsoft Active Accessibility, серверы должны предоставить клиентам сведения о специальных возможностях.
ms.assetid: 88be4bae-fdeb-467c-b5b1-19f2adc0575d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b92d70a33dc8d397ff84fc3b9901dba044741d3044f6a7b7f6d1226aa5b683
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614554"
---
# <a name="server-guidelines"></a>Рекомендации по серверам

Чтобы обеспечить работу Microsoft Active Accessibility, серверы должны предоставить клиентам сведения о специальных возможностях.

Для реализации [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)разработчики сервера должны следовать этому базовому процессу.

1.  Создайте объекты со специальными возможностями, реализовав свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) и методы для пользовательских элементов пользовательского интерфейса и для клиента приложения. не забудьте предоставить сдвоенный интерфейс, поддерживающий и **IAccessible** , и [**IDispatch**](idispatch-interface.md) , чтобы клиенты, написанные на Visual Basic майкрософт и различные языки сценариев, могли получить сведения об этих объектах.
2.  Вызовите [**нотифивиневент**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) , чтобы уведомить клиентов об изменениях в пользовательских элементах пользовательского интерфейса.
3.  Обработайте [**WM \_ GetObject**](wm-getobject.md) для предоставления доступа к доступным объектам.

Рекомендации и рекомендации по проектированию объектов со специальными возможностями см. в [Руководстве разработчика для Active Accessibility серверов](developer-s-guide-for-active-accessibility-servers.md).

## <a name="in-this-section"></a>Содержание раздела

-   [Как серверы реализуют дочерние идентификаторы](how-servers-implement-child-ids.md)

 

 




