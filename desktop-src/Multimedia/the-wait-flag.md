---
title: Флаг ожидания
description: Флаг ожидания
ms.assetid: b971ccd4-0507-4f05-adb3-d4930496034d
keywords:
- Флаг MCI_WAIT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e552650aca9cf104d2c87d7faddd0b6c85b5a6b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068632"
---
# <a name="the-wait-flag"></a><span data-ttu-id="dc4d7-104">Флаг ожидания</span><span class="sxs-lookup"><span data-stu-id="dc4d7-104">The Wait Flag</span></span>

<span data-ttu-id="dc4d7-105">Команды MCI обычно возвращаются пользователю немедленно, даже если выполнение действия, инициированного командой, занимает несколько минут.</span><span class="sxs-lookup"><span data-stu-id="dc4d7-105">MCI commands usually return to the user immediately, even if it takes several minutes to complete the action initiated by the command.</span></span> <span data-ttu-id="dc4d7-106">Можно использовать флаг ожидания (MCI \_ Wait), чтобы направить устройство в ожидание до завершения запрошенного действия перед возвратом управления приложению.</span><span class="sxs-lookup"><span data-stu-id="dc4d7-106">You can use the "wait" (MCI\_WAIT) flag to direct the device to wait until the requested action is completed before returning control to the application.</span></span>

<span data-ttu-id="dc4d7-107">Например, следующая команда [**Play**](play.md) не будет возвращать управление приложению до завершения воспроизведения:</span><span class="sxs-lookup"><span data-stu-id="dc4d7-107">For example, the following [**play**](play.md) command will not return control to the application until the playback completes:</span></span>


```C++
mciSendString("play mydevice from 0 to 100 wait", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



> [!Note]  
> <span data-ttu-id="dc4d7-108">Пользователь может отменить операцию ожидания, нажав клавишу Break.</span><span class="sxs-lookup"><span data-stu-id="dc4d7-108">The user can cancel a wait operation by pressing a break key.</span></span> <span data-ttu-id="dc4d7-109">По умолчанию этот раздел имеет значение CTRL + BREAK.</span><span class="sxs-lookup"><span data-stu-id="dc4d7-109">By default, this key is CTRL+BREAK.</span></span> <span data-ttu-id="dc4d7-110">Приложения могут переопределять этот ключ с помощью команды [**break**](break.md) ([**\_ прерывание MCI**](mci-break.md)).</span><span class="sxs-lookup"><span data-stu-id="dc4d7-110">Applications can redefine this key by using the [**break**](break.md) ([**MCI\_BREAK**](mci-break.md)) command.</span></span> <span data-ttu-id="dc4d7-111">(**В \_ разрыве MCI** используется структура [**MCI \_ break \_ пармс**](mci-break-parms.md) .) Когда операция ожидания отменяется, MCI пытается вернуть управление приложению, не прерывая команду, связанную с флагом "Wait".</span><span class="sxs-lookup"><span data-stu-id="dc4d7-111">(**MCI\_BREAK** uses the [**MCI\_BREAK\_PARMS**](mci-break-parms.md) structure.) When a wait operation is canceled, MCI attempts to return control to the application without interrupting the command associated with the "wait" flag.</span></span>

 

 

 




