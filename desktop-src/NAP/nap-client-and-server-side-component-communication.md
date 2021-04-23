---
title: Взаимодействие клиента NAP и компонентов на стороне сервера
description: Взаимодействие клиента NAP и компонентов на стороне сервера
ms.assetid: 7658cf0c-607b-44ba-b579-72082d0d1f51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07597ac80a1e02c4f8528b3c99050aefb5963988
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411298"
---
# <a name="nap-client-and-server-side-component-communication"></a><span data-ttu-id="bb7b8-103">Взаимодействие клиента NAP и компонентов на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="bb7b8-103">NAP Client and Server-side Component Communication</span></span>

> [!Note]  
> <span data-ttu-id="bb7b8-104">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="bb7b8-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="bb7b8-105">Компонент агента NAP может взаимодействовать с компонентом сервера администрирования NAP с помощью следующего процесса:</span><span class="sxs-lookup"><span data-stu-id="bb7b8-105">The NAP Agent component can communicate with the NAP Administration Server component through the following process:</span></span>

1.  <span data-ttu-id="bb7b8-106">Агент NAP передает Ссох в NAP EC.</span><span class="sxs-lookup"><span data-stu-id="bb7b8-106">The NAP Agent passes the SSoH to the NAP EC.</span></span>
2.  <span data-ttu-id="bb7b8-107">NAP EC передает Ссох в NAP ES.</span><span class="sxs-lookup"><span data-stu-id="bb7b8-107">The NAP EC passes the SSoH to the NAP ES.</span></span>
3.  <span data-ttu-id="bb7b8-108">NAP ES передает Ссох службе сервера политики сети (NPS).</span><span class="sxs-lookup"><span data-stu-id="bb7b8-108">The NAP ES passes the SSoH to the Network Policy Server (NPS) service.</span></span>
4.  <span data-ttu-id="bb7b8-109">Служба NPS передает Ссох на сервер администрирования NAP.</span><span class="sxs-lookup"><span data-stu-id="bb7b8-109">The NPS service passes the SSoH to the NAP Administration Server.</span></span>

<span data-ttu-id="bb7b8-110">SHA может взаимодействовать со своим соответствующим SHV с помощью следующего процесса:</span><span class="sxs-lookup"><span data-stu-id="bb7b8-110">An SHA can communicate with its corresponding SHV through the following process:</span></span>

1.  <span data-ttu-id="bb7b8-111">SHA передает свое состояние работоспособности агенту NAP.</span><span class="sxs-lookup"><span data-stu-id="bb7b8-111">The SHA passes its SoH to the NAP Agent.</span></span>
2.  <span data-ttu-id="bb7b8-112">Агент NAP передает SoH, содержащийся в Ссох, в NAP EC.</span><span class="sxs-lookup"><span data-stu-id="bb7b8-112">The NAP Agent passes the SoH, contained within the SSoH, to the NAP EC.</span></span>
3.  <span data-ttu-id="bb7b8-113">NAP EC передает SoH в NAP ES.</span><span class="sxs-lookup"><span data-stu-id="bb7b8-113">The NAP EC passes the SoH to the NAP ES.</span></span>
4.  <span data-ttu-id="bb7b8-114">NAP ES передает SoH на сервер администрирования NAP.</span><span class="sxs-lookup"><span data-stu-id="bb7b8-114">The NAP ES passes the SoH to the NAP Administration Server.</span></span>
5.  <span data-ttu-id="bb7b8-115">Сервер администрирования NAP передает SoH в SHV.</span><span class="sxs-lookup"><span data-stu-id="bb7b8-115">The NAP Administration Server passes the SoH to the SHV.</span></span>

<span data-ttu-id="bb7b8-116">На рисунке ниже показан процесс обмена данными от клиентских компонентов NAP к компонентам на стороне сервера NAP.</span><span class="sxs-lookup"><span data-stu-id="bb7b8-116">The figure below shows the communication process from NAP client components to NAP server-side components.</span></span>

![Архитектура обмена данными между клиентом и сервером на платформе NAP](images/nap-client-to-server-comm.png)

<span data-ttu-id="bb7b8-118">Сервер администрирования NAP может взаимодействовать с агентом NAP с помощью следующего процесса:</span><span class="sxs-lookup"><span data-stu-id="bb7b8-118">The NAP Administration Server can communicate with the NAP Agent through the following process:</span></span>

1.  <span data-ttu-id="bb7b8-119">Сервер администрирования NAP передает Сохрс в службу NPS.</span><span class="sxs-lookup"><span data-stu-id="bb7b8-119">The NAP Administration Server passes the SoHRs to the NPS service.</span></span>
2.  <span data-ttu-id="bb7b8-120">Служба NPS передает SSoHR в NAP ES.</span><span class="sxs-lookup"><span data-stu-id="bb7b8-120">The NPS service passes the SSoHR to the NAP ES.</span></span>
3.  <span data-ttu-id="bb7b8-121">NAP ES передает SSoHR в NAP EC.</span><span class="sxs-lookup"><span data-stu-id="bb7b8-121">The NAP ES passes the SSoHR to the NAP EC.</span></span>
4.  <span data-ttu-id="bb7b8-122">NAP EC передает SSoHR агенту NAP.</span><span class="sxs-lookup"><span data-stu-id="bb7b8-122">The NAP EC passes the SSoHR to the NAP Agent.</span></span>

<span data-ttu-id="bb7b8-123">SHV может взаимодействовать с соответствующим агентом SHA через следующий процесс:</span><span class="sxs-lookup"><span data-stu-id="bb7b8-123">The SHV can communicate with its corresponding SHA through the following process:</span></span>

1.  <span data-ttu-id="bb7b8-124">SHV передает свой SoHR на сервер администрирования NAP.</span><span class="sxs-lookup"><span data-stu-id="bb7b8-124">The SHV passes its SoHR to the NAP Administration Server.</span></span>
2.  <span data-ttu-id="bb7b8-125">Сервер администрирования NAP передает SoHR в службу NPS.</span><span class="sxs-lookup"><span data-stu-id="bb7b8-125">The NAP Administration Server passes the SoHR to the NPS service.</span></span>
3.  <span data-ttu-id="bb7b8-126">Служба NPS передает SoHR, содержащийся в SSoHR, в NAP ES.</span><span class="sxs-lookup"><span data-stu-id="bb7b8-126">The NPS service passes the SoHR, contained within the SSoHR, to the NAP ES.</span></span>
4.  <span data-ttu-id="bb7b8-127">NAP ES передает SoHR в NAP EC.</span><span class="sxs-lookup"><span data-stu-id="bb7b8-127">The NAP ES passes the SoHR to the NAP EC.</span></span>
5.  <span data-ttu-id="bb7b8-128">NAP EC передает SoHR агенту NAP.</span><span class="sxs-lookup"><span data-stu-id="bb7b8-128">The NAP EC passes the SoHR to the NAP Agent.</span></span>
6.  <span data-ttu-id="bb7b8-129">Агент NAP передает SoHR в SHA.</span><span class="sxs-lookup"><span data-stu-id="bb7b8-129">The NAP Agent passes the SoHR to the SHA.</span></span>

<span data-ttu-id="bb7b8-130">На рисунке ниже показан процесс обмена данными между компонентами на стороне сервера NAP и клиентскими компонентами NAP.</span><span class="sxs-lookup"><span data-stu-id="bb7b8-130">The figure below shows the communication process from NAP server-side components to NAP client components.</span></span>

![Архитектура обмена данными между сервером и клиентом на платформе NAP](images/nap-server-to-client-comm.png)

 

 




