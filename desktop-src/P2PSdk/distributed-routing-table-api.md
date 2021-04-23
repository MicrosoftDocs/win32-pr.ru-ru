---
description: API таблицы распределенной маршрутизации (DRT) позволяет приложениям публиковать и разрешать цифровые ключи в одноранговой сети.
ms.assetid: 17422d71-4c6d-458b-87b6-b31fc2b5bda5
title: API таблиц распределенной маршрутизации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f8c2b435e1c0c813fb279c40b9bbfa9afb6b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080797"
---
# <a name="distributed-routing-table-api"></a><span data-ttu-id="d1b4a-103">API таблиц распределенной маршрутизации</span><span class="sxs-lookup"><span data-stu-id="d1b4a-103">Distributed Routing Table API</span></span>

<span data-ttu-id="d1b4a-104">API таблицы распределенной маршрутизации (DRT) позволяет приложениям публиковать и разрешать цифровые ключи в одноранговой сети.</span><span class="sxs-lookup"><span data-stu-id="d1b4a-104">The Distributed Routing Table (DRT) API allows applications to publish and resolve numeric keys in a peer network.</span></span>

<span data-ttu-id="d1b4a-105">Приложение, использующее DRT, может выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="d1b4a-105">An application utilizing DRT can accomplish the following:</span></span>

-   <span data-ttu-id="d1b4a-106">Создание распределенных таблиц маршрутизации для конкретных приложений.</span><span class="sxs-lookup"><span data-stu-id="d1b4a-106">Create application-specific Distributed Routing Tables.</span></span>
-   <span data-ttu-id="d1b4a-107">Регистрация ключей и связывание этих ключей с IP-адресами и данными приложений.</span><span class="sxs-lookup"><span data-stu-id="d1b4a-107">Register keys, and associate these keys with IP addresses and application data.</span></span>
-   <span data-ttu-id="d1b4a-108">Выполните поиск ключей и получите связанные с ними IP-адреса и данные приложений.</span><span class="sxs-lookup"><span data-stu-id="d1b4a-108">Search for keys and retrieve the IP addresses and application data associated with them.</span></span> <span data-ttu-id="d1b4a-109">Эта функция может использоваться для создания распределенных хэш-таблиц (Дхтс), бессерверных систем разрешения имен и наложения сетей сетки многих топологий.</span><span class="sxs-lookup"><span data-stu-id="d1b4a-109">This functionality can be used to construct Distributed Hash Tables (DHTs), serverless name resolution systems, and overlay mesh networks of many topologies.</span></span>

> [!Note]  
> <span data-ttu-id="d1b4a-110">Администраторы и пользователи приложений с поддержкой DRT должны быть уверены в том, что конечные пользователи своих приложений знают, какие сведения публикуются.</span><span class="sxs-lookup"><span data-stu-id="d1b4a-110">The administrators and users of DRT-enabled applications should make the end users of their applications aware of the information being published.</span></span> <span data-ttu-id="d1b4a-111">Серверы Майкрософт не работают с этой технологией, и информация не отправляется в корпорацию Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="d1b4a-111">Microsoft servers are not employed by this technology and information is not sent to Microsoft.</span></span>

 

<span data-ttu-id="d1b4a-112">Предоставленная документация по этому API делится на три раздела.</span><span class="sxs-lookup"><span data-stu-id="d1b4a-112">The provided documentation for this API is divided into three sections.</span></span>



| <span data-ttu-id="d1b4a-113">Section</span><span class="sxs-lookup"><span data-stu-id="d1b4a-113">Section</span></span>                                                                                | <span data-ttu-id="d1b4a-114">Описание</span><span class="sxs-lookup"><span data-stu-id="d1b4a-114">Description</span></span>                                                                                                          |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1b4a-115">Сведения о таблицах распределенной маршрутизации</span><span class="sxs-lookup"><span data-stu-id="d1b4a-115">About Distributed Routing Tables</span></span>](about-distributed-routing-tables.md)               | <span data-ttu-id="d1b4a-116">Сведения о жизненном цикле и изменениях состояния API DRT.</span><span class="sxs-lookup"><span data-stu-id="d1b4a-116">Information detailing the life cycle and state changes of the DRT API.</span></span><br/>                                    |
| [<span data-ttu-id="d1b4a-117">Использование API таблиц распределенной маршрутизации</span><span class="sxs-lookup"><span data-stu-id="d1b4a-117">Using the Distributed Routing Table API</span></span>](using-the-distributed-routing-table-api.md) | <span data-ttu-id="d1b4a-118">Сведения об общем использовании API DRT.</span><span class="sxs-lookup"><span data-stu-id="d1b4a-118">Information detailing the general usage of the DRT API.</span></span><br/>                                                   |
| [<span data-ttu-id="d1b4a-119">Справочник по распределенной маршрутизации API таблиц</span><span class="sxs-lookup"><span data-stu-id="d1b4a-119">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md) | <span data-ttu-id="d1b4a-120">Сведения о функциях, структурах данных и перечислимых константах, составляющих API DRT.</span><span class="sxs-lookup"><span data-stu-id="d1b4a-120">Information detailing the functions, data structures, and enumerated constants that comprise the DRT API.</span></span><br/> |



 

 

 




