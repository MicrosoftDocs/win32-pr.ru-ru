---
description: Если действие Инсталлвалидате обнаруживает, что установка файла используется, отображает диалоговое окно Филесинусе и записывает в журнал следующие сведения.
ms.assetid: 59237d2c-6dda-4edc-bbaf-39c6b4c221b9
title: Ведение журнала запросов на перезагрузку
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a256f9042dc40633932a36e288ad18d8194f4739
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547002"
---
# <a name="logging-of-reboot-requests"></a><span data-ttu-id="20553-103">Ведение журнала запросов на перезагрузку</span><span class="sxs-lookup"><span data-stu-id="20553-103">Logging of Reboot Requests</span></span>

<span data-ttu-id="20553-104">Если [действие инсталлвалидате](installvalidate-action.md) обнаруживает, что установка файла используется, отображает [диалоговое окно филесинусе](filesinuse-dialog.md) и записывает в журнал следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="20553-104">If the [InstallValidate action](installvalidate-action.md) detects the installation of a file in use it displays the [FilesInUse Dialog](filesinuse-dialog.md) and logs the following information.</span></span>

``` syntax
Info 1603. The file E:\testdb\Test\CustAct1.dll is being held in use
by the following process: Name: test, Id: 137, Window Title: 'Test'.
```

<span data-ttu-id="20553-105">Если установщик обнаруживает, что будет перезаписывать файл, который используется, он записывает в журнал следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="20553-105">If the installer detects that it is about to overwrite a file that is in use, it logs the following information.</span></span>

``` syntax
Info 1603. The file E:\testdb\Test\CustAct2.dll is being held in use.

Info 1903.Scheduling reboot operation: Deleting file [filename]. Must 
reboot to complete operation.
```

<span data-ttu-id="20553-106">\[Токен filename \] может фактически содержать путь к файлу с расширением радиальными базисными функциями.</span><span class="sxs-lookup"><span data-stu-id="20553-106">The \[filename\] token may actually contain a path to a file with an .rbf extension.</span></span> <span data-ttu-id="20553-107">В этом случае файл. радиальными базисными функциями фактически является исходным файлом, регистрируемым сообщением 1603, которое было переименовано в радиальными базисными функциями-файл.</span><span class="sxs-lookup"><span data-stu-id="20553-107">In this case the .rbf file is actually the original file logged by the 1603 message which has been renamed to the .rbf file.</span></span> <span data-ttu-id="20553-108">Файл, который используется, сначала переименовывается с расширением радиальными базисными функциями, а затем удаляется.</span><span class="sxs-lookup"><span data-stu-id="20553-108">The file that's in use is first renamed with an .rbf extension and then deleted.</span></span>

<span data-ttu-id="20553-109">Чтобы получить дополнительные сведения о том, почему установщик пытается перезаписать этот конкретный файл, можно использовать параметр подробного ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="20553-109">To obtain more information about why the installer is attempting to overwrite this particular file, you can use the verbose logging option.</span></span> <span data-ttu-id="20553-110">Используйте \_ значение verbose инсталллогмоде в вызове [**мсиенаблелог**](/windows/desktop/api/Msi/nf-msi-msienableloga) или используйте параметр verbose Output в [параметрах командной строки](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="20553-110">Use the INSTALLLOGMODE\_VERBOSE value in a call to [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) or use the verbose output option of the [Command Line Options](command-line-options.md).</span></span> <span data-ttu-id="20553-111">В этом случае записываются следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="20553-111">This logs the following information.</span></span>

``` syntax
MSI (s) (D0:F0): File: E:\testdb\Test\CustAct2.dll;  Overwrite;  
REINSTALLMODE specifies all files to be overwritten
```

<span data-ttu-id="20553-112">В журнал будет включено сообщение, например "существующий файл имеет более раннюю версию" или "существующий файл поврежден (Недопустимая контрольная сумма)".</span><span class="sxs-lookup"><span data-stu-id="20553-112">The log will include a message such as "Existing file is a lower version" or "Existing file is corrupt (invalid checksum)"</span></span>

 

 



