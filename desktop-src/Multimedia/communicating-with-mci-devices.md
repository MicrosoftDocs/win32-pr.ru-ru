---
title: Взаимодействие с устройствами MCI
description: Взаимодействие с устройствами MCI
ms.assetid: 2408f8e4-d040-40f5-a880-1ecb8025656c
keywords:
- Макрос МЦивндсендстринг
- Функция mciSendString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7f5458cff0ef4c5c5f84e565fae06ade8796c4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105650324"
---
# <a name="communicating-with-mci-devices"></a><span data-ttu-id="4c429-105">Взаимодействие с устройствами MCI</span><span class="sxs-lookup"><span data-stu-id="4c429-105">Communicating with MCI Devices</span></span>

<span data-ttu-id="4c429-106">Драйвер каждого устройства MCI поддерживает список текущих параметров и возможностей, поэтому он может выдавать точный ответ при запросе информации.</span><span class="sxs-lookup"><span data-stu-id="4c429-106">The driver of each MCI device maintains a list of its current settings and capabilities, so it can issue an accurate response when it is queried for information.</span></span>

<span data-ttu-id="4c429-107">При необходимости взаимодействия с устройством MCI можно использовать макросы и функции МЦивнд.</span><span class="sxs-lookup"><span data-stu-id="4c429-107">When you want to communicate with an MCI device, you can use MCIWnd macros and functions.</span></span> <span data-ttu-id="4c429-108">Многие из наиболее распространенных команд и запросов MCI определяются как макросы.</span><span class="sxs-lookup"><span data-stu-id="4c429-108">Many of the most common MCI commands and queries are defined as macros.</span></span> <span data-ttu-id="4c429-109">Однако если задача, которую требуется выполнить, недоступна в качестве функции или макроса, команды MCI можно отправить непосредственно в драйвер устройства с помощью макроса [**мЦивндсендстринг**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) или формы сообщения или строки команд MCI.</span><span class="sxs-lookup"><span data-stu-id="4c429-109">However, if the task you want to perform is unavailable as a function or macro, you can send MCI commands directly to the device driver by using the [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) macro or by using either the message form or string form of the MCI commands.</span></span> <span data-ttu-id="4c429-110">Использование макроса **мЦивндсендстринг** эквивалентно использованию функции [**mciSendString**](/previous-versions//dd757161(v=vs.85)) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4c429-110">Using the **MCIWndSendString** macro is equivalent to using the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function as follows:</span></span>


```C++
mciSendString(sz, Null, 0, Null) 
```



<span data-ttu-id="4c429-111">Параметры [**мЦивндсендстринг**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) включают только обработчик окна и строковое форму команды.</span><span class="sxs-lookup"><span data-stu-id="4c429-111">The parameters of [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) include only the window handle and the string form of the command.</span></span> <span data-ttu-id="4c429-112">Чтобы получить сведения, возвращенные строковой командой, используйте макрос [**мЦивндретурнстринг**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) .</span><span class="sxs-lookup"><span data-stu-id="4c429-112">To retrieve the information returned by a string command, use the [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) macro.</span></span>

<span data-ttu-id="4c429-113">Дополнительные сведения о MCI см. в разделе [MCI](mci.md).</span><span class="sxs-lookup"><span data-stu-id="4c429-113">For more information about MCI, see [MCI](mci.md).</span></span>

> [!Note]  
> <span data-ttu-id="4c429-114">При использовании **мЦивндсендстринг** необходимо исключить псевдоним устройства из команды MCI.</span><span class="sxs-lookup"><span data-stu-id="4c429-114">You must exclude the device alias from the MCI command when you use **MCIWndSendString**.</span></span> <span data-ttu-id="4c429-115">Библиотека МЦивнд добавляет этот псевдоним при отправке команды устройству MCI.</span><span class="sxs-lookup"><span data-stu-id="4c429-115">The MCIWnd library adds this alias when it sends the command to the MCI device.</span></span>

 

 

 