---
description: При запуске клиента он выбирает пакет безопасности для своих транзакций с сервером, а затем связывается с этим сервером. Сервер выбирает один или несколько пакетов безопасности и ожидает подключения клиента.
ms.assetid: eaed162b-ef07-4295-93d9-6be91232a82e
title: Получение сведений о пакетах безопасности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca690575ff7f46ef5a5b1d971b1ab9fdd91f95e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154770"
---
# <a name="getting-information-about-security-packages"></a><span data-ttu-id="3fac2-104">Получение сведений о пакетах безопасности</span><span class="sxs-lookup"><span data-stu-id="3fac2-104">Getting Information About Security Packages</span></span>

<span data-ttu-id="3fac2-105">При запуске клиента он выбирает [*пакет безопасности*](/windows/desktop/SecGloss/s-gly) для своих транзакций с сервером, а затем связывается с этим сервером.</span><span class="sxs-lookup"><span data-stu-id="3fac2-105">When a client begins, it selects a [*security package*](/windows/desktop/SecGloss/s-gly) for its transactions with a server and then contacts that server.</span></span> <span data-ttu-id="3fac2-106">Сервер выбирает один или несколько пакетов безопасности и ожидает подключения клиента.</span><span class="sxs-lookup"><span data-stu-id="3fac2-106">A server selects one or more security packages and waits for a client connection.</span></span>

<span data-ttu-id="3fac2-107">Для получения подробных сведений о пакетах безопасности SSPI, доступных в определенном поставщике общих служб, можно вызвать функцию [**енумератесекуритипаккажес**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) , чтобы получить структуру [**секпкгинфо**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="3fac2-107">For specific information about the SSPI security packages available with a particular SSP, the [**EnumerateSecurityPackages**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) function can be called to retrieve a [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) structure.</span></span>

<span data-ttu-id="3fac2-108">Чтобы получить выходную структуру, вызывающий объект передает в функцию адрес указателя на тип возвращаемой структуры.</span><span class="sxs-lookup"><span data-stu-id="3fac2-108">To retrieve the output structure, the caller passes to the function the address of a pointer to the type of the return structure.</span></span> <span data-ttu-id="3fac2-109">Функция выделяет память и возвращает данные вызывающему объекту, присваивая аргументу адрес буфера возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="3fac2-109">The function allocates memory and returns the data to the caller by assigning the address of the return data buffer to the argument.</span></span> <span data-ttu-id="3fac2-110">Соглашение SSPI заключается в том, что функция выделяет память для структуры, а вызывающее приложение освобождает эту память с помощью [**фриконтекстбуффер**](/windows/desktop/api/Sspi/nf-sspi-freecontextbuffer).</span><span class="sxs-lookup"><span data-stu-id="3fac2-110">The SSPI convention is that the function allocates memory for the structure, and the calling application frees that memory using [**FreeContextBuffer**](/windows/desktop/api/Sspi/nf-sspi-freecontextbuffer).</span></span>

<span data-ttu-id="3fac2-111">Вызов функции [**куерисекуритипаккажеинфо**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa) извлекает атрибуты [*пакета безопасности*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="3fac2-111">Calling the [**QuerySecurityPackageInfo**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa) function retrieves the attributes of a [*security package*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="3fac2-112">Как сервер, так и клиент могут вызвать функцию **куерисекуритипаккажеинфо** , чтобы получить максимальную длину маркера безопасности из элемента **кбмакстокен** структуры [**секпкгинфо**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="3fac2-112">Both server and client can call the **QuerySecurityPackageInfo** function to get the maximum length of the security token from the **cbMaxToken** member of the [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) structure.</span></span> <span data-ttu-id="3fac2-113">Пример см. в описании вызова функции **куерисекуритипаккажеинфо** , показанной в разделе [Использование SSPI с сервером сокетов Windows](using-sspi-with-a-windows-sockets-server.md).</span><span class="sxs-lookup"><span data-stu-id="3fac2-113">For an example, see the call to the **QuerySecurityPackageInfo** function shown in [Using SSPI with a Windows Sockets Server](using-sspi-with-a-windows-sockets-server.md).</span></span>

<span data-ttu-id="3fac2-114">Дополнительные сведения о функциях пакета см. в разделе [Управление пакетами](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="3fac2-114">For more information on package functions, see [Package Management](authentication-functions.md).</span></span>

 

 
