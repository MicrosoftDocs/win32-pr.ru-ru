---
description: Помимо обычной регистрации компонента COM, для регистрации обработчиков наложения значков необходимо выполнить следующие шаги.
ms.assetid: 73EE5E69-969B-409E-9E8F-5837720EA0B3
title: Регистрация обработчиков наложения значков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cb58747adc9b754481f43fec825a4588e1606ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997695"
---
# <a name="how-to-register-icon-overlay-handlers"></a><span data-ttu-id="14030-103">Регистрация обработчиков наложения значков</span><span class="sxs-lookup"><span data-stu-id="14030-103">How to Register Icon Overlay Handlers</span></span>

<span data-ttu-id="14030-104">Помимо обычной регистрации компонента COM, для регистрации обработчиков наложения значков необходимо выполнить следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="14030-104">In addition to normal Component Object Model (COM) registration, the following steps must be completed in order to register icon overlay handlers.</span></span>

## <a name="instructions"></a><span data-ttu-id="14030-105">Инструкции</span><span class="sxs-lookup"><span data-stu-id="14030-105">Instructions</span></span>

### <a name="step-1-create-a-subkey-named-for-the-handler-under-this-key"></a><span data-ttu-id="14030-106">Шаг 1. Создание подраздела с именем для обработчика в этом разделе</span><span class="sxs-lookup"><span data-stu-id="14030-106">Step 1: Create a subkey named for the handler under this key</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ShellIconOverlayIdentifiers
```

### <a name="step-2-set-the-default-value-of-the-subkey-to-the-string-form-of-the-objects-class-identifier-clsidguid"></a><span data-ttu-id="14030-107">Шаг 2. Задание значения по умолчанию для подраздела в виде строки GUID идентификатора класса (CLSID) объекта</span><span class="sxs-lookup"><span data-stu-id="14030-107">Step 2: Set the default value of the subkey to the string form of the object's class identifier (CLSID)GUID</span></span>

<span data-ttu-id="14030-108">В следующем примере показано, как зарегистрировать обработчик наложения значков с именем Мйоверлай.</span><span class="sxs-lookup"><span data-stu-id="14030-108">The following example illustrates how to register an icon overlay handler named MyOverlay.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ShellIconOverlayIdentifiers
                     MyOverlay
                        (Default) = {MyOverlay CLSID GUID}
```

 

 



