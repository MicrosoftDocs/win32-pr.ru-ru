---
title: Установка компонента примера поставщика
description: После установки пакета SDK для ADSI из каталога установки перейдите к каталогу Samples \\ нетдс \\ ADSI \\ Samples \\ provider \\ Setup. Запустите Install.bat, как описано в файле README.TXT.
ms.assetid: 7bf4bf22-38ac-4b0d-946e-5f60c7693707
ms.tgt_platform: multiple
keywords:
- Установка примера поставщика компонентов ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92e58fb471385b862982904e69a432bec1a94e3b9aff0248fdacd9f5e9c7a3e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119333244"
---
# <a name="installing-the-example-provider-component"></a>Установка компонента примера поставщика

После установки пакета SDK для ADSI из каталога установки перейдите к каталогу Samples \\ нетдс \\ ADSI \\ Samples \\ provider \\ Setup. Запустите Install.bat, как описано в файле README.TXT.

Пример поставщика ADSI добавляет следующие подразделы и значения в реестр при запуске Install.batного файла:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               Sample = SampleNamespace
```

```
HKEY_CLASSES_ROOT
   SampleNamespace
      Clsid = {F46430D0-CBfB-11CE-A9F7-00AA00B67689}
```

```
HKEY_CLASSES_ROOT
   Sample
      Clsid = {F46430D1-CBfB-11CE-A9F7-00AA00B67689}
```

```
HKEY_CLASSES_ROOT
   CLSID
      {F46430D0-CBfB-11CE-A9F7-00AA00B67689}
         (Default) = Sample Namespace Object
         InprocServer32
            (Default) = adssmp.dll
            ThreadingModel = Both
         ProgID
            (Default) = SampleNamespace
         TypeLib
            (Default) = {F46430D2-CBfB-11CE-A9F7-00AA00B67689}
         Version
            (Default) = 0.0
```

```
HKEY_CLASSES_ROOT
   CLSID
      {F46430D1-CBfB-11CE-A9F7-00AA00B67689}
         (Default) = Sample Provider Object
         InprocServer32
            (Default) = adssmp.dll
            ThreadingModel = Both
         ProgID
            (Default) = Sample
         TypeLib
            (Default) = {F46430D2-CBfB-11CE-A9F7-00AA00B67689}
         Version
            (Default) = 0.0
```

Другие записи реестра для примера компонента поставщика существуют, так как в примере компонента поставщика реализована иерархия каталогов в реестре. Это не означает, что другим поставщикам нужно будет сделать то же самое.

 

 




