---
title: Вопросы программирования МГМ
description: При разработке клиентов группы многоадресной рассылки необходимо следовать приведенным ниже рекомендациям.
ms.assetid: 48451a76-81e0-4d60-acb3-c9ec55de32b4
keywords:
- Многоадресная рассылка, вопросы программирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e442de1dcb2da5a8664648587a88f05feaee970
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888740"
---
# <a name="mgm-programming-considerations"></a><span data-ttu-id="de772-104">Вопросы программирования МГМ</span><span class="sxs-lookup"><span data-stu-id="de772-104">MGM Programming Considerations</span></span>

<span data-ttu-id="de772-105">При разработке клиентов группы многоадресной рассылки необходимо следовать приведенным ниже рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="de772-105">When you are developing multicast group manager clients, observe the following guidelines:</span></span>

-   <span data-ttu-id="de772-106">Вызовы функций должны выполняться в рамках процесса маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="de772-106">Function calls must be made from within the router process.</span></span> <span data-ttu-id="de772-107">Если функции вызываются из другого процесса, их результаты будут недействительными. Клиент не будет взаимодействовать с диспетчером групп многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="de772-107">If functions are called from another process, their results will not be valid; the client will not interact with the multicast group manager.</span></span>
-   <span data-ttu-id="de772-108">Клиенты, использующие API МГМ, должны предоставлять собственную проверку ошибок, гарантируя передачу только допустимых данных в Диспетчер групп многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="de772-108">Clients that use the MGM API must provide their own error checking, ensuring that only valid data is passed to the multicast group manager.</span></span> <span data-ttu-id="de772-109">Функции МГМ не возвращают подробные сообщения об ошибках для недопустимых параметров. Ошибка \_ возвращается при неправильном \_ значении параметра без объяснения.</span><span class="sxs-lookup"><span data-stu-id="de772-109">MGM functions do not return detailed error messages about invalid parameters; the ERROR\_INVALID\_PARAMETER value is returned without explanation.</span></span>
-   <span data-ttu-id="de772-110">Клиенты должны соблюдать осторожность при использовании блокировок при вызове функций МГМ.</span><span class="sxs-lookup"><span data-stu-id="de772-110">Clients should exercise caution in using locks while calling MGM functions.</span></span> <span data-ttu-id="de772-111">Это может препятствовать взаимоблокировкам.</span><span class="sxs-lookup"><span data-stu-id="de772-111">Doing so can prevent deadlocks.</span></span> <span data-ttu-id="de772-112">При вызове функций МГМ клиенты не должны удерживать блокировки, которые могут одновременно храниться в обратном вызове от диспетчера групп многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="de772-112">When calling MGM functions, clients should not hold any locks that might simultaneously be held in a callback from the multicast group manager.</span></span>

 

 




