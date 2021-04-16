---
description: 'Существует два разных типа сетевых приложений сокетов: сервер и клиент.'
ms.assetid: 05e42384-1746-462d-82c7-8df848b4525e
title: О серверах и клиентах
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a951d23ba1c6ad4f0f5ffd1f674b056a36c3f8dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692314"
---
# <a name="about-servers-and-clients"></a><span data-ttu-id="2fef5-103">О серверах и клиентах</span><span class="sxs-lookup"><span data-stu-id="2fef5-103">About Servers and Clients</span></span>

<span data-ttu-id="2fef5-104">Существует два разных типа сетевых приложений сокетов: сервер и клиент.</span><span class="sxs-lookup"><span data-stu-id="2fef5-104">There are two distinct types of socket network applications: Server and Client.</span></span>

<span data-ttu-id="2fef5-105">Серверы и клиенты имеют разные поведения. Поэтому процесс их создания отличается.</span><span class="sxs-lookup"><span data-stu-id="2fef5-105">Servers and Clients have different behaviors; therefore, the process of creating them is different.</span></span> <span data-ttu-id="2fef5-106">Ниже приведена общая модель создания потокового сервера TCP/IP и клиента.</span><span class="sxs-lookup"><span data-stu-id="2fef5-106">What follows is the general model for creating a streaming TCP/IP Server and Client.</span></span>

## <a name="server"></a><span data-ttu-id="2fef5-107">Сервер</span><span class="sxs-lookup"><span data-stu-id="2fef5-107">Server</span></span>

1.  <span data-ttu-id="2fef5-108">Инициализируйте Winsock.</span><span class="sxs-lookup"><span data-stu-id="2fef5-108">Initialize Winsock.</span></span>
2.  <span data-ttu-id="2fef5-109">Создайте сокет.</span><span class="sxs-lookup"><span data-stu-id="2fef5-109">Create a socket.</span></span>
3.  <span data-ttu-id="2fef5-110">Привяжите сокет.</span><span class="sxs-lookup"><span data-stu-id="2fef5-110">Bind the socket.</span></span>
4.  <span data-ttu-id="2fef5-111">Прослушивание сокета для клиента.</span><span class="sxs-lookup"><span data-stu-id="2fef5-111">Listen on the socket for a client.</span></span>
5.  <span data-ttu-id="2fef5-112">Принимает соединение от клиента.</span><span class="sxs-lookup"><span data-stu-id="2fef5-112">Accept a connection from a client.</span></span>
6.  <span data-ttu-id="2fef5-113">Получение и отправка данных.</span><span class="sxs-lookup"><span data-stu-id="2fef5-113">Receive and send data.</span></span>
7.  <span data-ttu-id="2fef5-114">Производить отключение.</span><span class="sxs-lookup"><span data-stu-id="2fef5-114">Disconnect.</span></span>

## <a name="client"></a><span data-ttu-id="2fef5-115">Клиент</span><span class="sxs-lookup"><span data-stu-id="2fef5-115">Client</span></span>

1.  <span data-ttu-id="2fef5-116">Инициализируйте Winsock.</span><span class="sxs-lookup"><span data-stu-id="2fef5-116">Initialize Winsock.</span></span>
2.  <span data-ttu-id="2fef5-117">Создайте сокет.</span><span class="sxs-lookup"><span data-stu-id="2fef5-117">Create a socket.</span></span>
3.  <span data-ttu-id="2fef5-118">Подключитесь к серверу.</span><span class="sxs-lookup"><span data-stu-id="2fef5-118">Connect to the server.</span></span>
4.  <span data-ttu-id="2fef5-119">Отправка и получение данных.</span><span class="sxs-lookup"><span data-stu-id="2fef5-119">Send and receive data.</span></span>
5.  <span data-ttu-id="2fef5-120">Производить отключение.</span><span class="sxs-lookup"><span data-stu-id="2fef5-120">Disconnect.</span></span>

> [!Note]  
> <span data-ttu-id="2fef5-121">Некоторые шаги одинаковы для клиента и сервера.</span><span class="sxs-lookup"><span data-stu-id="2fef5-121">Some of the steps are the same for a client and a server.</span></span> <span data-ttu-id="2fef5-122">Эти действия реализуются практически одинаково.</span><span class="sxs-lookup"><span data-stu-id="2fef5-122">These steps are implemented almost exactly alike.</span></span> <span data-ttu-id="2fef5-123">Некоторые действия, описанные в этом руководстве, относятся к типу создаваемого приложения.</span><span class="sxs-lookup"><span data-stu-id="2fef5-123">Some of the steps in this guide will be specific to the type of application being created.</span></span>

 

<span data-ttu-id="2fef5-124">Первый шаг. [Создание базового приложения Winsock](creating-a-basic-winsock-application.md)</span><span class="sxs-lookup"><span data-stu-id="2fef5-124">First Step: [Creating a Basic Winsock Application](creating-a-basic-winsock-application.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="2fef5-125">См. также</span><span class="sxs-lookup"><span data-stu-id="2fef5-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fef5-126">начало работы с помощью Winsock</span><span class="sxs-lookup"><span data-stu-id="2fef5-126">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> </dl>

 

 



