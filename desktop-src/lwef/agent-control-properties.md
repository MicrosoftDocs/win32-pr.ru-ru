---
title: Свойства элемента управления агента
description: Свойства элемента управления агента
ms.assetid: e6a5b2db-9abf-4988-be41-fc7f4530507f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f5e80b10469e7e256b1b2bf3bcf55fb5a8a08b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067533"
---
# <a name="agent-control-properties"></a><span data-ttu-id="eb532-103">Свойства элемента управления агента</span><span class="sxs-lookup"><span data-stu-id="eb532-103">Agent Control Properties</span></span>

<span data-ttu-id="eb532-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="eb532-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="eb532-105">К следующим свойствам напрямую обращаются из элемента управления агента:</span><span class="sxs-lookup"><span data-stu-id="eb532-105">The following properties are directly accessed from the Agent control:</span></span>

-   [<span data-ttu-id="eb532-106">**Подключен**</span><span class="sxs-lookup"><span data-stu-id="eb532-106">**Connected**</span></span>](connected-property.md)
-   [<span data-ttu-id="eb532-107">**Имя**</span><span class="sxs-lookup"><span data-stu-id="eb532-107">**Name**</span></span>](name-property-a.md)
-   [<span data-ttu-id="eb532-108">**раисерекуестеррорс**</span><span class="sxs-lookup"><span data-stu-id="eb532-108">**RaiseRequestErrors**</span></span>](raiserequesterrors-property.md)

<span data-ttu-id="eb532-109">Кроме того, некоторые среды программирования могут назначать дополнительные свойства времени разработки или времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="eb532-109">In addition, some programming environments may assign additional design-time or run-time properties.</span></span> <span data-ttu-id="eb532-110">Например, Visual Basic добавляет свойства Left, index, Tag и Top, определяющие расположение элемента управления в форме, даже если элемент управления не отображается на странице формы во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="eb532-110">For example, Visual Basic adds Left, Index, Tag, and Top properties that define the location of the control on a form even though the control does not appear on the form's page at run time.</span></span>

<span data-ttu-id="eb532-111">Свойство suspended по-прежнему поддерживается для обратной совместимости, но всегда возвращает **значение false** , так как сервер больше не поддерживает состояние SUSPENDED.</span><span class="sxs-lookup"><span data-stu-id="eb532-111">The Suspended property is still supported for backward compatibility, but always returns **False** because the server no longer supports a suspended state.</span></span>

 

 




