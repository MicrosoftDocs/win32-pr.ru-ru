---
title: Записи реестра (COM)
ms.assetid: f4f8875c-6416-4919-b49b-bcd675efcbd2
description: 'Дополнительные сведения о: записи реестра (COM)'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368e9eb5e4c2174c5b4b90df6586b58135085c5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142631"
---
# <a name="registry-entries-com"></a><span data-ttu-id="0d236-103">Записи реестра (COM)</span><span class="sxs-lookup"><span data-stu-id="0d236-103">Registry Entries (COM)</span></span>

<span data-ttu-id="0d236-104">Значения реестра в следующих разделах реестра управляют аспектами функциональности COM:</span><span class="sxs-lookup"><span data-stu-id="0d236-104">Registry values in the following registry keys control aspects of the functionality of COM:</span></span>

-   [<span data-ttu-id="0d236-105">**\_ \_ \\ Классы программного обеспечения для локального компьютера hKey \\**</span><span class="sxs-lookup"><span data-stu-id="0d236-105">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes**</span></span>](hkey-local-machine-software-classes.md)
-   [<span data-ttu-id="0d236-106">**HKEY \_ по для локального \_ компьютера, \\ \\ Microsoft \\ OLE**</span><span class="sxs-lookup"><span data-stu-id="0d236-106">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Ole**</span></span>](hkey-local-machine-software-microsoft-ole.md)
-   [<span data-ttu-id="0d236-107">**HKEY \_ локальный \_ компьютер \\ программное обеспечение \\ Microsoft \\ Windows NT \\ CurrentVersion**</span><span class="sxs-lookup"><span data-stu-id="0d236-107">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion**</span></span>](hkey-local-machine-software-microsoft-windows-nt-currentversion.md)

<span data-ttu-id="0d236-108">Начиная с Windows Server 2003, COM использует только маркер текущего процесса, чтобы решить, к какому кусту реестра следует обращаться, а не к маркеру потока.</span><span class="sxs-lookup"><span data-stu-id="0d236-108">As of Windows Server 2003, COM uses only the current process token to decide which registry hive to access, not the thread token.</span></span> <span data-ttu-id="0d236-109">Если COM не удается получить доступ к кусту реестра профиля пользователя, он будет обращаться к кусту **\_ локальной \_ машины \\** в разделе hKey.</span><span class="sxs-lookup"><span data-stu-id="0d236-109">If COM is not able to access the user profile registry hive, it will access the **HKEY\_LOCAL\_MACHINE\\System** hive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d236-110">См. также</span><span class="sxs-lookup"><span data-stu-id="0d236-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d236-111">Реестр</span><span class="sxs-lookup"><span data-stu-id="0d236-111">Registry</span></span>](/windows/desktop/SysInfo/registry)
</dt> </dl>

 

 
