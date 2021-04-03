---
title: Рекомендации для клиентов
description: Разработчики клиентов должны использовать следующие функциональные возможности для получения сведений об элементах пользовательского интерфейса.
ms.assetid: 0e102e60-4d11-490e-88d5-dfadba620781
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ced411c24ed0b7aa3ab97cbe1ce2511d4e6b05
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "103987143"
---
# <a name="client-guidelines"></a>Рекомендации для клиентов

Разработчики клиентов должны использовать следующие функциональные возможности для получения сведений о элементах пользовательского интерфейса:

-   Чтобы получить интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) для объектов, вызовите [**акцессиблеобжектфромвиндов**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), [**акцессиблеобжектфромпоинт**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)или [**акцессиблеобжектфромевент**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).
-   Для проверки доступных объектов и управления ими используйте свойства и методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .
-   Чтобы получить [виневентс](winevents-overview.md), вызовите [**сетвиневенсук**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) , чтобы зарегистрировать функцию обратного вызова WinEvent для событий, относящихся к клиентскому приложению.

## <a name="in-this-section"></a>Содержание раздела

-   [Получение идентификаторов дочерних объектов клиентами](how-clients-obtain-child-ids.md)

 

 




