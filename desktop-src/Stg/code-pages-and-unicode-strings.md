---
title: Кодовые страницы и строки в Юникоде
description: Еще один вопрос при реализации IPropertySetStorage заключается в том, как имена свойств в Юникоде хранятся в свойстве с ИДЕНТИФИКАТОРом 0 (словарь имен свойств), в котором не используются строки в Юникоде.
ms.assetid: 830c90c9-d2a5-4ecf-8cb6-9950ed5320bf
keywords:
- Кодовые страницы и строки в Юникоде
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 508d508ec21e7e763a683e534cf485ebbeec018d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328720"
---
# <a name="code-pages-and-unicode-strings"></a>Кодовые страницы и строки в Юникоде

Еще один вопрос при реализации [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) заключается в том, как имена свойств в Юникоде хранятся в свойстве с идентификатором 0 (словарь имен свойств), в котором не используются строки в Юникоде.

В Юникоде официально указано значение кодовой страницы 1200. Чтобы сохранить значения Юникода в словаре имен свойств, используйте значение кодовой страницы 1200 для всего набора свойств (в свойстве с ИДЕНТИФИКАТОРом 1), которое указывается отсутствием флага **\_ ANSI Пропсетфлаг** в [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create). Учтите, что это побочный результат хранения всех строковых значений в свойстве, заданном в Юникоде. Во всех кодовых страницах число, найденное в начале **VT \_ LPSTR** , является числом байтов, а не числом символов. Это необходимо для обеспечения совместимости с клиентами более ранних версий.

Реализация составного файла [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) создает все новые наборы свойств полностью либо в Юникоде (кодовую страницу 1200), либо в текущей системной кодовой странице ANSI. Это управляется отсутствием или присутствием флага **\_ ANSI пропсетфлаг** в параметре *грффлагс* объекта [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create).

Создание и открытие наборов свойств в Юникоде. Для реализации этого не устанавливайте флаг **\_ ANSI пропсетфлаг** в параметре *грффлагс* объекта [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create). Избегайте использования значений **VT \_ LPSTR** и вместо этого используйте значения **VT \_ LPWSTR** . Если кодовая страница набора свойств — Unicode, строковые значения **VT \_ LPSTR** преобразуются в Юникод при сохранении и возвращаются в многобайтовые строковые значения при извлечении.

Установка флага **\_ ANSI пропсетфлаг** , сообщаемого с помощью вызова [**ипропертистораже:: stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat) , отражает, является ли базовая кодовая страница или не Unicode. Обратите внимание, что свойство с ИДЕНТИФИКАТОРом 1 может быть явно Прочитано для изучения кодовой страницы.

Доступ к свойству с ИДЕНТИФИКАТОРом 1 можно получить через вызов [**ипропертистораже:: реадмултипле**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple). Однако он доступен только для чтения и не может быть обновлен с помощью [**вритемултипле**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple). Кроме того, он не может быть удален с помощью [**делетемултипле**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple).

 

 




