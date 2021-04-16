---
description: Преобразование настройки можно сохранить в хранилище пакета установщик Windows, чтобы гарантировать, что преобразование всегда будет доступно при доступности пакета установки.
ms.assetid: d4c022d2-a8c4-4b4e-8a6c-b14e1bc6effe
title: Внедрение преобразований настройки в качестве подхранилища
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd275d36b37b2e29ae166a2a464a62495d2ca9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650863"
---
# <a name="embedding-customization-transforms-as-substorage"></a><span data-ttu-id="b805b-103">Внедрение преобразований настройки в качестве подхранилища</span><span class="sxs-lookup"><span data-stu-id="b805b-103">Embedding Customization Transforms as Substorage</span></span>

<span data-ttu-id="b805b-104">Преобразование настройки можно сохранить в хранилище пакета установщик Windows, чтобы гарантировать, что преобразование всегда будет доступно при доступности пакета установки.</span><span class="sxs-lookup"><span data-stu-id="b805b-104">You may store the customization transform in a storage of the Windows Installer package to guarantee that the transform is always available when the installation package is available.</span></span> <span data-ttu-id="b805b-105">См. статью [встроенные преобразования](embedded-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="b805b-105">See [Embedded Transforms](embedded-transforms.md).</span></span> <span data-ttu-id="b805b-106">Пример приведен в установщик Windows SDK в качестве служебной WiSubStg.vbs.</span><span class="sxs-lookup"><span data-stu-id="b805b-106">An example of this is provided in the Windows Installer SDK as the utility WiSubStg.vbs.</span></span> <span data-ttu-id="b805b-107">В следующем фрагменте кода, Emb.vbs, также показано использование [таблицы хранилищ](-storages-table.md) для добавления внедренного преобразования и предназначено для использования с сервером сценариев Windows.</span><span class="sxs-lookup"><span data-stu-id="b805b-107">The following snippet, Emb.vbs, also illustrates the use of the [Storages table](-storages-table.md) to add an embedded transform and is for use with Windows Script Host.</span></span>


```VB
'Emb.vbs. Argument(0) is the original database. Argument(1) is the
'    path to the transform file. Argument(2) is the name of the storage.
'
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
 WScript.Echo "Usage is emb.vbs [original database] [transform] [storage name]"
 WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Nothing
Set installer = Wscript.CreateObject("WindowsInstaller.Installer")
 
' Evaluate command-line arguments and set open and update modes
Dim databasePath: databasePath = Wscript.Arguments(0)
Dim importPath  : importPath = Wscript.Arguments(1)
Dim storageName : storageName = Wscript.Arguments(2)
 
' Open database and create a view on the _Storages table
Dim sqlQuery : sqlQuery = "SELECT `Name`,`Data` FROM _Storages"
Dim database : Set database = installer.OpenDatabase(databasePath, 1)
Dim view     : Set view = database.OpenView(sqlQuery)
 
'Create and Insert the row.
Dim record   : Set record = installer.CreateRecord(2)
record.StringData(1) = storageName
view.Execute record
 
'Insert storage - copy data into stream
record.SetStream 2, importPath
view.Modify 3, record
database.Commit
Set view = Nothing
Set database = Nothing
```



<span data-ttu-id="b805b-108">Чтобы добавить хранилище с именем MNPtrans1 в MNP2000.msi и содержащее преобразование, созданное при [добавлении сводных данных к преобразованию настройки](adding-summary-information-to-customization-transform.md), измените каталоги на папку, содержащую Emb.vbs, исходную базу данных и файл преобразования, а затем введите следующую командную строку.</span><span class="sxs-lookup"><span data-stu-id="b805b-108">To add a storage named MNPtrans1 to MNP2000.msi, and containing the transform you created in [Adding Summary Information to Customization Transform](adding-summary-information-to-customization-transform.md), change directories to the folder containing Emb.vbs, the original database, and the transform file, then enter the following command line.</span></span>

<span data-ttu-id="b805b-109">**Cscript.exe Emb.vbs MNP2000.msi Мнптранс. MST MNPtrans1**</span><span class="sxs-lookup"><span data-stu-id="b805b-109">**Cscript.exe Emb.vbs MNP2000.msi MNPtrans.mst MNPtrans1**</span></span>

<span data-ttu-id="b805b-110">Это завершает пример преобразования настройки.</span><span class="sxs-lookup"><span data-stu-id="b805b-110">This completes the customization transform example.</span></span> <span data-ttu-id="b805b-111">После внедрения преобразования в Мнптранс. MST преобразование всегда доступно в пакете установки.</span><span class="sxs-lookup"><span data-stu-id="b805b-111">After embedding the transform in MNPtrans.mst, the transform is always available with the installation package.</span></span> <span data-ttu-id="b805b-112">Файл Мнптранс. MST не должен располагаться в источнике, чтобы применить преобразование.</span><span class="sxs-lookup"><span data-stu-id="b805b-112">The file MNPtrans.mst does not need to be located at the source to apply the transform.</span></span>

<span data-ttu-id="b805b-113">Удалите Мнптранс. MST из папки, содержащей образец установочного пакета.</span><span class="sxs-lookup"><span data-stu-id="b805b-113">Remove MNPtrans.mst from the folder containing the sample installation package.</span></span> <span data-ttu-id="b805b-114">Щелкните значок MNP2000.msi, чтобы запустить установку, или используйте следующую командную строку.</span><span class="sxs-lookup"><span data-stu-id="b805b-114">Click the MNP2000.msi icon to launch an install or use the following command line.</span></span>

<span data-ttu-id="b805b-115">**msiexec/i MNP2000.msi**</span><span class="sxs-lookup"><span data-stu-id="b805b-115">**msiexec /i MNP2000.msi**</span></span>

<span data-ttu-id="b805b-116">Обратите внимание, что при этом устанавливается продукт без настроек.</span><span class="sxs-lookup"><span data-stu-id="b805b-116">Note that this installs the product without the customizations.</span></span> <span data-ttu-id="b805b-117">Чтобы установить с настройками, введите следующую команду в командной строке.</span><span class="sxs-lookup"><span data-stu-id="b805b-117">To install with the customizations, enter the following command line.</span></span> <span data-ttu-id="b805b-118">Используйте двоеточие, чтобы указать, что [**значение свойства**](transforms.md) Transforms ссылается на встроенное преобразование.</span><span class="sxs-lookup"><span data-stu-id="b805b-118">Use a colon to indicate that the value of the [**TRANSFORMS**](transforms.md) Property refers to an embedded transform.</span></span>

<span data-ttu-id="b805b-119">msiexec/i MNP2000.msi преобразования =: MNPtrans1</span><span class="sxs-lookup"><span data-stu-id="b805b-119">msiexec /i MNP2000.msi TRANSFORMS=:MNPtrans1</span></span>

<span data-ttu-id="b805b-120">Обратите внимание, что функция шлюза не отображается в дереве выбора компонентов и компоненты компонента шлюза не установлены, даже если в пользовательском интерфейсе выбран полный тип установки.</span><span class="sxs-lookup"><span data-stu-id="b805b-120">Note that the Gate feature does not appear in the feature selection tree and that the components of the Gate feature are not installed even if a Complete type of installation is selected in the user interface.</span></span>

## <a name="next-example"></a><span data-ttu-id="b805b-121">Следующий пример</span><span class="sxs-lookup"><span data-stu-id="b805b-121">Next example</span></span>

[<span data-ttu-id="b805b-122">Пример небольшого обновления исправлений</span><span class="sxs-lookup"><span data-stu-id="b805b-122">A Small Update Patching Example</span></span>](a-small-update-patching-example.md)

 

 



