---
title: Служба маршрутизации и удаленного доступа
description: .
ms.assetid: fa0a183a-0254-401e-8b78-441cb3f83e8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdaae9e54cd37bef1b45a3336eb389027ebf01ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672155"
---
# <a name="routing-and-remote-access-service"></a><span data-ttu-id="fd0a1-103">Служба маршрутизации и удаленного доступа</span><span class="sxs-lookup"><span data-stu-id="fd0a1-103">Routing and Remote Access Service</span></span>

## <a name="purpose"></a><span data-ttu-id="fd0a1-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="fd0a1-104">Purpose</span></span>

<span data-ttu-id="fd0a1-105">Службу удаленного доступа (RAS) можно использовать для создания клиентских приложений.</span><span class="sxs-lookup"><span data-stu-id="fd0a1-105">Remote Access Service (RAS) can be used to create client applications.</span></span> <span data-ttu-id="fd0a1-106">В этих приложениях отображаются общие диалоговые окна службы RAS, Управление подключениями и устройствами удаленного доступа и работа с записями в телефонной книге.</span><span class="sxs-lookup"><span data-stu-id="fd0a1-106">These applications display RAS common dialog boxes, manage remote access connections and devices, and manipulate phone-book entries.</span></span>

<span data-ttu-id="fd0a1-107">Интерфейсы API маршрутизации позволяют создавать приложения для администрирования возможностей маршрутизации операционной системы.</span><span class="sxs-lookup"><span data-stu-id="fd0a1-107">The Routing APIs make it possible to create applications to administer the routing capabilities of the operating system.</span></span>

<span data-ttu-id="fd0a1-108">Разработчики могут использовать интерфейсы API протокола маршрутизации для реализации протоколов маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="fd0a1-108">Developers can use the Routing Protocol APIs to implement routing protocols.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="fd0a1-109">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="fd0a1-109">Developer audience</span></span>

<span data-ttu-id="fd0a1-110">API-интерфейсы службы маршрутизации и удаленного доступа предназначены для использования программистами C/C++.</span><span class="sxs-lookup"><span data-stu-id="fd0a1-110">The Routing and Remote Access Service APIs are designed for use by C/C++ programmers.</span></span> <span data-ttu-id="fd0a1-111">Программисты также должны быть знакомы с основными понятиями сети.</span><span class="sxs-lookup"><span data-stu-id="fd0a1-111">Programmers should also be familiar with networking concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="fd0a1-112">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="fd0a1-112">Run-time requirements</span></span>

<span data-ttu-id="fd0a1-113">Дополнительные сведения о том, какие операционные системы поддерживают определенную функцию, см. в разделах о требованиях в документации.</span><span class="sxs-lookup"><span data-stu-id="fd0a1-113">For more specific information about which operating systems support a particular function, refer to the Requirements sections in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fd0a1-114">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="fd0a1-114">In this section</span></span>



| <span data-ttu-id="fd0a1-115">Раздел</span><span class="sxs-lookup"><span data-stu-id="fd0a1-115">Topic</span></span>                                                                                                             | <span data-ttu-id="fd0a1-116">Описание</span><span class="sxs-lookup"><span data-stu-id="fd0a1-116">Description</span></span>                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fd0a1-117">Архитектура служб маршрутизации и удаленного доступа</span><span class="sxs-lookup"><span data-stu-id="fd0a1-117">Routing and Remote Access Services Architecture</span></span>](routing-and-remote-access-services-architecture.md)<br/> | <span data-ttu-id="fd0a1-118">Общие сведения об архитектуре служб маршрутизации и удаленного доступа.</span><span class="sxs-lookup"><span data-stu-id="fd0a1-118">Overview of the Routing and Remote Access Services architecture.</span></span><br/>                                           |
| [<span data-ttu-id="fd0a1-119">Макет реестра маршрутизации и удаленного доступа</span><span class="sxs-lookup"><span data-stu-id="fd0a1-119">Routing and Remote Access Registry Layout</span></span>](routing-and-remote-access-registry-layout.md)<br/>             | <span data-ttu-id="fd0a1-120">Пример макета реестра для службы маршрутизатора</span><span class="sxs-lookup"><span data-stu-id="fd0a1-120">An example registry layout for the router service</span></span><br/>                                                          |
| [<span data-ttu-id="fd0a1-121">Коды ошибок маршрутизации и удаленного доступа</span><span class="sxs-lookup"><span data-stu-id="fd0a1-121">Routing and Remote Access Error Codes</span></span>](routing-and-remote-access-error-codes.md)<br/>                     | <span data-ttu-id="fd0a1-122">Список всех кодов ошибок маршрутизации и удаленного доступа.</span><span class="sxs-lookup"><span data-stu-id="fd0a1-122">List of all routing and remote access error codes.</span></span><br/>                                                         |
| [<span data-ttu-id="fd0a1-123">Удаленный доступ</span><span class="sxs-lookup"><span data-stu-id="fd0a1-123">Remote Access</span></span>](remote-access-start-page.md)<br/>                                                          | <span data-ttu-id="fd0a1-124">Документация по API-интерфейсам администрирования RAS и RAS.</span><span class="sxs-lookup"><span data-stu-id="fd0a1-124">Documentation for RAS and RAS Administration APIs.</span></span><br/>                                                         |
| [<span data-ttu-id="fd0a1-125">Маршрутизация</span><span class="sxs-lookup"><span data-stu-id="fd0a1-125">Routing</span></span>](routing-start-page.md)<br/>                                                                      | <span data-ttu-id="fd0a1-126">Документация по API управления маршрутизаторами и базы MIB.</span><span class="sxs-lookup"><span data-stu-id="fd0a1-126">Documentation for the Router Management and Management Information Base (MIB) APIs.</span></span><br/>                        |
| [<span data-ttu-id="fd0a1-127">Протоколы маршрутизации</span><span class="sxs-lookup"><span data-stu-id="fd0a1-127">Routing Protocols</span></span>](routing-protocols-start-page.md)<br/>                                                  | <span data-ttu-id="fd0a1-128">Документация по диспетчеру групп многоадресной рассылки, интерфейсу протокола маршрутизации и интерфейсам API диспетчера таблиц маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="fd0a1-128">Documentation for the Multicast Group Manager, Routing Protocol Interface, and Routing Table Manager APIs.</span></span><br/> |
| [<span data-ttu-id="fd0a1-129">Словарь терминов</span><span class="sxs-lookup"><span data-stu-id="fd0a1-129">Glossary</span></span>](glossary.md)<br/>                                                                               | <span data-ttu-id="fd0a1-130">Определения терминов, используемых в документации по службе маршрутизации и удаленного доступа.</span><span class="sxs-lookup"><span data-stu-id="fd0a1-130">Definitions for terms used in the Routing and Remote Access Service documentation.</span></span><br/>                         |



 

 

 





