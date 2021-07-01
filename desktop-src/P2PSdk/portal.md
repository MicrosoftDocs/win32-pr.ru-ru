---
description: Одноранговая сеть
ms.assetid: a85fe46c-ce5f-4978-aa37-a3666560426b
title: Одноранговая сеть
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed371f203d34166f1d84462a363326adc32100ae
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118609"
---
# <a name="peer-to-peer"></a><span data-ttu-id="6cc52-103">Одноранговая сеть</span><span class="sxs-lookup"><span data-stu-id="6cc52-103">Peer-to-Peer</span></span>

## <a name="purpose"></a><span data-ttu-id="6cc52-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="6cc52-104">Purpose</span></span>

<span data-ttu-id="6cc52-105">Одноранговые технологии используются для упрощения взаимодействия и совместной работы в распределенных сетях в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="6cc52-105">Peer-to-peer technologies are used to facilitate real-time communication and collaboration across distributed networks.</span></span>

<span data-ttu-id="6cc52-106">В одноранговой модели без использования серверов Интернета каждый пользователь компьютера может выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="6cc52-106">In the peer-to-peer model, without using Internet servers, each PC user can do the following:</span></span>

-   <span data-ttu-id="6cc52-107">Обмен данными</span><span class="sxs-lookup"><span data-stu-id="6cc52-107">Exchange data</span></span>
-   <span data-ttu-id="6cc52-108">Общий доступ к ресурсам</span><span class="sxs-lookup"><span data-stu-id="6cc52-108">Share resources</span></span>
-   <span data-ttu-id="6cc52-109">Обнаружение других пользователей</span><span class="sxs-lookup"><span data-stu-id="6cc52-109">Locate other users</span></span>
-   <span data-ttu-id="6cc52-110">Сообща</span><span class="sxs-lookup"><span data-stu-id="6cc52-110">Communicate</span></span>
-   <span data-ttu-id="6cc52-111">Непосредственная совместная работа в режиме реального времени</span><span class="sxs-lookup"><span data-stu-id="6cc52-111">Collaborate directly in real time</span></span>

<span data-ttu-id="6cc52-112">С помощью одноранговых технологий приложения, которые координируют использование циклов ЦП компьютера и хранилища, могут совместно использовать ресурсы в небольших или больших группах компьютеров, подключенных к Интернету.</span><span class="sxs-lookup"><span data-stu-id="6cc52-112">By using peer-to-peer technologies, applications that coordinate the use of computer CPU cycles and storage can share resources among small or large groups of computers connected to the Internet.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="6cc52-113">Где применимо</span><span class="sxs-lookup"><span data-stu-id="6cc52-113">Where applicable</span></span>

<span data-ttu-id="6cc52-114">Разработчики могут использовать одноранговую инфраструктуру для создания широкого спектра распределенных, специализированных и одноранговых приложений.</span><span class="sxs-lookup"><span data-stu-id="6cc52-114">Developers can use the Peer Infrastructure to create a wide range of distributed, ad-hoc, and peer-to-peer applications.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="6cc52-115">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="6cc52-115">Developer audience</span></span>

<span data-ttu-id="6cc52-116">Разработчики, использующие одноранговую инфраструктуру, должны быть знакомы с концепциями программирования C.</span><span class="sxs-lookup"><span data-stu-id="6cc52-116">Developers using the Peer Infrastructure should be familiar with C programming concepts.</span></span> <span data-ttu-id="6cc52-117">Разработчики, использующие поставщик пространства имен Winsock PNRP, должны быть знакомы с API Winsock.</span><span class="sxs-lookup"><span data-stu-id="6cc52-117">Developers using the PNRP Winsock Namespace Provider should be familiar with the Winsock API.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="6cc52-118">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="6cc52-118">Run-time requirements</span></span>

<span data-ttu-id="6cc52-119">Одноранговая инфраструктура поддерживается в Windows Vista, Windows XP с пакетом обновления 2 (SP2) и более поздних версиях, а также расширенный сетевой пакет для Windows XP, доступный для Windows XP с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="6cc52-119">The Peer Infrastructure is supported in Windows Vista, Windows XP with Service Pack 2 (SP2) and later as well the Advanced Networking Pack for Windows XP available for Windows XP with Service Pack 1 (SP1).</span></span> <span data-ttu-id="6cc52-120">Для одноранговой инфраструктуры необходимо установить протокол IPv6 и запустить его, чтобы обеспечить функционирование приложений одноранговой сети.</span><span class="sxs-lookup"><span data-stu-id="6cc52-120">The Peer-to-Peer Infrastructure requires that IPv6 be installed and initiated to allow peer networking applications to function.</span></span> <span data-ttu-id="6cc52-121">Использование одноранговой совместной работы поддерживается только в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6cc52-121">Use of Peer-to-Peer Collaboration is only supported in Windows Vista .</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6cc52-122">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="6cc52-122">In this section</span></span>



| <span data-ttu-id="6cc52-123">Раздел</span><span class="sxs-lookup"><span data-stu-id="6cc52-123">Topic</span></span>                                                     | <span data-ttu-id="6cc52-124">Описание</span><span class="sxs-lookup"><span data-stu-id="6cc52-124">Description</span></span>                                                                                         |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6cc52-125">Одноранговая инфраструктура</span><span class="sxs-lookup"><span data-stu-id="6cc52-125">Peer Infrastructure</span></span>](peer-infrastructure.md)<br/> | <span data-ttu-id="6cc52-126">Сведения о одноранговой инфраструктуре и протоколе PNRP.</span><span class="sxs-lookup"><span data-stu-id="6cc52-126">Information about the Peer Infrastructure and the Peer Name Resolution Protocol (PNRP).</span></span> <br/> |
| [<span data-ttu-id="6cc52-127">Одноранговая совместная работа</span><span class="sxs-lookup"><span data-stu-id="6cc52-127">Peer Collaboration</span></span>](peer-collaboration.md)<br/>   | <span data-ttu-id="6cc52-128">Сведения и справочные материалы, относящиеся к API одноранговой совместной работы.</span><span class="sxs-lookup"><span data-stu-id="6cc52-128">Information and reference material specific to the Peer Collaboration API.</span></span><br/>               |
| [<span data-ttu-id="6cc52-129">Одноранговое распределение</span><span class="sxs-lookup"><span data-stu-id="6cc52-129">Peer Distribution</span></span>](peer-distribution.md)<br/>     | <span data-ttu-id="6cc52-130">Информация и справочный материал, относящиеся к API однорангового распространения.</span><span class="sxs-lookup"><span data-stu-id="6cc52-130">Information and reference material specific to the Peer Distribution API.</span></span><br/>                |



 

## <a name="additional-resources"></a><span data-ttu-id="6cc52-131">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6cc52-131">Additional resources</span></span>

<span data-ttu-id="6cc52-132">Дополнительные сведения о одноранговых технологиях можно найти в следующих расположениях:</span><span class="sxs-lookup"><span data-stu-id="6cc52-132">Further information regarding Peer-to-Peer technologies can be found at the following locations:</span></span>

| <span data-ttu-id="6cc52-133">Раздел</span><span class="sxs-lookup"><span data-stu-id="6cc52-133">Topic</span></span>                                                                                                          | <span data-ttu-id="6cc52-134">Описание</span><span class="sxs-lookup"><span data-stu-id="6cc52-134">Description</span></span>                                                                                                               |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6cc52-135">Ресурсы для одноранговых сетей Windows</span><span class="sxs-lookup"><span data-stu-id="6cc52-135">Windows Peer Networking Resources</span></span>](https://www.microsoft.com/p2p)                       | <span data-ttu-id="6cc52-136">Доступ к опубликованным техническим документам, образцам и презентациям подробно рассматривается технология одноранговых сетей.</span><span class="sxs-lookup"><span data-stu-id="6cc52-136">Access published white-papers, samples, and presentations detailing the Peer Networking technology.</span></span><br/> |
| [<span data-ttu-id="6cc52-137">Блог о одноранговых сетях Майкрософт</span><span class="sxs-lookup"><span data-stu-id="6cc52-137">Microsoft Peer Networking Blog</span></span>](/archive/blogs/p2p/)                          | <span data-ttu-id="6cc52-138">Ознакомьтесь с последними записями в блоге группы разработчиков одноранговых сетей корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="6cc52-138">Read the latest blog entries from Microsoft's Peer Networking Team.</span></span><br/>                                 |
| [<span data-ttu-id="6cc52-139">Форум по одноранговым сетям MSDN</span><span class="sxs-lookup"><span data-stu-id="6cc52-139">MSDN Peer Networking Forum</span></span>](https://social.msdn.microsoft.com/forums/peertopeer/threads/)                              | <span data-ttu-id="6cc52-140">Обсуждение одноранговых технологий и совместная работа с другими разработчиками.</span><span class="sxs-lookup"><span data-stu-id="6cc52-140">Discuss Peer technologies and collaborate with other developers.</span></span><br/>                                    |
| [<span data-ttu-id="6cc52-141">Ресурсы для одноранговых сетей TechNet для ИТ-специалистов</span><span class="sxs-lookup"><span data-stu-id="6cc52-141">TechNet Peer Networking Resources for IT Professionals</span></span>](https://technet.microsoft.com/library/bb742623.aspx) | <span data-ttu-id="6cc52-142">Общие сведения о концептуальной сети, а также рекомендации, относящиеся к роли ИТ-специалиста.</span><span class="sxs-lookup"><span data-stu-id="6cc52-142">A conceptual Peer Networking overview, as well as guidance, specific to the IT Professional role.</span></span> <br/>  |



 

 

