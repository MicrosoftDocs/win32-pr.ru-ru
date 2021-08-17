---
title: Флаг ожидания
description: Флаг ожидания
ms.assetid: b971ccd4-0507-4f05-adb3-d4930496034d
keywords:
- Флаг MCI_WAIT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 311e1a55e756cfc3c1038f6ab3ccb4b708bb066dde962afff31006dcf39b7c4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801438"
---
# <a name="the-wait-flag"></a>Флаг ожидания

Команды MCI обычно возвращаются пользователю немедленно, даже если выполнение действия, инициированного командой, занимает несколько минут. Можно использовать флаг ожидания (MCI \_ Wait), чтобы направить устройство в ожидание до завершения запрошенного действия перед возвратом управления приложению.

Например, следующая команда [**Play**](play.md) не будет возвращать управление приложению до завершения воспроизведения:


```C++
mciSendString("play mydevice from 0 to 100 wait", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



> [!Note]  
> Пользователь может отменить операцию ожидания, нажав клавишу Break. По умолчанию этот раздел имеет значение CTRL + BREAK. Приложения могут переопределять этот ключ с помощью команды [**break**](break.md) ([**\_ прерывание MCI**](mci-break.md)). (**В \_ разрыве MCI** используется структура [**MCI \_ break \_ пармс**](mci-break-parms.md) .) Когда операция ожидания отменяется, MCI пытается вернуть управление приложению, не прерывая команду, связанную с флагом "Wait".

 

 

 




