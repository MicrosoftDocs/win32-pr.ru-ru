---
description: Читатели являются стандартными устройствами в системе смарт-карт. Управление ими осуществляется с помощью драйверов. они вводятся и удаляются из системы с помощью самонастраивающийся или через элемент устройства панели управления.
ms.assetid: 694902b9-e43c-4558-8fab-baa853f9fc4d
title: Устройства чтения смарт-карт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b6f4f5c4d1d487f136fb25052d44659f4b073bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651047"
---
# <a name="smart-card-readers"></a><span data-ttu-id="98dfc-104">Устройства чтения смарт-карт</span><span class="sxs-lookup"><span data-stu-id="98dfc-104">Smart Card Readers</span></span>

<span data-ttu-id="98dfc-105">Читатели являются стандартными устройствами в системе [*смарт-карт*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="98dfc-105">Readers are standard devices in a [*smart card*](../secgloss/s-gly.md) system.</span></span> <span data-ttu-id="98dfc-106">Управление ими осуществляется с помощью драйверов. они вводятся и удаляются из системы с помощью самонастраивающийся или через элемент устройства панели управления.</span><span class="sxs-lookup"><span data-stu-id="98dfc-106">They are controlled through drivers, and are introduced to and removed from the system through Plug and Play or through the Control Panel Devices item.</span></span>

<span data-ttu-id="98dfc-107">Каждый модуль чтения должен быть определен для использования [*подсистемой смарт-карт*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="98dfc-107">Each reader must be defined for use by the [*smart card subsystem*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="98dfc-108">Подсистема не несет ответственности за каких-либо средств чтения, которые не были предоставлены специально для него.</span><span class="sxs-lookup"><span data-stu-id="98dfc-108">The subsystem is not responsible for any reader not specifically given to it.</span></span>

<span data-ttu-id="98dfc-109">Устройства чтения смарт-карт можно разделить на логические группы, называемые группами читателей.</span><span class="sxs-lookup"><span data-stu-id="98dfc-109">Smart card readers can be divided into logical groups called reader groups.</span></span> <span data-ttu-id="98dfc-110">Эти группы могут определяться подсистемой, а также определяться администраторами и пользователями.</span><span class="sxs-lookup"><span data-stu-id="98dfc-110">These groups can be defined by the subsystem, as well as defined by administrators and users.</span></span> <span data-ttu-id="98dfc-111">Модуль чтения может принадлежать нескольким группам читателей.</span><span class="sxs-lookup"><span data-stu-id="98dfc-111">A reader can belong to more than one reader group</span></span>

<span data-ttu-id="98dfc-112">Подсистема смарт-карт определяет следующие группы.</span><span class="sxs-lookup"><span data-stu-id="98dfc-112">The smart card subsystem defines the following groups.</span></span>



| <span data-ttu-id="98dfc-113">Группа</span><span class="sxs-lookup"><span data-stu-id="98dfc-113">Group</span></span>                | <span data-ttu-id="98dfc-114">Описание</span><span class="sxs-lookup"><span data-stu-id="98dfc-114">Description</span></span>                                                                                                                                                                                            |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98dfc-115">Бросить $ Аллреадерс</span><span class="sxs-lookup"><span data-stu-id="98dfc-115">SCard$AllReaders</span></span>     | <span data-ttu-id="98dfc-116">Эта группа содержит все читатели в системе.</span><span class="sxs-lookup"><span data-stu-id="98dfc-116">This group contains all the readers in the system.</span></span> <span data-ttu-id="98dfc-117">Новый модуль чтения, предоставляемый подсистеме смарт-карт, автоматически включается в группу читателей уровня системы бросить $ Аллреадерс.</span><span class="sxs-lookup"><span data-stu-id="98dfc-117">A new reader given to the smart card subsystem is automatically included in the system-wide reader group, SCard$AllReaders.</span></span>                         |
| <span data-ttu-id="98dfc-118">Бросить $ Дефаултреадерс</span><span class="sxs-lookup"><span data-stu-id="98dfc-118">SCard$DefaultReaders</span></span> | <span data-ttu-id="98dfc-119">Эта группа по умолчанию, по одной для каждого [*терминала*](../secgloss/t-gly.md), содержит все устройства чтения, назначенные терминалу, которые не зарезервированы для конкретного использования.</span><span class="sxs-lookup"><span data-stu-id="98dfc-119">This default group, one for each [*terminal*](../secgloss/t-gly.md), contains all the readers assigned to the terminal that are not reserved for specific use.</span></span> |



 

 

 
