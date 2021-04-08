---
title: Расширенные сведения об ошибке для пользователя
description: Если доступны расширенные сведения об ошибке, компоненты, участвующие в создании расширенных сведений об ошибке, должны упростить поиск проблемы.
ms.assetid: 10c54f53-f449-4e7d-ba84-7b000beaee22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d6f52e45e3f181c5aaa0db196f9ce791581cc38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888539"
---
# <a name="extended-error-information-for-the-user"></a><span data-ttu-id="26a91-103">Расширенные сведения об ошибке для пользователя</span><span class="sxs-lookup"><span data-stu-id="26a91-103">Extended Error Information for the User</span></span>

<span data-ttu-id="26a91-104">Если доступны расширенные сведения об ошибке, компоненты, участвующие в создании расширенных сведений об ошибке, должны упростить поиск проблемы.</span><span class="sxs-lookup"><span data-stu-id="26a91-104">If extended error information is available, the components participating in the creation of the extended error information must make it easy to find the problem.</span></span> <span data-ttu-id="26a91-105">Первым шагом является проверка последней расширенной записи об ошибке и определение того, на каком компьютере и в каком процессе возникла проблема.</span><span class="sxs-lookup"><span data-stu-id="26a91-105">The first step is to review the last extended error record, and determine on which computer and which process the problem originated.</span></span> <span data-ttu-id="26a91-106">Это часто вызывает \_ ошибку RPC S \_ \* .</span><span class="sxs-lookup"><span data-stu-id="26a91-106">This is often the cause of the RPC\_S\_\* error.</span></span> <span data-ttu-id="26a91-107">Найдите расположение обнаружения и определите, что означают параметры для этого расположения обнаружения.</span><span class="sxs-lookup"><span data-stu-id="26a91-107">Find the detection location, and determine what the parameters for this detection location mean.</span></span> <span data-ttu-id="26a91-108">Обычно они указывают на сбой вызова функции или конкретной проверки.</span><span class="sxs-lookup"><span data-stu-id="26a91-108">Usually they indicate a failure of a function call or particular check.</span></span> <span data-ttu-id="26a91-109">Определите причину сбоя функции или проверки и выполните действия по исправлению.</span><span class="sxs-lookup"><span data-stu-id="26a91-109">From there, determine why the function or check fails, and take corrective action.</span></span>

<span data-ttu-id="26a91-110">Записи перед последней записью указывают путь, по которому произошла ошибка, и обычно служит в качестве работоспособности проверки, а не телеметрическую в процессе устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="26a91-110">The records before the last record indicate the path by which the error arrived, and generally serve as a sanity check rather than an aide in the troubleshooting process.</span></span>

 

 




