---
title: Использование QueryService для получения собственного интерфейса для объекта IAccessible
description: Разработчики сервера могут использовать этот метод для предоставления указателя на пользовательский узел документа для объекта IAccessible. В этом случае предполагается, что объекты IAccessible уже предоставлены. Этот метод позволяет клиентам получать пользовательский объект из объекта IAccessible.
ms.assetid: aaa0e840-f8c2-4f3d-9d97-1910f00c1041
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d971462154eb12789a74e8cc6edb5aed68c84b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070300"
---
# <a name="use-queryservice-to-retrieve-a-native-interface-for-an-iaccessible-object"></a>Использование QueryService для получения собственного интерфейса для объекта IAccessible

Разработчики сервера могут использовать этот метод для предоставления указателя на пользовательский узел документа для объекта [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . В этом случае предполагается, что объекты **IAccessible** уже предоставлены. Этот метод позволяет клиентам получать пользовательский объект из объекта **IAccessible** .

**Предоставление собственной объектной модели для IAccessible (серверы)**

1.  Добавьте поддержку интерфейса **IServiceProvider** для объекта [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .
2.  Определите идентификатор GUID, который представляет функциональные возможности получения пользовательского интерфейса из объектов [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Это называется ИДЕНТИФИКАТОРом службы. Вы можете использовать GUIDGEN.EXE для создания идентификатора службы или повторно использовать идентификатор интерфейса, если у вас есть пользовательский интерфейс.
3.  Реализуйте метод **IServiceProvider:: QueryService** , чтобы он возвращал указатель на пользовательский интерфейс при вызове с идентификатором службы, определенным ранее в этой процедуре. **QueryService** должен возвращать **значение NULL** для всех других значений идентификатора службы.
4.  Опубликуйте идентификатор службы, чтобы клиенты могли его использовать.

Клиенты могут использовать эту функцию для получения указателя на пользовательский объект из объекта [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

**Получение указателя на пользовательский объект из IAccessible (клиенты)**

1.  Вызовите [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))(идентификатор IID \_ ) в указателе на интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , чтобы получить указатель интерфейса **IServiceProvider** .
2.  Вызовите **IServiceProvider:: QueryService** с ОПУБЛИКОВАНным идентификатором службы, чтобы получить указатель на пользовательский объект для [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).
3.  Освободите интерфейс **IServiceProvider** , если он больше не нужен.

Для использования в разных процессах серверу может потребоваться зарегистрировать возвращенный интерфейс с помощью модели COM.

Этот метод используется в Microsoft Internet Explorer 4,0 и более поздних версий. Он позволяет клиентам получить указатель интерфейса **IHTMLElement2** , соответствующий объекту [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

 

 