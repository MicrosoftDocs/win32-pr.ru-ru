---
description: В этом разделе описываются расширения Winsock, относящиеся к обмену пакетами с Exchange/виртуализированными пакетами (IPX/SPX). В нем также описываются аспекты базовых функций Winsock, которые либо потребовали особого внимания, либо могут демонстрировать уникальное поведение.
ms.assetid: 8447e063-767a-40b8-b094-724393e85be2
title: Приложение Winsock IPX/SPX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c533781fa07c997d7f2363dd6b00d6b4213f22e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701791"
---
# <a name="winsock-ipxspx-annex"></a><span data-ttu-id="08dbe-104">Приложение Winsock IPX/SPX</span><span class="sxs-lookup"><span data-stu-id="08dbe-104">Winsock IPX/SPX Annex</span></span>

<span data-ttu-id="08dbe-105">В этом разделе описываются расширения Winsock, относящиеся к обмену пакетами с Exchange/виртуализированными пакетами (IPX/SPX).</span><span class="sxs-lookup"><span data-stu-id="08dbe-105">This section describes Winsock extensions specific to Internetwork Packet Exchange/Sequenced Packet Exchange (IPX/SPX).</span></span> <span data-ttu-id="08dbe-106">В нем также описываются аспекты базовых функций Winsock, которые либо потребовали особого внимания, либо могут демонстрировать уникальное поведение.</span><span class="sxs-lookup"><span data-stu-id="08dbe-106">It also describes aspects of base Winsock functions that either require special consideration or may exhibit unique behavior.</span></span>



| <span data-ttu-id="08dbe-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="08dbe-107">Element</span></span>          | <span data-ttu-id="08dbe-108">Описание</span><span class="sxs-lookup"><span data-stu-id="08dbe-108">Description</span></span>                                                                                                                                     |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08dbe-109">Имена протоколов</span><span class="sxs-lookup"><span data-stu-id="08dbe-109">Protocol name(s)</span></span> | <span data-ttu-id="08dbe-110">IPX, SPX</span><span class="sxs-lookup"><span data-stu-id="08dbe-110">IPX, SPX</span></span>                                                                                                                                        |
| <span data-ttu-id="08dbe-111">Описание</span><span class="sxs-lookup"><span data-stu-id="08dbe-111">Description</span></span>      | <span data-ttu-id="08dbe-112">Предоставляет транспортные службы на уровне сети IPX: IPX для ненадежных датаграмм, SPX для надежных потоков сообщений, ориентированных на подключение.</span><span class="sxs-lookup"><span data-stu-id="08dbe-112">Provides transport services over the IPX networking layer: IPX for unreliable datagrams, SPX for reliable, connection-oriented message streams.</span></span> |
| <span data-ttu-id="08dbe-113">Семейство адресов</span><span class="sxs-lookup"><span data-stu-id="08dbe-113">Address family</span></span>   | <span data-ttu-id="08dbe-114">AF \_ IPX</span><span class="sxs-lookup"><span data-stu-id="08dbe-114">AF\_IPX</span></span>                                                                                                                                         |
| <span data-ttu-id="08dbe-115">Файл заголовка</span><span class="sxs-lookup"><span data-stu-id="08dbe-115">Header file</span></span>      | <span data-ttu-id="08dbe-116">Всипкс. h</span><span class="sxs-lookup"><span data-stu-id="08dbe-116">Wsipx.h</span></span>                                                                                                                                         |



 

<span data-ttu-id="08dbe-117">В этом разделе описывается использование Winsock с семейством протоколов IPX, что позволяет использовать традиционные приложения IPX для переноса в Winsock.</span><span class="sxs-lookup"><span data-stu-id="08dbe-117">This section discusses how to use Winsock with the IPX family of protocols, enabling traditional IPX applications to be ported to Winsock.</span></span> <span data-ttu-id="08dbe-118">Сети IPX работают так же, как и IP-сети, поэтому при использовании IPX/SPX следует учитывать такие различия.</span><span class="sxs-lookup"><span data-stu-id="08dbe-118">IPX networks operate in a fundamentally different manner than IP networks, so such differences must be considered when using IPX/SPX.</span></span>

 

 



