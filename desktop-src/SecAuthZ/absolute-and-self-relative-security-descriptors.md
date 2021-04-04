---
description: Чтобы определить, является ли дескриптор безопасности самостоятельным или абсолютным, вызовите функцию Жетсекуритидескрипторконтрол и установите флаг "SE \_ Self \_ Relative" \_ параметра управления дескриптором безопасности \_ .
ms.assetid: dab2844b-7df9-446c-aacf-380a0a805cbc
title: Абсолютные и Self-Relative дескрипторы безопасности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b57406e194a31e79594394913055609e2981e5cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998723"
---
# <a name="absolute-and-self-relative-security-descriptors"></a>Абсолютные и Self-Relative дескрипторы безопасности

[*Дескриптор безопасности*](/windows/desktop/SecGloss/s-gly) может иметь либо [*абсолютный*](/windows/desktop/SecGloss/a-gly) , либо [*относительный*](/windows/desktop/SecGloss/s-gly) формат. В абсолютном формате дескриптор безопасности содержит указатели на сведения, а не на саму информацию. В автономном формате дескриптор безопасности хранит структуру [**\_ дескриптора безопасности**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) и связанные с ней сведения о безопасности в непрерывном блоке памяти. Чтобы определить, является ли дескриптор безопасности самостоятельным или абсолютным, вызовите функцию [**жетсекуритидескрипторконтрол**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) и установите флаг "SE \_ Self \_ Relative" параметра [**\_ \_ управления дескриптором безопасности**](security-descriptor-control.md) . Для преобразования между этими двумя форматами можно использовать функции [**макеселфрелативесд**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeselfrelativesd) и [**предполагался сбой makeabsolutesd**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeabsolutesd) .

Абсолютный формат полезен при создании дескриптора безопасности и указателей на все компоненты, например при наличии параметров по умолчанию для владельца, группы и избирательного списка управления доступом. В этом случае можно вызвать функцию [**InitializeSecurityDescriptor**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor) , чтобы инициализировать структуру [**\_ дескриптора безопасности**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) , а затем вызвать такие функции, как [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) , чтобы назначить дескриптору безопасности списки ACL и идентификаторы безопасности.

В автономном формате дескриптор безопасности всегда начинается со структуры [**\_ дескриптора безопасности**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) , но другие компоненты дескриптора безопасности могут следовать структуре в любом порядке. Вместо использования адресов памяти компоненты дескриптора безопасности определяются по смещению от начала дескриптора. Этот формат полезен, если дескриптор безопасности должен храниться на диске, передаваться по протоколу связи или копироваться в память.

За исключением [**предполагался сбой makeabsolutesd**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeabsolutesd), все функции, возвращающие дескриптор безопасности, используют автономный формат. Дескрипторы безопасности, передаваемые в качестве аргументов в функцию, могут быть либо самостоятельными, либо абсолютными формами. Дополнительные сведения см. в документации по функции.

 

 
