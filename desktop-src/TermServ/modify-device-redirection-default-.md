---
title: Изменение перенаправления устройств по умолчанию
description: Так как серверы шлюза удаленный рабочий стол пытаются применить безопасные политики перенаправления устройств перед передачей клиентского подключения через сервер узла сеансов удаленный рабочий стол, может потребоваться отключить это значение по умолчанию в некоторых случаях.
ms.assetid: 03F2617C-D478-4A51-9EEC-E9643CA831B7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 925099b94c75dca39d381bdf57ae9730fb840da7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888528"
---
# <a name="modify-device-redirection-default"></a><span data-ttu-id="c5dfc-103">Изменение перенаправления устройств по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c5dfc-103">Modify Device Redirection Default</span></span>

<span data-ttu-id="c5dfc-104">Так как серверы шлюза удаленный рабочий стол пытаются применить безопасные политики перенаправления устройств перед передачей клиентского подключения через сервер узла сеансов удаленный рабочий стол, может потребоваться отключить это значение по умолчанию в некоторых случаях.</span><span class="sxs-lookup"><span data-stu-id="c5dfc-104">Because Remote Desktop Gateway servers attempt to enforce secure device redirection policies before passing the client connection through to a Remote Desktop Session Host server, you may need to disable this default in some cases.</span></span>

<span data-ttu-id="c5dfc-105">В Windows Server 2008 R2 и более поздних версиях удаленный рабочий стол серверы шлюза по умолчанию будут пытаться применить политики безопасной перенаправления устройств перед передачей клиентского подключения через сервер узла сеансов удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="c5dfc-105">On Windows Server 2008 R2 and later, Remote Desktop Gateway servers will by default attempt to enforce secure device redirection policies before passing the client connection through to a Remote Desktop Session Host server.</span></span> <span data-ttu-id="c5dfc-106">Однако эта функция не поддерживается некоторыми серверами.</span><span class="sxs-lookup"><span data-stu-id="c5dfc-106">However, this feature is not supported by some servers.</span></span> <span data-ttu-id="c5dfc-107">Например, это не поддерживается для подключений к сеансам консоли Hyper-V, поэтому может потребоваться отключить значение по умолчанию для поддержки федеративной проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="c5dfc-107">For example, this is not supported for connections to Hyper-V console sessions, and it may be necessary to disable the default to support federated authentication.</span></span> <span data-ttu-id="c5dfc-108">В таких случаях эту функцию можно отключить, создав следующий раздел реестра, чтобы разрешить подключение к.</span><span class="sxs-lookup"><span data-stu-id="c5dfc-108">In these cases, this feature can be disabled by creating the following registry key to allow connections to go through.</span></span>

<span data-ttu-id="c5dfc-109">**HKEY \_ локальный \_ компьютер \\ программное обеспечение \\ Microsoft \\ Terminal Server шлюз \\ прердпдисаблерегкэй**</span><span class="sxs-lookup"><span data-stu-id="c5dfc-109">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Terminal Server Gateway\\preRDPDisableRegKey**</span></span>

<span data-ttu-id="c5dfc-110">Если этот ключ существует, шлюз удаленный рабочий стол не будет применять перенаправление устройств.</span><span class="sxs-lookup"><span data-stu-id="c5dfc-110">When this key exists, the Remote Desktop Gateway will not enforce device redirection.</span></span>

 

 




