---
title: Списки DACL NULL и пустые списки DACL (AD DS)
description: Наличие списка управления доступом (DACL) со значением NULL в атрибуте Нтсекуритидескриптор любого объекта может привести к серьезным угрозам безопасности.
ms.assetid: 32b786d2-e676-4402-ad22-550de9289494
ms.tgt_platform: multiple
keywords:
- Списки DACL со значением NULL и пустые DACL
- DACL Active Directory, NULL и Empty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a41e03917c1190b7926eca11db038e2143bcb91d142e0617d143d4d80bb6e601
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185799"
---
# <a name="null-dacls-and-empty-dacls-ad-ds"></a>Списки DACL NULL и пустые списки DACL (AD DS)

Наличие списка управления доступом (DACL) со значением NULL в атрибуте [**нтсекуритидескриптор**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) любого объекта может привести к серьезным угрозам безопасности. Пустой список DACL предоставляет полный доступ любому пользователю, который запрашивает его; Обычная проверка безопасности не выполняется в отношении объекта. Пустой список DACL не следует путать с пустым списком DACL. Пустой DACL — это правильно выделенный и инициализированный DACL, который не содержит записей контроля доступа (ACE). Пустой DACL не предоставляет доступа к объекту, которому он назначен.

Дополнительные сведения см. в статьях [DACL NULL и пустые списки DACL](/windows/desktop/SecAuthZ/null-dacls-and-empty-dacls).

 

 