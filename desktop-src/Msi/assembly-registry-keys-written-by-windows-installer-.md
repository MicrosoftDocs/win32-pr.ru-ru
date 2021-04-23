---
description: Если установщик Windows пакет устанавливает или объявляет сборки, установщик сохраняет сведения об этих сборках в локальном системном реестре.
ms.assetid: 1a6b0530-b5ad-49db-bc08-5b20d32420ef
title: Разделы реестра сборки, записанные установщик Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bdd2ea7d290659fa9c1578d89be9a77dcc5cc10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545183"
---
# <a name="assembly-registry-keys-written-by-windows-installer"></a><span data-ttu-id="4bc42-103">Разделы реестра сборки, записанные установщик Windows</span><span class="sxs-lookup"><span data-stu-id="4bc42-103">Assembly Registry Keys Written by Windows Installer</span></span>

<span data-ttu-id="4bc42-104">Если установщик Windows пакет устанавливает или объявляет сборки, установщик сохраняет сведения об этих сборках в локальном системном реестре.</span><span class="sxs-lookup"><span data-stu-id="4bc42-104">If a Windows Installer package installs or advertises assemblies, the installer stores information about those assemblies in the local system registry.</span></span> <span data-ttu-id="4bc42-105">Обратите внимание, что эти разделы реестра предназначены только для внутреннего использования установщик Windows и не должны полагаться на них в приложении.</span><span class="sxs-lookup"><span data-stu-id="4bc42-105">Please note that these registry keys are only intended to be used internally by Windows Installer and they should not be relied upon by your application.</span></span> <span data-ttu-id="4bc42-106">Содержимое, расположение и структура сведений, хранящихся в этих ключах, могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="4bc42-106">The content, location, and structure of information stored in these keys is subject to change.</span></span> <span data-ttu-id="4bc42-107">Для управления сборками приложения должны использовать [**мсипровидеассембли**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) .</span><span class="sxs-lookup"><span data-stu-id="4bc42-107">Applications should rely upon [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) to manage assemblies.</span></span>

<span data-ttu-id="4bc42-108">Сборки регистрируются по именам сборок.</span><span class="sxs-lookup"><span data-stu-id="4bc42-108">Assemblies are registered by their assembly names.</span></span> <span data-ttu-id="4bc42-109">Имена значений, хранящихся в следующих расположениях, являются именами сборок.</span><span class="sxs-lookup"><span data-stu-id="4bc42-109">The names of the values stored in the following locations are the assembly names.</span></span> <span data-ttu-id="4bc42-110">Фактические значения имеют тип REG \_ Multi \_ SZ и содержат данные, используемые [**мсипровидеассембли**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) для установки или восстановления сборок.</span><span class="sxs-lookup"><span data-stu-id="4bc42-110">The actual values are of the type REG\_MULTI\_SZ and contain data used by [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) to install or repair assemblies.</span></span>

## <a name="information-about-private-assemblies"></a><span data-ttu-id="4bc42-111">Сведения о закрытых сборках</span><span class="sxs-lookup"><span data-stu-id="4bc42-111">Information About Private Assemblies</span></span>

<span data-ttu-id="4bc42-112">Установщик Windows хранит сведения о частных сборках, выполненных установщик Windows пакетах, которые были установлены в качестве управляемых приложений для каждого пользователя в следующем разделе реестра:</span><span class="sxs-lookup"><span data-stu-id="4bc42-112">Windows Installer stores information about private assemblies carried by Windows Installer packages that have been installed as managed per-user applications under the following registry key:</span></span>

<span data-ttu-id="4bc42-113">**HKLM** \\ **Программное обеспечение** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Установщик** \\ **Управляемые** \\ **_Идентификатор безопасности пользователя_ *_\\_*** \\ Путь **сборок** установщика к \\ \* *_файлу конфигурации_* _</span><span class="sxs-lookup"><span data-stu-id="4bc42-113">**HKLM**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Installer**\\**Managed**\\**_User SID_*_\\_\* Installer**\\**Assemblies**\\**_path to config file_* _</span></span>

<span data-ttu-id="4bc42-114">Установщик Windows хранит сведения о частных сборках, выполненных установщик Windows пакетах, установленных для каждого пользователя в следующем разделе реестра:</span><span class="sxs-lookup"><span data-stu-id="4bc42-114">Windows Installer stores information about private assemblies carried by Windows Installer packages that have been installed per-user under the following registry key:</span></span>

<span data-ttu-id="4bc42-115">_*HKCU **\\** программное обеспечение **\\** **\\** путь сборок установщика Microsoft к **\\** **\\** _файлу конфигурации_*_</span><span class="sxs-lookup"><span data-stu-id="4bc42-115">_*HKCU **\\** Software **\\** Microsoft **\\** Installer **\\** Assemblies **\\**_path to config file_*_</span></span>

<span data-ttu-id="4bc42-116">Установщик Windows сохраняет сведения о частных сборках, выполненных установщик Windowsными пакетами и установленными для каждого компьютера, в следующем разделе реестра:</span><span class="sxs-lookup"><span data-stu-id="4bc42-116">Windows Installer stores information about private assemblies carried by Windows Installer packages and installed per-machine under the following registry key:</span></span>

<span data-ttu-id="4bc42-117">_***\\** Классы программного обеспечения HKLM **\\** **\\** **\\** сборки установщик **\\** _путь к файлу конфигурации_*_</span><span class="sxs-lookup"><span data-stu-id="4bc42-117">_*HKLM **\\** SOFTWARE **\\** Classes **\\** Installer **\\** Assemblies **\\**_path to config file_*_</span></span>

## <a name="information-about-global-or-shared-assemblies"></a><span data-ttu-id="4bc42-118">Сведения о глобальных или общих сборках</span><span class="sxs-lookup"><span data-stu-id="4bc42-118">Information About Global or Shared Assemblies</span></span>

<span data-ttu-id="4bc42-119">Установщик Windows хранит сведения об общих сборках, выполненных установщик Windows пакетах, которые были установлены в качестве управляемых приложений для каждого пользователя в следующем разделе реестра:</span><span class="sxs-lookup"><span data-stu-id="4bc42-119">Windows Installer stores information about shared assemblies carried by Windows Installer packages that have been installed as managed per-user applications under the following registry key:</span></span>

<span data-ttu-id="4bc42-120">_*HKLM **\\** Программное обеспечение **\\** **\\** **\\** **\\** управляемый установщиком Microsoft Windows CurrentVersion Installer **\\** **\\** _ИД безопасности_*_ для \\ ***\\** сборок **\\** установщика*\*</span><span class="sxs-lookup"><span data-stu-id="4bc42-120">_*HKLM **\\** SOFTWARE **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Installer **\\** Managed **\\**_User SID_*_\\_ *Installer **\\** Assemblies **\\** Global*\*</span></span>

<span data-ttu-id="4bc42-121">Установщик Windows хранит сведения об общих сборках, выполненных установщик Windowsными пакетами, установленными для каждого пользователя в следующем разделе реестра:</span><span class="sxs-lookup"><span data-stu-id="4bc42-121">Windows Installer stores information about shared assemblies carried by Windows Installer packages that have been installed per-user under the following registry key:</span></span>

<span data-ttu-id="4bc42-122">**HKCU** \\ **Программное обеспечение** \\ **Microsoft** \\ **Установщик** \\ **Сборки** \\ **Глобальный шаблон**</span><span class="sxs-lookup"><span data-stu-id="4bc42-122">**HKCU**\\**Software**\\**Microsoft**\\**Installer**\\**Assemblies**\\**Global**</span></span>

<span data-ttu-id="4bc42-123">Установщик Windows хранит сведения об общих сборках, выполненных установщик Windowsными пакетами и установленными для каждого компьютера, в следующем разделе реестра:</span><span class="sxs-lookup"><span data-stu-id="4bc42-123">Windows Installer stores information about shared assemblies carried by Windows Installer packages and installed per-machine under the following registry key:</span></span>

<span data-ttu-id="4bc42-124">**HKLM** \\ **Программное обеспечение** \\ **Классы** \\ **Установщик** \\ **Сборки** \\ **Глобальный шаблон**</span><span class="sxs-lookup"><span data-stu-id="4bc42-124">**HKLM**\\**SOFTWARE**\\**Classes**\\**Installer**\\**Assemblies**\\**Global**</span></span>

 

 



