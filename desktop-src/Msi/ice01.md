---
description: ICE01 проверяет работоспособность механизма ICE. В этом ICE для получения времени используется свойство Time, которое возвращает либо системное время, либо значение None.
ms.assetid: 070e330d-be88-4f39-92db-64cf3819e567
title: ICE01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32365688c11e6bf6323011bf8e30a5527258298e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808753"
---
# <a name="ice01"></a><span data-ttu-id="4db3c-104">ICE01</span><span class="sxs-lookup"><span data-stu-id="4db3c-104">ICE01</span></span>

<span data-ttu-id="4db3c-105">ICE01 проверяет работоспособность механизма ICE.</span><span class="sxs-lookup"><span data-stu-id="4db3c-105">ICE01 validates that the ICE mechanism is working.</span></span> <span data-ttu-id="4db3c-106">В этом ICE для получения времени используется свойство [**time**](time.md) , которое возвращает либо системное время, либо значение None.</span><span class="sxs-lookup"><span data-stu-id="4db3c-106">This ICE uses the [**Time**](time.md) property to get the time and returns either the system time or None.</span></span>

## <a name="result"></a><span data-ttu-id="4db3c-107">Результат</span><span class="sxs-lookup"><span data-stu-id="4db3c-107">Result</span></span>

<span data-ttu-id="4db3c-108">ICE01 отправляет сообщение, предоставляющее время, которое программа установки вызвала ICE01.</span><span class="sxs-lookup"><span data-stu-id="4db3c-108">ICE01 posts a message giving the time the installer called ICE01.</span></span> <span data-ttu-id="4db3c-109">Эта ICE никогда не должна возвращать ошибку.</span><span class="sxs-lookup"><span data-stu-id="4db3c-109">This ICE should never return an error.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4db3c-110">См. также</span><span class="sxs-lookup"><span data-stu-id="4db3c-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4db3c-111">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="4db3c-111">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



