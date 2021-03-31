---
title: Диспетчер подключений
description: Клиенты, которые хотят разрабатывать пользовательские номеронабирателя с помощью API службы удаленного доступа, могут изучить диспетчер подключений Майкрософт и пакет администрирования диспетчера подключений.
ms.assetid: c3227aea-ba36-44f6-b69d-2c6aa4be360e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7959482542630b6dc90149971df08f7944f83fc
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104069632"
---
# <a name="connection-manager"></a><span data-ttu-id="78b18-103">Диспетчер подключений</span><span class="sxs-lookup"><span data-stu-id="78b18-103">Connection Manager</span></span>

<span data-ttu-id="78b18-104">Клиенты, которые хотят разрабатывать пользовательские номеронабирателя с помощью API службы удаленного доступа, могут изучить диспетчер подключений Майкрософт и пакет администрирования диспетчера подключений.</span><span class="sxs-lookup"><span data-stu-id="78b18-104">Customers who intend to develop custom dialers using the Remote Access Service API may want to investigate Microsoft Connection Manager and the Connection Manager Administration Kit.</span></span> <span data-ttu-id="78b18-105">Диспетчер подключений является управляемым клиентом удаленного доступа Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="78b18-105">Connection Manager is Microsoft's managed remote access client.</span></span> <span data-ttu-id="78b18-106">Он позволяет администратору создать пакет конфигурации удаленного доступа, который будет распространяться удаленным пользователям администратора.</span><span class="sxs-lookup"><span data-stu-id="78b18-106">It allows an administrator to build a remote access configuration package to be distributed to the administrator's remote users.</span></span> <span data-ttu-id="78b18-107">Дополнительные сведения о диспетчере подключений и пакете администрирования диспетчера подключений см. в справке в Интернете для Microsoft Windows 2000 Server и более поздних операционных систем.</span><span class="sxs-lookup"><span data-stu-id="78b18-107">For more information on Connection Manager and the Connection Manager Administration Kit, see the online help for Microsoft Windows 2000 Server and later operating systems.</span></span>

<span data-ttu-id="78b18-108">Исходный код для примера настраиваемого действия диспетчера соединений можно найти в полном пакете SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="78b18-108">You can find the source code for a sample Connection Manager custom action in the complete Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="78b18-109">Пакет SDK для платформы можно загрузить на [веб-сайте корпорации Майкрософт](https://msdn.microsoft.com/windowsserver/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="78b18-109">The Platform SDK can be downloaded at the [Microsoft Web site](https://msdn.microsoft.com/windowsserver/bb980924.aspx).</span></span> <span data-ttu-id="78b18-110">После установки путь к образцу кода —% Install путь% \\ пакет Microsoft SDK \\ Samples \\ нетдс \\ RAS \\ ConnectionManager, где% путь установки указывает базовый каталог установки пакета SDK платформы (например, C: \\ Program Files).</span><span class="sxs-lookup"><span data-stu-id="78b18-110">After installation, the path to the sample code is %Install Path%\\Microsoft SDK\\Samples\\netds\\Ras\\ConnectionManager, where %Install Path% designates the base installation directory of the Platform SDK (for example, C:\\Program Files).</span></span>

<span data-ttu-id="78b18-111">Пользовательские действия позволяют клиенту удаленного доступа выполнять определенные действия в различных точках процесса подключения.</span><span class="sxs-lookup"><span data-stu-id="78b18-111">Custom actions make it possible for the remote access client to take specific actions at various points in the connection process.</span></span> <span data-ttu-id="78b18-112">Настраиваемое действие, показанное в примере, автоматически корректирует конфигурацию прокси-сервера для подключения на основе адреса сервера подключения.</span><span class="sxs-lookup"><span data-stu-id="78b18-112">The custom action demonstrated in the sample automatically adjusts the proxy server configuration for a connection based on the connection's server address.</span></span> <span data-ttu-id="78b18-113">Клиенты могут использовать этот пример в качестве отправной точки для создания собственных настраиваемых действий.</span><span class="sxs-lookup"><span data-stu-id="78b18-113">Customers can use this sample as a starting point for creating their own custom actions.</span></span>

 

 




