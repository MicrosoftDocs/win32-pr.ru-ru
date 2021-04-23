---
description: Чтобы применить преобразование настройки во время установки продукта, необходимо добавить информационный поток сводки в файл преобразования Мнптранс. MST, созданный при формировании преобразования настройки.
ms.assetid: 586f6c43-7449-4d06-9201-9b4b4919871e
title: Добавление сводных данных в преобразование настройки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64957fcf8f29ab8793517015c7018292ba9a6e69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650738"
---
# <a name="adding-summary-information-to-customization-transform"></a><span data-ttu-id="c84f0-103">Добавление сводных данных в преобразование настройки</span><span class="sxs-lookup"><span data-stu-id="c84f0-103">Adding Summary Information to Customization Transform</span></span>

<span data-ttu-id="c84f0-104">Чтобы применить преобразование настройки во время установки продукта, необходимо добавить [информационный поток сводки](summary-information-stream.md) в файл преобразования мнптранс. MST, созданный при [формировании преобразования настройки](generating-a-customization-transform.md).</span><span class="sxs-lookup"><span data-stu-id="c84f0-104">To apply the customization transform during an installation of the product, you must add a [Summary Information Stream](summary-information-stream.md) to the transform file MNPtrans.mst generated in [Generating a Customization Transform](generating-a-customization-transform.md).</span></span>

<span data-ttu-id="c84f0-105">Вы можете создать сводные данные для преобразования с помощью [**мсикреатетрансформсуммаринфо**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) или [**метода креатетрансформсуммаринфо**](database-createtransformsummaryinfo.md).</span><span class="sxs-lookup"><span data-stu-id="c84f0-105">You may generate summary information for a transform using [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) or the [**CreateTransformSummaryInfo Method**](database-createtransformsummaryinfo.md).</span></span> <span data-ttu-id="c84f0-106">Следующий фрагмент кода, Sum.vbs, иллюстрирует [**метод креатетрансформсуммаринфо**](database-createtransformsummaryinfo.md) и предназначен для использования с сервером сценариев Windows.</span><span class="sxs-lookup"><span data-stu-id="c84f0-106">The following snippet, Sum.vbs, illustrates the [**CreateTransformSummaryInfo Method**](database-createtransformsummaryinfo.md) and is for use with Windows Script Host.</span></span> <span data-ttu-id="c84f0-107">Обратите внимание, что этот пример не выполняет проверку и подавляет состояние ошибки.</span><span class="sxs-lookup"><span data-stu-id="c84f0-107">Note that this example performs no validation and suppresses no error conditions.</span></span>


```VB
'Sum.vbs. Argument(0) is the original database. Argument(1) is the
'    customized database. Argument(2) is the transform file.
 
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
    WScript.Echo "Usage is sum.vbs [original database] [customized database] [transform]"
    WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Nothing
Set installer = Wscript.CreateObject("WindowsInstaller.Installer") 
 
' Open databases and transform 
Dim database1 : Set database1 =
    installer.OpenDatabase(Wscript.Arguments(0), 0) 
Dim database2 : Set database2 =
    installer.OpenDatabase(Wscript.Arguments(1), 0) 
Dim transform : transform = Wscript.Arguments(2)
 
' Create and add Summary Information
Dim transinfo : transinfo =
    Database2.CreateTransformSummaryInfo(Database1, transform,0,0)
```



<span data-ttu-id="c84f0-108">Чтобы создать и добавить сводные данные в файл преобразования Мнптранс. MST, созданный при [формировании преобразования настройки](generating-a-customization-transform.md), измените каталоги на папку, содержащую Gen.vbs, исходную базу данных, обновленную базу данных и преобразование, а затем введите следующую командную строку.</span><span class="sxs-lookup"><span data-stu-id="c84f0-108">To create and add summary information to the transform file MNPtrans.mst you created in [Generating a Customization Transform](generating-a-customization-transform.md), change directories to the folder containing Gen.vbs, the original database, the updated database, and the transform, and enter the following command line.</span></span>

<span data-ttu-id="c84f0-109">**Cscript.exe Sum.vbs MNP2000.msi MNP2000t.msi Мнптранс. MST**</span><span class="sxs-lookup"><span data-stu-id="c84f0-109">**Cscript.exe Sum.vbs MNP2000.msi MNP2000t.msi MNPtrans.mst**</span></span>

<span data-ttu-id="c84f0-110">Щелкните значок MNP2000.msi, чтобы запустить установку, или используйте следующую командную строку.</span><span class="sxs-lookup"><span data-stu-id="c84f0-110">Click the MNP2000.msi icon to launch an install or use the following command line.</span></span>

<span data-ttu-id="c84f0-111">**msiexec/i MNP2000.msi**</span><span class="sxs-lookup"><span data-stu-id="c84f0-111">**msiexec /i MNP2000.msi**</span></span>

<span data-ttu-id="c84f0-112">При этом продукт устанавливается без настроек.</span><span class="sxs-lookup"><span data-stu-id="c84f0-112">This installs the product without the customizations.</span></span> <span data-ttu-id="c84f0-113">Чтобы установить с настройками, введите следующую командную строку.</span><span class="sxs-lookup"><span data-stu-id="c84f0-113">To install with the customization, enter the following command line.</span></span> <span data-ttu-id="c84f0-114">Обратите внимание, что значение [**Свойства**](transforms.md) Transforms ссылается на файл преобразования, расположенный в источнике.</span><span class="sxs-lookup"><span data-stu-id="c84f0-114">Note that the value of the [**TRANSFORMS**](transforms.md) Property refers to transform file located at the source.</span></span>

<span data-ttu-id="c84f0-115">**msiexec/i MNP2000.msi преобразования = Мнптранс. MST**</span><span class="sxs-lookup"><span data-stu-id="c84f0-115">**msiexec /i MNP2000.msi TRANSFORMS=MNPtrans.mst**</span></span>

<span data-ttu-id="c84f0-116">Функция шлюза не отображается в дереве выбора компонентов, а компоненты компонента шлюза не устанавливаются, даже если в пользовательском интерфейсе выбран полный тип установки.</span><span class="sxs-lookup"><span data-stu-id="c84f0-116">The Gate feature does not appear in the feature selection tree and the components of the Gate feature are not installed even if a Complete type of installation is selected in the user interface.</span></span>

[<span data-ttu-id="c84f0-117">Продолжить</span><span class="sxs-lookup"><span data-stu-id="c84f0-117">Continue</span></span>](embedding-customization-transforms-as-substorage.md)

 

 



