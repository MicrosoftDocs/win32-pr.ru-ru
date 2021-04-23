---
title: О Windows Connect Now
description: Windows Connect Now (WCN) предоставляет простой и безопасный механизм для точек доступа к сети и устройств (например, принтеров, камер и компьютеров) для подключения и настройки Exchange.
ms.assetid: 5c654800-e58b-4a94-b7a6-9a603f540603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0118c6a053c480a36138f8dae850ee0862501944
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134419"
---
# <a name="about-windows-connect-now"></a><span data-ttu-id="d4836-103">О Windows Connect Now</span><span class="sxs-lookup"><span data-stu-id="d4836-103">About Windows Connect Now</span></span>

<span data-ttu-id="d4836-104">Windows Connect Now (WCN) предоставляет простой и безопасный механизм для точек доступа к сети и устройств (например, принтеров, камер и компьютеров) для подключения и настройки Exchange.</span><span class="sxs-lookup"><span data-stu-id="d4836-104">Windows Connect Now (WCN) provides a simple and secure mechanism for network access points and devices (like printers, camera, and PCs) to connect and exchange settings.</span></span> <span data-ttu-id="d4836-105">Этот API является Wi-Fi реализацией корпорацией Майкрософт протокола/Ви-фи Protected Configuration (WPS), которая была создана Wi-Fi Alliance в качестве решения для домашних сетей и малых предприятий.</span><span class="sxs-lookup"><span data-stu-id="d4836-105">This API is the Microsoft implementation of the Wi-Fi Protected Setup (WPS)/Wi-Fi Simple Configuration (WSC) protocol, which was created by the Wi-Fi Alliance as a solution for home networking and small businesses.</span></span> <span data-ttu-id="d4836-106">Эта технология не предназначена для корпоративных сценариев.</span><span class="sxs-lookup"><span data-stu-id="d4836-106">This technology is not intended for enterprise scenarios.</span></span>

> [!Note]  
> <span data-ttu-id="d4836-107">Имя спецификации изменилось между версией 1.0 h и версией 2.</span><span class="sxs-lookup"><span data-stu-id="d4836-107">The specification name changed between version 1.0h and version 2.</span></span> <span data-ttu-id="d4836-108">Спецификация версии 1.0 h называлась Wi-Fi защищенная установка (WPS).</span><span class="sxs-lookup"><span data-stu-id="d4836-108">The version 1.0h specification was named Wi-Fi Protected Setup (WPS).</span></span> <span data-ttu-id="d4836-109">Начиная с спецификации версии 2, спецификация называется Wi-Fi Simple Configuration (WSC).</span><span class="sxs-lookup"><span data-stu-id="d4836-109">Starting with version 2 specification, the specification is named Wi-Fi Simple Configuration (WSC).</span></span> <span data-ttu-id="d4836-110">В нашей документации термины WPS и WSC используются взаимозаменяемыми, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="d4836-110">In our documentation, the terms WPS and WSC are used interchangeably unless noted.</span></span>

 

<span data-ttu-id="d4836-111">Windows Connect теперь позволяет приложениям искать устройства с поддержкой WCN с помощью [API обнаружения функций](/previous-versions/windows/desktop/fundisc/fd-portal).</span><span class="sxs-lookup"><span data-stu-id="d4836-111">Windows Connect Now enables applications to search for WCN-capable devices using the [Function Discovery API](/previous-versions/windows/desktop/fundisc/fd-portal).</span></span> <span data-ttu-id="d4836-112">Область поиска можно сократить до определенного идентификатора SSID, состояния, категории или даже расширить для включения всех устройств с поддержкой WCN.</span><span class="sxs-lookup"><span data-stu-id="d4836-112">The scope of a search can be narrowed down to a specific SSID, state, category, or even broadened to include all WCN-capable devices.</span></span> <span data-ttu-id="d4836-113">После обнаружения устройств API WCN позволяет обмениваться данными с устройством с поддержкой WCN для упрощения настройки или подключения.</span><span class="sxs-lookup"><span data-stu-id="d4836-113">Once devices are located, the WCN API allows communication with the WCN-capable device in order to facilitate configuration or connectivity.</span></span>

 

 