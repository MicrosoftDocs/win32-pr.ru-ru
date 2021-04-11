---
description: Создайте список управления доступом (ACL) с помощью низкоуровневых функций, выделите буфер для ACL и инициализируйте его, вызвав функцию Инитиализеакл.
ms.assetid: 9dcbbd4c-b3b3-43fd-b3a6-0637a53a455a
title: Низкоуровневые ACL и функции ACE низкого уровня
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac63c17d84996afe9bdc43d0ccdd021db69ab488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912423"
---
# <a name="low-level-acl-and-ace-functions"></a>Низкоуровневые ACL и функции ACE низкого уровня

Чтобы создать [*список управления доступом*](/windows/desktop/SecGloss/a-gly) (ACL) с помощью низкоуровневых функций, выделите БУФЕР для ACL, а затем инициализируйте его, вызвав функцию [**инитиализеакл**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializeacl) . Чтобы добавить [*записи управления доступом*](/windows/desktop/SecGloss/a-gly) (ACE) в конец [*списка управления доступом на уровне пользователей*](/windows/desktop/SecGloss/d-gly) (DACL), используйте функции [**аддакцессалловедаце**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedace) и [**аддакцессдениедаце**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedace) . Функция [**аддаудитакцессаце**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addauditaccessace) добавляет ACE в конец [*системного списка управления доступом*](/windows/desktop/SecGloss/s-gly) (SACL). Функцию [**аддаце**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace) можно использовать для добавления одного или нескольких записей ACE в указанную позиции в списке управления доступом. Функция **аддаце** также позволяет добавить наследуемый ACE в ACL. Функция [**делетеаце**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-deleteace) удаляет запись ACE из указанной должности в списке управления доступом. Функция [**жетаце**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getace) извлекает элемент ACE из указанной должности в списке управления доступом. Функция [**финдфирстфриаце**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-findfirstfreeace) извлекает указатель на первый свободный байт в ACL.

Чтобы изменить существующий список ACL в [*дескрипторе безопасности*](/windows/desktop/SecGloss/s-gly)объекта, используйте функцию [**жетсекуритидескриптордакл**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl) или [**жетсекуритидескрипторсакл**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl) , чтобы получить существующий список ACL. Для копирования записей ACE из существующего списка ACL можно использовать функцию [**жетаце**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getace) . После выделения и инициализации нового списка ACL используйте такие функции, как [**аддакцессалловедаце**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedace) и [**аддаце**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace) , чтобы добавить к нему записи ACE. После завершения создания нового списка ACL используйте функцию [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) или [**сетсекуритидескрипторсакл**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl) , чтобы добавить новый список управления доступом к дескриптору безопасности объекта.

Вы можете использовать функции [**аддакцессалловедобжектаце**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace), [**аддакцессдениедобжектаце**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedobjectace)или [**Аддаудитакцессобжектаце**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addauditaccessobjectace) , чтобы добавить [записи ACE для конкретного объекта](object-specific-aces.md) в конец списка ACL.

 

 
