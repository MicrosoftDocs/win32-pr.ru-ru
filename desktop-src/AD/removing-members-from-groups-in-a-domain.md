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
# <a name="removing-members-from-groups-in-a-domain"></a>Удаление членов из групп в домене

Вы можете удалить пользователей, группы или контакты из групп. Атрибут **member** объекта **Group** содержит все непосредственные члены группы.

Самый простой способ удалить член из группы — вызвать метод [**иадсграуп. Remove**](/windows/desktop/api/iads/nf-iads-iadsgroup-remove) в интерфейсе [**иадсграуп**](/windows/desktop/api/iads/nn-iads-iadsgroup) объекта группы, из которого необходимо удалить элементы.

 

 