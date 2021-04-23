---
description: Интерфейс поставщика службы Windows Sockets (Winsock).
ms.assetid: 59ac7ce6-10e7-40ac-bdce-dc01251b0bc5
title: Winsock SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ecf63a45f5175a86b8f5eb2a77ef0293182e38f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650834"
---
# <a name="winsock-spi"></a><span data-ttu-id="e07e2-103">Winsock SPI</span><span class="sxs-lookup"><span data-stu-id="e07e2-103">Winsock SPI</span></span>

<span data-ttu-id="e07e2-104">Интерфейс поставщика услуг Winsock или Winsock SPI является специализированной дисциплиной Winsock, используемой для создания поставщиков. в таких поставщиках транспорта, как TCP/IP или IPX/SPX, используется протокол Winsock SPI, как и поставщики пространства имен, такие как система именования доменов Интернета (DNS).</span><span class="sxs-lookup"><span data-stu-id="e07e2-104">The Winsock Service Provider Interface, or Winsock SPI, is a specialized discipline of Winsock used to create providers; transport providers such as TCP/IP or IPX/SPX protocol stacks use the Winsock SPI, as do namespace providers such as the Internet's Domain Naming System (DNS).</span></span>

<span data-ttu-id="e07e2-105">Традиционное сетевое программирование, например включение взаимодействия приложений по сети, не требует использования интерфейсов Winsock SPI. Вместо этого используйте стандартные интерфейсы [Winsock](winsock-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="e07e2-105">Traditional network programming, such as enabling applications to communicate over the network, does not require use of Winsock SPI interfaces; use standard [Winsock](winsock-reference.md) interfaces instead.</span></span>

 

<span data-ttu-id="e07e2-106">В стандарте Winsock SPI используется следующее соглашение об именовании префикса функции.</span><span class="sxs-lookup"><span data-stu-id="e07e2-106">The Winsock SPI uses the following function prefix naming convention.</span></span>



| <span data-ttu-id="e07e2-107">Prefix</span><span class="sxs-lookup"><span data-stu-id="e07e2-107">Prefix</span></span> | <span data-ttu-id="e07e2-108">Значение</span><span class="sxs-lookup"><span data-stu-id="e07e2-108">Meaning</span></span>                          | <span data-ttu-id="e07e2-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e07e2-109">Description</span></span>                                       |
|--------|----------------------------------|---------------------------------------------------|
| <span data-ttu-id="e07e2-110">WPS</span><span class="sxs-lookup"><span data-stu-id="e07e2-110">WSP</span></span>    | <span data-ttu-id="e07e2-111">Поставщик службы сокетов Windows</span><span class="sxs-lookup"><span data-stu-id="e07e2-111">Windows Sockets Service Provider</span></span> | <span data-ttu-id="e07e2-112">Точки входа поставщика услуг транспорта</span><span class="sxs-lookup"><span data-stu-id="e07e2-112">Transport service provider entry points</span></span>           |
| <span data-ttu-id="e07e2-113">впу</span><span class="sxs-lookup"><span data-stu-id="e07e2-113">WPU</span></span>    | <span data-ttu-id="e07e2-114">Вызов поставщика сокетов Windows</span><span class="sxs-lookup"><span data-stu-id="e07e2-114">Windows Sockets Provider Upcall</span></span>  | <span data-ttu-id="e07e2-115">Ws2 \_32.dll точки входа для поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="e07e2-115">Ws2\_32.dll entry points for service providers</span></span>    |
| <span data-ttu-id="e07e2-116">WSC</span><span class="sxs-lookup"><span data-stu-id="e07e2-116">WSC</span></span>    | <span data-ttu-id="e07e2-117">Конфигурация сокетов Windows</span><span class="sxs-lookup"><span data-stu-id="e07e2-117">Windows Sockets Configuration</span></span>    | <span data-ttu-id="e07e2-118">WS2 \_32.dll точки входа для приложений установки</span><span class="sxs-lookup"><span data-stu-id="e07e2-118">WS2\_32.dll entry points for installation applets</span></span> |
| <span data-ttu-id="e07e2-119">NSP</span><span class="sxs-lookup"><span data-stu-id="e07e2-119">NSP</span></span>    | <span data-ttu-id="e07e2-120">Поставщик пространства имен</span><span class="sxs-lookup"><span data-stu-id="e07e2-120">Namespace Provider</span></span>               | <span data-ttu-id="e07e2-121">Точки входа поставщика пространства имен</span><span class="sxs-lookup"><span data-stu-id="e07e2-121">Namespace provider entry points</span></span>                   |



 

 

 



