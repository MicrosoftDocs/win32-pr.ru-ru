---
description: Интерфейсы документов предоставляют доступ к компонентам пакета XPS, которые определяют структуру документа в OM-модели XPS.
ms.assetid: 3302d164-81ad-4198-a116-f967e7a14147
title: Интерфейсы документа OM модели XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc191c4c0b8ec5571331022321a8ae829587022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656587"
---
# <a name="xps-om-document-interfaces"></a>Интерфейсы документа OM модели XPS

Интерфейсы документов предоставляют доступ к компонентам пакета XPS, которые определяют структуру документа в OM-модели XPS. В следующей таблице перечислены интерфейсы документов.



| Имя интерфейса                                                      | Логические дочерние интерфейсы                                      | Описание                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**икспсомдокументсекуенце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> | [**икспсомдокумент**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>           | Представляет набор документов, которые связаны друг с другом в упорядоченном списке.<br/> Дочерние интерфейсы собираются в интерфейсе [**икспсомдокументколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection) .<br/>                                                                                                                                                                                                  |
| [**икспсомдокумент**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>                 | [**икспсомпажереференце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/> | Представляет отдельную часть FixedDocument и связывает коллекцию ссылок на страницы в документе.<br/> Дочерние интерфейсы собираются в интерфейсе [**икспсомпажереференцеколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) .<br/> Структура документа предоставляется в интерфейсе [**икспсомдокументструктурересаурце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource) .<br/> |
| [**икспсомпажереференце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/>       | [**икспсомпаже**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/>                   | Неплотная виртуальная версия страницы в документе. Ссылка на страницу описывает основные характеристики страницы (например, ее измерения), но не включает содержимое страницы.<br/>                                                                                                                                                                                             |
| [**икспсомнамеколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)<br/>     | Нет<br/>                                               | Коллекция объектов страницы, являющихся объектами гиперссылок.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**икспсомпартресаурцес**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)<br/>       | Нет<br/>                                               | Коллекция ресурсов частей, связанных со страницей.<br/>                                                                                                                                                                                                                                                                                                                                |



 

## <a name="contents"></a>Содержимое

-   [Работа с интерфейсами икспсомдокументсекуенце](working-with-xpsomdocumentsequence-interfaces.md) содержит сведения об использовании следующих интерфейсов:
    -   [**икспсомдокументсекуенце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
    -   [**икспсомдокументколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)
-   [Работа с интерфейсами икспсомдокумент](working-with-xpsomdocument-interfaces.md) содержит сведения об использовании следующих интерфейсов:
    -   [**икспсомдокумент**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
    -   [**икспсомпажереференцеколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)
    -   [**икспсомдокументструктурересаурце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)
-   [Работа с интерфейсами икспсомпажереференце](working-with-xpsompagereference-interfaces.md) содержит сведения об использовании следующих интерфейсов:
    -   [**икспсомпажереференце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
    -   [**икспсомпаже**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
    -   [**икспсомнамеколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)
    -   [**икспсомпартресаурцес**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)

 

 




