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
# <a name="how-to-register-icon-overlay-handlers"></a>Регистрация обработчиков наложения значков

Помимо обычной регистрации компонента COM, для регистрации обработчиков наложения значков необходимо выполнить следующие шаги.

## <a name="instructions"></a>Инструкции

### <a name="step-1-create-a-subkey-named-for-the-handler-under-this-key"></a>Шаг 1. Создание подраздела с именем для обработчика в этом разделе

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ShellIconOverlayIdentifiers
```

### <a name="step-2-set-the-default-value-of-the-subkey-to-the-string-form-of-the-objects-class-identifier-clsidguid"></a>Шаг 2. Задание значения по умолчанию для подраздела в виде строки GUID идентификатора класса (CLSID) объекта

В следующем примере показано, как зарегистрировать обработчик наложения значков с именем Мйоверлай.

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

 

 



