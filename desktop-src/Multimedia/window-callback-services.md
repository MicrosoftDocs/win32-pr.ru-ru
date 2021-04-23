---
title: Службы обратного вызова окна
description: Службы обратного вызова окна
ms.assetid: 227602e5-7ea1-4afd-ac88-cfeabe746d1f
keywords:
- мультимедиа аудио, окна службы обратного вызова
- звуковые, оконные службы обратного вызова
- Audio миксерс, службы обратного вызова Window
- миксерс, службы обратного вызова окон
- службы обратного вызова окна
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48faf2dd94b61f5d4fc47e073fe0f3875bcbb503
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487648"
---
# <a name="window-callback-services"></a><span data-ttu-id="a5e1a-108">Службы обратного вызова окна</span><span class="sxs-lookup"><span data-stu-id="a5e1a-108">Window Callback Services</span></span>

<span data-ttu-id="a5e1a-109">Службы микшера предоставляют службы обратного вызова окна, чтобы приложение могла обрабатывать сообщения от драйверов микшера.</span><span class="sxs-lookup"><span data-stu-id="a5e1a-109">The mixer services provide window callback services so that your application can process messages from mixer drivers.</span></span> <span data-ttu-id="a5e1a-110">Чтобы использовать эти службы, укажите флаг окна ОБРАТНОго вызова \_ в параметре *фдвопен* и маркер окна в параметре *двкаллбакк* функции [**миксеропен**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) .</span><span class="sxs-lookup"><span data-stu-id="a5e1a-110">To use these services, specify the CALLBACK\_WINDOW flag in the *fdwOpen* parameter and a window handle in the *dwCallback* parameter of the [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) function.</span></span> <span data-ttu-id="a5e1a-111">Сообщения драйвера отправляются в функцию Window PROCEDURE для окна, определяемого маркером в *двкаллбакк*.</span><span class="sxs-lookup"><span data-stu-id="a5e1a-111">Driver messages are sent to the window procedure function for the window identified by the handle in *dwCallback*.</span></span> <span data-ttu-id="a5e1a-112">Сообщения относятся к типу звукового устройства.</span><span class="sxs-lookup"><span data-stu-id="a5e1a-112">The messages are specific to the audio device type.</span></span>

 

 