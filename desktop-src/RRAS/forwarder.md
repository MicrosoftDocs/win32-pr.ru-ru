---
title: Сервер пересылки
description: Сервер пересылки является компонентом режима ядра маршрутизатора, который отвечает за пересылку данных из одного интерфейса маршрутизатора в другие.
ms.assetid: 69cdbefa-9137-48cb-940a-badfb3f4f231
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52885000a9f1fcc117cd1fefc207531b9b524e74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068022"
---
# <a name="forwarder"></a><span data-ttu-id="b2326-103">Сервер пересылки</span><span class="sxs-lookup"><span data-stu-id="b2326-103">Forwarder</span></span>

<span data-ttu-id="b2326-104">Сервер пересылки является компонентом режима ядра маршрутизатора, который отвечает за пересылку данных из одного интерфейса маршрутизатора в другие.</span><span class="sxs-lookup"><span data-stu-id="b2326-104">The forwarder is the kernel-mode component of the router that is responsible for forwarding data from one router interface to the others.</span></span> <span data-ttu-id="b2326-105">Сервер пересылки также определяет, предназначен ли пакет для локальной доставки, является ли он направленным из другого интерфейса или обоими.</span><span class="sxs-lookup"><span data-stu-id="b2326-105">The forwarder also decides whether a packet is destined for local delivery, whether it is destined to be forwarded out of another interface, or both.</span></span>

<span data-ttu-id="b2326-106">Существует два сервера пересылки в режиме ядра: одноадресная рассылка и многоадресная рассылка.</span><span class="sxs-lookup"><span data-stu-id="b2326-106">There are two kernel-mode forwarders: unicast and multicast.</span></span>

<span data-ttu-id="b2326-107">Диспетчер маршрутизаторов получает лучшие маршруты ко всем местам назначения из диспетчера таблиц маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="b2326-107">The router manager obtains the best routes to all destinations from the routing table manager.</span></span> <span data-ttu-id="b2326-108">Эти маршруты передаются в одноадресный перенаправитель.</span><span class="sxs-lookup"><span data-stu-id="b2326-108">These routes are passed to the unicast forwarder.</span></span> <span data-ttu-id="b2326-109">Одноадресный перенаправитель использует эти маршруты для выполнения фактической пересылки данных одноадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="b2326-109">The unicast forwarder uses these routes to perform the actual forwarding of unicast data.</span></span> <span data-ttu-id="b2326-110">Таким образом, одноадресный перенаправитель поддерживает кэш лучших маршрутов в представлении одноадресной рассылки таблицы маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="b2326-110">In this manner, the unicast forwarder maintains a cache of the best routes in the unicast view of the routing table.</span></span>

<span data-ttu-id="b2326-111">Диспетчер групп многоадресной рассылки использует сведения из представления многоадресной рассылки таблицы маршрутизации для добавления записей многоадресной рассылки в многоадресный сервер пересылки.</span><span class="sxs-lookup"><span data-stu-id="b2326-111">The multicast group manager uses information from the multicast view of the routing table to add multicast forwarding entries to the multicast forwarder.</span></span>

 

 




