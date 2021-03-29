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
# <a name="services-and-the-registry"></a><span data-ttu-id="32217-104">Службы и реестр</span><span class="sxs-lookup"><span data-stu-id="32217-104">Services and the Registry</span></span>

<span data-ttu-id="32217-105">Служба не должна обращаться к **\_ \_ корневому каталогу** **hKey \_ Current \_ User** или hKey classes, особенно при олицетворении пользователя.</span><span class="sxs-lookup"><span data-stu-id="32217-105">A service should not access **HKEY\_CURRENT\_USER** or **HKEY\_CLASSES\_ROOT**, especially when impersonating a user.</span></span> <span data-ttu-id="32217-106">Вместо этого используйте функцию [**регопенкуррентусер**](/windows/desktop/api/winreg/nf-winreg-regopencurrentuser) или [**регопенусерклассесрут**](/windows/desktop/api/winreg/nf-winreg-regopenuserclassesroot) .</span><span class="sxs-lookup"><span data-stu-id="32217-106">Instead, use the [**RegOpenCurrentUser**](/windows/desktop/api/winreg/nf-winreg-regopencurrentuser) or [**RegOpenUserClassesRoot**](/windows/desktop/api/winreg/nf-winreg-regopenuserclassesroot) function.</span></span>

<span data-ttu-id="32217-107">Если вы попытаетесь получить доступ к **\_ \_ корневому каталогу** **hKey для \_ текущего \_ пользователя** или hKey classes из службы, может произойти сбой или он работает, но существует базовая утечка, которая может привести к проблемам с загрузкой или выгрузкой профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="32217-107">If you attempt to access **HKEY\_CURRENT\_USER** or **HKEY\_CLASSES\_ROOT** from a service it may fail, or it may appear to work but there is an underlying leak that can lead to problems loading or unloading the user profile.</span></span>

 

 
