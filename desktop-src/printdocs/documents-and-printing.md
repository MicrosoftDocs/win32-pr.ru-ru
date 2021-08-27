---
description: в этих разделах описываются документы и функции печати Windows, позволяющие приложениям сохранять, просматривать и печатать.
ms.assetid: 20e56af6-9598-4d6a-a2bf-454cef8a3368
title: 'Документы и печать '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87d7af92af0615dcb11d2623be8f2e21ae813aa1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472370"
---
# <a name="documents-and-printing"></a>Документы и печать 

в этих разделах описываются документы и функции печати Windows, позволяющие приложениям сохранять, просматривать и печатать.

## <a name="in-this-section"></a>В этом разделе




| Раздел | Описание | 
|-------|-------------|
| <a href="/windows/desktop/printdocs/what-s-new-for-printing-in-windows-vnext">Новые возможности печати</a><br /> | Windows 8 поддерживает <a href="/previous-versions/windows/apps/hh465225(v=win.10)">печать для приложений Windows store с помощью JavaScript и HTML</a> и <a href="/previous-versions/windows/apps/hh465196(v=win.10)">печати для Windows приложений магазина с помощью C#/VB/C + + и XAML</a>.<br /> Windows 8 также включает новый API на основе COM, обеспечивающий полную поддержку Open XPS и доступ к частям новых драйверов принтеров, которые Windows 8 поддерживаются. Дополнительные сведения о новом API см. в разделе <a href="/windows/desktop/printdocs/tailored-app-printing-api">Печать пакета документа API</a>.<br /> Windows программа "входящие" драйвера принтера гарантирует, что Windows 8 включает поддержку высокой доли популярных принтеров.<br /> | 
| <a href="/windows/desktop/printdocs/jobbindalldocuments">XPS-документы</a><br /> | Сведения об API документов XPS цифровые подписи XPS.<br /><ul><li><a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">API документов XPS</a><br /> api документов xps — это собственный интерфейс api Windows, поддерживающий OM-элемент xps. API документов XPS появился в Windows 7 и может использоваться в программах пользовательского режима и драйверах принтера XPSDrv.<br /></li><li><a href="/previous-versions/windows/desktop/ff819108(v=vs.85)">API цифровой подписи XPS</a><br /> Цифровые подписи XPS позволяют подписывать документы, проверять удостоверение подписавшего и указывать, изменился ли документ XPS с момента подписания.<br /></li></ul> | 
| <a href="printdocs-printing.md">Вывод на печать</a><br /> | Сведения о функциях печати, поддерживаемых Windows. Эти функции включают в себя следующие:<br /><ul><li><a href="/windows/desktop/printdocs/tailored-app-printing-api">API пакета печати документа</a><br /> Предоставляет приложения с интерфейсом, который позволяет управлять пакетом <strong>PrintDocument</strong> .<br /></li><li><a href="print-spooler-api.md">API диспетчера очереди печати</a><br /> Предоставляет интерфейс диспетчера очереди печати, чтобы приложения могли управлять принтерами и заданиями печати.<br /></li><li><a href="print-ticket-api.md">API билетов на печать</a><br /> Предоставляет приложения с функциями для управления и преобразования билетов на печать.<br /></li><li><a href="gdi-printing.md">API печати GDI</a><br /> Предоставляет приложения с независимым от устройства интерфейсом печати. <br /></li><li><p><a href="xps-printing.md">API печати XPS</a><br /> Предоставляет интерфейс диспетчера очереди печати, который приложения могут использовать для отправки XPS-документов на принтер.</p><blockquote>[!Note]<br />API печати XPS не поддерживается и может быть изменен или недоступен в будущем. Вместо этого клиентские приложения должны использовать <a href="/windows/desktop/printdocs/tailored-app-printing-api">API пакета печати документов</a> .</blockquote><p><br /><br /></p></li></ul> | 
| <a href="/windows/desktop/printdocs/printschema">Схема печати</a><br /> | Схема печати и связанные с ней технологии описывают функции принтера и указывают параметры печати документа для принтеров и просмотра приложений. <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">Спецификация печати схемы</a> — это загружаемый документ, содержащий сведения о схеме печати и способах ее использования в документах и печати. Сведения в Интернете, содержащиеся в этом разделе, предоставляются только для информации и могут неточно отражать текущую версию <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">спецификации схемы печати</a>.<br /> Актуальные сведения о проектировании см. в <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">спецификации схемы печати</a> .<br /> | 




 

## <a name="additional-resources"></a>Дополнительные ресурсы

пример [приложения для печати](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208)) демонстрирует, как выполнить печать из приложения Windows Store, начиная с Windows 8.

функции, описанные в этом разделе, предназначены для собственного Windows программирования. сведения о том, как использовать аналогичные функции в программировании .net (управляемый), см. в разделе [Windows Presentation Foundation документы](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).

Документы XPS основаны на API [упаковки](/previous-versions/windows/desktop/opc/packaging) . См. API упаковки для более низкого уровня доступа к содержимому документа XPS.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[двунаправленное взаимодействие с принтерами (Центр разработки оборудования)](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>
