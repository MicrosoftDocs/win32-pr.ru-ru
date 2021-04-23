---
description: Начиная с Windows Vista диспетчер управления службами (SCM) поддерживает удаленные вызовы процедур по протоколу управления передачей (RPC/TCP) и именованным каналам (RPC/NP).
ms.assetid: c51732f6-c22f-4726-afaa-13a8948ac44f
title: Службы и RPC/TCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fdb2ef3b21f280ba4e5078d302813de41a5a43a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664365"
---
# <a name="services-and-rpctcp"></a><span data-ttu-id="c7a88-103">Службы и RPC/TCP</span><span class="sxs-lookup"><span data-stu-id="c7a88-103">Services and RPC/TCP</span></span>

<span data-ttu-id="c7a88-104">Начиная с Windows Vista диспетчер управления службами (SCM) поддерживает удаленные вызовы процедур по протоколу управления передачей (RPC/TCP) и именованным каналам (RPC/NP).</span><span class="sxs-lookup"><span data-stu-id="c7a88-104">Starting with Windows Vista, the service control manager (SCM) supports remote procedure calls over both Transmission Control Protocol (RPC/TCP) and named pipes (RPC/NP).</span></span> <span data-ttu-id="c7a88-105">Функции SCM на стороне клиента используют RPC/TCP по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c7a88-105">Client-side SCM functions use RPC/TCP by default.</span></span>

<span data-ttu-id="c7a88-106">RPC/TCP подходит для большинства приложений, использующих функции SCM удаленно, таких как средства удаленного администрирования или мониторинга.</span><span class="sxs-lookup"><span data-stu-id="c7a88-106">RPC/TCP is appropriate for most applications that use SCM functions remotely, such as remote administration or monitoring tools.</span></span> <span data-ttu-id="c7a88-107">Однако для обеспечения совместимости и производительности некоторым приложениям может потребоваться отключить RPC/TCP, задав значения реестра, описанные в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="c7a88-107">However, for compatibility and performance, some applications might need to disable RPC/TCP by setting the registry values described in this topic.</span></span>

<span data-ttu-id="c7a88-108">Когда служба вызывает удаленную функцию SCM, клиентский модуль SCM сначала пытается использовать RPC/TCP для связи со службой SCM на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="c7a88-108">When a service calls a remote SCM function, the client-side SCM first attempts to use RPC/TCP to communicate with the server-side SCM.</span></span> <span data-ttu-id="c7a88-109">Если сервер работает под управлением версии Windows, поддерживающей RPC/TCP и разрешающей трафик RPC/TCP, подключение RPC/ТКПП будет выполняться.</span><span class="sxs-lookup"><span data-stu-id="c7a88-109">If the server is running a version of Windows that supports RPC/TCP and allows RPC/TCP traffic, the RPC/TCPP connection will succeed.</span></span> <span data-ttu-id="c7a88-110">Если сервер работает под управлением версии Windows, которая не поддерживает RPC/TCP, или поддерживает RPC/TCP, но работает за брандмауэром, который разрешает только именованный канал, истекает время ожидания подключения RPC/TCP, и SCM повторяет подключение к RPC/NP.</span><span class="sxs-lookup"><span data-stu-id="c7a88-110">If the server is running a version of Windows that does not support RPC/TCP, or supports RPC/TCP but is operating behind a firewall which allows only named pipe traffic, the RPC/TCP connection times out and the SCM retries the connection with RPC/NP.</span></span> <span data-ttu-id="c7a88-111">В конечном итоге это будет выполнено, но может занять некоторое время (обычно более 20 секунд), в результате чего функция [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) будет заблокирована.</span><span class="sxs-lookup"><span data-stu-id="c7a88-111">This will succeed eventually but can take some time (typically more than 20 seconds), causing the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function to appear blocked.</span></span>

<span data-ttu-id="c7a88-112">Протокол TCP не содержит учетные данные пользователя, указанные с помощью команды **net use** .</span><span class="sxs-lookup"><span data-stu-id="c7a88-112">TCP does not carry user credentials specified with a **net use** command.</span></span> <span data-ttu-id="c7a88-113">Таким образом, если RPC/TCP включен и **sc.exe** используется для попытки доступа к указанной службе, команда может завершиться ошибкой с отказом в доступе.</span><span class="sxs-lookup"><span data-stu-id="c7a88-113">Therefore, if RPC/TCP is enabled and **sc.exe** is used to attempt to access the specified service, the command could fail with access denied.</span></span> <span data-ttu-id="c7a88-114">Отключение RPC/TCP на стороне клиента приводит к тому, что команда **sc.exe** использует именованный канал, который содержит учетные данные пользователя, поэтому команда будет выполнена.</span><span class="sxs-lookup"><span data-stu-id="c7a88-114">Disabling RPC/TCP on the client side causes the **sc.exe** command to use a named pipe that does carry user credentials, so the command will succeed.</span></span> <span data-ttu-id="c7a88-115">Сведения о sc.exe см. [в разделе Управление службой с помощью SC](controlling-a-service-using-sc.md).</span><span class="sxs-lookup"><span data-stu-id="c7a88-115">For information about sc.exe, see [Controlling a Service Using SC](controlling-a-service-using-sc.md).</span></span>

> [!Note]  
> <span data-ttu-id="c7a88-116">Служба не должна предоставлять явные учетные данные команде **net use** , так как эти учетные данные могут быть случайно предоставлены за пределами границ службы.</span><span class="sxs-lookup"><span data-stu-id="c7a88-116">A service should not provide explicit credentials to a **net use** command, because those credentials might be inadvertently shared outside of the service boundaries.</span></span> <span data-ttu-id="c7a88-117">Вместо этого служба должна использовать [олицетворение клиента](/windows/desktop/SecAuthZ/client-impersonation) для олицетворения пользователя.</span><span class="sxs-lookup"><span data-stu-id="c7a88-117">Instead, the service should use [client impersonation](/windows/desktop/SecAuthZ/client-impersonation) to impersonate the user.</span></span>

 

### <a name="rpctcp-registry-values"></a><span data-ttu-id="c7a88-118">Значения реестра RPC/TCP</span><span class="sxs-lookup"><span data-stu-id="c7a88-118">RPC/TCP Registry Values</span></span>

<span data-ttu-id="c7a88-119">Управление RPC/TCP осуществляется с помощью значений реестра **скмапиконнектионпарам**, **дисаблерпковерткп** и **дисаблеремотескмендпоинтс** , которые находятся в ключе управления **" \_ Локальная \_ машина**" в папке hKey \\  \\ **CurrentControlSet** \\  .</span><span class="sxs-lookup"><span data-stu-id="c7a88-119">RPC/TCP is controlled by the **SCMApiConnectionParam**, **DisableRPCOverTCP**, and **DisableRemoteScmEndpoints** registry values, which are all under the **HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control** key.</span></span> <span data-ttu-id="c7a88-120">Все эти значения имеют \_ тип данных reg DWORD.</span><span class="sxs-lookup"><span data-stu-id="c7a88-120">All of these values have a REG\_DWORD data type.</span></span> <span data-ttu-id="c7a88-121">В следующих процедурах показано, как использовать эти значения реестра для управления RPC/TCP.</span><span class="sxs-lookup"><span data-stu-id="c7a88-121">The following procedures show how to use these registry values to control RPC/TCP.</span></span>

<span data-ttu-id="c7a88-122">В следующей процедуре описывается, как отключить RPC/TCP на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="c7a88-122">The following procedure describes how to disable RPC/TCP on the client side.</span></span>

<span data-ttu-id="c7a88-123">**Отключение RPC/TCP на стороне клиента**</span><span class="sxs-lookup"><span data-stu-id="c7a88-123">**To disable RPC/TCP on the client side**</span></span>

1.  <span data-ttu-id="c7a88-124">Объедините значение реестра **скмапиконнектионпарам** со значением маски 0x80000000.</span><span class="sxs-lookup"><span data-stu-id="c7a88-124">Combine the **SCMApiConnectionParam** registry value with the mask value 0x80000000.</span></span>
2.  <span data-ttu-id="c7a88-125">Перезапустите приложение, вызывающее функцию [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) .</span><span class="sxs-lookup"><span data-stu-id="c7a88-125">Restart the application that calls the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function.</span></span>

<span data-ttu-id="c7a88-126">В следующей процедуре описывается, как отключить TCP на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="c7a88-126">The following procedure describes how to disable TCP on the server side.</span></span>

<span data-ttu-id="c7a88-127">**Отключение протокола TCP на стороне сервера**</span><span class="sxs-lookup"><span data-stu-id="c7a88-127">**To disable TCP on the server side**</span></span>

1.  <span data-ttu-id="c7a88-128">Присвойте параметру реестра **дисаблерпковерткп** значение 1.</span><span class="sxs-lookup"><span data-stu-id="c7a88-128">Set the **DisableRPCOverTCP** registry value to 1.</span></span>
2.  <span data-ttu-id="c7a88-129">Перезапустите сервер.</span><span class="sxs-lookup"><span data-stu-id="c7a88-129">Restart the server.</span></span>

<span data-ttu-id="c7a88-130">В следующей процедуре описывается, как отключить RPC/TCP и RPC/NP на сервере (например, чтобы уменьшить поверхность атаки).</span><span class="sxs-lookup"><span data-stu-id="c7a88-130">The following procedure describes how to disable both RPC/TCP and RPC/NP on the server (for example, to reduce the attack surface).</span></span>

<span data-ttu-id="c7a88-131">**Отключение RPC/TCP и RPC/NP на сервере**</span><span class="sxs-lookup"><span data-stu-id="c7a88-131">**To disable both RPC/TCP and RPC/NP on the server**</span></span>

1.  <span data-ttu-id="c7a88-132">Присвойте параметру реестра **дисаблеремотескмендпоинтс** значение 1.</span><span class="sxs-lookup"><span data-stu-id="c7a88-132">Set the **DisableRemoteScmEndpoints** registry value to 1.</span></span>
2.  <span data-ttu-id="c7a88-133">Перезапустите сервер.</span><span class="sxs-lookup"><span data-stu-id="c7a88-133">Restart the server.</span></span>

<span data-ttu-id="c7a88-134">Значение реестра **скмапиконнектионпарам** можно также использовать для указания интервала времени ожидания RPC/TCP в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="c7a88-134">The **SCMApiConnectionParam** registry value can also be used to specify the RPC/TCP time-out interval, in milliseconds.</span></span> <span data-ttu-id="c7a88-135">Например, значение 30 000 указывает интервал времени ожидания 30 секунд.</span><span class="sxs-lookup"><span data-stu-id="c7a88-135">For example, a value of 30,000 specifies a time-out interval of 30 seconds.</span></span> <span data-ttu-id="c7a88-136">Значение по умолчанию — 21 000 (21 секунда).</span><span class="sxs-lookup"><span data-stu-id="c7a88-136">The default is 21,000 (21 seconds).</span></span>

 

 
