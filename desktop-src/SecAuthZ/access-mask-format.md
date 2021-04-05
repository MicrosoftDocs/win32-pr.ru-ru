---
description: Все защищаемые объекты упорядочивают свои права доступа, используя формат маски доступа, как показано на следующем рисунке.
ms.assetid: c7b97cd8-66b6-42dc-b75b-2c0adb87d020
title: Формат маски доступа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2f6c66c99ed93dca399825621dfbd0cc01c2ec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910623"
---
# <a name="access-mask-format"></a><span data-ttu-id="4b5f9-103">Формат маски доступа</span><span class="sxs-lookup"><span data-stu-id="4b5f9-103">Access Mask Format</span></span>

<span data-ttu-id="4b5f9-104">Все защищаемые объекты упорядочивают свои права доступа, используя формат [*маски доступа*](/windows/desktop/SecGloss/a-gly) , как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="4b5f9-104">All securable objects arrange their access rights by using the [*access mask*](/windows/desktop/SecGloss/a-gly) format shown in the following illustration.</span></span>

![Формат маски доступа](images/accctrl4.png)

<span data-ttu-id="4b5f9-106">В этом формате 16 младших разрядов предназначены для доступа к конкретным объектам, а следующие 8 бит предназначены для [стандартных прав доступа](standard-access-rights.md), которые применяются к большинству типов объектов, а 4 старшие биты используются для указания [универсальных прав доступа](generic-access-rights.md) , которые каждый тип объектов может сопоставлять с набором стандартных и зависящих от объекта прав.</span><span class="sxs-lookup"><span data-stu-id="4b5f9-106">In this format, the low-order 16 bits are for object-specific access rights, the next 8 bits are for [standard access rights](standard-access-rights.md), which apply to most types of objects, and the 4 high-order bits are used to specify [generic access rights](generic-access-rights.md) that each object type can map to a set of standard and object-specific rights.</span></span> <span data-ttu-id="4b5f9-107">\_ \_ Бит безопасности системы доступа соответствует [право доступа к SACL объекта](sacl-access-right.md).</span><span class="sxs-lookup"><span data-stu-id="4b5f9-107">The ACCESS\_SYSTEM\_SECURITY bit corresponds to the [right to access the object's SACL](sacl-access-right.md).</span></span>

 

 
