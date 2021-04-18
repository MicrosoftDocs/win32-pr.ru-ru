---
title: Модуль записи XML
description: Модуль записи XML — это API для выпуска XML. По сути, модуль записи XML записывает один узел XML за раз, но существуют дополнительные вспомогательные API для упрощения создания последовательности узлов.
ms.assetid: 69d50793-1d5b-4fc7-bf69-128f8e23a98d
keywords:
- Веб-службы модуля записи XML для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085a02b3aca33ffa3b31e4579d47068a683ee4d8
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "105710401"
---
# <a name="xml-writer"></a>Модуль записи XML

Модуль записи XML — это API для выпуска XML. По сути, модуль записи XML записывает один [узел XML](xml-node.md) за раз, но существуют дополнительные вспомогательные API для упрощения создания последовательности узлов.


Поддерживаются следующие типы выходных данных модуля записи:

-   [**Буфер в памяти закодированных байтов**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [**Поток**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   [XML-буфер](xml-buffer.md)

С модулем записи XML используются следующие обратные вызовы:

-   [**\_ \_ обратный вызов динамической строки WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_dynamic_string_callback)
-   [**\_ \_ обратный вызов по запросу WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_pull_bytes_callback)
-   [**\_ \_ обратный вызов push-уведомлений WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_push_bytes_callback)
-   [**\_ \_ обратный вызов записи WS**](/windows/desktop/api/WebServices/nc-webservices-ws_write_callback)

С модулем записи XML используются следующие перечисления:

-   [**набор \_ символов WS**](/windows/desktop/api/WebServices/ne-webservices-ws_charset)
-   [**\_ \_ тип кодирования модуля записи XML \_ WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_encoding_type)
-   [**\_ \_ \_ тип выходных данных модуля записи XML WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_output_type)
-   [**\_ \_ идентификатор свойства модуля записи XML \_ WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_property_id)

С модулем записи XML используются следующие функции:

-   [**вскопиноде**](/windows/desktop/api/WebServices/nf-webservices-wscopynode)
-   [**вскреатевритер**](/windows/desktop/api/WebServices/nf-webservices-wscreatewriter)
-   [**всфлушвритер**](/windows/desktop/api/WebServices/nf-webservices-wsflushwriter)
-   [**всфривритер**](/windows/desktop/api/WebServices/nf-webservices-wsfreewriter)
-   [**всжетпрефиксфромнамеспаце**](/windows/desktop/api/WebServices/nf-webservices-wsgetprefixfromnamespace)
-   [**всжетвритерпоситион**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition)
-   [**всжетвритерпроперти**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterproperty)
-   [**всмовевритер**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter)
-   [**вспуллбитес**](/windows/desktop/api/WebServices/nf-webservices-wspullbytes)
-   [**вспушбитес**](/windows/desktop/api/WebServices/nf-webservices-wspushbytes)
-   [**вссетаутпут**](/windows/desktop/api/WebServices/nf-webservices-wssetoutput)
-   [**вссетаутпуттобуффер**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer)
-   [**вссетвритерпоситион**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition)
-   [**всвритеаррай**](/windows/desktop/api/WebServices/nf-webservices-wswritearray)
-   [**всвритебитес**](/windows/desktop/api/WebServices/nf-webservices-wswritebytes)
-   [**всвритечарс**](/windows/desktop/api/WebServices/nf-webservices-wswritechars)
-   [**WsWriteCharsUtf8**](/windows/desktop/api/WebServices/nf-webservices-wswritecharsutf8)
-   [**всвритиндаттрибуте**](/windows/desktop/api/WebServices/nf-webservices-wswriteendattribute)
-   [**всвритиндкдата**](/windows/desktop/api/WebServices/nf-webservices-wswriteendcdata)
-   [**всвритинделемент**](/windows/desktop/api/WebServices/nf-webservices-wswriteendelement)
-   [**всвритеноде**](/windows/desktop/api/WebServices/nf-webservices-wswritenode)
-   [**всвритекуалифиеднаме**](/windows/desktop/api/WebServices/nf-webservices-wswritequalifiedname)
-   [**всвритестартаттрибуте**](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute)
-   [**всвритестарткдата**](/windows/desktop/api/WebServices/nf-webservices-wswritestartcdata)
-   [**всвритестартелемент**](/windows/desktop/api/WebServices/nf-webservices-wswritestartelement)
-   [**всвритетекст**](/windows/desktop/api/WebServices/nf-webservices-wswritetext)
-   [**всвритевалуе**](/windows/desktop/api/WebServices/nf-webservices-wswritevalue)
-   [**всвритексмлнсаттрибуте**](/windows/desktop/api/WebServices/nf-webservices-wswritexmlnsattribute)

С модулем записи XML используется следующий маркер:

-   [\_ \_ модуль записи XML WS](ws-xml-writer.md)

С модулем записи XML используются следующие структуры:

-   [**\_ \_ \_ двоичное кодирование модуля записи XML WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_binary_encoding)
-   [**\_ \_ \_ выходные данные буфера модуля записи XML WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [**\_ \_ кодирование модуля записи XML WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_encoding)
-   [**\_ \_ Кодирование MTOM модуля записи XML \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_mtom_encoding)
-   [**\_ \_ выходные данные модуля записи XML WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_output)
-   [**\_ \_ Свойства модуля записи XML WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_properties)
-   [**\_ \_ свойство модуля записи XML WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_property)
-   [**\_ \_ \_ выходные данные потока модуля записи XML WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   [**\_ \_ Кодировка текста для модуля записи XML \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_text_encoding)

 

 




