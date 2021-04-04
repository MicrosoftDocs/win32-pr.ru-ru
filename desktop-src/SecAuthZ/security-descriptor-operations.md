---
description: Используйте функции Жетсекуритинфо и Жетнамедсекуритинфо для получения указателя на дескриптор безопасности объектов.
ms.assetid: 834f1b58-d403-4899-865e-5721a37587e9
title: Операции с дескрипторами безопасности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5574a504468a4f4bb7dc14effe1f4717d695846
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154751"
---
# <a name="security-descriptor-operations"></a>Операции с дескрипторами безопасности

API Windows предоставляет функции для получения и установки компонентов [*дескриптора безопасности*](/windows/desktop/SecGloss/s-gly) , связанного с защищаемым объектом. Используйте функции [**жетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) и [**жетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) для получения указателя на дескриптор безопасности объекта. Эти функции могут также получать указатели на отдельные компоненты дескриптора безопасности: DACL, SACL, владелец SID и идентификатор безопасности основной группы. Используйте функции [**сетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) и [**сетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) , чтобы задать компоненты дескриптора безопасности объекта.

В общем случае следует использовать [**жетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) и [**сетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) с объектами, идентифицируемыми по маркеру, а также [**сетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) и [**жетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) с объектами, идентифицируемыми по имени. Дополнительные сведения о конкретных функциях, используемых при работе с объектами различных типов, см. в разделе [защищаемые объекты](securable-objects.md).

API Windows предоставляет дополнительные функции для управления компонентами дескриптора безопасности. Сведения о работе со списками управления доступом (DACL или SACL) см. в разделе [Получение сведений из ACL](getting-information-from-an-acl.md) и [Создание или изменение списка управления доступом](creating-or-modifying-an-acl.md). Сведения об идентификаторах безопасности см. в разделе [идентификаторы защиты](security-identifiers.md) (SID).

Чтобы получить сведения об элементе управления в дескрипторе безопасности, вызовите функцию [**жетсекуритидескрипторконтрол**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) . Чтобы задать контрольные биты, связанные с автоматическим наследованием ACE, вызовите функцию [**сетсекуритидескрипторконтрол**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) . Другие управляющие биты задаются различными функциями, заданными компонентом дескриптора безопасности. Например, если вы используете [**сетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) для изменения списка DACL объекта, функция устанавливает или очищает биты соответствующим образом, чтобы указать, имеет ли дескриптор безопасности список DACL, является ли он DACL по умолчанию и т. д. Еще один пример — контрольные биты [*диспетчера ресурсов*](/windows/desktop/SecGloss/r-gly) (RM), содержащиеся в дескрипторе безопасности. Эти биты используются в соответствии с реализацией диспетчера ресурсов и доступны через функции [**жетсекуритидескрипторрмконтрол**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorrmcontrol) и [**сетсекуритидескрипторрмконтрол**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorrmcontrol) .

 

 
