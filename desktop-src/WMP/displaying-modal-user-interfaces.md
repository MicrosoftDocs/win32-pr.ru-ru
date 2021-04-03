---
title: Отображение модальных пользовательских интерфейсов
description: Отображение модальных пользовательских интерфейсов
ms.assetid: 748a8db7-159d-4043-beac-e0516327bcef
keywords:
- Подключаемые модули проигрывателя Windows Media, отображение диалоговых окон и сообщений
- подключаемые модули, отображение диалоговых окон и сообщений
- подключаемые модули пользовательского интерфейса, отображение диалоговых окон и сообщений
- Подключаемые модули пользовательского интерфейса, отображение диалоговых окон и сообщений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d96387ca46864064c7b6ff7b9cd3dba8187eed0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780063"
---
# <a name="displaying-modal-user-interfaces"></a><span data-ttu-id="83638-107">Отображение модальных пользовательских интерфейсов</span><span class="sxs-lookup"><span data-stu-id="83638-107">Displaying Modal User Interfaces</span></span>

<span data-ttu-id="83638-108">Подключаемые модули пользовательского интерфейса не должны отображать модальные диалоговые окна или окна сообщений в ответ на вызовы методов из проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="83638-108">UI plug-ins should not display modal dialog boxes or message boxes in response to method calls from Windows Media Player.</span></span> <span data-ttu-id="83638-109">Например, не выводите окно сообщения от реализации **ивмпплугинуи:: Create**.</span><span class="sxs-lookup"><span data-stu-id="83638-109">For example, do not display a message box from your implementation of **IWMPPluginUI::Create**.</span></span>

<span data-ttu-id="83638-110">Если необходимо отобразить диалоговое окно или сообщение из реализации метода подключаемого модуля пользовательского интерфейса, вызываемого проигрывателем, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="83638-110">If you must display a dialog box or message box from a UI plug-in method implementation that is called by the Player, you must follow these steps:</span></span>

1.  <span data-ttu-id="83638-111">Регистрация нового сообщения окна с помощью **регистервиндовмессаже**.</span><span class="sxs-lookup"><span data-stu-id="83638-111">Register a new window message using **RegisterWindowMessage**.</span></span>
2.  <span data-ttu-id="83638-112">Отправьте сообщение окна, зарегистрированное в окне подключаемого модуля пользовательского интерфейса, используя **сообщение**.</span><span class="sxs-lookup"><span data-stu-id="83638-112">Send the window message you registered to your UI plug-in window using **PostMessage**.</span></span>
3.  <span data-ttu-id="83638-113">Отображение диалогового окна или сообщения из обработчика сообщений для нового сообщения окна.</span><span class="sxs-lookup"><span data-stu-id="83638-113">Show the dialog box or message box from the message handler for your new window message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83638-114">См. также</span><span class="sxs-lookup"><span data-stu-id="83638-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83638-115">**Общие сведения о подключаемом модуле пользовательского интерфейса**</span><span class="sxs-lookup"><span data-stu-id="83638-115">**UI Plug-in Overview**</span></span>](ui-plug-in-overview.md)
</dt> </dl>

 

 




