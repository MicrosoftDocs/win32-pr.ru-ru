---
description: Рекомендуемым методом для создания пакета исправлений является использование средства создания исправлений, например Msimsp.exe для вызова Уикреатепатчпаккаже в Patchwiz.dll. Msimsp.exe и PatchWiz.dll предоставляются в пакете SDK для установщик Windows.
ms.assetid: 7fa661aa-d52c-4b08-961f-90ec778f02ff
title: Создание пакета исправлений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ef64ac66cd0201ae99080ec86e32230bc88407b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998809"
---
# <a name="generating-a-patch-package"></a>Создание пакета исправлений

Рекомендуемым методом для создания пакета исправлений является использование средства создания исправлений, например [Msimsp.exe](msimsp-exe.md) для вызова [уикреатепатчпаккаже](uicreatepatchpackage-patchwiz-dll-.md) в [Patchwiz.dll](patchwiz-dll.md). Msimsp.exe и PatchWiz.dll предоставляются в пакете SDK для установщик Windows.

В следующем примере командная строка использует Msimsp.exe и файл PCP, созданный при [создании файла свойств создания исправления](creating-a-patch-creation-properties-file.md) , чтобы создать пример пакета исправлений MNP2000. MSP.

**Msimsp.exe-s C: \\ Примечание \_ установщика \\ Patch \\ MNP2000. PCP-p C: \\ Замечание \_ установщика \\ Patch \\ MNP2000. MSP**

Созданное средство создания исправлений может создать пакет исправлений, вызвав [уикреатепатчпаккаже](uicreatepatchpackage-patchwiz-dll-.md) , как показано ниже.

``` syntax
UiCreatePatchPackage ("C:\\Note_Installer\\Patch\\MNP2000.pcp", "C:\\Note_Installer\\Patch\\MNP2000.msp", NULL, NULL, "", TRUE)
```

[Продолжить](applying-a-patch-package-to-a-local-installation.md)

 

 



