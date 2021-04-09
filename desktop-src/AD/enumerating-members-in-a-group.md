---
title: Перечисление членов в группе
description: Члены группы хранятся в атрибуте с несколькими значениями, называемом Member.
ms.assetid: 28cafdbe-e599-4b1d-a384-264f41d81c79
ms.tgt_platform: multiple
keywords:
- Перечисление членов в группе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2d051999bf8efeadb0c5a8899b31f813b8bf42
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104133686"
---
# <a name="enumerating-members-in-a-group"></a>Перечисление членов в группе

Члены группы хранятся в атрибуте с несколькими значениями, называемом **member**. Для групп с небольшим и средним членством используйте метод [**иадсграуп. members**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) , чтобы получить указатель на объект [**иадсмемберс**](/windows/desktop/api/iads/nn-iads-iadsmembers) , содержащий список всех элементов. Затем используйте [**иадсмемберс:: Get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum) , чтобы получить объект перечислителя, который можно использовать для перечисления элементов.

Если ожидаемое членство в группе будет составлять 1000 или более членов, используйте для извлечения пользователей по одному диапазону за раз. Дополнительные сведения об использовании различных компонентов для перечисления элементов см. в разделе [Перечисление групп, содержащих много элементов](enumerating-groups-that-contain-many-members.md).

 

 