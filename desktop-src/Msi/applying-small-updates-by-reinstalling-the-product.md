---
description: Небольшое обновление можно применить к приложению полностью или частично, переустановив приложение из командной строки или из программы.
ms.assetid: 6f8b68da-7748-436d-bc95-96e39cf42143
title: Применение небольших обновлений путем переустановки продукта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27b97ff0274baac5a4ec30df244394a609ed525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998292"
---
# <a name="applying-small-updates-by-reinstalling-the-product"></a><span data-ttu-id="06e64-103">Применение небольших обновлений путем переустановки продукта</span><span class="sxs-lookup"><span data-stu-id="06e64-103">Applying Small Updates by Reinstalling the Product</span></span>

<span data-ttu-id="06e64-104">Небольшое обновление можно применить к приложению полностью или частично, переустановив приложение из командной строки или из программы.</span><span class="sxs-lookup"><span data-stu-id="06e64-104">A small update can be applied to an application by completely or partially reinstalling the application from the command line or from a program.</span></span>

<span data-ttu-id="06e64-105">**Распространение небольшого обновления для текущих пользователей (полная переустановка) из командной строки**</span><span class="sxs-lookup"><span data-stu-id="06e64-105">**To propagate the small update to current users (this is a complete reinstall) from the command line**</span></span>

1.  <span data-ttu-id="06e64-106">В командной строке используйте команду **msiexec/фвомус \[** _path to updated. MSI File_ *_\]_* или **msiexec/i \[** _path to updated. MSI File_ *_\] REINSTALL = ALL REINSTALLMODE = vomus REINSTALL_*.</span><span class="sxs-lookup"><span data-stu-id="06e64-106">From the command line use either: **msiexec /fvomus \[**_path to updated .msi file_*_\]_* or **msiexec /I \[**_path to updated .msi file_*_\] REINSTALL=ALL REINSTALLMODE=vomus_*.</span></span>
2.  <span data-ttu-id="06e64-107">Обновленный MSI-файл кэшируется на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="06e64-107">The updated .msi file is cached on the user's computer.</span></span> <span data-ttu-id="06e64-108">Обратите внимание, что пользователь не может переустановить продукт с помощью компонента "Установка и удаление программ", так как обновленный MSI-файл еще не находится на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="06e64-108">Note that it is not possible for the user to reinstall the product using Add/Remove Programs because the updated .msi file is not yet on the user's computer.</span></span>

<span data-ttu-id="06e64-109">**Распространение небольшого обновления для текущих пользователей (полная переустановка) из программы**</span><span class="sxs-lookup"><span data-stu-id="06e64-109">**To propagate a small update to current users (this is a complete reinstall) from a program**</span></span>

1.  <span data-ttu-id="06e64-110">В программе вызовите [**мсиреинсталлпродукт**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) и укажите пакет REINSTALLMODE \_ , REINSTALLMODE \_ филеолдерверсион, REINSTALLMODE \_ МАЧИНЕДАТА, REINSTALLMODE \_ USERDATA и REINSTALLMODE \_ SHORTCUT.</span><span class="sxs-lookup"><span data-stu-id="06e64-110">From a program, call [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) and specify REINSTALLMODE\_PACKAGE, REINSTALLMODE\_FILEOLDERVERSION, REINSTALLMODE\_MACHINEDATA, REINSTALLMODE\_USERDATA, and REINSTALLMODE\_SHORTCUT</span></span>
2.  <span data-ttu-id="06e64-111">Обновленный MSI-файл кэшируется на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="06e64-111">The updated .msi file is cached on the user's computer.</span></span>

<span data-ttu-id="06e64-112">Следующий метод запускает переустановку только тех компонентов или компонентов, которые затрагиваются небольшим обновлением.</span><span class="sxs-lookup"><span data-stu-id="06e64-112">The following method launches a reinstallation of only those features or components that are affected by the small update.</span></span>

<span data-ttu-id="06e64-113">**Распространение небольшого обновления для текущих пользователей (частичная переустановка)**</span><span class="sxs-lookup"><span data-stu-id="06e64-113">**To propagate a small update to current users (this is a partial reinstall)**</span></span>

1.  <span data-ttu-id="06e64-114">Получите список имен компонентов и компонентов, затрагиваемых небольшим обновлением.</span><span class="sxs-lookup"><span data-stu-id="06e64-114">Obtain a list of the names of features and components that are affected by the small update.</span></span>
2.  <span data-ttu-id="06e64-115">В командной строке используйте: **msiexec/i \[** _путь к обновлению. MSI File_ *_\] REINSTALL \[ =_*_список_компонентов \] List_ **REINSTALLMODE = vomus REINSTALL**.</span><span class="sxs-lookup"><span data-stu-id="06e64-115">From the command prompt use: **msiexec /I \[**_path to updated .msi file_*_\] REINSTALL=\[_*_Feature list\]_ **REINSTALLMODE=vomus**.</span></span>
3.  <span data-ttu-id="06e64-116">Обновленный MSI-файл кэшируется на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="06e64-116">The updated .msi file is cached on the user's computer.</span></span>

 

 



