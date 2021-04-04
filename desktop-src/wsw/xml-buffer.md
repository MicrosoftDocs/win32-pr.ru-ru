---
title: XML-буфер
description: XML-буфер предоставляет эффективное хранилище в памяти для произвольных XML-данных.
ms.assetid: e379628b-c6f8-48b1-8109-59fb604f2bcb
keywords:
- Веб-службы буфера XML для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab71121dc451c9ccb186c754d537836f9e899fa9
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103988002"
---
# <a name="xml-buffer"></a>XML-буфер

XML-буфер предоставляет эффективное хранилище в памяти для произвольных XML-данных.


Для чтения данных из буфера XML используйте [средство чтения XML](xml-reader.md) и вызовите [**вссетинпуттобуффер**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer) с помощью XML-буфера. Модуль чтения будет расположен в начале документа.

Чтобы вставить данные в буфер, используйте [модуль записи XML](xml-writer.md) и вызовите [**вссетаутпуттобуффер**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer) с помощью XML-буфера. Модуль записи будет расположен в конце документа.

После того как для модуля чтения задается XML-буфер, помимо всех API-интерфейсов средства чтения XML, [**всмовереадер**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader) может использоваться для навигации по документу. [**Всжетреадерпоситион**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) и [**вссетреадерпоситион**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition) также могут использоваться для записи позиций в документ и возврата к нему позже.

После установки модуля записи в буфер XML, помимо всех API-интерфейсов модуля записи XML, [**всмовевритер**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter) может использоваться для перемещения по модулю записи через документ. [**Всжетвритерпоситион**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) и [**вссетвритерпоситион**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition) также могут использоваться для записи позиций в документ и возврата к нему позже. Модуль записи всегда вставляет данные перед узлом, на котором он расположен.

Узлы могут быть удалены из буфера XML путем получения расположения узла с помощью [**всжетреадерпоситион**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) или [**всжетвритерпоситион**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) и последующего вызова [**всремовеноде**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode) с этой позицией. Для элементов это приведет к удалению элемента, всех его дочерних элементов, включая соответствующий элемент End.

Значение координаты представляется [**\_ \_ \_ позицией узла WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position). Позиции относятся к конкретному XML-буферу и допустимы только при условии, что XML-буфер является допустимым.

С XML-буферами используются следующие перечисления:

-   [**\_Переместить \_ в**](/windows/desktop/api/WebServices/ne-webservices-ws_move_to)
-   [**\_ \_ \_ идентификатор свойства XML-буфера WS \_**](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_property_id)

Для XML-буферов используются следующие функции:

-   [**вскреатексмлбуффер**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlbuffer)
-   [**всремовеноде**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode)

Для XML-буферов используется следующий маркер:

-   [\_XML- \_ буфер WS](ws-xml-buffer.md)

Для XML-буферов используются следующие структуры:

-   [**\_свойство "XML- \_ буфер WS" \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_buffer_property)
-   [**\_ \_ расположение узла WS \_ XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position)

 

 




