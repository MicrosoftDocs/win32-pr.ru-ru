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
# <a name="printing-documents-and-printing"></a><span data-ttu-id="cee80-103">Печать (документы и печать)</span><span class="sxs-lookup"><span data-stu-id="cee80-103">Printing (Documents and Printing)</span></span>

<span data-ttu-id="cee80-104">Windows предоставляет приложениям полный набор функций, позволяющих выполнять печать на различных устройствах, таких как лазерные принтеры, векторные плоттеры, растровые принтеры и факсимильные компьютеры.</span><span class="sxs-lookup"><span data-stu-id="cee80-104">Windows provides applications with a complete set of functions that allow printing to various devices, such as laser printers, vector plotters, raster printers, and fax machines.</span></span>

## <a name="desktop-app-printing"></a><span data-ttu-id="cee80-105">Настольное приложение для печати</span><span class="sxs-lookup"><span data-stu-id="cee80-105">Desktop App Printing</span></span>

<span data-ttu-id="cee80-106">Программисты Windows могут выбрать несколько различных технологий для печати из их приложений.</span><span class="sxs-lookup"><span data-stu-id="cee80-106">Windows programmers can select from several different technologies to print from their application.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cee80-107">Технология</span><span class="sxs-lookup"><span data-stu-id="cee80-107">Technology</span></span></th>
<th><span data-ttu-id="cee80-108">Описание</span><span class="sxs-lookup"><span data-stu-id="cee80-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cee80-109"><a href="/windows/desktop/printdocs/tailored-app-printing-api">API пакета печати документа</a></span><span class="sxs-lookup"><span data-stu-id="cee80-109"><a href="/windows/desktop/printdocs/tailored-app-printing-api">Print Document Package API</a></span></span><br/></td>
<td><span data-ttu-id="cee80-110">Предоставляет интерфейс, позволяющий приложению получать доступ к пакету печати документа и управлять им.</span><span class="sxs-lookup"><span data-stu-id="cee80-110">Provides an interface that allows an application to access and manage the print document package.</span></span> <span data-ttu-id="cee80-111">Этот API доступен в Windows 8 и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="cee80-111">This API is available with Windows 8 and later versions of Windows.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cee80-112"><a href="print-spooler-api.md">API диспетчера очереди печати</a></span><span class="sxs-lookup"><span data-stu-id="cee80-112"><a href="print-spooler-api.md">Print Spooler API</a></span></span><br/></td>
<td><span data-ttu-id="cee80-113">Предоставляет интерфейс диспетчера очереди печати, чтобы приложения могли управлять принтерами и заданиями печати.</span><span class="sxs-lookup"><span data-stu-id="cee80-113">Provides an interface to the print spooler so that applications can manage printers and print jobs.</span></span><br/> <span data-ttu-id="cee80-114">Приложения используют <a href="print-spooler-api.md">API диспетчера очереди печати</a> для запуска, завершения, управления и настройки заданий печати, управляемых диспетчером очереди печати, независимо от того, используется ли для печати содержимого <a href="/windows/desktop/printdocs/tailored-app-printing-api">API пакета печати</a> или <a href="gdi-printing.md">API печати GDI</a> .</span><span class="sxs-lookup"><span data-stu-id="cee80-114">Applications use the <a href="print-spooler-api.md">Print Spooler API</a> to start, stop, control, and configure print jobs managed by the print spooler whether they use the <a href="/windows/desktop/printdocs/tailored-app-printing-api">Print Document Package API</a> or the <a href="gdi-printing.md">GDI Print API</a> to print the content.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cee80-115"><a href="print-ticket-api.md">API билетов на печать</a></span><span class="sxs-lookup"><span data-stu-id="cee80-115"><a href="print-ticket-api.md">Print Ticket API</a></span></span><br/></td>
<td><span data-ttu-id="cee80-116">Предоставляет приложения с функциями для управления и преобразования билетов на печать.</span><span class="sxs-lookup"><span data-stu-id="cee80-116">Provides applications with functions to manage and convert print tickets.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cee80-117"><a href="gdi-printing.md">API печати GDI</a></span><span class="sxs-lookup"><span data-stu-id="cee80-117"><a href="gdi-printing.md">GDI Print API</a></span></span><br/></td>
<td><span data-ttu-id="cee80-118">Предоставляет приложения с независимым от устройства интерфейсом печати.</span><span class="sxs-lookup"><span data-stu-id="cee80-118">Provides applications with a device-independent printing interface.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cee80-119">Разработчики, пишущие приложения для Windows Vista и более поздних версий Windows, должны использовать <a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">API документов XPS</a> в своих приложениях.</span><span class="sxs-lookup"><span data-stu-id="cee80-119">Developers who are writing applications for Windows Vista and later versions of Windows should consider using the <a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">XPS Document API</a> in their application.</span></span>
</blockquote>
<br/> <span data-ttu-id="cee80-120"><a href="gdi-printing.md">API печати GDI</a> подходит для приложений, которые должны работать в Windows XP и более ранних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="cee80-120">The <a href="gdi-printing.md">GDI Print API</a> is suitable for applications that must run on Windows XP and earlier versions of Windows.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="cee80-121">На следующем рисунке представлено обобщенное представление того, как взаимосвязаны различные API-интерфейсы печати.</span><span class="sxs-lookup"><span data-stu-id="cee80-121">The following illustration provides a high-level view of how the different printing APIs are related.</span></span>

![Схема, показывающая, как собственное приложение Windows может использовать API-интерфейсы печати](images/print-apis.png)

 

<span data-ttu-id="cee80-123">[API пакета печати документов](./tailored-app-printing-api.md)в этом разделе описывают пакет печати документов и интерфейсы предварительного просмотра, которые можно использовать в Windows 8 и более поздних версиях Windows Desktop.</span><span class="sxs-lookup"><span data-stu-id="cee80-123">The [Print Document Package API](./tailored-app-printing-api.md)s in this section describe the print document package and print preview interfaces that you can use with Windows 8 and later versions of Windows desktop.</span></span>

<span data-ttu-id="cee80-124">Дополнительные сведения о печати из приложений Магазина Windows, написанных на JavaScript и HTML, см. в разделе [Печать (приложения для Магазина Windows, использующие JavaScript и HTML)](/previous-versions/windows/apps/hh465225(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="cee80-124">For more info about printing from Windows Store apps that are written in JavaScript and HTML, see [Printing (Windows Store apps using JavaScript and HTML)](/previous-versions/windows/apps/hh465225(v=win.10)).</span></span> <span data-ttu-id="cee80-125">Дополнительные сведения о печати из приложений Магазина Windows, написанных на C#, Microsoft Visual Basic или C++ и XAML, см. в разделе [Печать (приложения для Магазина Windows на языке C)](/previous-versions/windows/apps/hh465196(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="cee80-125">For more info about printing from Windows Store apps that are written in C#, Microsoft Visual Basic, or C++ and XAML, see [Printing (Windows Store apps using C)](/previous-versions/windows/apps/hh465196(v=win.10)).</span></span>

> [!Note]  
> <span data-ttu-id="cee80-126">Список интерфейсов API печати для настольных приложений, которые также можно использовать в приложениях для Магазина Windows, см. в разделе [Win32 и com для приложений Магазина Windows (печать и документы)](/uwp/win32-and-com/win32-and-com-for-uwp-apps) .</span><span class="sxs-lookup"><span data-stu-id="cee80-126">See [Win32 and COM for Windows Store apps (printing and documents)](/uwp/win32-and-com/win32-and-com-for-uwp-apps) for the list of the Desktop App Printing APIs that can also be used in Windows Store apps.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="cee80-127">См. также</span><span class="sxs-lookup"><span data-stu-id="cee80-127">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="cee80-128">[API документов XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cee80-128">[XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="cee80-129">Двунаправленное взаимодействие с принтерами (центр разработки оборудования)</span><span class="sxs-lookup"><span data-stu-id="cee80-129">Bidirectional printer communications (Hardware Dev Center)</span></span>](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>

