---
description: ICEM01 проверяет работоспособность механизма ICE. В этом ICE для получения времени используется свойство Time, которое возвращает либо системное время, либо значение None.
ms.assetid: f3b7677d-6b2e-4aa0-92eb-1b1e62cdf0a6
title: ICEM01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca7f2ffb3fcf5e3d50a3937a1f17fddd3a912f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154806"
---
# <a name="icem01"></a><span data-ttu-id="40864-104">ICEM01</span><span class="sxs-lookup"><span data-stu-id="40864-104">ICEM01</span></span>

<span data-ttu-id="40864-105">ICEM01 проверяет работоспособность механизма ICE.</span><span class="sxs-lookup"><span data-stu-id="40864-105">ICEM01 validates that the ICE mechanism is working.</span></span> <span data-ttu-id="40864-106">В этом ICE для получения времени используется свойство [**time**](time.md) , которое возвращает либо системное время, либо значение None.</span><span class="sxs-lookup"><span data-stu-id="40864-106">This ICE uses the [**Time**](time.md) property to get the time and returns either the system time or None.</span></span>

<span data-ttu-id="40864-107">Модуль слияния ICEs хранится в файле слияния Module. CUB, который называется Мержемод. CUB, а не в файле. CUB, содержащем значение ICEs, используемое для проверки пакета.</span><span class="sxs-lookup"><span data-stu-id="40864-107">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="40864-108">Результат</span><span class="sxs-lookup"><span data-stu-id="40864-108">Result</span></span>

<span data-ttu-id="40864-109">ICEM01 отправляет сообщение, предоставляющее время, которое программа установки вызвала ICEM01.</span><span class="sxs-lookup"><span data-stu-id="40864-109">ICEM01 posts a message giving the time the installer called ICEM01.</span></span> <span data-ttu-id="40864-110">Эта ICE никогда не должна возвращать ошибку.</span><span class="sxs-lookup"><span data-stu-id="40864-110">This ICE should never return an error.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40864-111">См. также</span><span class="sxs-lookup"><span data-stu-id="40864-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40864-112">Ссылка на модуль слияния ICE</span><span class="sxs-lookup"><span data-stu-id="40864-112">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



