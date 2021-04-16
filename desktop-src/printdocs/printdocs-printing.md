---
description: Windows предоставляет приложениям полный набор функций, позволяющих выполнять печать на различных устройствах, таких как лазерные принтеры, векторные плоттеры, растровые принтеры и факсимильные компьютеры.
ms.assetid: e5c115b0-9c1e-46e7-8fb5-eddbc2c75298
title: Печать (документы и печать)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 607e845ffc525701489a53c2a6b4628eceb5840d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712245"
---
# <a name="printing-documents-and-printing"></a>Печать (документы и печать)

Windows предоставляет приложениям полный набор функций, позволяющих выполнять печать на различных устройствах, таких как лазерные принтеры, векторные плоттеры, растровые принтеры и факсимильные компьютеры.

## <a name="desktop-app-printing"></a>Настольное приложение для печати

Программисты Windows могут выбрать несколько различных технологий для печати из их приложений.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Технология</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/printdocs/tailored-app-printing-api">API пакета печати документа</a><br/></td>
<td>Предоставляет интерфейс, позволяющий приложению получать доступ к пакету печати документа и управлять им. Этот API доступен в Windows 8 и более поздних версиях Windows.<br/></td>
</tr>
<tr class="even">
<td><a href="print-spooler-api.md">API диспетчера очереди печати</a><br/></td>
<td>Предоставляет интерфейс диспетчера очереди печати, чтобы приложения могли управлять принтерами и заданиями печати.<br/> Приложения используют <a href="print-spooler-api.md">API диспетчера очереди печати</a> для запуска, завершения, управления и настройки заданий печати, управляемых диспетчером очереди печати, независимо от того, используется ли для печати содержимого <a href="/windows/desktop/printdocs/tailored-app-printing-api">API пакета печати</a> или <a href="gdi-printing.md">API печати GDI</a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="print-ticket-api.md">API билетов на печать</a><br/></td>
<td>Предоставляет приложения с функциями для управления и преобразования билетов на печать.<br/></td>
</tr>
<tr class="even">
<td><a href="gdi-printing.md">API печати GDI</a><br/></td>
<td>Предоставляет приложения с независимым от устройства интерфейсом печати. <br/>
<blockquote>
[!Note]<br />
Разработчики, пишущие приложения для Windows Vista и более поздних версий Windows, должны использовать <a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">API документов XPS</a> в своих приложениях.
</blockquote>
<br/> <a href="gdi-printing.md">API печати GDI</a> подходит для приложений, которые должны работать в Windows XP и более ранних версиях Windows.<br/></td>
</tr>
</tbody>
</table>



 

На следующем рисунке представлено обобщенное представление того, как взаимосвязаны различные API-интерфейсы печати.

![Схема, показывающая, как собственное приложение Windows может использовать API-интерфейсы печати](images/print-apis.png)

 

[API пакета печати документов](./tailored-app-printing-api.md)в этом разделе описывают пакет печати документов и интерфейсы предварительного просмотра, которые можно использовать в Windows 8 и более поздних версиях Windows Desktop.

Дополнительные сведения о печати из приложений Магазина Windows, написанных на JavaScript и HTML, см. в разделе [Печать (приложения для Магазина Windows, использующие JavaScript и HTML)](/previous-versions/windows/apps/hh465225(v=win.10)). Дополнительные сведения о печати из приложений Магазина Windows, написанных на C#, Microsoft Visual Basic или C++ и XAML, см. в разделе [Печать (приложения для Магазина Windows на языке C)](/previous-versions/windows/apps/hh465196(v=win.10)).

> [!Note]  
> Список интерфейсов API печати для настольных приложений, которые также можно использовать в приложениях для Магазина Windows, см. в разделе [Win32 и com для приложений Магазина Windows (печать и документы)](/uwp/win32-and-com/win32-and-com-for-uwp-apps) .

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[API документов XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))
</dt> <dt>

[Двунаправленное взаимодействие с принтерами (центр разработки оборудования)](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>

