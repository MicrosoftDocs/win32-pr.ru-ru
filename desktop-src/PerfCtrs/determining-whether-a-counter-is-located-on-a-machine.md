---
description: Чтобы определить, установлен ли счетчик на определенном компьютере, вызовите Пдхвалидатепас с полным путем к счетчику. Функция возвращает значение "ошибка", \_ Если счетчик находится на указанном компьютере.
ms.assetid: 5533a8d8-3621-4ce7-984c-c3895adef531
title: Определение того, находится ли счетчик на компьютере
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 795878e2f9c97989fe924737ec7f8e7f14bdc67c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998525"
---
# <a name="determining-whether-a-counter-is-located-on-a-computer"></a><span data-ttu-id="0ba07-104">Определение того, находится ли счетчик на компьютере</span><span class="sxs-lookup"><span data-stu-id="0ba07-104">Determining Whether a Counter Is Located on a Computer</span></span>

<span data-ttu-id="0ba07-105">Чтобы определить, установлен ли счетчик на определенном компьютере, вызовите [**пдхвалидатепас**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) с полным путем к счетчику.</span><span class="sxs-lookup"><span data-stu-id="0ba07-105">To determine if a counter is installed on a particular computer, call [**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) with the fully qualified counter path.</span></span> <span data-ttu-id="0ba07-106">Функция возвращает значение "ошибка", \_ Если счетчик находится на указанном компьютере.</span><span class="sxs-lookup"><span data-stu-id="0ba07-106">The function returns ERROR\_SUCCESS if the counter is located on the specified computer.</span></span>

<span data-ttu-id="0ba07-107">[**Пдхвалидатепас**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) проверяет весь путь; Таким образом, если какой либо объект, экземпляр или счетчик в пути не существует, возвращаемое значение указывает на это.</span><span class="sxs-lookup"><span data-stu-id="0ba07-107">[**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) validates the entire path; therefore, if any object, instance, or counter in the path does not exist, the return value indicates so.</span></span> <span data-ttu-id="0ba07-108">**Пдхвалидатепас** проверяет указанный путь счетчика в следующем порядке: компьютер, объект производительности, экземпляр и счетчик.</span><span class="sxs-lookup"><span data-stu-id="0ba07-108">**PdhValidatePath** verifies the specified counter path in this order: computer, performance object, instance, and counter.</span></span>

 

 



