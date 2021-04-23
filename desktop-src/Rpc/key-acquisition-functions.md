---
title: Функции приобретения ключей
description: По умолчанию поставщик общих служб предоставляет ключи шифрования для серверных программ, запрашивающих их. Каждый поставщик общих служб реализует собственную систему создания ключей. Формат ключей, создаваемых поставщиком общих служб, зависит от поставщика общих служб.
ms.assetid: 0ba7212c-6ee8-4a92-94d0-f09f84b05bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36a8c8e8cfb2f3b4f8f241b2401878576cbe7f90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888983"
---
# <a name="key-acquisition-functions"></a><span data-ttu-id="c9685-105">Функции приобретения ключей</span><span class="sxs-lookup"><span data-stu-id="c9685-105">Key Acquisition Functions</span></span>

<span data-ttu-id="c9685-106">По умолчанию поставщик общих служб предоставляет ключи шифрования для серверных программ, запрашивающих их.</span><span class="sxs-lookup"><span data-stu-id="c9685-106">By default, the SSP supplies encryption keys to server programs that request them.</span></span> <span data-ttu-id="c9685-107">Каждый поставщик общих служб реализует собственную систему создания ключей.</span><span class="sxs-lookup"><span data-stu-id="c9685-107">Each SSP implements its own system of generating keys.</span></span> <span data-ttu-id="c9685-108">Формат ключей, создаваемых поставщиком общих служб, зависит от поставщика общих служб.</span><span class="sxs-lookup"><span data-stu-id="c9685-108">The format of the keys that the SSP generates are specific to the SSP.</span></span>

<span data-ttu-id="c9685-109">RPC предоставляет возможность переопределения метода создания ключей шифрования по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c9685-109">RPC provides you with the ability to override the default method of generating encryption keys.</span></span> <span data-ttu-id="c9685-110">Приложение может вызвать функцию [**рпксерверрегистераусинфо**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) и передать ему указатель на функцию получения ключа.</span><span class="sxs-lookup"><span data-stu-id="c9685-110">Your application can call the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function and pass it a pointer to a key acquisition function.</span></span> <span data-ttu-id="c9685-111">Функцию приобретения ключа можно написать так, чтобы она создавала ключи с помощью любого выбранного метода.</span><span class="sxs-lookup"><span data-stu-id="c9685-111">You can write the key acquisition function so that it generates keys using any method you choose.</span></span> <span data-ttu-id="c9685-112">Однако ключ, который он передает в серверную программу, должен соответствовать формату, который требуется для поставщика общих служб.</span><span class="sxs-lookup"><span data-stu-id="c9685-112">However, the key it passes to the server program must match the format that the SSP requires.</span></span>

> [!Note]  
> <span data-ttu-id="c9685-113">Большинству приложений не требуется использовать функции приобретения ключа, и можно просто указать **значение NULL** для всех параметров, в которых запрашивается функция получения ключа.</span><span class="sxs-lookup"><span data-stu-id="c9685-113">Most applications do not need to use key acquisition functions, and can simply supply **NULL** to all parameters where a key acquisition function is requested.</span></span>

 

 

 




