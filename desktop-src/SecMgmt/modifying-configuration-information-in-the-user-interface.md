---
description: Расширение оснастки "вложение" должно позволять пользователю изменять сведения о конфигурации службы.
ms.assetid: fb36fcce-5a69-49cd-8cd3-b0b048f2f566
title: Изменение сведений о конфигурации в пользовательском интерфейсе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 414e2ab1475ec1c3241d60b96d182a522c299a9f5cf6134f50339c2088c99d9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005122"
---
# <a name="modifying-configuration-information-in-the-user-interface"></a>Изменение сведений о конфигурации в пользовательском интерфейсе

Расширение оснастки "вложение" должно позволять пользователю изменять сведения о конфигурации службы. Измененные данные должны храниться в расширении оснастки «вложение» до тех пор, пока оснастка настройки безопасности не вызовет методы интерфейса [**исцесвкаттачментперсистинфо**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) для получения информации.

Чтобы избежать утечек памяти, освободите память, выделенную подключаемым модулем, вызвав [**исцесвкаттачментперсистинфо:: фрибуффер**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentpersistinfo-freebuffer).

 

 



