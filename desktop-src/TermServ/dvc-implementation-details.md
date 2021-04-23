---
title: Сведения о реализации DVC
description: В этом разделе содержатся сведения о создании клиентского модуля динамического виртуального канала (DVC).
ms.assetid: 338556d9-e9a7-4926-a09c-8e2ce1627467
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 876722736a95b45918d8a5b9e229f4f9eda5840b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672043"
---
# <a name="dvc-implementation-details"></a><span data-ttu-id="7dc8d-103">Сведения о реализации DVC</span><span class="sxs-lookup"><span data-stu-id="7dc8d-103">DVC Implementation Details</span></span>

<span data-ttu-id="7dc8d-104">В этом разделе содержатся сведения о создании клиентского модуля динамического виртуального канала (DVC).</span><span class="sxs-lookup"><span data-stu-id="7dc8d-104">This section contains information about how to write a dynamic virtual channel (DVC) client module.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7dc8d-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="7dc8d-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="7dc8d-106">Написание клиентского модуля DVC</span><span class="sxs-lookup"><span data-stu-id="7dc8d-106">Writing a Client DVC Module</span></span>](writing-a-client-dvc-component.md)
</dt> <dd>

<span data-ttu-id="7dc8d-107">Чтобы создать клиентский модуль динамического виртуального канала (DVC), сначала необходимо реализовать и зарегистрировать подключаемый модуль клиента подключение к удаленному рабочему столу (RDC).</span><span class="sxs-lookup"><span data-stu-id="7dc8d-107">To write a dynamic virtual channel (DVC) client module, you must first implement and register a Remote Desktop Connection (RDC) client plug-in.</span></span>

</dd> <dt>

[<span data-ttu-id="7dc8d-108">Регистрация подключаемого модуля DVC</span><span class="sxs-lookup"><span data-stu-id="7dc8d-108">DVC plug-in registration</span></span>](dvc-plug-in-registration.md)
</dt> <dd>

<span data-ttu-id="7dc8d-109">Описание синтаксиса для записи подключаемого модуля динамического виртуального канала (DVC) для клиента подключение к удаленному рабочему столу (RDC).</span><span class="sxs-lookup"><span data-stu-id="7dc8d-109">Describes syntax for the dynamic virtual channel (DVC) plug-in entry for the Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="7dc8d-110">Запуск прослушивателя DVC</span><span class="sxs-lookup"><span data-stu-id="7dc8d-110">Starting a DVC Listener</span></span>](starting-a-dvc-listener.md)
</dt> <dd>

<span data-ttu-id="7dc8d-111">Чтобы установить успешное подключение между двумя модулями динамических виртуальных каналов (DVC), работающими на клиенте подключение к удаленному рабочему столу (RDC), необходимо запустить прослушиватель DVC и в состоянии прослушивания.</span><span class="sxs-lookup"><span data-stu-id="7dc8d-111">To establish a successful connection between two dynamic virtual channel (DVC) modules that are running on the Remote Desktop Connection (RDC) client and server, a DVC listener must be running and in a listening state.</span></span>

</dd> <dt>

[<span data-ttu-id="7dc8d-112">Принятие подключения</span><span class="sxs-lookup"><span data-stu-id="7dc8d-112">Accepting a Connection</span></span>](accepting-a-connection.md)
</dt> <dd>

<span data-ttu-id="7dc8d-113">В некоторый момент времени клиент динамического виртуального канала (DVC) запрашивает подключение к прослушивателю DVC.</span><span class="sxs-lookup"><span data-stu-id="7dc8d-113">At some point in time, the dynamic virtual channel (DVC) client will request a connection to the DVC listener.</span></span>

</dd> <dt>

[<span data-ttu-id="7dc8d-114">Запись данных с помощью канала DVC</span><span class="sxs-lookup"><span data-stu-id="7dc8d-114">Writing Data by Using a DVC Channel</span></span>](writing-data-by-using-a-dvc-channel.md)
</dt> <dd>

<span data-ttu-id="7dc8d-115">Запись данных канала с помощью динамического виртуального канала (DVC) является симметричным для сервера узла сеансов удаленный рабочий стол (узла сеансов удаленных рабочих столов) и клиента.</span><span class="sxs-lookup"><span data-stu-id="7dc8d-115">Writing channel data by using a dynamic virtual channel (DVC) is symmetric for both the Remote Desktop Session Host (RD Session Host) server and the client.</span></span>

</dd> <dt>

[<span data-ttu-id="7dc8d-116">Тестирование и отладка</span><span class="sxs-lookup"><span data-stu-id="7dc8d-116">Testing and Debugging</span></span>](testing-and-debugging.md)
</dt> <dd>

<span data-ttu-id="7dc8d-117">Существует прослушиватель "echo", реализованный клиентом подключение к удаленному рабочему столу (RDC), который всегда присутствует и ожидает входящих подключений.</span><span class="sxs-lookup"><span data-stu-id="7dc8d-117">There is an "echo" listener that is implemented by the Remote Desktop Connection (RDC) client, which is always present and listening for incoming connections.</span></span>

</dd> <dt>

[<span data-ttu-id="7dc8d-118">Пример подключаемого модуля клиента DVC</span><span class="sxs-lookup"><span data-stu-id="7dc8d-118">DVC Client Plug-in Example</span></span>](dvc-client-plug-in-example.md)
</dt> <dd>

<span data-ttu-id="7dc8d-119">Пример кода C++, демонстрирующий создание подключаемого модуля динамического виртуального канала (DVC) клиента подключение к удаленному рабочему столу (RDC).</span><span class="sxs-lookup"><span data-stu-id="7dc8d-119">C++ code sample that shows how to create a Remote Desktop Connection (RDC) client dynamic virtual channel (DVC) plug-in.</span></span>

</dd> <dt>

[<span data-ttu-id="7dc8d-120">Пример серверного модуля DVC</span><span class="sxs-lookup"><span data-stu-id="7dc8d-120">DVC Server Module Example</span></span>](dvc-server-component-example.md)
</dt> <dd>

<span data-ttu-id="7dc8d-121">Пример кода C++, демонстрирующий создание модуля динамического виртуального канала (DVC) на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="7dc8d-121">C++ code sample that shows how to create the server-side dynamic virtual channel (DVC) module.</span></span>

</dd> </dl>

 

 




