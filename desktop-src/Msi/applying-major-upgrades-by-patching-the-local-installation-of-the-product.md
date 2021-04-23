---
description: К приложению можно применить значительное обновление путем исправления локальной установки приложения из командной строки или с помощью исполняемого файла.
ms.assetid: be651457-5c66-478b-89d5-3d7607702b8e
title: Применение основных обновлений путем исправления локальной установки продукта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 043d106ed9f8d6455ab4412959b70854a526a4e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909100"
---
# <a name="applying-major-upgrades-by-patching-the-local-installation-of-the-product"></a><span data-ttu-id="f644b-103">Применение основных обновлений путем исправления локальной установки продукта</span><span class="sxs-lookup"><span data-stu-id="f644b-103">Applying Major Upgrades by Patching the Local Installation of the Product</span></span>

<span data-ttu-id="f644b-104">К приложению можно применить значительное обновление путем исправления локальной установки приложения из командной строки или с помощью исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="f644b-104">A major upgrade can be applied to an application by patching the local installation of the application from the command line or by using an executable.</span></span>

> [!Note]  
> <span data-ttu-id="f644b-105">Не рекомендуется предоставлять значительное обновление в качестве пакета исправлений, так как пакет исправлений для обновления не может быть Виртуализирован с другими обновлениями, а так как исправление не является [удаляемым](uninstallable-patches.md).</span><span class="sxs-lookup"><span data-stu-id="f644b-105">Providing a major upgrade as a patch package is not recommended because a major upgrade patch package cannot be sequenced with other updates and because the patch is not an [uninstallable patch](uninstallable-patches.md).</span></span> <span data-ttu-id="f644b-106">Служебную программу [Msimsp.exe](msimsp-exe.md) нельзя использовать для создания пакета исправлений, который применяет значительное обновление.</span><span class="sxs-lookup"><span data-stu-id="f644b-106">The [Msimsp.exe](msimsp-exe.md) utility cannot be used to generate a patch package that applies a major upgrade.</span></span> <span data-ttu-id="f644b-107">Вместо этого примените основные обновления, как описано в разделе [применение основных обновлений путем установки продукта](applying-major-upgrades-by-installing-the-product.md).</span><span class="sxs-lookup"><span data-stu-id="f644b-107">Instead, apply major upgrades as described in [Applying Major Upgrades by Installing the Product](applying-major-upgrades-by-installing-the-product.md).</span></span>

 

<span data-ttu-id="f644b-108">**Установка основного исправления обновления для локальной установки продукта**</span><span class="sxs-lookup"><span data-stu-id="f644b-108">**To apply a major upgrade patch to a local installation of the product**</span></span>

1.  <span data-ttu-id="f644b-109">Запустите установку исправления из командной строки или с помощью исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="f644b-109">Launch the installation of the patch from the command line or by using an executable.</span></span> <span data-ttu-id="f644b-110">Чтобы запустить из командной строки, используйте msiexec/p patch. MSP.</span><span class="sxs-lookup"><span data-stu-id="f644b-110">To launch from the command line, use msiexec /p patch.msp.</span></span> <span data-ttu-id="f644b-111">Чтобы запустить из исполняемого файла, вызовите [**мсиапплипатч**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) или [**метод апплипатч**](installer-applypatch.md) и укажите те же аргументы командной строки.</span><span class="sxs-lookup"><span data-stu-id="f644b-111">To launch from an executable, call [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or the [**ApplyPatch Method**](installer-applypatch.md) and provide the same command line arguments.</span></span>
2.  <span data-ttu-id="f644b-112">При установке обновления клиента установщик игнорирует источник установки и переходит к исправлению файлов, уже установленных на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="f644b-112">When patching a client installation, the installer ignores the installation source and proceeds to patch the files that are already installed on the user's computer.</span></span>
3.  <span data-ttu-id="f644b-113">Установщик изменяет все исправленные компоненты, помеченные как запущенные с исходного кода, на локальный запуск.</span><span class="sxs-lookup"><span data-stu-id="f644b-113">The installer changes any patched components marked as run-from-source to run-locally.</span></span> <span data-ttu-id="f644b-114">Пользователи не могут запускать эти компоненты из источника, пока исправление остается на компьютере.</span><span class="sxs-lookup"><span data-stu-id="f644b-114">Users are unable to run these components from the source as long as the patch remains on the computer.</span></span>
4.  <span data-ttu-id="f644b-115">Установщик добавляет любые преобразования, используемые для обновления MSI-файла, или добавляет сведения о конкретном исправлении в профиль пользователя.</span><span class="sxs-lookup"><span data-stu-id="f644b-115">The installer adds any transforms used to update the .msi file or adds patch-specific information to the user's profile.</span></span>
5.  <span data-ttu-id="f644b-116">Установщик кэширует MSI-файл на компьютере пользователя, чтобы он мог выполнять установку по требованию, переустанавливать и восстанавливать приложение.</span><span class="sxs-lookup"><span data-stu-id="f644b-116">The installer caches the .msi file on the user's computer so that it can perform installation-on-demand, reinstall, and repair of the application.</span></span> <span data-ttu-id="f644b-117">После применения исправления к автономной установке установщик ссылается на два или более исходных списка внешних файлов: один для исходного источника и один для каждого примененного исправления.</span><span class="sxs-lookup"><span data-stu-id="f644b-117">After a patch is applied to a stand alone installation, the installer references two or more source lists to external files: one for the original source and one for each patch that has been applied.</span></span>

 

 



