---
description: Как правило, поставщик услуг мультимедиа (MSP) реализует создание терминалов.
ms.assetid: 203fccc0-aa5a-4ec3-97d3-546c36018d52
title: Написание подключаемого терминала
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6cbfe2da0c121fcee820d47fd57216840d23c59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542439"
---
# <a name="writing-a-pluggable-terminal"></a><span data-ttu-id="f0826-103">Написание подключаемого терминала</span><span class="sxs-lookup"><span data-stu-id="f0826-103">Writing a Pluggable Terminal</span></span>

<span data-ttu-id="f0826-104">Как правило, поставщик услуг мультимедиа (MSP) реализует создание терминалов.</span><span class="sxs-lookup"><span data-stu-id="f0826-104">Normally, a media service provider (MSP) implements terminal creation.</span></span> <span data-ttu-id="f0826-105">Начиная с Windows 2000 с пакетом обновления 1 (SP1), TAPI 3 включает в себя подключаемые терминалы, позволяющие приложению реализовать создание терминалов.</span><span class="sxs-lookup"><span data-stu-id="f0826-105">Starting with Windows 2000 SP1, TAPI 3 includes pluggable terminals to allow an application to implement terminal creation.</span></span> <span data-ttu-id="f0826-106">Дополнительные сведения об использовании этих терминалов см. в обзоре [реализации подключаемых терминалов](implementing-pluggable-terminals.md) .</span><span class="sxs-lookup"><span data-stu-id="f0826-106">Please see the overview on [implementing pluggable terminals](implementing-pluggable-terminals.md) for additional information on using these terminals.</span></span>

<span data-ttu-id="f0826-107">Не следует использовать подключаемые терминалы, так как все возможности терминала будут доступны только после того, как MSP полностью знает его.</span><span class="sxs-lookup"><span data-stu-id="f0826-107">You should not use pluggable terminals routinely because the full capabilities of a terminal will only be available when an MSP is fully aware of it.</span></span> <span data-ttu-id="f0826-108">Кроме того, не следует пытаться реализовать подключаемые терминалы, если вы уже не знакомы с написанием поставщиков услуг мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f0826-108">Further, you should not attempt to implement pluggable terminals unless you are already familiar with writing media service providers.</span></span> <span data-ttu-id="f0826-109">Методы и потенциальные проблемы очень похожи.</span><span class="sxs-lookup"><span data-stu-id="f0826-109">The techniques and potential problems involved are quite similar.</span></span>

<span data-ttu-id="f0826-110">Подготавливается к Специальному варианту подключаемого терминала, который в настоящее время существует в ситуации, когда сервер конференций должен добавить клиенты, не относящиеся к Windows 2000 с пакетом обновления 1 (SP1) или многоадресную рассылку пакетов H. 323, на многосторонние конференции SDP/IP.</span><span class="sxs-lookup"><span data-stu-id="f0826-110">Provision for a special case of pluggable terminal currently exists for the situation of a conferencing server that needs to add non-Windows 2000 SP1 or nonmulticast H.323 clients to TAPI 3 multiparty SDP/IP multicast conferences.</span></span>

 

 



