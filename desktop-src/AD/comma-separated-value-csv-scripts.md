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
# <a name="comma-separated-value-csv-scripts"></a>Скрипты значений с разделителями-запятыми (CSV)

Windows 2000 включает программу командной строки CSVDE для импорта объектов каталога с помощью CSV-файлов и экспорта объектов каталога в виде CSV-файлов. Сценарии CSV создаются для простоты использования. Первая строка скрипта определяет атрибуты в следующих строках. Столбцы разделяются запятыми. Формат файла совместим с форматом Microsoft Excel. csv, что позволяет легко создавать файлы. Используйте Excel или любой другой инструмент, который может читать и записывать CSV-файлы. CSVDE поддерживает Юникод.

## <a name="example-csv-file"></a>Пример CSV-файла

В следующем примере кода представлен CSV-файл, в который добавляется вспомогательный класс.

``` syntax
DN,adminDisplayName,cn,defaultHidingValue,defaultObjectCategory,description,governsID,lDAPDisplayName,mayContain,mustContain,distinguishedName,objectCategory,objectClass,objectClassCategory,possSuperiors,name,rDNAttID,schemaIDGUID,subClassOf,auxiliaryClass,defaultSecurityDescriptor
"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=Fabrikam,DC=com",My-Test-Auxiliary-Class1,My-Test-Auxiliary-Class1,FALSE,"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=Fabrikam,DC=com",Test class used to show how to add an auxiliary class.,1.2.840.113556.1.4.7000.159.24.10.611.11,myTestAuxiliaryClass1,myTestAttributeDNString,description;myTestAttributeUnicodeString,"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=fabrikam,DC=com","CN=Class-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=fabrikam,DC=com",classSchema,3,domainDNS;container,My-Test-Auxiliary-Class1,cn,X'9a6b3176c5dbd2118bd00000f875b660',top,,
```

 

 




