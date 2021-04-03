---
title: Регистрация конечных точек
description: Регистрация серверной программы на карте конечных точек хост-сервера позволяет клиентским программам определить конечную точку (обычно это порт TCP/IP или именованный канал), который прослушивает серверная программа.
ms.assetid: d09874f8-2b55-4af2-bfe1-8978301d6692
keywords:
- Удаленный вызов процедур RPC, задачи, регистрация конечных точек
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f23e02aaae18a9d28b989d16850693a8a8f0678e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772863"
---
# <a name="registering-endpoints"></a><span data-ttu-id="7d7af-104">Регистрация конечных точек</span><span class="sxs-lookup"><span data-stu-id="7d7af-104">Registering Endpoints</span></span>

<span data-ttu-id="7d7af-105">Регистрация серверной программы на карте конечных точек хост-сервера позволяет клиентским программам определить конечную точку (обычно это порт TCP/IP или именованный канал), который прослушивает серверная программа.</span><span class="sxs-lookup"><span data-stu-id="7d7af-105">Registering the server program in the endpoint map of the server host computer enables client programs to determine which endpoint (usually a TCP/IP port or a named pipe) the server program is listening to.</span></span> <span data-ttu-id="7d7af-106">Чтобы зарегистрироваться в карте конечных точек серверной системы узла, серверная программа вызывает функцию [**рпцепрегистер**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) , как показано в следующем фрагменте кода:</span><span class="sxs-lookup"><span data-stu-id="7d7af-106">To register itself in the server host system's endpoint map, a server program calls the [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) function as shown in the following code fragment:</span></span>


```C++
// This example assumes that MyInterface_v1_0_s_ifspec is a valid data
// structure that represents the interface being registered. The 
// variable is a valid pointer to a binding vector.
RPC_STATUS status;
status = RpcEpRegister(
    MyInterface_v1_0_s_ifspec,
    rpcBindingVector,
    NULL,
    NULL);
```



<span data-ttu-id="7d7af-107">Первым параметром для [**рпцепрегистер**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) является структура, представляющая интерфейс.</span><span class="sxs-lookup"><span data-stu-id="7d7af-107">The first parameter to [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) is the structure that represents the interface.</span></span> <span data-ttu-id="7d7af-108">Его можно найти в файле заголовка, созданном компилятором MIDL из файла MIDL для этого распределенного приложения.</span><span class="sxs-lookup"><span data-stu-id="7d7af-108">You can find it in the header file that the MIDL compiler generated from your MIDL file for this distributed application.</span></span> <span data-ttu-id="7d7af-109">См. раздел [Разработка интерфейса](developing-the-interface.md).</span><span class="sxs-lookup"><span data-stu-id="7d7af-109">See [Developing the Interface](developing-the-interface.md).</span></span> <span data-ttu-id="7d7af-110">Далее **рпцепрегистер** требуется, чтобы приложение передавало набор дескрипторов привязки, которые хранятся в векторе привязки.</span><span class="sxs-lookup"><span data-stu-id="7d7af-110">Next, **RpcEpRegister** needs your application to pass a set of binding handles that are stored in a binding vector.</span></span>

<span data-ttu-id="7d7af-111">Кроме регистрации имен интерфейсов, серверное приложение также может регистрировать ИДЕНТИФИКАТОРы объектов на карте конечных точек.</span><span class="sxs-lookup"><span data-stu-id="7d7af-111">In addition to registering interface names, your server application can also register object UUIDs in the endpoint map.</span></span> <span data-ttu-id="7d7af-112">В этом примере нет UUID объекта для регистрации, поэтому третий параметр [**рпцепрегистер**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="7d7af-112">In this example, there are no object UUIDs to register, so the third parameter to [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) is set to **NULL**.</span></span>

<span data-ttu-id="7d7af-113">Последний параметр представляет собой строку комментария.</span><span class="sxs-lookup"><span data-stu-id="7d7af-113">The last parameter is a comment string.</span></span> <span data-ttu-id="7d7af-114">Несмотря на то, что библиотека времени выполнения RPC не использует эту строку, рекомендуется задать строку, так как она повышает управляемость системы.</span><span class="sxs-lookup"><span data-stu-id="7d7af-114">Although the RPC run-time library does not use this string, setting the string is recommended, as it improves manageability of the system.</span></span> <span data-ttu-id="7d7af-115">Системный администратор может использовать строку для определения портов, используемых приложениями, которые затем можно использовать для определения портов, управляемых брандмауэрами.</span><span class="sxs-lookup"><span data-stu-id="7d7af-115">A system administrator can use the string to detect which ports are used by which applications, which can then be used to determine which ports to be managed by firewalls.</span></span>

 

 




