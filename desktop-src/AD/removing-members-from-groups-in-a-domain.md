---
title: Удаление членов из групп в домене
description: Вы можете удалить пользователей, группы или контакты из групп.
ms.assetid: 036f2882-7da9-4293-87a0-a087235b212f
ms.tgt_platform: multiple
keywords:
- группы AD, удаление участников из групп в домене
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab7600d98e75447c55fd84d783ff5263fc63bde
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789486"
---
# <a name="removing-members-from-groups-in-a-domain"></a><span data-ttu-id="c4cd2-104">Удаление членов из групп в домене</span><span class="sxs-lookup"><span data-stu-id="c4cd2-104">Removing Members from Groups in a Domain</span></span>

<span data-ttu-id="c4cd2-105">Вы можете удалить пользователей, группы или контакты из групп.</span><span class="sxs-lookup"><span data-stu-id="c4cd2-105">You can remove users, groups, or contacts from groups.</span></span> <span data-ttu-id="c4cd2-106">Атрибут **member** объекта **Group** содержит все непосредственные члены группы.</span><span class="sxs-lookup"><span data-stu-id="c4cd2-106">The **member** attribute of the **group** object contains all direct members of the group.</span></span>

<span data-ttu-id="c4cd2-107">Самый простой способ удалить член из группы — вызвать метод [**иадсграуп. Remove**](/windows/desktop/api/iads/nf-iads-iadsgroup-remove) в интерфейсе [**иадсграуп**](/windows/desktop/api/iads/nn-iads-iadsgroup) объекта группы, из которого необходимо удалить элементы.</span><span class="sxs-lookup"><span data-stu-id="c4cd2-107">The simplest way to remove a member from a group is to call the [**IADsGroup.Remove**](/windows/desktop/api/iads/nf-iads-iadsgroup-remove) method on the [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) interface of the group object you want to remove members from.</span></span>

 

 