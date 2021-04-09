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
# <a name="registry-entries-com"></a>Записи реестра (COM)

Значения реестра в следующих разделах реестра управляют аспектами функциональности COM:

-   [**\_ \_ \\ Классы программного обеспечения для локального компьютера hKey \\**](hkey-local-machine-software-classes.md)
-   [**HKEY \_ по для локального \_ компьютера, \\ \\ Microsoft \\ OLE**](hkey-local-machine-software-microsoft-ole.md)
-   [**HKEY \_ локальный \_ компьютер \\ программное обеспечение \\ Microsoft \\ Windows NT \\ CurrentVersion**](hkey-local-machine-software-microsoft-windows-nt-currentversion.md)

Начиная с Windows Server 2003, COM использует только маркер текущего процесса, чтобы решить, к какому кусту реестра следует обращаться, а не к маркеру потока. Если COM не удается получить доступ к кусту реестра профиля пользователя, он будет обращаться к кусту **\_ локальной \_ машины \\** в разделе hKey.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Реестр](/windows/desktop/SysInfo/registry)
</dt> </dl>

 

 
