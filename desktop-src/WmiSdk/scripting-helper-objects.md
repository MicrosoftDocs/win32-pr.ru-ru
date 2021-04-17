---
description: Инструментарий WMI имеет несколько вспомогательных объектов сценариев, которые предоставляют преобразования, необходимые скриптам.
ms.assetid: 832660b7-2992-4d1f-af16-7b8f0477b187
ms.tgt_platform: multiple
title: Вспомогательные объекты сценариев
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 028079e49a2007d99b81f7832c4bce3cb016701d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711663"
---
# <a name="scripting-helper-objects"></a><span data-ttu-id="396bc-103">Вспомогательные объекты сценариев</span><span class="sxs-lookup"><span data-stu-id="396bc-103">Scripting Helper Objects</span></span>

<span data-ttu-id="396bc-104">Инструментарий WMI имеет несколько вспомогательных объектов сценариев, которые предоставляют преобразования, необходимые скриптам.</span><span class="sxs-lookup"><span data-stu-id="396bc-104">WMI has several scripting helper objects that supply the conversions required by scripts.</span></span>

<span data-ttu-id="396bc-105">Вспомогательные объекты сценариев WMI включают:</span><span class="sxs-lookup"><span data-stu-id="396bc-105">WMI scripting helper objects include:</span></span>

-   [<span data-ttu-id="396bc-106">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="396bc-106">**SWbemDateTime**</span></span>](swbemdatetime.md)
-   [<span data-ttu-id="396bc-107">**свбемобжектпас**</span><span class="sxs-lookup"><span data-stu-id="396bc-107">**SWbemObjectPath**</span></span>](swbemobjectpath.md)
-   [<span data-ttu-id="396bc-108">**\_Секуритидескрипторхелпер Win32**</span><span class="sxs-lookup"><span data-stu-id="396bc-108">**Win32\_SecurityDescriptorHelper**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)

<span data-ttu-id="396bc-109">Вспомогательные объекты разбирают структуры составных данных, чтобы скрипт не требовал синтаксического анализа структуры для получения каких-либо частей.</span><span class="sxs-lookup"><span data-stu-id="396bc-109">The helper objects break down composite data structures so that a script is not required to parse the structure to obtain any of the pieces.</span></span> <span data-ttu-id="396bc-110">Например, структура **DateTime WMI** не может быть отображена напрямую и отличается от других структур данных Windows DateTime, например **\_ даты VT**.</span><span class="sxs-lookup"><span data-stu-id="396bc-110">For example, the **WMI DATETIME** structure cannot be displayed directly, and is different from other Windows datetime data structures, such as **VT\_DATE**.</span></span>

## <a name="swbemdatetime"></a><span data-ttu-id="396bc-111">SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="396bc-111">SWbemDateTime</span></span>

<span data-ttu-id="396bc-112">Объект [**SWbemDateTime**](swbemdatetime.md) предоставляет свойства, которые анализируют день, месяц, год, время суток и т. д.</span><span class="sxs-lookup"><span data-stu-id="396bc-112">The [**SWbemDateTime**](swbemdatetime.md) object provides properties that parse out the day, month, year, time of day, and so on.</span></span> <span data-ttu-id="396bc-113">Он также предоставляет методы преобразования для преобразования даты и времени инструментарий управления Windows (WMI) (WMI) в форматы **\_ даты VT** и [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="396bc-113">It also provides conversion methods to convert the Windows Management Instrumentation (WMI) datetime to and from the **VT\_Date** and [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) formats.</span></span> <span data-ttu-id="396bc-114">Для параметров безопасности Internet Explorer (IE) объектом **SWbemDateTime** является единственный объект скрипта WMI, помеченный как безопасный для инициализации и безопасный для создания скриптов.</span><span class="sxs-lookup"><span data-stu-id="396bc-114">For Internet Explorer (IE) security settings, the **SWbemDateTime** object is the only WMI scripting object that is marked safe for initialization and safe for scripting.</span></span> <span data-ttu-id="396bc-115">Дополнительные сведения и примеры преобразований даты и времени см. в разделе [даты и](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx) время, а также в статье на TechNet Скриптцентер [о времени (и о датах)](https://www.microsoft.com/technet/technetmag/issues/2006/07/ScriptingGuy/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="396bc-115">For more information and examples of date and time conversions, see [Dates and Times](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx) and the article on TechNet ScriptCenter [It's About Time (Oh, and About Dates, too)](https://www.microsoft.com/technet/technetmag/issues/2006/07/ScriptingGuy/default.aspx).</span></span>

## <a name="swbemobjectpath"></a><span data-ttu-id="396bc-116">свбемобжектпас</span><span class="sxs-lookup"><span data-stu-id="396bc-116">SWbemObjectPath</span></span>

<span data-ttu-id="396bc-117">Свойства [**свбемобжектпас**](swbemobjectpath.md) предоставляют абсолютный путь к объекту, но также разбивается на части пути WMI, такие как сервер, пространство имен, класс или относительный путь.</span><span class="sxs-lookup"><span data-stu-id="396bc-117">The properties of [**SWbemObjectPath**](swbemobjectpath.md) supply the absolute path of an object, but also break out the parts of the WMI path, such as server, namespace, class, or relative path.</span></span> <span data-ttu-id="396bc-118">Объект позволяет задать параметры безопасности пути, получить значения ключей объектов, представляющих путь, определить, является ли объект одноэлементным и т. д.</span><span class="sxs-lookup"><span data-stu-id="396bc-118">The object allows you to set the security of the path, obtain the key values of the objects representing the path, determine if an object is a singleton, and so on.</span></span> <span data-ttu-id="396bc-119">Дополнительные сведения о работе с путями объектов WMI см. [в разделе Описание расположения объекта WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="396bc-119">For more information about working with WMI object paths, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

## <a name="win32_securitydescriptorhelper"></a><span data-ttu-id="396bc-120">\_Секуритидескрипторхелпер Win32</span><span class="sxs-lookup"><span data-stu-id="396bc-120">Win32\_SecurityDescriptorHelper</span></span>

<span data-ttu-id="396bc-121">Класс [**Win32 \_ секуритидескрипторхелпер**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) преобразует дескриптор безопасности защищаемого объекта из одного формата в другой.</span><span class="sxs-lookup"><span data-stu-id="396bc-121">The [**Win32\_SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) class converts the security descriptor of a securable object from one format to another.</span></span>

<span data-ttu-id="396bc-122">Многие объекты, такие как принтеры, пространства имен WMI, разделы реестра или приложения DCOM, имеют дескрипторы безопасности, управляющие доступом к объекту.</span><span class="sxs-lookup"><span data-stu-id="396bc-122">Many objects, such as printers, WMI namespaces, registry keys, or DCOM applications, have security descriptors that control access to the object.</span></span> <span data-ttu-id="396bc-123">Инструментарий WMI можно использовать для обнаружения или изменения пользователей, имеющих доступ к этим объектам, путем получения или установки дескриптора безопасности, связанного с объектом.</span><span class="sxs-lookup"><span data-stu-id="396bc-123">You can use WMI to discover or change who has access to these objects by getting or setting the security descriptor associated with the object.</span></span>

<span data-ttu-id="396bc-124">Однако различные методы могут получать дескрипторы безопасности в двоичном массиве байтов, формате [языка определения дескрипторов безопасности](/windows/desktop/SecAuthZ/security-descriptor-string-format) (SDDL) или в качестве экземпляра [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="396bc-124">However, different methods may obtain security descriptors in a binary byte array, [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-string-format) (SDDL) format, or as an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="396bc-125">Двоичный массив байтов дескриптора безопасности не должен обрабатываться, за исключением методов C++, предназначенных для [операций с дескрипторами безопасности](/windows/desktop/SecAuthZ/security-descriptor-operations).</span><span class="sxs-lookup"><span data-stu-id="396bc-125">The binary byte array form of a security descriptor should not be manipulated except by the C++ methods designed for [Security Descriptor Operations](/windows/desktop/SecAuthZ/security-descriptor-operations).</span></span> <span data-ttu-id="396bc-126">Дескрипторы в SDDL находятся в строках, но по-прежнему неудобно для работы.</span><span class="sxs-lookup"><span data-stu-id="396bc-126">Descriptors in SDDL are in strings, but are still awkward to manipulate.</span></span> <span data-ttu-id="396bc-127">Простейшим форматом для управления является **Win32 \_ SecurityDescriptor**, поскольку он содержит внедренные объекты для доверенных лиц, ACE и SID.</span><span class="sxs-lookup"><span data-stu-id="396bc-127">The easiest format to manipulate is **Win32\_SecurityDescriptor**, because it contains embedded objects for trustee, ACE, and SID.</span></span> <span data-ttu-id="396bc-128">Дополнительные сведения о структуре дескрипторов безопасности в WMI см. в разделе [объекты дескрипторов безопасности WMI](wmi-security-descriptor-objects.md).</span><span class="sxs-lookup"><span data-stu-id="396bc-128">For more information about the structure of security descriptors in WMI, see [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md).</span></span> <span data-ttu-id="396bc-129">Дополнительные сведения о преобразовании см. [в разделе Изменение параметров безопасности доступа для защищаемых объектов](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="396bc-129">For more information about how to do conversions, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="396bc-130">См. также</span><span class="sxs-lookup"><span data-stu-id="396bc-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="396bc-131">Создание сценариев в WMI</span><span class="sxs-lookup"><span data-stu-id="396bc-131">Scripting in WMI</span></span>](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> </dl>

 

 
