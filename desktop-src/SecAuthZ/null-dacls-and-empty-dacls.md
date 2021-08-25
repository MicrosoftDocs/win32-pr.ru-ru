---
description: Пустой список DACL предоставляет полный доступ любому пользователю, который его запрашивает. Пустой DACL — это правильно выделенный и инициализированный DACL, который не содержит записей контроля доступа. Пустой DACL не предоставляет доступа к объекту, которому он назначен.
ms.assetid: 26e5c98d-bbdc-4f9f-96e0-18d1c429f1e6
title: Списки DACL NULL и пустые списки DACL (авторизация)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51c15f9a3aeed120ff91dc19a091232721c623683d90f0c9cdccbc065516eea8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907824"
---
# <a name="null-dacls-and-empty-dacls-authorization"></a>Списки DACL NULL и пустые списки DACL (авторизация)

Если [*избирательный список управления доступом*](/windows/desktop/SecGloss/d-gly) (DACL), принадлежащий [*дескриптору безопасности*](/windows/desktop/SecGloss/s-gly) объекта, имеет значение **null**, создается пустой список DACL. Пустой список DACL предоставляет полный доступ любому пользователю, который запрашивает его; Обычная проверка безопасности не выполняется в отношении объекта. Пустой список DACL не следует путать с пустым списком DACL. Пустой DACL — это правильно выделенный и инициализированный DACL, который не содержит [*записей контроля доступа*](/windows/desktop/SecGloss/a-gly) (ACE). Пустой DACL не предоставляет доступа к объекту, которому он назначен.

Пример создания списка DACL см. в разделе [Создание списка DACL](/windows/desktop/SecBP/creating-a-dacl).

 

 
