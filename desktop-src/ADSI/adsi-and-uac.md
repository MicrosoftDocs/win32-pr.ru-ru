---
title: Интерфейсы ADSI и управление учетными записями пользователей
description: В Windows и Windows Server есть контроль учетных записей, который имеет последствия для приложений, использующих интерфейсы Active Directory служб (ADSI).
ms.assetid: 0b286252-8c24-4a18-9dc6-063ca158a8ff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36fc88169a8710228a3bf70283aaccd4b4ac42e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070616"
---
# <a name="adsi-and-user-account-control"></a><span data-ttu-id="af061-103">Интерфейсы ADSI и управление учетными записями пользователей</span><span class="sxs-lookup"><span data-stu-id="af061-103">ADSI and User Account Control</span></span>

<span data-ttu-id="af061-104">В Windows и Windows Server есть [контроль учетных записей](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10)), который имеет последствия для приложений, использующих [интерфейсы Active Directory служб](active-directory-service-interfaces-adsi.md) (ADSI).</span><span class="sxs-lookup"><span data-stu-id="af061-104">Windows and Windows Server have [User Account Control](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10)), which has ramifications for applications that use [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) (ADSI).</span></span> <span data-ttu-id="af061-105">В частности, эти интерфейсы были созданы для запуска с учетной записью пользователя с правами администратора на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="af061-105">Specifically, these interfaces were designed to be run by a user account with administrator privileges on the local computer.</span></span>

<span data-ttu-id="af061-106">**Проблема.**</span><span class="sxs-lookup"><span data-stu-id="af061-106">**Problem**</span></span>

<span data-ttu-id="af061-107">Каждый раз, когда приложение подключается к каталогу и пытается создать объект ADSI, [Active Directoryная схема](/windows/desktop/ADSchema/active-directory-schema) проверяется на наличие изменений.</span><span class="sxs-lookup"><span data-stu-id="af061-107">Every time an application connects to the directory and attempts to create an ADSI object, the [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) is checked for changes.</span></span> <span data-ttu-id="af061-108">Если с момента последнего подключения он изменился, схема загружается и сохраняется в кэше на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="af061-108">If it has changed since the last connection, the schema is downloaded and stored in a cache on the local computer.</span></span> <span data-ttu-id="af061-109">В версиях Windows, предшествовавших Windows Vista, расположением по умолчанию для этого кэша было</span><span class="sxs-lookup"><span data-stu-id="af061-109">In versions of Windows prior to Windows Vista, the default location for this cache was</span></span>

`%systemroot%\SchCache\`

<span data-ttu-id="af061-110">Однако приложения, работающие с учетными записями Standard (то есть без прав администратора), не будут иметь доступа к этому каталогу, поэтому приложения, использующие интерфейсы ADSI, которые выполняются в этом режиме, будут скачивать схему при каждом подключении, что повлияет на пропускную способность и производительность.</span><span class="sxs-lookup"><span data-stu-id="af061-110">However, applications run by standard (that is, non-administrator) accounts will not have access to this directory, and consequently, applications that use ADSI interfaces that are run in this mode will download the schema on every connection, which will impact throughput and performance.</span></span>

<span data-ttu-id="af061-111">**Решения**</span><span class="sxs-lookup"><span data-stu-id="af061-111">**Solutions**</span></span>

<span data-ttu-id="af061-112">*Один пользователь* . для устранения этой проблемы существуют новые ключи управления реестром поставщика ADSI, которые определяют расположения реестра и расположения файлов для кэшированных [Active Directory объектов схемы](/windows/desktop/ADSchema/active-directory-schema) .</span><span class="sxs-lookup"><span data-stu-id="af061-112">*Single user* - To resolve this issue, there are new ADSI Provider registry control keys that determine the registry locations and file locations for cached [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) objects.</span></span> <span data-ttu-id="af061-113">Если раздел реестра</span><span class="sxs-lookup"><span data-stu-id="af061-113">If the registry key</span></span>

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\adsi\Cache\PerMachine`

<span data-ttu-id="af061-114">имеет значение 0 (ноль), каждый пользователь будет иметь другое место хранения для ADSI; разделы реестра будут храниться в</span><span class="sxs-lookup"><span data-stu-id="af061-114">is set to 0 (zero), each user will have a different storage location for ADSI; registry keys will be stored in</span></span>

`HKEY_CURRENT_USER\Software\Microsoft\ADs\Providers\LDAP\`

<span data-ttu-id="af061-115">файлы кэша будут храниться в</span><span class="sxs-lookup"><span data-stu-id="af061-115">and cache files will be stored in</span></span>

`%LOCALAPPDATA%\Microsoft\Windows\SchCache`

<span data-ttu-id="af061-116">Эти параметры являются параметрами по умолчанию на компьютерах под управлением Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="af061-116">These settings are the default settings on computers running Windows Server 2008 or Windows Vista.</span></span>

<span data-ttu-id="af061-117">*Несколько пользователей* . Если приложения ADSI выполняются на компьютере с несколькими учетными записями пользователей (например, на веб-сервере), предпочтительнее не иметь большого количества копий кэша [Active Directory схемы](/windows/desktop/ADSchema/active-directory-schema) , используя большие объемы дискового пространства.</span><span class="sxs-lookup"><span data-stu-id="af061-117">*Multi-user* - If you are running ADSI applications on a computer with many user accounts (for example, a web server), then it's preferable not to have many copies of the [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) cache using up large amounts of disk space.</span></span> <span data-ttu-id="af061-118">Настройка раздела реестра</span><span class="sxs-lookup"><span data-stu-id="af061-118">Setting the registry key</span></span>

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\adsi\Cache\PerMachine`

<span data-ttu-id="af061-119">в 1 (один) вернет ADSI к предыдущему поведению; все объекты [схемы Active Directory](/windows/desktop/ADSchema/active-directory-schema) будут храниться в их предыдущих расположениях. раздел реестра будет находиться в</span><span class="sxs-lookup"><span data-stu-id="af061-119">to 1 (one) will revert ADSI to the previous behavior; all [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) objects will be stored in their previous locations; the registry key will be in</span></span>

`HKEY_LOCAL_MACHINE\Software\Microsoft\ADs\Providers\LDAP`

<span data-ttu-id="af061-120">и файл кэша будет находиться в</span><span class="sxs-lookup"><span data-stu-id="af061-120">and the cache file will be in</span></span>

`%systemroot%\SchCache`

<span data-ttu-id="af061-121">В этом случае учетные записи администратора должны запустить приложение, что приведет к кэшированию файла схемы в глобальном расположении для будущего использования пользователями с меньшими правами.</span><span class="sxs-lookup"><span data-stu-id="af061-121">In this case, administrator accounts should run the application, which will cause the schema file to be cached in the global location for future use by the less privileged users.</span></span>

 

 