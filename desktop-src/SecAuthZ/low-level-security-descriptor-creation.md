---
description: Функции для создания дескриптора безопасности и получения и установки компонентов дескриптора безопасности.
ms.assetid: d07dab5a-7c06-40c4-aa59-fa0baaaa77e7
title: Создание дескриптора безопасности низкого уровня
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdafc99fe4d01c24e68a076aecc035843452205b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651090"
---
# <a name="low-level-security-descriptor-creation"></a>Создание дескриптора безопасности низкого уровня

Низкий уровень контроля доступа предоставляет набор функций для создания [*дескриптора безопасности*](/windows/desktop/SecGloss/s-gly) и получения и установки компонентов дескриптора безопасности. Низкоуровневые функции для инициализации и установки компонентов дескриптора безопасности работают только с абсолютными дескрипторами безопасности. Низкоуровневые функции для получения компонентов дескриптора безопасности работают как с [абсолютными, так и с самостоятельными дескрипторами безопасности](absolute-and-self-relative-security-descriptors.md).

Функция [**InitializeSecurityDescriptor**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor) инициализирует буфер [**\_ дескриптора безопасности**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) . Инициализированный дескриптор безопасности имеет [*абсолютный*](/windows/desktop/SecGloss/a-gly) формат и не имеет владельца, основной группы, [*избирательного списка управления доступом*](/windows/desktop/SecGloss/d-gly) (DACL) или [*системного списка управления доступом*](/windows/desktop/SecGloss/s-gly) (SACL). Для получения или задания определенных компонентов указанного дескриптора безопасности можно использовать следующие низкоуровневые функции.



| Функция                                                             | Описание                                                                                                                                                               |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**жетсекуритидескрипторконтрол**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) | Извлекает сведения об исправлении и управлении из дескриптора безопасности.                                                                                                    |
| [**жетсекуритидескриптордакл**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl)       | Извлекает список DACL из дескриптора безопасности.                                                                                                                            |
| [**жетсекуритидескрипторграуп**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorgroup)     | Извлекает [*идентификатор безопасности*](/windows/desktop/SecGloss/s-gly) (SID) основной группы из дескриптора безопасности. |
| [**жетсекуритидескрипторленгс**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorlength)   | Возвращает длину дескриптора безопасности.                                                                                                                              |
| [**Функций getsecuritydescriptorowner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)     | Получает ИД безопасности владельца из дескриптора безопасности.                                                                                                                       |
| [**жетсекуритидескрипторсакл**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl)       | Извлекает список SACL из дескриптора безопасности.                                                                                                                            |
| [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl)       | Помещает список DACL в дескриптор безопасности, заменяя все существующие списки DACL.                                                                                                    |
| [**SetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorgroup)     | Задает идентификатор безопасности основной группы дескриптора.                                                                                                                      |
| [**SetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner)     | Задает ИД безопасности владельца дескриптора безопасности.                                                                                                                              |
| [**сетсекуритидескрипторсакл**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl)       | Помещает список SACL в дескриптор безопасности, заменяя все существующие SACL.                                                                                                    |



 

Чтобы проверить уровень редакции и структурную [*целостность*](/windows/desktop/SecGloss/i-gly) дескриптора безопасности, вызовите функцию [**исвалидсекуритидескриптор**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-isvalidsecuritydescriptor) .

 

 
