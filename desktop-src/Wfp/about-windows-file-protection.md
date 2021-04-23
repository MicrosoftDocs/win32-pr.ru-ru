---
description: Защита ресурсов Windows (WRP) предотвращает замену необходимых системных файлов, папок и разделов реестра, которые устанавливаются в составе операционной системы.
ms.assetid: 39069f57-d9f6-4890-ba87-37175184d7a2
title: О защита ресурсов Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c102225a547c4e454c3fb67ac94f715cd3adf8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702898"
---
# <a name="about-windows-resource-protection"></a><span data-ttu-id="442a8-103">О защита ресурсов Windows</span><span class="sxs-lookup"><span data-stu-id="442a8-103">About Windows Resource Protection</span></span>

<span data-ttu-id="442a8-104">Защита ресурсов Windows (WRP) предотвращает замену необходимых системных файлов, папок и разделов реестра, которые устанавливаются в составе операционной системы.</span><span class="sxs-lookup"><span data-stu-id="442a8-104">Windows Resource Protection (WRP) prevents the replacement of essential system files, folders, and registry keys that are installed as part of the operating system.</span></span> <span data-ttu-id="442a8-105">Она стала доступной начиная с Windows Server 2008 и Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="442a8-105">It became available starting with Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="442a8-106">Разрешение на полный доступ для изменения ресурсов, защищенных WRP, ограничено TrustedInstaller.</span><span class="sxs-lookup"><span data-stu-id="442a8-106">Permission for full access to modify WRP-protected resources is restricted to TrustedInstaller.</span></span> <span data-ttu-id="442a8-107">Ресурсы, защищенные WRP, можно изменять только с помощью [поддерживаемых механизмов замены ресурсов](supported-file-replacement-mechanisms.md) в службе установщика модулей Windows.</span><span class="sxs-lookup"><span data-stu-id="442a8-107">WRP-protected resources can only be changed using the [Supported Resource Replacement Mechanisms](supported-file-replacement-mechanisms.md) with the Windows Modules Installer service.</span></span> <span data-ttu-id="442a8-108">Защита этих ресурсов предотвращает сбои приложений и операционных систем.</span><span class="sxs-lookup"><span data-stu-id="442a8-108">Protecting these resources prevents application and operating system failures.</span></span>

<span data-ttu-id="442a8-109">Приложения не должны пытаться изменить ресурсы, защищенные WRP, так как они используются Windows и другими приложениями.</span><span class="sxs-lookup"><span data-stu-id="442a8-109">Applications should not attempt to modify WRP-protected resources because these are used by Windows and other applications.</span></span> <span data-ttu-id="442a8-110">Если приложение пытается изменить ресурс, защищенное WRP, оно может иметь следующие результаты.</span><span class="sxs-lookup"><span data-stu-id="442a8-110">If an application attempts to modify a WRP-protected resource, it can have the following results.</span></span>

-   <span data-ttu-id="442a8-111">Установщики приложений, которые пытаются заменить, изменить или удалить критические файлы Windows или разделы реестра, могут не установить приложение и получить сообщение об ошибке, сообщающее, что доступ к ресурсу запрещен.</span><span class="sxs-lookup"><span data-stu-id="442a8-111">Application installers that attempt to replace, modify, or delete critical Windows files or registry keys may fail to install the application and will receive an error message stating that access to the resource was denied.</span></span>
-   <span data-ttu-id="442a8-112">Приложения, пытающиеся добавить или удалить подразделы или изменить значения защищенных разделов реестра, могут завершиться с ошибкой и получат сообщение об ошибке, сообщающее, что доступ к ресурсу запрещен.</span><span class="sxs-lookup"><span data-stu-id="442a8-112">Applications that attempt to add or remove sub-keys or change the values of protected registry keys may fail and will receive an error message stating that access to the resource was denied.</span></span>
-   <span data-ttu-id="442a8-113">Приложения, использующие запись любых данных в защищенные разделы реестра, папки или файлы, могут завершиться ошибкой.</span><span class="sxs-lookup"><span data-stu-id="442a8-113">Applications that rely on writing any information into protected registry keys, folders, or files may fail.</span></span>

<span data-ttu-id="442a8-114">WRP — это новое имя для защиты файлов Windows (WFP).</span><span class="sxs-lookup"><span data-stu-id="442a8-114">WRP is the new name for Windows File Protection (WFP).</span></span> <span data-ttu-id="442a8-115">WRP защищает разделы и папки реестра, а также ключевые системные файлы.</span><span class="sxs-lookup"><span data-stu-id="442a8-115">WRP protects registry keys and folders as well as essential system files.</span></span> <span data-ttu-id="442a8-116">WFP был доступен в Microsoft Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="442a8-116">WFP was available in Microsoft Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="442a8-117">WRP заменяет WFP в Windows Server 2008 и Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="442a8-117">WRP replaces WFP in Windows Server 2008 and Windows Vista.</span></span>

<span data-ttu-id="442a8-118">В следующих разделах описывается WRP:</span><span class="sxs-lookup"><span data-stu-id="442a8-118">The following topics describe WRP:</span></span>

-   [<span data-ttu-id="442a8-119">Список защищенных ресурсов</span><span class="sxs-lookup"><span data-stu-id="442a8-119">Protected Resource List</span></span>](protected-file-list.md)
-   [<span data-ttu-id="442a8-120">Обнаружение замены ресурсов</span><span class="sxs-lookup"><span data-stu-id="442a8-120">Detecting Resource Replacement</span></span>](detecting-file-replacement.md)
-   [<span data-ttu-id="442a8-121">Поддерживаемые механизмы замены ресурсов</span><span class="sxs-lookup"><span data-stu-id="442a8-121">Supported Resource Replacement Mechanisms</span></span>](supported-file-replacement-mechanisms.md)
-   [<span data-ttu-id="442a8-122">Средство проверки системных файлов</span><span class="sxs-lookup"><span data-stu-id="442a8-122">System File Checker</span></span>](system-file-checker.md)
-   [<span data-ttu-id="442a8-123">Рекомендации по удаленному администрированию</span><span class="sxs-lookup"><span data-stu-id="442a8-123">Remote Administration Considerations</span></span>](remote-administration-considerations.md)

 

 



