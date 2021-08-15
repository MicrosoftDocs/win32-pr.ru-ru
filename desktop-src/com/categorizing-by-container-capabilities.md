---
title: Категоризация по возможностям контейнеров
description: Компоненты часто нуждаются в определенных функциональных возможностях контейнера и не будут работать с контейнером, который не обеспечивает поддержку.
ms.assetid: 11002f3e-17de-4e05-a2df-0c9e6326846d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67811a40c2c1bbffd4529b3f7c885a0d3e2bea19bda04035ffb80b601c266807
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310891"
---
# <a name="categorizing-by-container-capabilities"></a>Категоризация по возможностям контейнеров

Компоненты часто нуждаются в определенных функциональных возможностях контейнера и не будут работать с контейнером, который не обеспечивает поддержку. Пользовательский интерфейс должен отфильтровать компоненты, для которых требуются функции, которые не поддерживаются контейнером. Для этого компоненты можно классифицировать по требуемым функциональным возможностям контейнера.

Пример компонентов, которые нуждаются в функциональных возможностях из контейнера и не работают в контейнерах, которые не поддерживают эту функциональность, — это простые элементы управления Frame OLE. Классификация по возможностям контейнеров выполняется с помощью дополнительного раздела реестра в ключе CLSID компонента:

``` syntax
;The CLSID for "Simple Frame Control" is {123456FF-ABCD-4321-0101-00000000000C}HKEY_CASSES_ROOT\CLSID\{12346FF-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for simple frame controls is {...CATID_SimpleFrameControl...} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_SimpleFrameControl...}
HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Required Categories\{...CATID_SimpleFrameControl...}
 
```

Как показано в этом примере, компонент может принадлежать к категориям компонентов, которые указывают на поддерживаемые функциональные возможности, а также к категориям компонентов, которые указывают на требуемую функциональность.

В следующем примере элемент управления "Кнопка" является универсальным элементом управления OLE, который не поддерживает никаких дополнительных функциональных возможностей. Он будет работать в любом контейнере управления OLE.

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories\{...CATID_Control...}
 
```

сравните предыдущий пример со следующим примером, в котором мидбконтрол может использовать Visual Basic привязки данных, если контейнер поддерживает его. однако он определен таким образом, что он будет работать в контейнерах, которые не поддерживают Visual Basic привязки данных (возможно, с помощью другого API базы данных):

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_VBDatabound...}
 
```

Элемент управления GroupBox — это простой элемент управления Frame. Он основывается на контейнере, реализующем интерфейс [**исимплефрамесите**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) , и будет работать правильно только в таких контейнерах:

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_SimpleFrame...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Required Categories\{...CATID_SimpleFrame...}
 
```

контейнер, поддерживающий Visual Basic привязанные к данным элементы управления, но не поддерживающий простые элементы управления frame, будет указывать catid \_ элемента управления и catid \_ вбдатабаунд в пользовательском интерфейсе элемента управления insert. Список элементов управления, отображаемых для пользователя, будет содержать \_ кнопку CLSID и \_ мидбконтрол CLSID. \_Группа CLSID не будет отображаться.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Связывание значков с категорией](associating-icons-with-a-category.md)
</dt> <dt>

[Категоризация по возможностям компонентов](categorizing-by-component-capabilities.md)
</dt> <dt>

[Классы и ассоциации по умолчанию](default-classes-and-associations.md)
</dt> <dt>

[Определение категорий компонентов](defining-component-categories.md)
</dt> <dt>

[Диспетчер категорий компонентов](the-component-categories-manager.md)
</dt> </dl>

 

 




