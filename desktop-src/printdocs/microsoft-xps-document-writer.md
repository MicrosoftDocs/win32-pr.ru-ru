---
description: Модуль записи XPS-документов (Майкрософт) (МКСДВ) — это драйвер, который позволяет приложению Windows создавать файлы документов XPS в версиях Windows, начиная с Windows XP с пакетом обновления 2 (SP2).
ms.assetid: cb431700-f10f-4c53-9944-d6769895595d
title: Модуль записи XPS-документов (Майкрософт) (МКСДВ)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c355460112167577c2b6867774c402182084d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693597"
---
# <a name="microsoft-xps-document-writer-mxdw"></a><span data-ttu-id="7ca4f-103">Модуль записи XPS-документов (Майкрософт) (МКСДВ)</span><span class="sxs-lookup"><span data-stu-id="7ca4f-103">Microsoft XPS Document Writer (MXDW)</span></span>

<span data-ttu-id="7ca4f-104">Модуль записи XPS-документов (Майкрософт) (МКСДВ) — это драйвер, который позволяет приложению Windows создавать файлы документов XPS в версиях Windows, начиная с Windows XP с пакетом обновления 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="7ca4f-104">The Microsoft XPS Document Writer (MXDW) is a print-to-file driver that enables a Windows application to create XML Paper Specification (XPS) document files on versions of Windows starting with Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="7ca4f-105">Использование МКСДВ позволяет приложению Windows сохранять содержимое как документ XPS, не изменяя программный код приложения.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-105">Using the MXDW makes it possible for a Windows application to save its content as an XPS document without changing any of the application's program code.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="7ca4f-106">Назначение</span><span class="sxs-lookup"><span data-stu-id="7ca4f-106">When to Use</span></span>

<span data-ttu-id="7ca4f-107">Как пользователь, вы выбрали МКСДВ, когда хотите создать документ XPS из приложения Windows, которое не поддерживает сохранение его содержимого в виде XPS-документа.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-107">As a user, you would select the MXDW when you want to create an XPS document from a Windows application that does not have the option to save its content as an XPS document.</span></span>

<span data-ttu-id="7ca4f-108">Разработчикам приложений рекомендуется МКСДВ пользователям, желающим создавать XPS-документы, если приложение не предлагает возможность сохранения в виде документа XPS.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-108">As an application developer, you would recommend the MXDW to users who want to create XPS documents when your application does not offer the option to save as an XPS document.</span></span> <span data-ttu-id="7ca4f-109">Дополнительные сведения о спецификации документа XML и документах XPS см. в [статье Спецификация XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) и [Спецификация XPS и загрузка лицензий](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span><span class="sxs-lookup"><span data-stu-id="7ca4f-109">For more information on the XML Paper Specification and XPS documents, see [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) and [XPS Specification and License Downloads](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span></span>

<span data-ttu-id="7ca4f-110">МКСДВ устанавливается автоматически в Windows Vista и более поздних версиях Windows и может быть загружен и установлен в Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-110">The MXDW is installed automatically on Windows Vista and later versions of Windows and can be downloaded and installed on Windows XP with SP2 and Windows Server 2003.</span></span>

## <a name="installation"></a><span data-ttu-id="7ca4f-111">Установка</span><span class="sxs-lookup"><span data-stu-id="7ca4f-111">Installation</span></span>

<span data-ttu-id="7ca4f-112">В Windows Vista и более поздних версиях Windows МКСДВ устанавливается автоматически при установке операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-112">On Windows Vista and later versions of Windows, the MXDW is installed automatically when the operating system is installed.</span></span>

<span data-ttu-id="7ca4f-113">**Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003**: Скачайте и установите .net Framework 3,0 или необходимый пакет XPS из [центра загрузки Майкрософт](https://www.microsoft.com/downloads/en/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="7ca4f-113">**Windows XP with SP2 and Windows Server 2003**: Download and install either .Net Framework 3.0 or the XPS Essential Pack from the [Microsoft Download Center](https://www.microsoft.com/downloads/en/default.aspx).</span></span>

## <a name="how-to-use"></a><span data-ttu-id="7ca4f-114">Использование</span><span class="sxs-lookup"><span data-stu-id="7ca4f-114">How to Use</span></span>

<span data-ttu-id="7ca4f-115">При установке МКСДВ отображается в виде доступной очереди печати в диалоговом окне Печать, представленном приложением.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-115">When installed, the MXDW appears as an available print queue in the Print dialog box presented by an application.</span></span> <span data-ttu-id="7ca4f-116">Если в качестве принтера выбран МКСДВ, пользователю будет предложено ввести имя файла для создания в качестве документа XPS, записывающего выходные данные для печати приложения.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-116">When the MXDW is selected as the printer, the user is prompted for the file name to create as the XPS Document that captures the print output of the application.</span></span>

<span data-ttu-id="7ca4f-117">На следующем рисунке показан МКСДВ, выбранный в качестве принтера в диалоговом окне Windows Vista Common Print.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-117">The following image shows the MXDW being selected as the printer in the Windows Vista common print dialog box.</span></span>

![Изображение диалогового окна «Печать», в котором отображается выбор средства записи документов XPS (Microsoft) (мксдв)](images/choosingmxdwinvista.gif)

<span data-ttu-id="7ca4f-119">Разработчики приложений могут настраивать выходные данные МКСДВ с помощью [параметров конфигурации мксдв](mxdw-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="7ca4f-119">Application developers can customize the output of MXDW using the [MXDW configuration settings](mxdw-configuration-settings.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ca4f-120">См. также</span><span class="sxs-lookup"><span data-stu-id="7ca4f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ca4f-121">XPS</span><span class="sxs-lookup"><span data-stu-id="7ca4f-121">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[<span data-ttu-id="7ca4f-122">Спецификация XPS и загрузка лицензий</span><span class="sxs-lookup"><span data-stu-id="7ca4f-122">XPS Specification and License Downloads</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

<span data-ttu-id="7ca4f-123">[Средство соответствия isXPS](/previous-versions/dotnet/netframework-3.0/aa348104(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7ca4f-123">[isXPS Conformance Tool](/previous-versions/dotnet/netframework-3.0/aa348104(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7ca4f-124">Параметры конфигурации МКСДВ</span><span class="sxs-lookup"><span data-stu-id="7ca4f-124">MXDW configuration settings</span></span>](mxdw-configuration-settings.md)
</dt> </dl>

 

 
