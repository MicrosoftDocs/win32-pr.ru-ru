---
description: Терминал с многодорожкностью можно рассматривать как терминал, который является коллекцией других терминалов. Каждый дочерний терминал (a &\# 0034; track&\# 0034;) может быть терминалом с несколькими дорожками или терминалом с одной дорожкой.
ms.assetid: bf23bc26-5763-45a3-a63d-e43ce2480956
title: О терминалах с многодорожкностью
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58042236c737f6ab0b933699d75e19358f6e6b81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673722"
---
# <a name="about-multitrack-terminals"></a><span data-ttu-id="0a9fe-104">О терминалах с многодорожкностью</span><span class="sxs-lookup"><span data-stu-id="0a9fe-104">About Multitrack Terminals</span></span>

<span data-ttu-id="0a9fe-105">Терминал с многодорожкностью можно рассматривать как терминал, который является коллекцией других терминалов.</span><span class="sxs-lookup"><span data-stu-id="0a9fe-105">A multitrack terminal can be thought of as a terminal that is a collection of other terminals.</span></span> <span data-ttu-id="0a9fe-106">Каждый дочерний терминал ("Track") может быть терминалом с несколькими дорожками или терминалом с одной дорожкой.</span><span class="sxs-lookup"><span data-stu-id="0a9fe-106">Each child terminal (a "track") can be a multitrack terminal or a single-track terminal.</span></span>

<span data-ttu-id="0a9fe-107">Все терминалы многодорожкности предоставляют интерфейс [**итмултитракктерминал**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) , который включает универсальные методы для перечисления, создания и удаления терминалов из терминала с многодорожкностью.</span><span class="sxs-lookup"><span data-stu-id="0a9fe-107">All multitrack terminals expose the [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) interface, which includes generic methods for enumerating, creating, and removing track terminals from a multitrack terminal.</span></span> <span data-ttu-id="0a9fe-108">Все терминалы, одна и многодорожкные, предоставляют интерфейс [**иттерминал**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) .</span><span class="sxs-lookup"><span data-stu-id="0a9fe-108">All terminals, single-track and multitrack, expose the [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface.</span></span>

<span data-ttu-id="0a9fe-109">Клиент, имеющий указатель на интерфейс [**иттерминал**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) , может определить, является ли терминал многодорожкным или единственной записью, запрашивая интерфейс [**итмултитракктерминал**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) , который доступен только для терминалов с несколькими дорожками.</span><span class="sxs-lookup"><span data-stu-id="0a9fe-109">A client that has a pointer to an [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface can discover whether the terminal is multitrack or single-track by querying the terminal for the [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) interface, which is exposed only on multitrack terminals.</span></span>

<span data-ttu-id="0a9fe-110">Родительский терминал может использовать интерфейс [**иттерминал**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) своих терминалов Track или может потребовать, чтобы терминалы мониторинга могли предоставлять частные интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="0a9fe-110">The parent terminal may use the [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface of its track terminals, or it may require track terminals to expose private interfaces.</span></span>

<span data-ttu-id="0a9fe-111">Дополнительные сведения см. в разделе [Tracking терминала](track-terminals.md).</span><span class="sxs-lookup"><span data-stu-id="0a9fe-111">For more information, see [Track Terminals](track-terminals.md).</span></span>

 

 
