---
description: Право доступа \_ безопасности системы доступа \_ контролирует возможность получения или задания списка SACL в дескрипторе безопасности объектов. система предоставляет это право доступа, если в \_ \_ маркере доступа запрашивающего потока включена привилегия SE имя безопасности.
ms.assetid: 88198243-dae5-49ac-9d54-bfae7a3a0b1a
title: Право доступа к SACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88256664db25c6e906f3b4ca0459217a29d0cc7c0e2dd544c1cf198bc24fff5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780519"
---
# <a name="sacl-access-right"></a>Право доступа к SACL

Право доступа \_ безопасности системы доступа \_ контролирует возможность получения или задания списка SACL в [*дескрипторе безопасности*](/windows/desktop/SecGloss/s-gly)объекта. система предоставляет это право доступа только в том случае, если в \_ \_ [*маркере доступа*](/windows/desktop/SecGloss/a-gly) запрашивающего потока включена привилегия SE имя безопасности.

**Доступ к SACL объекта**

1.  вызовите функцию [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) , чтобы включить \_ \_ привилегию SE имя безопасности.
2.  Запросите \_ право доступа системы \_ безопасности при открытии маркера объекта.
3.  Возвращает или задает список SACL объекта с помощью такой функции, как [**жетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) или [**сетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo).
4.  вызовите [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) , чтобы отключить \_ \_ привилегию SE имени безопасности.

чтобы получить доступ к SACL с помощью функций [**жетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) или [**сетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) , включите \_ \_ привилегию SE имя безопасности. Функция внутренне запрашивает право доступа.

Право доступа \_ безопасности системы доступа недопустимо \_ в списке DACL, так как списки DACL не контролируют доступ к SACL. Тем не менее можно использовать право доступа \_ System \_ Security в списке SACL для аудита попыток использовать право доступа.

 

 
