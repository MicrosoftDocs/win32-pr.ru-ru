---
description: Рекомендуемым методом для создания пакета исправлений является использование средства создания исправлений, например Msimsp.exe для вызова Уикреатепатчпаккаже в Patchwiz.dll. Msimsp.exe и PatchWiz.dll предоставляются в пакете SDK для установщик Windows.
ms.assetid: 7fa661aa-d52c-4b08-961f-90ec778f02ff
title: Создание пакета исправлений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0577c678bbb378da425ff438a0e165dcba95d6e1fc1eecc1d9c311fe2c78bca2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581434"
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

 

 



