---
description: Показано, как убедиться, что приложение отображается в меню открыть с помощью и в диалоговом окне для классических приложений и доступно в качестве приложения Магазина Windows по умолчанию для указанных типов файлов.
ms.assetid: DFCC07A6-BED5-41A8-86DC-130082AE665A
title: Включение приложения в диалоговое окно «Открыть с помощью»
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 218dcbfe6dc34770208c017f0e13cfda7686430c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909540"
---
# <a name="how-to-include-an-application-in-the-open-with-dialog-box"></a>Включение приложения в диалоговое окно «Открыть с помощью»

Показано, как убедиться, что приложение отображается в меню **Открыть с помощью** и в диалоговом окне для классических приложений и доступно в качестве приложения Магазина Windows по умолчанию для указанных типов файлов.

## <a name="instructions"></a>Инструкции

### <a name="for-each-file-type-add-your-application-to-the-openwithprogids-registry-subkey"></a>Для каждого типа файлов добавьте приложение в подраздел реестра Опенвиспрогидс.

Добавьте идентификатор ProgID в качестве имени значения с типом значения REG \_ None или REG \_ SZ и пустой строкой в качестве значения данных.

В следующих примерах реестра показаны записи, связывающие InfoPath и Microsoft Visual Studio с типом XML-файла.

```
HKEY_CLASSES_ROOT
   .xml
      OpenWithProgids
         InfoPath.Document.3 REG_SZ
         VisualStudio.xml.10.0 REG_SZ
```

## <a name="remarks"></a>Примечания

Подключ **опенвиспрогидс** является предпочтительным для **опенвислист** для обнаружения приложения. Дополнительные сведения об этих подразделах см. в разделе [Настройка дополнительных подразделов и атрибутов расширения типов файлов](fa-file-types.md).

**Опенвислист** предназначен только для устаревших приложений (только exe) в операционных системах, предшествующих Windows XP.

```
HKEY_CLASSES_ROOT
   .xml
      OpenWithList
         AlternateProgram1.exe
         AlternateProgram2.exe
```

 

 



