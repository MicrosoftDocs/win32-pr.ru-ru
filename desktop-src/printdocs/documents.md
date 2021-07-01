---
description: В этом разделе описываются технологии документов, поддерживаемые Microsoft Windows.
ms.assetid: 14ae2c97-8596-46db-a55c-ef706d2cd00b
title: XPS-документы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 625c2f04a43db9433fe125b52a4bbc08e37fb4f4
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119989"
---
# <a name="xps-documents"></a><span data-ttu-id="52480-103">XPS-документы</span><span class="sxs-lookup"><span data-stu-id="52480-103">XPS Documents</span></span>

<span data-ttu-id="52480-104">В этом разделе описываются технологии документов, поддерживаемые Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="52480-104">This section describes the document technologies that are supported by Microsoft Windows.</span></span>

-   [<span data-ttu-id="52480-105">Выбор технологии документов</span><span class="sxs-lookup"><span data-stu-id="52480-105">Choosing a Document Technology</span></span>](#choosing-a-document-technology)
-   [<span data-ttu-id="52480-106">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="52480-106">In This Section</span></span>](#in-this-section)
-   [<span data-ttu-id="52480-107">Средства документов XPS</span><span class="sxs-lookup"><span data-stu-id="52480-107">XPS Document Tools</span></span>](#xps-document-tools)
-   [<span data-ttu-id="52480-108">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="52480-108">Related topics</span></span>](#related-topics)


## <a name="choosing-a-document-technology"></a><span data-ttu-id="52480-109">Выбор технологии документов</span><span class="sxs-lookup"><span data-stu-id="52480-109">Choosing a Document Technology</span></span>

<span data-ttu-id="52480-110">Корпорация Майкрософт предоставляет несколько различных технологий документов для поддержки различных приложений для работы с документами:</span><span class="sxs-lookup"><span data-stu-id="52480-110">Microsoft provides several different document technologies to support a variety of document applications:</span></span>

-   <span data-ttu-id="52480-111">**XPS и Опенкспс**</span><span class="sxs-lookup"><span data-stu-id="52480-111">**XPS and OpenXPS**</span></span>

    <span data-ttu-id="52480-112">XPS и Опенкспс поддерживаются в Windows 8 и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="52480-112">XPS and OpenXPS are supported in Windows 8 and later versions of Windows.</span></span> <span data-ttu-id="52480-113">Чтобы определить правильный сценарий использования для XPS и Опенкспс, см. предыдущую схему.</span><span class="sxs-lookup"><span data-stu-id="52480-113">See the preceding diagram to determine the correct usage scenario for XPS and OpenXPS.</span></span> <span data-ttu-id="52480-114">Дополнительные сведения об этих технологиях документов см. в [статье Спецификация Open XML Paper (опенкспс)](https://www.ecma-international.org/publications/standards/Ecma-388.htm).</span><span class="sxs-lookup"><span data-stu-id="52480-114">For more information about these document technologies, see [Open XML Paper Specification (OpenXPS)](https://www.ecma-international.org/publications/standards/Ecma-388.htm).</span></span>

    <span data-ttu-id="52480-115">В случае использования Опенкспс с Windows 8 и Windows Server 2012 поддержка предоставляется только через [API документа XPS](documents-xps.md) .</span><span class="sxs-lookup"><span data-stu-id="52480-115">In the case of using OpenXPS with Windows 8 and Windows Server 2012, support is only provided via the [XPS Document API](documents-xps.md)</span></span>

    <span data-ttu-id="52480-116">Если необходимо выполнить преобразование между Microsoft XPS (МСКСПС) и Опенкспс, то корпорация Майкрософт предоставила средство (XPSConverter.exe), которое позволяет преобразовать документы МСКСПС в формат Опенкспс и наоборот.</span><span class="sxs-lookup"><span data-stu-id="52480-116">If you need to convert between Microsoft XPS (MSXPS) and OpenXPS, then Microsoft has provided a tool (XPSConverter.exe) that allows you to convert MSXPS-formatted documents to the OpenXPS format and vice versa.</span></span> <span data-ttu-id="52480-117">Средство входит в комплект Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="52480-117">The tool is part of the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="52480-118">Чтобы скачать WDK, см. статью [как получить WDK](/windows-hardware/drivers/download-the-wdk).</span><span class="sxs-lookup"><span data-stu-id="52480-118">To download the WDK, see [How to get the WDK](/windows-hardware/drivers/download-the-wdk).</span></span>

    <span data-ttu-id="52480-119">Дополнительные сведения о Опенкспс и Windows 8 см. в разделе [Поддержка опенкспс в Windows](/windows-hardware/drivers/print/driver-support-for-openxps).</span><span class="sxs-lookup"><span data-stu-id="52480-119">And for more information about OpenXPS and Windows 8, see [OpenXPS Support in Windows](/windows-hardware/drivers/print/driver-support-for-openxps).</span></span>

-   <span data-ttu-id="52480-120">**API документов XPS**</span><span class="sxs-lookup"><span data-stu-id="52480-120">**XPS Document API**</span></span>

    <span data-ttu-id="52480-121">API документов XPS — это собственный API Windows, поддерживающий OM-модель XPS.</span><span class="sxs-lookup"><span data-stu-id="52480-121">The XPS Document API is a native Windows API that supports the XPS OM.</span></span> <span data-ttu-id="52480-122">API документов XPS появился в Windows 7 и может использоваться в программах пользовательского режима и драйверах принтера XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="52480-122">The XPS Document API was introduced in Windows 7 and can be used in user-mode programs and XPSDrv printer drivers.</span></span>

    <span data-ttu-id="52480-123">Дополнительные сведения см. в статье API документов XPS и [API цифровой подписи XPS](xps-digital-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="52480-123">For more information, see the XPS Document API, and [XPS Digital Signature API](xps-digital-signatures.md).</span></span>

    <span data-ttu-id="52480-124">\*API документов XPS также поддерживается в Windows Vista с пакетом обновления 2 (SP2) с обновлением платформы для Windows Vista и Windows Server 2008 с пакетом обновления 2 (SP2) с помощью обновления платформы для Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="52480-124">\*The XPS Document API is also supported in Windows Vista with Service Pack 2 (SP2) with the Platform Update for Windows Vista and Windows Server 2008 with SP2 using the Platform Update for Windows Server 2008.</span></span> <span data-ttu-id="52480-125">Дополнительные сведения об обновлении платформы для Windows Vista или обновления платформы для Windows Server 2008 см. в [статье обновление платформы для Windows Vista](/windows/desktop/win7ip/platform-update-for-windows-vista-portal) .</span><span class="sxs-lookup"><span data-stu-id="52480-125">For more information about the Platform Update for Windows Vista or the Platform Update for Windows Server 2008, see [Platform Update for Windows Vista](/windows/desktop/win7ip/platform-update-for-windows-vista-portal)</span></span>

-   <span data-ttu-id="52480-126">**.NET Framework**</span><span class="sxs-lookup"><span data-stu-id="52480-126">**.NET Framework**</span></span>

    <span data-ttu-id="52480-127">Платформа .NET Framework обеспечивает поддержку документов XPS для программ, управляемых в пользовательском режиме.</span><span class="sxs-lookup"><span data-stu-id="52480-127">.NET Framework provides XPS document support to user-mode, managed-code programs.</span></span>

    <span data-ttu-id="52480-128">Платформа .NET Framework 3,0 поддерживается в Windows XP с пакетом обновления 2 (SP2) и более поздними версиями клиентских операционных систем Windows, а также на Windows Server 2003 с пакетом обновления 2 (SP2) и более поздних версиях операционных систем Windows Server.</span><span class="sxs-lookup"><span data-stu-id="52480-128">.NET Framework 3.0 is supported on Windows XP with Service Pack 2 (SP2) and later versions of Windows client operating systems, and on Windows Server 2003 with Service Pack 2 (SP2) and later versions of Windows server operating systems.</span></span>

    <span data-ttu-id="52480-129">Платформа .NET Framework 3,5 поддерживается в версиях клиентских операционных систем Windows XP и в Windows Server 2003 и более поздних версиях операционных систем Windows Server.</span><span class="sxs-lookup"><span data-stu-id="52480-129">.NET Framework 3.5 is supported on Windows XP versions of Windows client operating systems, and on Windows Server 2003 and later versions of Windows server operating systems.</span></span>

    > [!Note]  
    > <span data-ttu-id="52480-130">Рекомендуется использовать платформа .NET Framework для создания документов XPS только в клиентских приложениях, а не в серверных приложениях, если приложение не будет периодически завершать работу, как если бы оно было клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="52480-130">We recommend the use of .NET Framework for creating XPS documents in client applications only, not in server applications unless the application exits periodically, as it would if it were a client application.</span></span>

     

    <span data-ttu-id="52480-131">Дополнительные сведения о поддержке документов в платформа .NET Framework см. в разделе [Windows Presentation Foundation документы](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="52480-131">For more information about document support in .NET Framework, see [Windows Presentation Foundation Documents](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).</span></span>

> [!Note]  
> <span data-ttu-id="52480-132">Для работы с XPS-документами в программе Используйте собственный API документа XPS или платформа .NET Framework. одновременное использование обоих в одной программе не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="52480-132">To work with XPS documents in a program, use either the native XPS Document API or the .NET Framework; simultaneous use of both in the same program is not supported.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="52480-133">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="52480-133">In This Section</span></span>

<span data-ttu-id="52480-134">В этом разделе описаны собственные технологии документов Windows, поддерживаемые Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="52480-134">This section describes the native Windows document technologies that are supported by Microsoft Windows.</span></span>



| <span data-ttu-id="52480-135">Технология документов</span><span class="sxs-lookup"><span data-stu-id="52480-135">Document technology</span></span>                                                                   | <span data-ttu-id="52480-136">Описание</span><span class="sxs-lookup"><span data-stu-id="52480-136">Description</span></span>                                                                                                                                                                                                                                |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="52480-137">API документов XPS</span><span class="sxs-lookup"><span data-stu-id="52480-137">XPS Document API</span></span>](documents-xps.md)<br/>                   | <span data-ttu-id="52480-138">Предоставляет надежный формат для электронной бумаги.</span><span class="sxs-lookup"><span data-stu-id="52480-138">Provides a trustworthy format for electronic paper.</span></span><br/> <span data-ttu-id="52480-139">API документа XPS, описанный в этом разделе, предоставляет программам и драйверам печати доступ к содержимому и метаданным документа XPS.</span><span class="sxs-lookup"><span data-stu-id="52480-139">The XPS Document API that is described in this section gives programs and XPSDrv print drivers access to the content and metadata of an XPS document.</span></span><br/> |
| [<span data-ttu-id="52480-140">API цифровой подписи XPS</span><span class="sxs-lookup"><span data-stu-id="52480-140">XPS Digital Signature API</span></span>](xps-digital-signatures.md)<br/> | <span data-ttu-id="52480-141">Включает подписывание документов, проверку удостоверения подписавшего и указывает, изменился ли документ XPS с момента подписания.</span><span class="sxs-lookup"><span data-stu-id="52480-141">Enables document signing, verification of the signer's identity, and indication of whether an XPS document has changed since it was signed.</span></span><br/>                                                                          |
| [<span data-ttu-id="52480-142">Глоссарий XPS-документов</span><span class="sxs-lookup"><span data-stu-id="52480-142">XPS Documents Glossary</span></span>](xpsapi-glossary.md)<br/>           | <span data-ttu-id="52480-143">Определения терминов, используемых [API документов XPS](documents-xps.md) и [API цифровой подписи XPS](xps-digital-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="52480-143">Definitions of terms used by the [XPS Document API](documents-xps.md) and the [XPS Digital Signature API](xps-digital-signatures.md).</span></span><br/>                                                                              |



 

## <a name="xps-document-tools"></a><span data-ttu-id="52480-144">Средства документов XPS</span><span class="sxs-lookup"><span data-stu-id="52480-144">XPS Document Tools</span></span>

<span data-ttu-id="52480-145">Доступны следующие средства для тестирования и устранения неполадок в файлах XPS-документов.</span><span class="sxs-lookup"><span data-stu-id="52480-145">The following tools are available to assist you with testing and troubleshooting of XPS document files.</span></span>

-   <span data-ttu-id="52480-146">[IsXPS](/previous-versions/aa348104(v=vs.110))</span><span class="sxs-lookup"><span data-stu-id="52480-146">[IsXPS](/previous-versions/aa348104(v=vs.110))</span></span>

    <span data-ttu-id="52480-147">Проверяет соответствие файла спецификациям формата XML (XPS) и спецификации Open Packaging Conventions (OPC).</span><span class="sxs-lookup"><span data-stu-id="52480-147">Tests a file's conformity to the XML Paper Specification (XPS) and the Open Packaging Conventions (OPC) Specification.</span></span>

-   [<span data-ttu-id="52480-148">кспсанализер</span><span class="sxs-lookup"><span data-stu-id="52480-148">XpsAnalyzer</span></span>](/windows-hardware/drivers/devtest/xpsanalyzer)

    <span data-ttu-id="52480-149">Средство командной строки, которое анализирует файлы документов XPS на совместимость со спецификацией XPS 1,0.</span><span class="sxs-lookup"><span data-stu-id="52480-149">A command-prompt tool that analyzes XPS document files for compatibility with the XPS 1.0 specification.</span></span>

-   <span data-ttu-id="52480-150">[птконформ](/previous-versions/dd327476(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="52480-150">[PTConform](/previous-versions/dd327476(v=msdn.10))</span></span>

    <span data-ttu-id="52480-151">Средство, проверяющее допустимость документов PrintTicket и PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="52480-151">A tool that checks the validity of PrintTicket and PrintCapabilities documents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52480-152">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="52480-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52480-153">API печати XPS</span><span class="sxs-lookup"><span data-stu-id="52480-153">XPS Print API</span></span>](./printing-with-the-xpsprint-api.md)
</dt> <dt>

[<span data-ttu-id="52480-154">Упаковка</span><span class="sxs-lookup"><span data-stu-id="52480-154">Packaging</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="52480-155">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="52480-155">Printing</span></span>](./printdocs-printing.md)
</dt> <dt>
  
<span data-ttu-id="52480-156">[Пример программы печати](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208))</span><span class="sxs-lookup"><span data-stu-id="52480-156">[Print Sample Program](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208))</span></span>
</dt> </dl>

 

