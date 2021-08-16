---
title: Сведения о реестре поставщика
description: В этом разделе показано, какие ключи и значения необходимо задать при добавлении поставщика ADSI.
ms.assetid: 87293b63-03ad-4be9-b327-313fdebac611
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 813ad37d77d532e3c9bec91bcc3eda1f0aaf703f09dd3cf1b61ac059d7d7493b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838870"
---
# <a name="provider-registry-information"></a>Сведения о реестре поставщика

Поставщик зарегистрирован в ADSI со следующими ключами и значениями:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               provider = <provider namespace>
```

поставщик регистрируется в Windows со следующими ключами и значениями:

```
HKEY_CLASSES_ROOT
   provider
      Clsid
         (Default) = <provider CLSID>
```

```
HKEY_CLASSES_ROOT
   CLSID
      provider CLSID
         (Default) = <friendly display name>
         InProcServer32
            (Default) = <provider DLL filename>
            ThreadingModel = Both
         ProgID = <provider object name>
         TypeLib = <provider TypeLib CLSID>
         Version = <provider version number>
```

пространство имен поставщика регистрируется в Windows со следующими ключами и значениями:

```
HKEY_CLASSES_ROOT
   provider namespace
      Clsid
         (Default) = <provider namespace CLSID>
```

```
HKEY_CLASSES_ROOT
   CLSID
      provider namespace CLSID
         (Default) = <friendly display name>
         InProcServer32
            (Default) = <provider namespace DLL filename>
            ThreadingModel = Both
         ProgID = <provider namespace object name>
         TypeLib = <provider namespace TypeLib CLSID>
         Version = <provider namespace version number>
```

В предыдущих абзацах *поставщик* является идентификатором объекта верхнего уровня поставщика. *Пространство имен Provider* — это идентификатор объекта, реализующего пространство имен поставщика.

Конкретный пример см. в разделе [Установка компонента поставщика примера](installing-the-example-provider-component.md).

 

 




