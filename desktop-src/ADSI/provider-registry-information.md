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
# <a name="provider-registry-information"></a><span data-ttu-id="47182-103">Сведения о реестре поставщика</span><span class="sxs-lookup"><span data-stu-id="47182-103">Provider Registry Information</span></span>

<span data-ttu-id="47182-104">Поставщик зарегистрирован в ADSI со следующими ключами и значениями:</span><span class="sxs-lookup"><span data-stu-id="47182-104">The provider is registered with ADSI with the following keys and values:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               provider = <provider namespace>
```

<span data-ttu-id="47182-105">Поставщик зарегистрирован в Windows со следующими ключами и значениями:</span><span class="sxs-lookup"><span data-stu-id="47182-105">The provider is registered with Windows with the following keys and values:</span></span>

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

<span data-ttu-id="47182-106">Пространство имен поставщика регистрируется в Windows со следующими ключами и значениями:</span><span class="sxs-lookup"><span data-stu-id="47182-106">The provider namespace is registered with Windows with the following keys and values:</span></span>

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

<span data-ttu-id="47182-107">В предыдущих абзацах *поставщик* является идентификатором объекта верхнего уровня поставщика.</span><span class="sxs-lookup"><span data-stu-id="47182-107">In the previous paragraphs, the *provider* is the identifier of the provider's top-level object.</span></span> <span data-ttu-id="47182-108">*Пространство имен Provider* — это идентификатор объекта, реализующего пространство имен поставщика.</span><span class="sxs-lookup"><span data-stu-id="47182-108">The *provider namespace* is the identifier of the object which implements the provider's namespace.</span></span>

<span data-ttu-id="47182-109">Конкретный пример см. в разделе [Установка компонента поставщика примера](installing-the-example-provider-component.md).</span><span class="sxs-lookup"><span data-stu-id="47182-109">For a specific example, see [Installing the Example Provider Component](installing-the-example-provider-component.md).</span></span>

 

 




