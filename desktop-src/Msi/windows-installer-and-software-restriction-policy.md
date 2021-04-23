---
description: Установщик Windows интегрирована с политикой ограниченного использования программ в Microsoft Windows XP.
ms.assetid: b1e58336-8908-45ee-86f0-81b2314fa77a
title: установщик Windows и политика ограниченного использования программ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b080a1ed9a1396f4ac212e73d1fda6e2719bf40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673972"
---
# <a name="windows-installer-and-software-restriction-policy"></a><span data-ttu-id="208f3-103">установщик Windows и политика ограниченного использования программ</span><span class="sxs-lookup"><span data-stu-id="208f3-103">Windows Installer and Software Restriction Policy</span></span>

<span data-ttu-id="208f3-104">Установщик Windows интегрирована с политикой ограниченного использования программ в Microsoft Windows XP.</span><span class="sxs-lookup"><span data-stu-id="208f3-104">Windows Installer is integrated with Software Restriction Policy in Microsoft Windows XP.</span></span> <span data-ttu-id="208f3-105">Политику ограниченного использования программ можно настроить с помощью групповой политики.</span><span class="sxs-lookup"><span data-stu-id="208f3-105">Software Restriction Policy is configurable through group policy.</span></span> <span data-ttu-id="208f3-106">Политика ограниченного использования программ позволяет администратору ограничить запуск файлов администраторами и администраторами в зависимости от пути, зоны URL-адреса, хэша или критерия издателя.</span><span class="sxs-lookup"><span data-stu-id="208f3-106">Software Restriction Policy allows an administrator to restrict both administrators and nonadministrators from running files based upon the path, URL zone, hash, or publisher criteria.</span></span> <span data-ttu-id="208f3-107">Политика ограниченного использования программ имеет два уровня: неограниченные и запрещенные.</span><span class="sxs-lookup"><span data-stu-id="208f3-107">Software Restriction Policy has two levels: unrestricted and disallowed.</span></span> <span data-ttu-id="208f3-108">Установщик Windows устанавливает только пакеты, разрешенные для запуска на неограниченном уровне.</span><span class="sxs-lookup"><span data-stu-id="208f3-108">The Windows Installer only installs packages allowed to run at the unrestricted level.</span></span>

<span data-ttu-id="208f3-109">Также необходимо разрешить выполнение исправлений или преобразований на неограниченном уровне.</span><span class="sxs-lookup"><span data-stu-id="208f3-109">Patches or transforms must also be allowed to run at the unrestricted level.</span></span> <span data-ttu-id="208f3-110">Если пакет, исправление или преобразование настроены для запуска на уровне, отличном от неограниченного, установщик Windows отображает сообщение об ошибке и регистрирует запись в журнале событий приложений.</span><span class="sxs-lookup"><span data-stu-id="208f3-110">If a package, patch, or transform is configured to run at a level different from unrestricted, the Windows Installer displays an error message and logs an entry in the application event log.</span></span> <span data-ttu-id="208f3-111">Политика ограниченного использования программ оценивается при первом установке приложения, при применении нового исправления и повторном кэшировании пакета установки.</span><span class="sxs-lookup"><span data-stu-id="208f3-111">Software restriction policy is evaluated the first time an application is installed, when a new patch is applied, and when the installation package is re-cached.</span></span>

<span data-ttu-id="208f3-112">Если пакет, исправление или преобразование ограничены, установщик Windows отображает сообщение об ошибке и записывает запись [журнала](event-logging.md) событий в журнал событий приложений.</span><span class="sxs-lookup"><span data-stu-id="208f3-112">If a package, patch, or transform is restricted, the Windows Installer displays an error message and writes an [Event Logging](event-logging.md) entry in the application event log.</span></span> <span data-ttu-id="208f3-113">Политика ограниченного использования программ оценивается при первом установке приложения, при применении нового исправления и повторном кэшировании пакета установки.</span><span class="sxs-lookup"><span data-stu-id="208f3-113">Software restriction policy is evaluated the first time an application is installed, when a new patch is applied, and when the installation package is re-cached.</span></span>

<span data-ttu-id="208f3-114">Дополнительные сведения о политике ограниченного использования программ см. в документации по продукту и [выполните поиск на сайте TechNet](https://www.microsoft.com/technet/sitemap.mspx).</span><span class="sxs-lookup"><span data-stu-id="208f3-114">For more information on software restriction policy, consult the product documentation and [search the TechNet Site](https://www.microsoft.com/technet/sitemap.mspx).</span></span>

 

 



