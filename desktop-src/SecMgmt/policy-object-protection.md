---
description: Описание защиты объекта политики по умолчанию.
ms.assetid: e2d65ebf-5fbd-4e25-9862-a8188abb5492
title: Защита объектов политики
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 802fea6ce37a070c8230c3c9993df78a45f439bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809317"
---
# <a name="policy-object-protection"></a><span data-ttu-id="b8aa5-103">Защита объектов политики</span><span class="sxs-lookup"><span data-stu-id="b8aa5-103">Policy Object Protection</span></span>

<span data-ttu-id="b8aa5-104">Объект [**политики**](policy-object.md) защищен по умолчанию со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="b8aa5-104">The [**Policy**](policy-object.md) object is protected by default with the following settings:</span></span>

-   <span data-ttu-id="b8aa5-105">В мире локальной группы есть универсальный \_ доступ для выполнения.</span><span class="sxs-lookup"><span data-stu-id="b8aa5-105">The local group WORLD has GENERIC\_EXECUTE access.</span></span>
-   <span data-ttu-id="b8aa5-106">Известной системе идентификации предоставляется \_ доступ ко всем политикам \_ .</span><span class="sxs-lookup"><span data-stu-id="b8aa5-106">The well-known ID System is granted POLICY\_ALL\_ACCESS.</span></span>
-   <span data-ttu-id="b8aa5-107">ЛОКАЛЬНЫЙ администратор локальной группы \_ имеет универсальное \_ чтение, универсальную \_ запись и универсальный \_ доступ для выполнения.</span><span class="sxs-lookup"><span data-stu-id="b8aa5-107">The local group LOCAL\_ADMIN has GENERIC\_READ, GENERIC\_WRITE, and GENERIC\_EXECUTE access.</span></span>
-   <span data-ttu-id="b8aa5-108">Группа "локальный \_ Администратор" назначена как владелец и основная группа этого объекта.</span><span class="sxs-lookup"><span data-stu-id="b8aa5-108">The group LOCAL\_ADMIN is assigned as owner and primary group of this object.</span></span>

<span data-ttu-id="b8aa5-109">Невозможно создать или уничтожить объект [**политики**](policy-object.md) .</span><span class="sxs-lookup"><span data-stu-id="b8aa5-109">The [**Policy**](policy-object.md) object cannot be created or destroyed.</span></span>

 

 



