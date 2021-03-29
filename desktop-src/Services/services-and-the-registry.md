---
description: Служба не должна обращаться к \_ \_ корневому каталогу hKey Current User или hKey \_ Classes \_ , особенно при олицетворении пользователя. Вместо этого используйте функцию Регопенкуррентусер или Регопенусерклассесрут.
ms.assetid: 8ad6c081-7ac0-4557-88dc-d8f1ec139926
title: Службы и реестр
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669da912d5eb2a76981ff6e08293acccb1e313fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664363"
---
# <a name="services-and-the-registry"></a>Службы и реестр

Служба не должна обращаться к **\_ \_ корневому каталогу** **hKey \_ Current \_ User** или hKey classes, особенно при олицетворении пользователя. Вместо этого используйте функцию [**регопенкуррентусер**](/windows/desktop/api/winreg/nf-winreg-regopencurrentuser) или [**регопенусерклассесрут**](/windows/desktop/api/winreg/nf-winreg-regopenuserclassesroot) .

Если вы попытаетесь получить доступ к **\_ \_ корневому каталогу** **hKey для \_ текущего \_ пользователя** или hKey classes из службы, может произойти сбой или он работает, но существует базовая утечка, которая может привести к проблемам с загрузкой или выгрузкой профиля пользователя.

 

 
