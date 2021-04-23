---
description: Winsock предоставляет интерфейс поставщика услуг для создания служб Winsock, обычно называемый Winsock SPI.
ms.assetid: e3d21dd8-2b58-4108-857d-a075b8be68b0
title: Сведения об использовании Winsock SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe70d5d381505085e2794a57a1183e8bec505917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145124"
---
# <a name="about-the-winsock-spi"></a><span data-ttu-id="bc747-103">Сведения об использовании Winsock SPI</span><span class="sxs-lookup"><span data-stu-id="bc747-103">About the Winsock SPI</span></span>

<span data-ttu-id="bc747-104">Winsock предоставляет интерфейс поставщика услуг для создания служб Winsock, обычно называемый Winsock SPI.</span><span class="sxs-lookup"><span data-stu-id="bc747-104">Winsock provides a Service Provider Interface for creating Winsock services, commonly referred to as the Winsock SPI.</span></span> <span data-ttu-id="bc747-105">Существует два типа поставщиков услуг: поставщики транспорта и поставщики пространств имен.</span><span class="sxs-lookup"><span data-stu-id="bc747-105">Two types of service providers exist: transport providers and namespace providers.</span></span> <span data-ttu-id="bc747-106">Примеры поставщиков транспорта включают в себя стеки протоколов, такие как TCP/IP или IPX/SPX, а пример поставщика пространства имен — интерфейс системы доменных имен (DNS) в Интернете.</span><span class="sxs-lookup"><span data-stu-id="bc747-106">Examples of transport providers include protocol stacks such as TCP/IP or IPX/SPX, while an example of a namespace provider would be an interface to the Internet's Domain Naming System (DNS).</span></span> <span data-ttu-id="bc747-107">Отдельные разделы спецификации интерфейса поставщика услуг относятся к каждому типу поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="bc747-107">Separate sections of the service provider interface specification apply to each type of service provider.</span></span>

<span data-ttu-id="bc747-108">Поставщики услуг [транспорта](transport-service-providers-2.md) и [пространств имен](name-space-service-providers-2.md) должны быть зарегистрированы в \_32.dll Ws2 во время их установки.</span><span class="sxs-lookup"><span data-stu-id="bc747-108">[Transport](transport-service-providers-2.md) and [namespace](name-space-service-providers-2.md) service providers must be registered with the Ws2\_32.dll at the time they are installed.</span></span> <span data-ttu-id="bc747-109">Эту регистрацию необходимо выполнять только один раз для каждого поставщика, так как необходимые сведения сохраняются в постоянном хранилище.</span><span class="sxs-lookup"><span data-stu-id="bc747-109">This registration need only be done once for each provider as the necessary information is retained in persistent storage.</span></span>

 

 



