---
description: Замена защищенных ресурсов поддерживается следующими механизмами.
ms.assetid: a757e6cf-59df-4894-a0dc-40174b0aa147
title: Поддерживаемые механизмы замены ресурсов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2aaaa1d9cc8d24d8cd172be71ee40790bf8161a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702896"
---
# <a name="supported-resource-replacement-mechanisms"></a><span data-ttu-id="a3f3d-103">Поддерживаемые механизмы замены ресурсов</span><span class="sxs-lookup"><span data-stu-id="a3f3d-103">Supported Resource Replacement Mechanisms</span></span>

<span data-ttu-id="a3f3d-104">Замена защищенных ресурсов поддерживается следующими механизмами.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-104">Replacement of protected resources is supported through the following mechanisms.</span></span>

<span data-ttu-id="a3f3d-105">Разрешение на полный доступ к изменению ресурсов, защищенных WRP, в Windows Vista и Windows Server 2008 ограничено TrustedInstaller со службой установщика модулей Windows с помощью следующих механизмов:</span><span class="sxs-lookup"><span data-stu-id="a3f3d-105">Permission for full access to modify WRP-protected resources on Windows Vista and Windows Server 2008 is restricted to TrustedInstaller with the Windows Modules Installer service using the following mechanisms:</span></span>

-   <span data-ttu-id="a3f3d-106">Пакеты обновления Windows, устанавливаемые TrustedInstaller.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-106">Windows Service Packs installed by TrustedInstaller.</span></span>
-   <span data-ttu-id="a3f3d-107">Исправления, установленные TrustedInstaller.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-107">Hotfixes installed by TrustedInstaller.</span></span>
-   <span data-ttu-id="a3f3d-108">Обновления операционной системы, установленные TrustedInstaller.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-108">Operating system upgrades installed by TrustedInstaller.</span></span>
-   <span data-ttu-id="a3f3d-109">Центр обновления Windows, установленный TrustedInstaller.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-109">Windows Update installed by TrustedInstaller.</span></span>

<span data-ttu-id="a3f3d-110">Приложения и установщики, пытающиеся заменить ресурс, защищенный WRP, другими способами, кроме указанных методов, получают доступ для изменения ресурса и создания сообщения об ошибке отказа в доступе.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-110">Applications and installers attempting to replace a WRP-protected resource by means other than these specified methods are denied access to change the resource and generate an access denied error message.</span></span>

<span data-ttu-id="a3f3d-111">Для хорошо известных установщиков, пытающихся заменить защищенные WRP ресурсы, сообщения об отказе в доступе и ошибке могут быть подавлены.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-111">For well-known installers attempting to replace WRP-protected resources, the access denied error and error message may be suppressed.</span></span> <span data-ttu-id="a3f3d-112">В этом случае операция возвращается успешно, сообщение об ошибке и ошибке подавляется, но изменения не применяются к ресурсу, защищенному WRP.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-112">In this case, the operation returns successfully, the error and error message are suppressed, but no changes are applied to the WRP-protected resource.</span></span> <span data-ttu-id="a3f3d-113">Ошибка может быть подавлена для хорошо известного установщика только при соблюдении всех следующих условий.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-113">The error may be suppressed for a well-known installer only when all of the following criteria are satisfied:</span></span>

-   <span data-ttu-id="a3f3d-114">Это устаревшее приложение.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-114">This is a legacy application.</span></span> <span data-ttu-id="a3f3d-115">Приложение не включает манифест с requestedExecutionlevel, который идентифицирует приложение, разработанное для Windows Vista или Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-115">The application does not include a manifest with a requestedExecutionlevel that identifies the application as designed for Windows Vista or Windows Server 2008.</span></span>
-   <span data-ttu-id="a3f3d-116">Ошибка отказа в доступе связана только с попыткой изменения ресурса, защищенного WRP.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-116">The access denied error is caused only by the attempt to modify a WRP-protected resource.</span></span>
-   <span data-ttu-id="a3f3d-117">Администратор устанавливает приложение.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-117">An Administrator is installing the application.</span></span>

<span data-ttu-id="a3f3d-118">Сведения об использовании установщик Windows с WRP см. в разделе [использование установщик Windows и защита ресурсов Windows](/windows/desktop/Msi/windows-resource-protection-on-windows-vista) в пакете SDK для [установщик Windows](/windows/desktop/Msi/windows-installer-portal) .</span><span class="sxs-lookup"><span data-stu-id="a3f3d-118">For information about using the Windows Installer with WRP, see [Using Windows Installer and Windows Resource Protection](/windows/desktop/Msi/windows-resource-protection-on-windows-vista) in the [Windows Installer](/windows/desktop/Msi/windows-installer-portal) SDK.</span></span>

<span data-ttu-id="a3f3d-119">**Windows Server 2003 и Windows XP:** Замена системных файлов, защищенных с помощью WFP, поддерживается только с помощью следующих механизмов:</span><span class="sxs-lookup"><span data-stu-id="a3f3d-119">**Windows Server 2003 and Windows XP:** Replacement of WFP-protected system files is supported only through the following mechanisms:</span></span>

-   <span data-ttu-id="a3f3d-120">Установка пакета обновления Windows с помощью Update.exe</span><span class="sxs-lookup"><span data-stu-id="a3f3d-120">Windows Service Pack installation using Update.exe</span></span>
-   <span data-ttu-id="a3f3d-121">Исправления, установленные с помощью Hotfix.exe</span><span class="sxs-lookup"><span data-stu-id="a3f3d-121">Hotfixes installed using Hotfix.exe</span></span>
-   <span data-ttu-id="a3f3d-122">Обновление операционной системы с помощью Winnt32.exe</span><span class="sxs-lookup"><span data-stu-id="a3f3d-122">Operating system upgrades using Winnt32.exe</span></span>
-   <span data-ttu-id="a3f3d-123">Центра обновления Windows;</span><span class="sxs-lookup"><span data-stu-id="a3f3d-123">Windows Update</span></span>

<span data-ttu-id="a3f3d-124">Замена защищенных файлов средствами, отличными от указанных методов, приводит к восстановлению исходных файлов с помощью WFP.</span><span class="sxs-lookup"><span data-stu-id="a3f3d-124">Replacing protected files by means other than these specified methods results in the original files being restored by WFP.</span></span>

 

 
