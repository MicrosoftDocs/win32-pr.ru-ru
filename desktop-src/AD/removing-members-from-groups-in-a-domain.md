---
title: Удаление членов из групп в домене
description: Вы можете удалить пользователей, группы или контакты из групп.
ms.assetid: 036f2882-7da9-4293-87a0-a087235b212f
ms.tgt_platform: multiple
keywords:
- группы AD, удаление участников из групп в домене
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f282cf2938996059ad13fe74bc9818e984967d1c8f3a4dbfffae7b505cbe1b9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025162"
---
# <a name="removing-members-from-groups-in-a-domain"></a>Удаление членов из групп в домене

Вы можете удалить пользователей, группы или контакты из групп. Атрибут **member** объекта **Group** содержит все непосредственные члены группы.

Самый простой способ удалить член из группы — вызвать метод [**иадсграуп. Remove**](/windows/desktop/api/iads/nf-iads-iadsgroup-remove) в интерфейсе [**иадсграуп**](/windows/desktop/api/iads/nn-iads-iadsgroup) объекта группы, из которого необходимо удалить элементы.

 

 