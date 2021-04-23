---
description: Каждая строка имеет один или несколько каналов. Поставщики услуг обычно обрабатывают, как каналы предоставляются в качестве адресов приложению, а конечному пользователю или серверу не требуются определенные знания о каналах.
ms.assetid: 8c7d38e0-1863-461f-9225-7a0b419532a3
title: Канал (API телефонии)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b793a23c945cad79c9e2401ab6944302e908fd73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543007"
---
# <a name="channel-telephony-api"></a><span data-ttu-id="7067a-104">Канал (API телефонии)</span><span class="sxs-lookup"><span data-stu-id="7067a-104">Channel (Telephony API)</span></span>

<span data-ttu-id="7067a-105">Каждая строка имеет один или несколько каналов.</span><span class="sxs-lookup"><span data-stu-id="7067a-105">Each line has one or more channels.</span></span> <span data-ttu-id="7067a-106">Поставщики услуг обычно обрабатывают, как каналы предоставляются в качестве адресов приложению, а конечному пользователю или серверу не требуются определенные знания о каналах.</span><span class="sxs-lookup"><span data-stu-id="7067a-106">The service providers normally handle how channels are exposed as addresses to an application, and the end user or server does not require specific knowledge of channels.</span></span>

<span data-ttu-id="7067a-107">Каналы идентичны и поэтому взаимозаменяемы.</span><span class="sxs-lookup"><span data-stu-id="7067a-107">Channels are identical and therefore interchangeable.</span></span> <span data-ttu-id="7067a-108">В POTS (обычная старая телефонная служба) в строке имеется ровно один канал, и канал используется исключительно для голоса.</span><span class="sxs-lookup"><span data-stu-id="7067a-108">In POTS (Plain Old Telephone Service), exactly one channel exists on a line, and the channel is used exclusively for voice.</span></span> <span data-ttu-id="7067a-109">В линии ISDN одновременно может существовать не менее трех (и не более 30) каналов.</span><span class="sxs-lookup"><span data-stu-id="7067a-109">With ISDN, at least three (and as many as 30 or more) channels can exist on a line simultaneously.</span></span>

<span data-ttu-id="7067a-110">Каждый канал может иметь свой собственный адрес, то есть линия может иметь столько адресов, сколько есть каналов.</span><span class="sxs-lookup"><span data-stu-id="7067a-110">Each channel can have its own address, which means a line could have as many addresses as it has channels.</span></span> <span data-ttu-id="7067a-111">Точная связь между каналами и адресами, предоставляемыми приложению, зависит от реализации поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="7067a-111">The precise relationship between channels and addresses exposed to an application is dependent on a service provider's implementation.</span></span>

<span data-ttu-id="7067a-112">Некоторые поставщики услуг поддерживают назначение нескольких адресов одному каналу.</span><span class="sxs-lookup"><span data-stu-id="7067a-112">Some service providers support the assignment of more than one address to a single channel.</span></span> <span data-ttu-id="7067a-113">В POTS-строках несколько адресов возможны в различных системах, например при прямом наборе номеров или различении звонков, которые являются услугами дополнительной платы, предоставляемой телефонной компанией.</span><span class="sxs-lookup"><span data-stu-id="7067a-113">On POTS lines, multiple addresses are made possible by various systems, such as direct inward dialing (DID) or distinctive ringing, which are extra-fee services that the telephone company provides.</span></span>

<span data-ttu-id="7067a-114">Многие крупные организации используют для входящих вызовов.</span><span class="sxs-lookup"><span data-stu-id="7067a-114">Many large corporations use DID for incoming calls.</span></span> <span data-ttu-id="7067a-115">Перед подключением к подключению номер расширения назначения сообщает УАТС, в результате чего расширение будет звонить вместо телефона оператора.</span><span class="sxs-lookup"><span data-stu-id="7067a-115">Before a call is connected, its destination extension number is signaled to the PBX, which causes the extension to ring instead of the operator's phone.</span></span> <span data-ttu-id="7067a-116">Примером различения звонков в частной домашней папке может быть то, что родители использовали один адрес, потомки другого и Факс-компьютер в третьем.</span><span class="sxs-lookup"><span data-stu-id="7067a-116">An example of distinctive ringing in a private home would be if the parents used one address, the children another, and a fax machine a third.</span></span> <span data-ttu-id="7067a-117">Так как только одна линия соединяет дом с телефонной сетью, все телефонные звонки при вызове отображаются, но шаблон кольца различается в зависимости от номера абонентской стороны.</span><span class="sxs-lookup"><span data-stu-id="7067a-117">Because only one line connects the house to the telephone network, all phones ring when a call appears, but the ring pattern is different depending on the number that the calling party dialed.</span></span> <span data-ttu-id="7067a-118">С помощью различения звонков пользователи узнают, для кого предназначен входящий звонок, а компьютер факса отвечает на вызовы, распознающим собственный стиль звонка.</span><span class="sxs-lookup"><span data-stu-id="7067a-118">With distinctive ringing, the people know who the incoming call is for, and the fax machine answers its calls by recognizing its own ringing style.</span></span>

<span data-ttu-id="7067a-119">В ISDN различные каналы B могут не иметь отдельных адресов.</span><span class="sxs-lookup"><span data-stu-id="7067a-119">In ISDN, the various B channels might not have separate addresses.</span></span> <span data-ttu-id="7067a-120">Так как эти каналы B могут находиться на одном и том же адресе, это поставщик услуг (а не приложение или пользователь, который набирает номер), который назначает вызовы этим каналам.</span><span class="sxs-lookup"><span data-stu-id="7067a-120">Because these B channels might be on the same address, it is the service provider (and not the application or a person who has dialed the number) that assigns calls to these channels.</span></span>

 

 



