---
description: Локализованные версии таблицы ошибок и таблицы Актионтекст предоставляются пакетом SDK для установщик Windows. Версии этих таблиц с ошибками и Актионте. для французского языка находятся в папке Intl пакета SDK установщик Windows.
ms.assetid: 8de687c8-c7da-497e-8a90-2404096ad100
title: Импорт локализованных таблиц ошибок и Актионтекст
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15d48a68ca1053a1a1c66899a17802ac337c3ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650970"
---
# <a name="importing-localized-error-and-actiontext-tables"></a><span data-ttu-id="d6f5d-104">Импорт локализованных таблиц ошибок и Актионтекст</span><span class="sxs-lookup"><span data-stu-id="d6f5d-104">Importing Localized Error and ActionText Tables</span></span>

<span data-ttu-id="d6f5d-105">Локализованные версии [таблицы ошибок](error-table.md) и [таблицы актионтекст](actiontext-table.md) предоставляются пакетом SDK для установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="d6f5d-105">Localized language versions of the [Error table](error-table.md) and [ActionText table](actiontext-table.md) are provided by the Windows Installer SDK.</span></span> <span data-ttu-id="d6f5d-106">Версии этих таблиц с ошибками и Актионте. для французского языка находятся в папке Intl пакета SDK установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="d6f5d-106">The French language versions of these tables, Error.FRA and ActionTe.FRA, are located in the Intl folder of the Windows Installer SDK.</span></span>

<span data-ttu-id="d6f5d-107">Вы можете использовать редактор таблиц Orca или служебную программу Msidb.exe, поставляемую с пакетом SDK, для импорта французских версий этих таблиц в базу данных.</span><span class="sxs-lookup"><span data-stu-id="d6f5d-107">You may use the table editor Orca or the utility Msidb.exe provided with the SDK to import the French versions of these tables into the database.</span></span>

<span data-ttu-id="d6f5d-108">Пример использования [**мсидатабасеимпорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) и [**метода Import**](database-import.md) [**объекта базы данных**](database-object.md) предоставляется в пакете SDK установщик Windows в качестве служебной WiImport.vbs.</span><span class="sxs-lookup"><span data-stu-id="d6f5d-108">An example of using [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) and the [**Import Method**](database-import.md) of the [**Database object**](database-object.md) is provided in the Windows Installer SDK as the utility WiImport.vbs.</span></span> <span data-ttu-id="d6f5d-109">В следующем фрагменте кода, Imp.vbs, также иллюстрируется использование метода Import и предназначено для использования с сервером сценариев Windows.</span><span class="sxs-lookup"><span data-stu-id="d6f5d-109">The following snippet, Imp.vbs, also illustrates the use of the Import method and is for use with Windows Script Host.</span></span>


```VB
'Imp.vbs. Argument(0) is the original database. Argument(1) is the
'    path of the folder containing the file to be imported. Argument(2) is the name of the file to be imported.
'
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
    WScript.Echo "Usage is imp.vbs [original database] [folder path] [import file]"
    WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Wscript.CreateObject("WindowsInstaller.Installer")
Dim databasePath : databasePath = Wscript.Arguments(0)
Dim folder : folder = Wscript.Arguments(1)
 
' Open database and process file
Dim database : Set database = installer.OpenDatabase(databasePath, 1)
Dim table : table = Wscript.Arguments(2)
database.Import folder, table 
 
' Commit database changes
database.Commit 'commit changes
Wscript.Quit 0
```



<span data-ttu-id="d6f5d-110">Чтобы импортировать и заменить таблицу ошибок с ошибкой. параметром, можно использовать командную строку, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="d6f5d-110">To import and replace the Error table with Error.FRA you may use a command line such as the following.</span></span>

<span data-ttu-id="d6f5d-111">**Cscript Imp.vbs MNPFren.msi C: \\ Примечание \_ об установщике для \\ французского языка (ошибка).**</span><span class="sxs-lookup"><span data-stu-id="d6f5d-111">**Cscript Imp.vbs MNPFren.msi C:\\Note\_Installer\\French Error.FRA**</span></span>

<span data-ttu-id="d6f5d-112">Чтобы импортировать и заменить таблицу Актионтекст с помощью Актионте., можно использовать командную строку, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="d6f5d-112">To import and replace the ActionText table with ActionTe.FRA you may use a command line such as the following.</span></span>

<span data-ttu-id="d6f5d-113">**Cscript Imp.vbs MNPFren.msi C: \\ Примечание \_ установщик \\ Французская актионте.**</span><span class="sxs-lookup"><span data-stu-id="d6f5d-113">**Cscript Imp.vbs MNPFren.msi C:\\Note\_Installer\\French ActionTe.FRA**</span></span>

<span data-ttu-id="d6f5d-114">Повторно запустите проверку на MNPFren.msi, как описано в разделе [Проверка обновления установки](validating-an-installation-upgrade.md).</span><span class="sxs-lookup"><span data-stu-id="d6f5d-114">Rerun validation on MNPFren.msi as described in [Validating an Installation Upgrade](validating-an-installation-upgrade.md).</span></span>

[<span data-ttu-id="d6f5d-115">Продолжить</span><span class="sxs-lookup"><span data-stu-id="d6f5d-115">Continue</span></span>](localizing-database-columns.md)

 

 



