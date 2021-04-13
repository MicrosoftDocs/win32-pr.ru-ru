---
title: Сведения о реестре поставщика
description: В этом разделе показано, какие ключи и значения необходимо задать при добавлении поставщика ADSI.
ms.assetid: 87293b63-03ad-4be9-b327-313fdebac611
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 790a80964bdcc6111a4c167056a0b85bda23e147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410597"
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

Поставщик зарегистрирован в Windows со следующими ключами и значениями:

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

Пространство имен поставщика регистрируется в Windows со следующими ключами и значениями:

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

 

 




