---
description: Защищенное серверное приложение должно проверять права доступа клиентов перед предоставлением клиенту доступа к защищенному закрытому объекту.
ms.assetid: dce4dd10-1d5f-40a3-8a7e-ec708d3123c7
title: Проверка доступа к частным объектам
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f31f8ed05c16eed09cdd45da78f8fe58ecf41e283f6e6c37e7bc0480e63422d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783178"
---
# <a name="checking-access-to-private-objects"></a>Проверка доступа к частным объектам

Защищенное серверное приложение должно проверить права доступа клиента, прежде чем разрешить клиенту доступ к защищенному закрытому объекту. Для этого сервер передает [*маркер олицетворения*](/windows/desktop/SecGloss/i-gly), дескриптор безопасности и набор запрошенных прав доступа для [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck). [*Записи контроля доступа*](/windows/desktop/SecGloss/a-gly) (ACE) в списке DACL [*дескриптора безопасности*](/windows/desktop/SecGloss/s-gly) указывают права доступа, разрешенные или запрещенные для различных доверенных лиц. Функция **AccessCheck** сравнивает доверенное лицо в каждом ACE с доверенными лицами, указанными в токене олицетворения. Описание алгоритма, используемого для предоставления или запрета доступа, см. в статье [Управление доступом к объекту в DACL](how-dacls-control-access-to-an-object.md).

Функция [**акцессчеккандаудиталарм**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) выполняет аналогичную проверку доступа. Кроме того, он создает записи аудита в журнале событий безопасности в зависимости от списка SACL в дескрипторе безопасности.

Функции [**акцессчеккбитипе**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype) и [**Акцессчеккбитипеандаудиталарм**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytypeandauditalarma) похожи на [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) и [**акцессчеккандаудиталарм**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) , за исключением того, что они позволяют проверять доступ к вложенным объектам объекта, таким как наборы свойств или свойства. Функции [**акцессчеккбитипересултлист**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) и [**акцессчеккбитипересултлистандаудиталарм**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma) также похожи на **AccessCheck** , за исключением того, что они предоставляют результаты проверки доступа для каждого подобъекта в иерархии свойств и наборов свойств объекта. Эти функции используют структуру [**\_ \_ списка типов объектов**](/windows/desktop/api/Winnt/ns-winnt-object_type_list) для описания иерархии объектов, для которых установлен флажок доступ. Функции, создающие сообщение аудита, используют тип перечисления тип [**\_ \_ события аудита**](/windows/desktop/api/Winnt/ne-winnt-audit_event_type) , чтобы указать, является ли проверяемый объект объектом службы каталогов. Дополнительные сведения об иерархии объекта и его подобъектов см. [в разделе ACE для управления доступом к свойствам объекта](aces-to-control-access-to-an-object-s-properties.md).

Запрошенные права доступа, передаваемые в функции [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) и [**акцессчеккандаудиталарм**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) , не должны включать [Общие права доступа](generic-access-rights.md). Сервер может использовать функцию [**мапженерикмаск**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-mapgenericmask) для преобразования любых общих прав доступа к соответствующим определенным и стандартным правам в соответствии с сопоставлением, указанным в структуре [**универсального \_ сопоставления**](/windows/desktop/api/Winnt/ns-winnt-generic_mapping) .

Функции [**ареаллакцессесгрантед**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-areallaccessesgranted) и [**ареанякцессесгрантед**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-areanyaccessesgranted) сравнивают запрошенную [*маску доступа*](/windows/desktop/SecGloss/a-gly) с предоставленной маской доступа.

Пример кода, в котором используется функция [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) , см. [в разделе Проверка клиентского доступа с помощью ACL в C++](verifying-client-access-with-acls-in-c--.md).

Функция [**конверттоаутоинхеритприватеобжектсекурити**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) создает и возвращает дескриптор безопасности в формате, который позволяет автоматически распространять наследуемые ACE. Этот дескриптор безопасности содержит все ACE, унаследованные и неунаследованные в текущем дескрипторе безопасности и в [*автономном*](/windows/desktop/SecGloss/s-gly) формате. Функция **конверттоаутоинхеритприватеобжектсекурити** определяет, являются ли элементы ACE унаследованными или ненаследованными путем сравнения всех записей ACE в текущем дескрипторе безопасности со всеми записями ACE в родительском дескрипторе безопасности. Между двумя группами ACE может не быть однозначного соответствия. Например, ACE, который разрешает разрешение на чтение и запись, может быть эквивалентен двум записям ACE: ACE, который допускает разрешение на чтение, и запись ACE, которая разрешает разрешение на запись. Родительский дескриптор безопасности не может быть указан, если текущий дескриптор безопасности является родительским.

 

 
