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
# <a name="how-to-include-an-application-in-the-open-with-dialog-box"></a><span data-ttu-id="eedcd-103">Включение приложения в диалоговое окно «Открыть с помощью»</span><span class="sxs-lookup"><span data-stu-id="eedcd-103">How to Include an Application in the Open With Dialog Box</span></span>

<span data-ttu-id="eedcd-104">Показано, как убедиться, что приложение отображается в меню **Открыть с помощью** и в диалоговом окне для классических приложений и доступно в качестве приложения Магазина Windows по умолчанию для указанных типов файлов.</span><span class="sxs-lookup"><span data-stu-id="eedcd-104">Illustrates how to ensure your application appears in the **Open With** menu and dialog box for desktop apps, and is available as a default Windows Store app for specified file types.</span></span>

## <a name="instructions"></a><span data-ttu-id="eedcd-105">Инструкции</span><span class="sxs-lookup"><span data-stu-id="eedcd-105">Instructions</span></span>

### <a name="for-each-file-type-add-your-application-to-the-openwithprogids-registry-subkey"></a><span data-ttu-id="eedcd-106">Для каждого типа файлов добавьте приложение в подраздел реестра Опенвиспрогидс.</span><span class="sxs-lookup"><span data-stu-id="eedcd-106">For each file type, add your application to the OpenWithProgIds registry subkey.</span></span>

<span data-ttu-id="eedcd-107">Добавьте идентификатор ProgID в качестве имени значения с типом значения REG \_ None или REG \_ SZ и пустой строкой в качестве значения данных.</span><span class="sxs-lookup"><span data-stu-id="eedcd-107">Add your ProgID as a value name, with the value type of either REG\_NONE or REG\_SZ and an empty string as the data value.</span></span>

<span data-ttu-id="eedcd-108">В следующих примерах реестра показаны записи, связывающие InfoPath и Microsoft Visual Studio с типом XML-файла.</span><span class="sxs-lookup"><span data-stu-id="eedcd-108">The following registry examples show entries associating InfoPath and for Microsoft Visual Studio with the XML file type.</span></span>

```
HKEY_CLASSES_ROOT
   .xml
      OpenWithProgids
         InfoPath.Document.3 REG_SZ
         VisualStudio.xml.10.0 REG_SZ
```

## <a name="remarks"></a><span data-ttu-id="eedcd-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="eedcd-109">Remarks</span></span>

<span data-ttu-id="eedcd-110">Подключ **опенвиспрогидс** является предпочтительным для **опенвислист** для обнаружения приложения.</span><span class="sxs-lookup"><span data-stu-id="eedcd-110">The **OpenWithProgids** subkey is preferred to **OpenWithList** to identify an application.</span></span> <span data-ttu-id="eedcd-111">Дополнительные сведения об этих подразделах см. в разделе [Настройка дополнительных подразделов и атрибутов расширения типов файлов](fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="eedcd-111">For more information on these subkeys, see [Setting Optional Subkeys and File Type Extension Attributes](fa-file-types.md).</span></span>

<span data-ttu-id="eedcd-112">**Опенвислист** предназначен только для устаревших приложений (только exe) в операционных системах, предшествующих Windows XP.</span><span class="sxs-lookup"><span data-stu-id="eedcd-112">**OpenWithList** is intended only for legacy apps (must be .exe only) on operating systems prior to Windows XP.</span></span>

```
HKEY_CLASSES_ROOT
   .xml
      OpenWithList
         AlternateProgram1.exe
         AlternateProgram2.exe
```

 

 



