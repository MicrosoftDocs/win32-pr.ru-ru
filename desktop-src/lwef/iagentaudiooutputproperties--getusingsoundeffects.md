---
title: Иажентаудиуутпутпропертиес Жетусингсаундеффектс
description: Иажентаудиуутпутпропертиес Жетусингсаундеффектс
ms.assetid: 3ccf90b1-a2aa-482a-9f96-85d735532c11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e83314acfc67ce8bea4a0f0d305f6d5d490a92e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776175"
---
# <a name="iagentaudiooutputpropertiesgetusingsoundeffects"></a><span data-ttu-id="8486c-103">Иажентаудиуутпутпропертиес:: Жетусингсаундеффектс</span><span class="sxs-lookup"><span data-stu-id="8486c-103">IAgentAudioOutputProperties::GetUsingSoundEffects</span></span>

<span data-ttu-id="8486c-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8486c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetUsingSoundEffects(
long * pbUsingSoundEffects  // address of variable sound effects output 
);                          // setting 
```

<span data-ttu-id="8486c-105">Получает значение, указывающее, включен ли вывод звуковых эффектов.</span><span class="sxs-lookup"><span data-stu-id="8486c-105">Retrieves a value indicating whether sound effects output is enabled.</span></span>

-   <span data-ttu-id="8486c-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="8486c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="8486c-107"><span id="pbUsingSoundEffects"></span><span id="pbusingsoundeffects"></span><span id="PBUSINGSOUNDEFFECTS"></span>*пбусингсаундеффектс*</span><span class="sxs-lookup"><span data-stu-id="8486c-107"><span id="pbUsingSoundEffects"></span><span id="pbusingsoundeffects"></span><span id="PBUSINGSOUNDEFFECTS"></span>*pbUsingSoundEffects*</span></span>
</dt> <dd>

<span data-ttu-id="8486c-108">Адрес переменной, принимающей **значение true** , если в настоящий момент включен вывод звуковых эффектов и **значение false** в случае отключения.</span><span class="sxs-lookup"><span data-stu-id="8486c-108">Address of a variable that receives **True** if the sound effects output is currently enabled and **False** if disabled.</span></span>

</dd> </dl>

<span data-ttu-id="8486c-109">Звуковые эффекты для анимации символа назначаются в редакторе символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="8486c-109">Sound effects for a character's animation are assigned in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="8486c-110">Поскольку этот параметр влияет на вывод звуковых эффектов для всех символов, только пользователь может изменить это свойство на странице свойств Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="8486c-110">Because this setting affects sound effects output for all characters, only the user can change this property in the Microsoft Agent property sheet.</span></span>

 

 




