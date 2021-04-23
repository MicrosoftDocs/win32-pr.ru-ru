---
title: Скрипты значений с разделителями-запятыми (CSV)
description: Windows 2000 включает программу командной строки CSVDE для импорта объектов каталога с помощью CSV-файлов и экспорта объектов каталога в виде CSV-файлов.
ms.assetid: fda242eb-7561-444f-b560-94bd87fe4e39
ms.tgt_platform: multiple
keywords:
- Скрипты значений с разделителями-запятыми
- Скрипты, разделенные запятыми значения AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec737f971bd7e462b8f6f0ef6e9e3df786a207cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772737"
---
# <a name="comma-separated-value-csv-scripts"></a><span data-ttu-id="582fa-105">Скрипты значений с разделителями-запятыми (CSV)</span><span class="sxs-lookup"><span data-stu-id="582fa-105">Comma-separated Value (CSV) Scripts</span></span>

<span data-ttu-id="582fa-106">Windows 2000 включает программу командной строки CSVDE для импорта объектов каталога с помощью CSV-файлов и экспорта объектов каталога в виде CSV-файлов.</span><span class="sxs-lookup"><span data-stu-id="582fa-106">Windows 2000 includes a command-line utility, CSVDE, to import directory objects using .csv files and export directory objects as .csv files.</span></span> <span data-ttu-id="582fa-107">Сценарии CSV создаются для простоты использования.</span><span class="sxs-lookup"><span data-stu-id="582fa-107">CSV scripts are created for ease-of-use.</span></span> <span data-ttu-id="582fa-108">Первая строка скрипта определяет атрибуты в следующих строках.</span><span class="sxs-lookup"><span data-stu-id="582fa-108">The first line in the script identifies the attributes in the lines that follow.</span></span> <span data-ttu-id="582fa-109">Столбцы разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="582fa-109">Columns are separated by commas.</span></span> <span data-ttu-id="582fa-110">Формат файла совместим с форматом Microsoft Excel. csv, что позволяет легко создавать файлы.</span><span class="sxs-lookup"><span data-stu-id="582fa-110">The file format is compatible with the Microsoft Excel .csv format, so that files are easily created.</span></span> <span data-ttu-id="582fa-111">Используйте Excel или любой другой инструмент, который может читать и записывать CSV-файлы.</span><span class="sxs-lookup"><span data-stu-id="582fa-111">Use Excel or any other tool that can read and write .csv files.</span></span> <span data-ttu-id="582fa-112">CSVDE поддерживает Юникод.</span><span class="sxs-lookup"><span data-stu-id="582fa-112">CSVDE supports Unicode.</span></span>

## <a name="example-csv-file"></a><span data-ttu-id="582fa-113">Пример CSV-файла</span><span class="sxs-lookup"><span data-stu-id="582fa-113">Example CSV File</span></span>

<span data-ttu-id="582fa-114">В следующем примере кода представлен CSV-файл, в который добавляется вспомогательный класс.</span><span class="sxs-lookup"><span data-stu-id="582fa-114">The following code example is a CSV file that adds an auxiliary class.</span></span>

``` syntax
DN,adminDisplayName,cn,defaultHidingValue,defaultObjectCategory,description,governsID,lDAPDisplayName,mayContain,mustContain,distinguishedName,objectCategory,objectClass,objectClassCategory,possSuperiors,name,rDNAttID,schemaIDGUID,subClassOf,auxiliaryClass,defaultSecurityDescriptor
"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=Fabrikam,DC=com",My-Test-Auxiliary-Class1,My-Test-Auxiliary-Class1,FALSE,"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=Fabrikam,DC=com",Test class used to show how to add an auxiliary class.,1.2.840.113556.1.4.7000.159.24.10.611.11,myTestAuxiliaryClass1,myTestAttributeDNString,description;myTestAttributeUnicodeString,"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=fabrikam,DC=com","CN=Class-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=fabrikam,DC=com",classSchema,3,domainDNS;container,My-Test-Auxiliary-Class1,cn,X'9a6b3176c5dbd2118bd00000f875b660',top,,
```

 

 




