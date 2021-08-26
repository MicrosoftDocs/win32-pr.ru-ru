---
title: Получение элементов автоматизации пользовательского интерфейса
description: В этом разделе описаны различные способы получения интерфейсов Иуиаутоматионелемент для элементов пользовательского интерфейса.
ms.assetid: 8675851a-4a72-4cbe-ab71-ed6fc891be17
keywords:
- Клиенты, получение элементов модели автоматизации пользовательского интерфейса
- Клиенты, элементы модели автоматизации пользовательского интерфейса
- Клиенты, корневые элементы
- Клиенты, область поиска
- Модель автоматизации пользовательского интерфейса, получение элементов
- Модель автоматизации пользовательского интерфейса, элементы
- Модель автоматизации пользовательского интерфейса, корневые элементы
- Модель автоматизации пользовательского интерфейса, условия
- Модель автоматизации пользовательского интерфейса, область поиска
- получение элементов модели автоматизации пользовательского интерфейса
- корневые элементы
- область поиска
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: f2ecf8a30f468e7a7ca4df60465993fa7acdc1e8eef1c8537d8c3d796132cb82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997744"
---
# <a name="obtaining-ui-automation-elements"></a>Получение элементов автоматизации пользовательского интерфейса

В этом разделе описаны различные способы получения интерфейсов [**иуиаутоматионелемент**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) для элементов пользовательского интерфейса.

**Иуиаутоматионелемент** используется в [примере приложения клиента содержимого документов модели автоматизации пользовательского интерфейса](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/UIAutomationDocumentClient).

## <a name="root-element"></a>Корневой элемент

Хотя элементы могут быть получены непосредственно с помощью методов, таких как [**иуиаутоматион:: GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), некоторым клиентским приложениям требуется представление иерархической структуры элементов, известной как дерево автоматизации пользовательского интерфейса. Корневым элементом этой иерархии является Рабочий стол. Этот элемент можно получить с помощью метода [**иуиаутоматион:: жетрутелемент**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getrootelement) или метода [**Иуиаутоматион:: жетрутелементбуилдкаче**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getrootelementbuildcache) . Оба эти метода извлекают указатель интерфейса [**иуиаутоматионелемент**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) . Можно выполнять поиск элементов-потомков с помощью методов, таких как [**иуиаутоматионелемент:: FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) и [**FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall).

> [!Note]  
> В общем случае следует попытаться получить только прямые дочерние элементы корневого элемента. Поиск потомков может выполнять итерацию сотен или тысяч элементов. Если вы пытаетесь получить определенный элемент на более низком уровне, необходимо запустить поиск из окна приложения или из контейнера на более низком уровне.

 

## <a name="conditions"></a>Условия

Для большинства методов, используемых для получения элементов автоматизации пользовательского интерфейса, необходимо указать условие. Условие — это набор критериев, определяющих элементы, которые требуется получить. Условие представлено интерфейсом [**иуиаутоматионкондитион**](/windows/win32/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition) .

Простейшим условием является истинное условие, представляющее собой предопределенный объект, указывающий, что должны возвращаться все элементы в области поиска. Условие false является обратным условием для истинного условия и менее полезно, так как оно предотвратит возможность обнаружения каких-либо элементов. Получить интерфейс к истинному условию можно с помощью [**иуиаутоматион:: креатетруекондитион**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createtruecondition).

Три других предопределенных условия, доступные в качестве свойств объекта [**иуиаутоматион**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) , можно использовать отдельно или в сочетании с другими условиями: [**Иуиаутоматион:: контентвиевкондитион**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewcondition), [**контролвиевкондитион**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_controlviewcondition)и [**раввиевкондитион**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_rawviewcondition). **Раввиевкондитион**, используемый сама по себе, эквивалентен истинному условию, так как не фильтрует элементы по свойствам [**Иуиаутоматионелемент:: куррентисконтролелемент**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) или [**куррентисконтентелемент**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) .

Другие условия строятся на основе объектов условий, каждый из которых задает значение свойства. Например, условие свойства может указывать, что элемент включен или поддерживает определенный шаблон элемента управления.

Условия, использующие логическую логику, можно комбинировать путем вызова [**иуиаутоматион:: креатеандкондитион**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createandcondition), [**креатеоркондитион**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createorcondition), [**креатеноткондитион**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createnotcondition)и связанных методов.

## <a name="search-scope"></a>Область поиска

Поиск, выполняемый с помощью [**иуиаутоматионелемент:: FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) или [**FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) , должен иметь область и начальную позицию.

> [!Note]  
> Любые комментарии об этих двух методах также применяются к [**иуиаутоматионелемент:: финдфирстбуилдкаче**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache) и [**финдаллбуилдкаче**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findallbuildcache).

 

Область определяет пространство вокруг начальной позиции, в которой выполняется поиск. Это может быть сам элемент, его элементы того же уровня, его родитель, непосредственные дочерние элементы и его потомки. Имейте в виду, что методы **Find** не поддерживают поиск по дереву Microsoft UI Automation; Это значит, что поиск элементов-предков не поддерживается.

Область поиска определяется побитовым сочетанием значений из перечисляемого типа [**TreeScope**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope) .

## <a name="finding-a-known-element"></a>Поиск известного элемента

Чтобы найти известный элемент, идентифицируемый по имени, ИДЕНТИФИКАТОРу автоматизации или другому свойству или сочетанию свойств, проще всего использовать метод [**иуиаутоматионелемент:: FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) . Если искомый элемент является окном приложения, то начальной точкой поиска может быть корневой элемент.

Такой способ поиска элементов автоматизации пользовательского интерфейса наиболее удобен в сценариях автоматического тестирования.

Пример кода, в котором показано, как найти известный элемент, см. в разделе [Поиск элемента по имени](uiauto-howto-find-ui-elements.md).

## <a name="finding-elements-in-a-subtree"></a>Поиск элементов в поддереве

Чтобы найти все элементы, соответствующие определенным условиям и связанные с известным элементом, можно вызвать [**иуиаутоматионелемент:: FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) для известного элемента. Например, этот метод используется для получения элементов списка или пунктов меню из списка или меню или для определения всех элементов управления в диалоговом окне.

Пример кода, в котором показано, как найти элементы в поддереве, см. в разделе [Поиск связанных элементов](uiauto-howto-find-ui-elements.md).

## <a name="walking-a-subtree"></a>Обход поддерева

Если у вас нет сведений о приложениях, которые может использовать клиент, можно создать поддерево всех интересующих элементов с помощью [**иуиаутоматионтривалкер**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker). Клиент может сделать это, например, в ответ на событие изменения фокуса; то есть, когда приложение или элемент управления получает фокус ввода, клиент автоматизации пользовательского интерфейса проверяет дочерние элементы и, возможно, все потомки элемента с фокусом.

Имейте в виду, что прохождение дерева модели автоматизации пользовательского интерфейса занимает много ресурсов. Пройдите по дереву только в том случае, когда невозможно использовать методы [**иуиаутоматионелемент:: FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst), [**FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall)или [**буилдупдатедкаче**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-buildupdatedcache) .

Вы можете определить собственный обход дерева, передав пользовательское условие в [**иуиаутоматион:: креатетривалкер**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createtreewalker), или можно использовать один из следующих предопределенных объектов, определенных как свойства базового [**иуиаутоматион**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).



| Объект                                                              | Назначение                                                                                                                                                      |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**контентвиеввалкер**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewwalker) | Находит только те элементы, свойство [**иуиаутоматионелемент:: куррентисконтентелемент**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) которых имеет **значение true**. |
| [**контролвиеввалкер**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_controlviewwalker) | Находит только те элементы, свойство [**иуиаутоматионелемент:: куррентисконтролелемент**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) которых имеет **значение true**. |
| [**раввиеввалкер**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_rawviewwalker)         | Поиск всех элементов.                                                                                                                                          |



 

После получения [**иуиаутоматионтривалкер**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker)вызовите методы **Иуиаутоматионтривалкер:: жеткскскс** для навигации по элементам поддерева, передав элемент, с которого начинается проход.

Метод [**иуиаутоматионтривалкер:: нормализация**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtreewalker-normalizeelement) можно использовать для перехода к элементу в поддереве из другого элемента, который не является частью представления. Например, предположим, что вы создаете представление поддерева с помощью [**иуиаутоматион:: контентвиеввалкер**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewwalker). Приложение получает уведомление о том, что полоса прокрутки получила фокус ввода. Поскольку полоса прокрутки не является элементом содержимого, она отсутствует в представлении поддерева. Однако можно передать [**иуиаутоматионелемент**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) , представляющий полосу прокрутки, в **Иуиаутоматионтривалкер:: нормализацию** и получить ближайший предк, который находится в представлении содержимого.

Примеры кода, демонстрирующие использование интерфейса [**иуиаутоматионтривалкер**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) , см. в разделе [Пошаговое руководство по дереву модели автоматизации пользовательского интерфейса](uiauto-howto-walk-uiautomation-tree.md).

## <a name="other-ways-to-retrieve-an-element"></a>Другие способы получения элемента

Помимо поиска и навигации можно получить [**иуиаутоматионелемент**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) следующими способами.

### <a name="from-an-event"></a>Из события

Когда приложение получает событие автоматизации пользовательского интерфейса, исходный объект, переданный обработчику событий, представлен [**иуиаутоматионелемент**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement). Например, если вы подписались на события изменения фокуса, источником, передаваемым в [**иуиаутоматионфокусчанжедевенсандлер**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler) , будет элемент, получивший фокус. Дополнительные сведения см. [в разделе Подписка на события модели автоматизации пользовательского интерфейса](uiauto-eventsforclients.md).

### <a name="from-a-point"></a>Из точки

Чтобы получить [**иуиаутоматионелемент**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) из экранных координат, например позиции курсора, используйте метод [**Иуиаутоматион:: елементфромпоинт**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint) .

### <a name="from-a-window-handle"></a>Из дескриптора окна

Чтобы получить [**иуиаутоматионелемент**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) из **HWND**, используйте метод [**иуиаутоматион:: елементфромхандле**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle) .

### <a name="from-the-focused-control"></a>Из элемента управления с фокусом

Чтобы получить объект [**иуиаутоматионелемент**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) , представляющий элемент управления с сортировкой, используйте метод [**Иуиаутоматион:: GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement) .

## <a name="related-topics"></a>Связанные темы

[Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md)

[Пример приложения клиента содержимого документов модели автоматизации пользовательского интерфейса](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/UIAutomationDocumentClient)
