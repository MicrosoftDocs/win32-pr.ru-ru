---
description: Чтобы установить соединение между клиентом и сервером с помощью протокола SMB Microsoft, необходимо сначала определить диалект с самым высоким уровнем функциональности, который поддерживает клиент и сервер.
ms.assetid: ad48391b-fcc7-4e58-83bb-6084503c8d61
title: Диалекты протокола SMB (Майкрософт)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f35d3fbcaa3345e2981df797f115e88064e38f04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497301"
---
# <a name="microsoft-smb-protocol-dialects"></a><span data-ttu-id="0584c-103">Диалекты протокола SMB (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="0584c-103">Microsoft SMB Protocol Dialects</span></span>

<span data-ttu-id="0584c-104">Список пакетов сообщений протокола Microsoft SMB увеличился в течение нескольких лет, чтобы обеспечить повышение функциональности протокола SMB Microsoft, а теперь числа в сотнях.</span><span class="sxs-lookup"><span data-stu-id="0584c-104">The list of Microsoft SMB Protocol message packets has grown over the years to accommodate the increasing functionality of Microsoft SMB Protocol, and now numbers in the hundreds.</span></span> <span data-ttu-id="0584c-105">Каждый этап его роста отмечается стандартным набором пакетов или диалектом.</span><span class="sxs-lookup"><span data-stu-id="0584c-105">Each stage of its growth is marked by a standard packet set, or dialect.</span></span> <span data-ttu-id="0584c-106">Каждый диалект определяется стандартной строкой, такой как "Компьютерная программа для ПК 1,0", "сети MICROSOFT 3,0", "DOS LANMAN 2,1" или "NT LM 0,12".</span><span class="sxs-lookup"><span data-stu-id="0584c-106">Each dialect is identified by a standard string such as "PC NETWORK PROGRAM 1.0", "MICROSOFT NETWORKS 3.0", "DOS LANMAN 2.1", or "NT LM 0.12".</span></span> <span data-ttu-id="0584c-107">Первая строка определяет первый диалект SMB, а последняя строка идентифицирует CIFS, первый диалект протокола SMB Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0584c-107">The first string identifies the first dialect of SMB, and the last string identifies CIFS, the first dialect of Microsoft SMB Protocol.</span></span>

<span data-ttu-id="0584c-108">Большинство клиентов Windows поддерживают по крайней мере шесть разных разновидностей протокола SMB Microsoft, поэтому один из первых шагов в установке подключения между клиентом и сервером с помощью протокола SMB Microsoft — определение диалекта с самым высоким уровнем функциональности, поддерживаемым как клиентом, так и сервером.</span><span class="sxs-lookup"><span data-stu-id="0584c-108">Most Windows clients support at least six different dialects of Microsoft SMB Protocol, so one of the first steps in establishing a connection between a client and a server using Microsoft SMB Protocol is to determine the dialect with the highest level of functionality that both the client and server support.</span></span> <span data-ttu-id="0584c-109">Этот процесс известен как «согласование диалекта».</span><span class="sxs-lookup"><span data-stu-id="0584c-109">This process is known as "negotiating the dialect."</span></span> <span data-ttu-id="0584c-110">Указанные выше строки диалекта включены в запрос на согласование диалекта и пакеты ответа для этой цели.</span><span class="sxs-lookup"><span data-stu-id="0584c-110">The dialect strings mentioned above are included in the dialect negotiation request and response packets for this purpose.</span></span>

 

 



