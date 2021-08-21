---
title: Скрипты значений с разделителями-запятыми (CSV)
description: Windows 2000 включает программу командной строки CSVDE для импорта объектов каталога с помощью .csv файлов и экспорта объектов каталога в виде .csv файлов.
ms.assetid: fda242eb-7561-444f-b560-94bd87fe4e39
ms.tgt_platform: multiple
keywords:
- Скрипты значений с разделителями-запятыми
- Скрипты, разделенные запятыми значения AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3764593303f7f2a81c524df16665c74afd1c83909e8286511090ee6c84323bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118022450"
---
# <a name="comma-separated-value-csv-scripts"></a>Скрипты значений с разделителями-запятыми (CSV)

Windows 2000 включает программу командной строки CSVDE для импорта объектов каталога с помощью .csv файлов и экспорта объектов каталога в виде .csv файлов. Сценарии CSV создаются для простоты использования. Первая строка скрипта определяет атрибуты в следующих строках. Столбцы разделяются запятыми. формат файла совместим с форматом Microsoft Excel .csv, что позволяет легко создавать файлы. используйте Excel или любое другое средство, которое может считывать и записывать файлы .csv. CSVDE поддерживает Юникод.

## <a name="example-csv-file"></a>Пример CSV-файла

В следующем примере кода представлен CSV-файл, в который добавляется вспомогательный класс.

``` syntax
DN,adminDisplayName,cn,defaultHidingValue,defaultObjectCategory,description,governsID,lDAPDisplayName,mayContain,mustContain,distinguishedName,objectCategory,objectClass,objectClassCategory,possSuperiors,name,rDNAttID,schemaIDGUID,subClassOf,auxiliaryClass,defaultSecurityDescriptor
"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=Fabrikam,DC=com",My-Test-Auxiliary-Class1,My-Test-Auxiliary-Class1,FALSE,"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=Fabrikam,DC=com",Test class used to show how to add an auxiliary class.,1.2.840.113556.1.4.7000.159.24.10.611.11,myTestAuxiliaryClass1,myTestAttributeDNString,description;myTestAttributeUnicodeString,"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=fabrikam,DC=com","CN=Class-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=fabrikam,DC=com",classSchema,3,domainDNS;container,My-Test-Auxiliary-Class1,cn,X'9a6b3176c5dbd2118bd00000f875b660',top,,
```

 

 




