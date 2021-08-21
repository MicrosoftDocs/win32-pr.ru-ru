---
description: Служба не должна обращаться к \_ \_ корневому каталогу hKey Current User или hKey \_ Classes \_ , особенно при олицетворении пользователя. Вместо этого используйте функцию Регопенкуррентусер или Регопенусерклассесрут.
ms.assetid: 8ad6c081-7ac0-4557-88dc-d8f1ec139926
title: Службы и реестр
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6bb5b20a5564805572c1863581bb041d8d886d660d727ead4aa3fb753a50609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117967091"
---
# <a name="services-and-the-registry"></a>Службы и реестр

Служба не должна обращаться к **\_ \_ корневому каталогу** **hKey \_ Current \_ User** или hKey classes, особенно при олицетворении пользователя. Вместо этого используйте функцию [**регопенкуррентусер**](/windows/desktop/api/winreg/nf-winreg-regopencurrentuser) или [**регопенусерклассесрут**](/windows/desktop/api/winreg/nf-winreg-regopenuserclassesroot) .

Если вы попытаетесь получить доступ к **\_ \_ корневому каталогу** **hKey для \_ текущего \_ пользователя** или hKey classes из службы, может произойти сбой или он работает, но существует базовая утечка, которая может привести к проблемам с загрузкой или выгрузкой профиля пользователя.

 

 
