---
description: Небольшое обновление можно применить к приложению путем исправления локальной установки приложения.
ms.assetid: 2a04ffd0-d5b6-44f3-bef2-73f59179aed1
title: Применение небольших обновлений путем исправления локальной установки продукта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bced3e7f69761ff3e270046718eedb9032cab8a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998293"
---
# <a name="applying-small-updates-by-patching-the-local-installation-of-the-product"></a><span data-ttu-id="f5ce1-103">Применение небольших обновлений путем исправления локальной установки продукта</span><span class="sxs-lookup"><span data-stu-id="f5ce1-103">Applying Small Updates by Patching the Local Installation of the Product</span></span>

<span data-ttu-id="f5ce1-104">Небольшое обновление можно применить к приложению путем исправления локальной установки приложения.</span><span class="sxs-lookup"><span data-stu-id="f5ce1-104">A small update can be applied to an application by patching the local installation of the application.</span></span>

<span data-ttu-id="f5ce1-105">**Установка небольшого исправления обновления для локальной установки продукта**</span><span class="sxs-lookup"><span data-stu-id="f5ce1-105">**To apply a small update patch to a local installation of the product**</span></span>

1.  <span data-ttu-id="f5ce1-106">Запустите установку исправления из командной строки или с помощью исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="f5ce1-106">Launch the installation of the patch from the command line or by using an executable.</span></span> <span data-ttu-id="f5ce1-107">Чтобы запустить из командной строки, используйте **msiexec/p patch. MSP REINSTALL = \[**_список_компонентов List_ *_\] REINSTALLMODE = omus_*.</span><span class="sxs-lookup"><span data-stu-id="f5ce1-107">To launch from the command line, use **msiexec /p patch.msp REINSTALL=\[**_Feature list_*_\] REINSTALLMODE=omus_*.</span></span> <span data-ttu-id="f5ce1-108">Чтобы запустить из исполняемого файла, вызовите [**мсиапплипатч**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) или [**метод апплипатч**](installer-applypatch.md) и укажите те же аргументы командной строки.</span><span class="sxs-lookup"><span data-stu-id="f5ce1-108">To launch from an executable, call [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or the [**ApplyPatch Method**](installer-applypatch.md) and provide the same command line arguments.</span></span>
2.  <span data-ttu-id="f5ce1-109">При установке обновления клиента установщик игнорирует источник установки и переходит к исправлению файлов, уже установленных на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="f5ce1-109">When patching a client installation, the installer ignores the installation source and proceeds to patch the files that are already installed on the user's computer.</span></span>
3.  <span data-ttu-id="f5ce1-110">Установщик изменяет все исправленные компоненты, помеченные как запущенные с исходного кода, на локальный запуск.</span><span class="sxs-lookup"><span data-stu-id="f5ce1-110">The installer changes any patched components marked as run-from-source to run-locally.</span></span> <span data-ttu-id="f5ce1-111">Пользователи не могут запускать эти компоненты из источника, пока исправление остается на компьютере.</span><span class="sxs-lookup"><span data-stu-id="f5ce1-111">Users are unable to run these components from the source as long as the patch remains on the computer.</span></span>
4.  <span data-ttu-id="f5ce1-112">Установщик добавляет любые преобразования, используемые для обновления MSI-файла, или добавляет сведения о конкретном исправлении в профиль пользователя.</span><span class="sxs-lookup"><span data-stu-id="f5ce1-112">The installer adds any transforms used to update the .msi file or adds patch-specific information to the user's profile.</span></span>
5.  <span data-ttu-id="f5ce1-113">Установщик кэширует MSI-файл на компьютере пользователя, чтобы он мог выполнять установку по требованию, переустанавливать и восстанавливать приложение.</span><span class="sxs-lookup"><span data-stu-id="f5ce1-113">The installer caches the .msi file on the user's computer so that it can perform installation-on-demand, reinstall, and repair of the application.</span></span> <span data-ttu-id="f5ce1-114">После применения исправления к автономной установке установщик ссылается на два или более исходных списка внешних файлов: один для исходного источника и один для каждого примененного исправления.</span><span class="sxs-lookup"><span data-stu-id="f5ce1-114">After a patch is applied to a standalone installation, the installer references two or more source lists to external files: one for the original source and one for each patch that has been applied.</span></span>

 

 



