---
title: Категоризация по возможностям контейнеров
description: Компоненты часто нуждаются в определенных функциональных возможностях контейнера и не будут работать с контейнером, который не обеспечивает поддержку.
ms.assetid: 11002f3e-17de-4e05-a2df-0c9e6326846d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987546c20ff77a40666bb74689466a15fab989a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068542"
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

Сравните предыдущий пример со следующим примером, в котором Мидбконтрол может использовать Visual Basic привязки данных, если контейнер поддерживает его. Однако он определен таким образом, что он будет работать в контейнерах, которые не поддерживают Visual Basic привязки данных (возможно, с помощью другого API базы данных):

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

Контейнер, поддерживающий Visual Basic привязанные к данным элементы управления, но не поддерживающий простые элементы управления Frame, будет указывать CATID \_ элемента управления и CATID \_ вбдатабаунд в пользовательском интерфейсе элемента управления INSERT. Список элементов управления, отображаемых для пользователя, будет содержать \_ кнопку CLSID и \_ мидбконтрол CLSID. \_Группа CLSID не будет отображаться.

## <a name="related-topics"></a>См. также

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

 

 




