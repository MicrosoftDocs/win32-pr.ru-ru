---
description: Маршрутизатор с несколькими поставщиками (MPR) вызывает Нпжеткапс, чтобы узнать, когда будут запущены поставщики сети (Ниндекс имеет значение ВННК \_ Start).
ms.assetid: f57bd8ff-647d-42f8-abaf-7937b24416dd
title: Переопределение интервала времени ожидания MPR по умолчанию
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4308d94f4b16a7f67786c8a0856f23922e6f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999094"
---
# <a name="overriding-the-default-mpr-time-out-interval"></a><span data-ttu-id="a0237-103">Переопределение интервала времени ожидания MPR по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a0237-103">Overriding the Default MPR Time-out Interval</span></span>

<span data-ttu-id="a0237-104">[*Маршрутизатор с несколькими поставщиками*](../secgloss/m-gly.md) (MPR) вызывает [**нпжеткапс**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) , чтобы узнать, когда будут запущены поставщики сети (*ниндекс* имеет значение вннк \_ Start).</span><span class="sxs-lookup"><span data-stu-id="a0237-104">The [*Multiple Provider Router*](../secgloss/m-gly.md) (MPR) calls [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) to find out when the network providers will start (*nIndex* is set to WNNC\_START).</span></span> <span data-ttu-id="a0237-105">Затем многопротокольный маршрутизатор ожидает превышение времени ожидания, заданное всеми поставщиками сети, прежде чем он предоставит объединенную сеть пользователю.</span><span class="sxs-lookup"><span data-stu-id="a0237-105">The MPR then waits for the longest time-out period specified by all network providers before it presents the consolidated network to the user.</span></span> <span data-ttu-id="a0237-106">Если один из сетевых поставщиков не знает, когда он начнется, то для этого поставщика используется время ожидания по умолчанию (60 секунд).</span><span class="sxs-lookup"><span data-stu-id="a0237-106">If one of the network providers does not know when it will start, MPR uses a default time-out of 60 seconds for that provider.</span></span>

<span data-ttu-id="a0237-107">При необходимости администратор может переопределить время ожидания по умолчанию, создав следующий реестр реестра с регистром **\_ DWORD** , где *n* — интервал времени ожидания в миллисекундах:</span><span class="sxs-lookup"><span data-stu-id="a0237-107">If necessary, the administrator can override the default time-out by creating the following **REG\_DWORD** registry time-out, where *n* is the time-out interval in milliseconds:</span></span>

<span data-ttu-id="a0237-108">**HKey \_ \_** \\  \\  \\ **Элемент управления** CurrentControlSet системы локального компьютера \\ **нетворкпровидер** \\ **ресторетимеаут**  =  *n*</span><span class="sxs-lookup"><span data-stu-id="a0237-108">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**NetworkProvider**\\**RestoreTimeout** = *n*</span></span>

<span data-ttu-id="a0237-109">В следующем псевдокоде показан полный логический поток для обработки истечения времени ожидания многопротокольного алгоритма.</span><span class="sxs-lookup"><span data-stu-id="a0237-109">The following pseudocode shows the complete logic flow for time-out handling by the MPR.</span></span>


```C++
If there is a RegistryTimeout,
Then MaxTimeout = RegistryTimeout.
Otherwise,
MaxTimeout = 0.
For each provider,
if the provider does not supply a time-out and
if there is a RegistryTimeout,
ProviderTimeout is set to RegistryTimeout.
Otherwise,
ProviderTimeout is set to DefaultTimeout.
Otherwise,
If the ProviderTimeout is longer than MaxTimeout,
MaxTimeout = ProviderTimeout.
```



 

 
