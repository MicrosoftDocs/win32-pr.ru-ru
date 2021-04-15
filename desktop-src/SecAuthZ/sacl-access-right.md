---
description: Право доступа \_ безопасности системы доступа \_ контролирует возможность получения или задания списка SACL в дескрипторе безопасности объектов. Система предоставляет это право доступа, если \_ \_ в маркере доступа запрашивающего потока включена привилегия предоставления имени безопасности SE.
ms.assetid: 88198243-dae5-49ac-9d54-bfae7a3a0b1a
title: Право доступа к SACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2366f30748a93294d4f30122102d656fb2590d34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662567"
---
# <a name="sacl-access-right"></a>Право доступа к SACL

Право доступа \_ безопасности системы доступа \_ контролирует возможность получения или задания списка SACL в [*дескрипторе безопасности*](/windows/desktop/SecGloss/s-gly)объекта. Система предоставляет это право доступа только в том случае, \_ Если \_ в [*маркере доступа*](/windows/desktop/SecGloss/a-gly) запрашивающего потока включена привилегия разрешения имен безопасности SE.

**Доступ к SACL объекта**

1.  Вызовите функцию [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) , чтобы включить \_ \_ привилегию имени безопасности SE.
2.  Запросите \_ право доступа системы \_ безопасности при открытии маркера объекта.
3.  Возвращает или задает список SACL объекта с помощью такой функции, как [**жетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) или [**сетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo).
4.  Вызовите [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) , чтобы отключить \_ \_ привилегию имени безопасности SE.

Чтобы получить доступ к SACL с помощью функций [**жетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) или [**сетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) , включите \_ привилегию SE- \_ имя безопасности. Функция внутренне запрашивает право доступа.

Право доступа \_ безопасности системы доступа недопустимо \_ в списке DACL, так как списки DACL не контролируют доступ к SACL. Тем не менее можно использовать право доступа \_ System \_ Security в списке SACL для аудита попыток использовать право доступа.

 

 
