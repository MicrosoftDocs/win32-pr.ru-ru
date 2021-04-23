---
description: Включает масштабируемость локального порта для сокета.
ms.assetid: c5142baf-9e2d-4c06-8719-9090fd2d9487
title: SO_PORT_SCALABILITY (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 565caeb472ac5cb15061d32b47a048a9a210885e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144956"
---
# <a name="so_port_scalability"></a><span data-ttu-id="ab7e6-103">Итак \_ , \_ масштабируемость портов</span><span class="sxs-lookup"><span data-stu-id="ab7e6-103">SO\_PORT\_SCALABILITY</span></span>

<span data-ttu-id="ab7e6-104">Параметр сокета **\_ \_ масштабируемости для порта** обеспечивает масштабируемость локальных портов для сокета.</span><span class="sxs-lookup"><span data-stu-id="ab7e6-104">The **SO\_PORT\_SCALABILITY** socket option enables local port scalability for a socket.</span></span>

<dl> <dt>

<span data-ttu-id="ab7e6-105"><span id="SO_PORT_SCALABILITY"></span><span id="so_port_scalability"></span>**Итак \_ , \_ масштабируемость портов**</span><span class="sxs-lookup"><span data-stu-id="ab7e6-105"><span id="SO_PORT_SCALABILITY"></span><span id="so_port_scalability"></span>**SO\_PORT\_SCALABILITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab7e6-106">0x3006</span><span class="sxs-lookup"><span data-stu-id="ab7e6-106">0x3006</span></span>
</dt> <dt>



<span data-ttu-id="ab7e6-107">Параметр сокета **\_ \_ масштабируемости** "на уровень" обеспечивает масштабируемость локального порта, позволяя максимально увеличить выделение портов, выделяя порты с подстановочными знаками несколько раз для разных пар портов локальных адресов на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="ab7e6-107">The **SO\_PORT\_SCALABILITY** socket option enables local port scalability by allowing port allocation to be maximized by allocating wildcard ports multiple times for different local address port pairs on a local machine.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab7e6-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ab7e6-108">Remarks</span></span>

<span data-ttu-id="ab7e6-109">Примечание. на платформах, где \_ \_ поддерживаются как настолько масштабируемые, так и \_ многократно используемые \_ уникастпорт, предпочтительнее использовать для \_ повторного использования \_ уникастпорт.</span><span class="sxs-lookup"><span data-stu-id="ab7e6-109">Note: on platforms where both SO\_PORT\_SCALABILITY and SO\_REUSE\_UNICASTPORT are supported, prefer to use SO\_REUSE\_UNICASTPORT.</span></span>

<span data-ttu-id="ab7e6-110">В средах прокси-сервера имеются проблемы масштабируемости, так как доступность локального порта ограничена.</span><span class="sxs-lookup"><span data-stu-id="ab7e6-110">Proxy server environments have scalability issues because of limited local port availability.</span></span> <span data-ttu-id="ab7e6-111">Одним из способов решения этой проблемы является добавление на компьютер дополнительных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="ab7e6-111">One way to work around this is to add more IP addresses to the machine.</span></span> <span data-ttu-id="ab7e6-112">Однако по умолчанию для портов с подстановочными знаками, используемых с функцией [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) , ограничен размер динамического диапазона портов на локальном компьютере (до 64 000 портов, но обычно меньше), независимо от количества IP-адресов на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="ab7e6-112">However, by default wildcard ports used with the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function are limited to the size of the dynamic port range on the local machine (up to 64K ports, but usually less) no matter the number of IP addresses on the local machine.</span></span> <span data-ttu-id="ab7e6-113">Для решения этой проблемы приложение должно поддерживать собственный пул портов с резервированием портов или с помощью эвристики.</span><span class="sxs-lookup"><span data-stu-id="ab7e6-113">Working around this requires the application to maintain its own port pool either with port reservation or by using heuristics.</span></span>

<span data-ttu-id="ab7e6-114">Чтобы не допустить наличия всех приложений, требующих масштабируемости, управлять собственным пулом портов и обеспечить более высокую масштабируемость при обеспечении совместимости приложений, в Windows Server 2008 появился вариант сокета **\_ \_ масштабируемости** , позволяющий максимально увеличить выделение портов по шаблону.</span><span class="sxs-lookup"><span data-stu-id="ab7e6-114">To avoid having every application that requires scalability manage its own port pool, and to allow for greater scalability while maintaining application compatibility, Windows Server 2008 introduced the **SO\_PORT\_SCALABILITY** socket option to help maximize wildcard port allocation.</span></span> <span data-ttu-id="ab7e6-115">Выделение портов разворачивается, позволяя приложению распределять порты с подстановочными знаками для каждого уникального локального адреса и пары портов.</span><span class="sxs-lookup"><span data-stu-id="ab7e6-115">Port allocation is maximized by allowing an application to allocate wildcard ports for each unique local address and port pair.</span></span> <span data-ttu-id="ab7e6-116">Таким образом, если на локальном компьютере есть четыре IP-адреса, то для запросов функций [**привязки**](/windows/desktop/api/winsock/nf-winsock-bind) с подстановочными знаками можно выделить до 256 Кбайт портов с подстановочными знаками (64 k портов × 4).</span><span class="sxs-lookup"><span data-stu-id="ab7e6-116">So if a local machine has four IP addresses, then up to 256 K wildcard ports (64 K ports × 4 IP addresses) can be allocated by wildcard [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function requests.</span></span>

<span data-ttu-id="ab7e6-117">Если для сокета установлен параметр Socket **\_ \_ масштабируемости** , а вызов функции [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) выполняется для указанного адреса и порта с подстановочными знаками (для параметра *Name* задан определенный адрес и порт 0), то Winsock выделяет порт для указанного адреса.</span><span class="sxs-lookup"><span data-stu-id="ab7e6-117">When the **SO\_PORT\_SCALABILITY** socket option is set on a socket and a call to the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is made for a specified address and wildcard port (the *name* parameter is set with a specific address and a port of 0), Winsock will allocate a port for the specified address.</span></span> <span data-ttu-id="ab7e6-118">Это выделение будет основано на всех возможных IP-адресах и портах/на адрес на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="ab7e6-118">This allocation will be based on all of the possible IP addresses and ports/per address on the local computer.</span></span> <span data-ttu-id="ab7e6-119">Если порт с подстановочными знаками запрашивается с помощью параметра **для обеспечения \_ \_ масштабируемости порта** , этот порт не может быть выделен другим сокетом без параметра **для обеспечения \_ \_ масштабируемости порта** .</span><span class="sxs-lookup"><span data-stu-id="ab7e6-119">If a wildcard port is acquired using the **SO\_PORT\_SCALABILITY** option, that port cannot be allocated by another socket without the **SO\_PORT\_SCALABILITY** option.</span></span> <span data-ttu-id="ab7e6-120">Это ограничение используется, чтобы избежать проблем с обратной совместимостью приложений, которые предполагают, что локальный порт с подстановочными знаками нельзя использовать повторно.</span><span class="sxs-lookup"><span data-stu-id="ab7e6-120">This restriction is in place to avoid backward-compatibility problems with applications that assume a wildcard local port cannot be reused.</span></span> <span data-ttu-id="ab7e6-121">Обратите внимание, что это означает, что приложения, которые запрашивают большое количество портов, использующих такую **\_ \_ масштабируемость портов,** могут разгрузить устаревшие приложения портов.</span><span class="sxs-lookup"><span data-stu-id="ab7e6-121">Note that this means that applications which acquire a large number of ports using **SO\_PORT\_SCALABILITY** can starve legacy applications of ports.</span></span> <span data-ttu-id="ab7e6-122">Если все доступные временные порты были получены по крайней мере для одного адреса с **таким \_ уровнем \_ масштабируемости** , то больше не может использоваться выделение портов с подстановочными знаками без параметра Socket.</span><span class="sxs-lookup"><span data-stu-id="ab7e6-122">If all available ephemeral ports have been acquired for at least one address with **SO\_PORT\_SCALABILITY** , then no more wildcard port allocations are possible without the socket option.</span></span>

<span data-ttu-id="ab7e6-123">Чтобы обеспечить любой результат, перед вызовом функции [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) необходимо установить параметр для **обеспечения \_ \_ масштабируемости порта** .</span><span class="sxs-lookup"><span data-stu-id="ab7e6-123">To have any effect, the **SO\_PORT\_SCALABILITY** option must be set before the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called.</span></span> <span data-ttu-id="ab7e6-124">Ниже приведен пример того, как это будет использоваться на компьютере с двумя адресами:</span><span class="sxs-lookup"><span data-stu-id="ab7e6-124">An example of how this would be used on a computer with two addresses is outlined below:</span></span>

-   <span data-ttu-id="ab7e6-125">Функция [**сокета**](/windows/desktop/api/Winsock2/nf-winsock2-socket) вызывается процессом для создания сокета.</span><span class="sxs-lookup"><span data-stu-id="ab7e6-125">The [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function is called by a process to create a socket.</span></span>
-   <span data-ttu-id="ab7e6-126">Функция [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) вызывается для включения параметра so-Socket **\_ \_ масштабируемости** для только что созданного сокета.</span><span class="sxs-lookup"><span data-stu-id="ab7e6-126">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function is called to enable the **SO\_PORT\_SCALABILITY** socket option on the newly created socket.</span></span>
-   <span data-ttu-id="ab7e6-127">Функция [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) вызывается для выполнения привязки на одном из IP-адресов локального компьютера и порта 0.</span><span class="sxs-lookup"><span data-stu-id="ab7e6-127">The [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called to do a bind on one of the local computer's IP addresses and port 0.</span></span>
-   <span data-ttu-id="ab7e6-128">Затем вызывается функция [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) для подключения к УДАЛЕННОМУ IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="ab7e6-128">The [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) function is then called to connect to a remote IP address.</span></span> <span data-ttu-id="ab7e6-129">При необходимости сокет используется приложением.</span><span class="sxs-lookup"><span data-stu-id="ab7e6-129">The socket is used by the application as needed.</span></span>
-   <span data-ttu-id="ab7e6-130">Функция [**сокета**](/windows/desktop/api/Winsock2/nf-winsock2-socket) вызывается тем же процессом (возможно, другим потоком) для создания второго сокета.</span><span class="sxs-lookup"><span data-stu-id="ab7e6-130">A [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function is called by the same process (possibly a different thread) to create a second socket.</span></span>
-   <span data-ttu-id="ab7e6-131">Функция [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) вызывается для включения параметра so-Socket **\_ \_ масштабируемости** для вновь созданного второго сокета.</span><span class="sxs-lookup"><span data-stu-id="ab7e6-131">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function is called to enable the **SO\_PORT\_SCALABILITY** socket option on the newly created second socket.</span></span>
-   <span data-ttu-id="ab7e6-132">Функция [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) вызывается с вторым IP-адресом и портом 0 локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="ab7e6-132">The [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called with the local computer's second IP address and port 0.</span></span> <span data-ttu-id="ab7e6-133">Даже если все порты были предварительно выделены, этот вызов выполняется успешно, так как на локальном компьютере доступно несколько IP-адресов, а для обоих сокетов в одном процессе установлен параметр Socket **\_ \_ масштабируемости Port** .</span><span class="sxs-lookup"><span data-stu-id="ab7e6-133">Even when all ports have been previously allocated, this call succeeds because there are multiple IP addresses available on the local computer and the **SO\_PORT\_SCALABILITY** socket option was set on both sockets in the same process.</span></span>
-   <span data-ttu-id="ab7e6-134">Затем вызывается функция [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) для подключения к УДАЛЕННОМУ IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="ab7e6-134">The [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) function is then called to connect to a remote IP address.</span></span> <span data-ttu-id="ab7e6-135">При необходимости второй сокет используется приложением.</span><span class="sxs-lookup"><span data-stu-id="ab7e6-135">The second socket is used by the application as needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab7e6-136">Требования</span><span class="sxs-lookup"><span data-stu-id="ab7e6-136">Requirements</span></span>



| <span data-ttu-id="ab7e6-137">Требование</span><span class="sxs-lookup"><span data-stu-id="ab7e6-137">Requirement</span></span> | <span data-ttu-id="ab7e6-138">Значение</span><span class="sxs-lookup"><span data-stu-id="ab7e6-138">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ab7e6-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ab7e6-139">Minimum supported client</span></span><br/> | <span data-ttu-id="ab7e6-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ab7e6-140">None supported</span></span><br/>                                                           |
| <span data-ttu-id="ab7e6-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ab7e6-141">Minimum supported server</span></span><br/> | <span data-ttu-id="ab7e6-142">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ab7e6-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ab7e6-143">Header</span><span class="sxs-lookup"><span data-stu-id="ab7e6-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab7e6-144"><dt>Ws2def. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab7e6-144"><dt>Ws2def.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab7e6-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ab7e6-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab7e6-146">**жетсоккопт**</span><span class="sxs-lookup"><span data-stu-id="ab7e6-146">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="ab7e6-147">**сетсоккопт**</span><span class="sxs-lookup"><span data-stu-id="ab7e6-147">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[<span data-ttu-id="ab7e6-148">**\_Параметры сокета сокета Sol**</span><span class="sxs-lookup"><span data-stu-id="ab7e6-148">**SOL\_SOCKET Socket Options**</span></span>](sol-socket-socket-options.md)
</dt> <dt>

[<span data-ttu-id="ab7e6-149">**Параметры сокета**</span><span class="sxs-lookup"><span data-stu-id="ab7e6-149">**Socket Options**</span></span>](socket-options.md)
</dt> </dl>

 

 




