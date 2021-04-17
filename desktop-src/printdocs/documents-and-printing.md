---
description: В этих разделах описываются документы и функции печати Windows, позволяющие сохранять, просматривать и печатать приложения.
ms.assetid: 20e56af6-9598-4d6a-a2bf-454cef8a3368
title: 'Документы и печать '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19b23ae7040586d550c47f3fedc59104d83fe818
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105674569"
---
# <a name="documents-and-printing"></a>Документы и печать 

В этих разделах описываются документы и функции печати Windows, позволяющие сохранять, просматривать и печатать приложения.

## <a name="in-this-section"></a>В этом разделе



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Раздел</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/printdocs/what-s-new-for-printing-in-windows-vnext">Новые возможности печати</a><br/></td>
<td>Windows 8 поддерживает <a href="/previous-versions/windows/apps/hh465225(v=win.10)">Печать приложений для Магазина Windows с помощью JavaScript и HTML</a> и <a href="/previous-versions/windows/apps/hh465196(v=win.10)">Печать для приложений Магазина Windows с помощью C#/VB/C + + и XAML</a>.<br/> Windows 8 также включает новый API на основе COM, обеспечивающий полную поддержку Open XPS и доступ к частям новых драйверов принтеров, поддерживаемых Windows 8. Дополнительные сведения о новом API см. в разделе <a href="/windows/desktop/printdocs/tailored-app-printing-api">Печать пакета документа API</a>.<br/> Программа "Входящие" драйвера печати Windows гарантирует, что в Windows 8 включена поддержка высокой доли популярных принтеров.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/printdocs/jobbindalldocuments">XPS-документы</a><br/></td>
<td>Сведения об API документов XPS цифровые подписи XPS.<br/>
<ul>
<li><a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">API документов XPS</a><br/> API документов XPS — это собственный API Windows, поддерживающий OM-модель XPS. API документов XPS появился в Windows 7 и может использоваться в программах пользовательского режима и драйверах принтера XPSDrv.<br/></li>
<li><a href="/previous-versions/windows/desktop/ff819108(v=vs.85)">API цифровой подписи XPS</a><br/> Цифровые подписи XPS позволяют подписывать документы, проверять удостоверение подписавшего и указывать, изменился ли документ XPS с момента подписания.<br/></li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="printdocs-printing.md">Вывод на печать</a><br/></td>
<td>Сведения о функциях печати, поддерживаемых Windows. Эти функции включают в себя следующие.<br/>
<ul>
<li><a href="/windows/desktop/printdocs/tailored-app-printing-api">API пакета печати документа</a><br/> Предоставляет приложения с интерфейсом, который позволяет управлять пакетом <strong>PrintDocument</strong> .<br/></li>
<li><a href="print-spooler-api.md">API диспетчера очереди печати</a><br/> Предоставляет интерфейс диспетчера очереди печати, чтобы приложения могли управлять принтерами и заданиями печати.<br/></li>
<li><a href="print-ticket-api.md">API билетов на печать</a><br/> Предоставляет приложения с функциями для управления и преобразования билетов на печать.<br/></li>
<li><a href="gdi-printing.md">API печати GDI</a><br/> Предоставляет приложения с независимым от устройства интерфейсом печати. <br/></li>
<li><p><a href="xps-printing.md">API печати XPS</a><br/> Предоставляет интерфейс диспетчера очереди печати, который приложения могут использовать для отправки XPS-документов на принтер.</p>
<blockquote>
[!Note]<br />
API печати XPS не поддерживается и может быть изменен или недоступен в будущем. Вместо этого клиентские приложения должны использовать <a href="/windows/desktop/printdocs/tailored-app-printing-api">API пакета печати документов</a> .
</blockquote>
<p><br/> <br/></p></li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/printdocs/printschema">Схема печати</a><br/></td>
<td>Схема печати и связанные с ней технологии описывают функции принтера и указывают параметры печати документа для принтеров и просмотра приложений. <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">Спецификация печати схемы</a> — это загружаемый документ, содержащий сведения о схеме печати и способах ее использования в документах и печати. Сведения в Интернете, содержащиеся в этом разделе, предоставляются только для информации и могут неточно отражать текущую версию <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">спецификации схемы печати</a>.<br/> Актуальные сведения о проектировании см. в <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">спецификации схемы печати</a> .<br/></td>
</tr>
</tbody>
</table>



 

## <a name="additional-resources"></a>Дополнительные ресурсы

Пример [приложения для печати](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208)) демонстрирует, как выполнить печать из приложения Магазина Windows, начиная с Windows 8.

Функции, описанные в этом разделе, предназначены для собственного программирования Windows. Сведения о том, как использовать аналогичные функции в программировании .NET (управляемый), см. в разделе [Windows Presentation Foundation документы](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).

Документы XPS основаны на API [упаковки](/previous-versions/windows/desktop/opc/packaging) . См. API упаковки для более низкого уровня доступа к содержимому документа XPS.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Двунаправленное взаимодействие с принтерами (центр разработки оборудования)](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>
