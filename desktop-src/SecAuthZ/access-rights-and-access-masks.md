---
description: Право доступа — это битовый флаг, соответствующий определенному набору операций, которые поток может выполнять над защищаемым объектом.
ms.assetid: da67c486-d2e7-4632-ac7a-c18aabc3f21d
title: Права доступа и маски доступа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1238766e2e4c8629b6c3a508b30d1e8832314d2e8ddd5ffdf4a1b93085f3c64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118914361"
---
# <a name="access-rights-and-access-masks"></a>Права доступа и маски доступа

*Право доступа* — это битовый флаг, соответствующий определенному набору операций, которые поток может выполнять над защищаемым объектом. Например, раздел реестра имеет \_ \_ право доступа к набору значений ключа, которое соответствует возможности потока для установки значения в ключе. Если поток пытается выполнить операцию над объектом, но не имеет необходимого права доступа к объекту, система не выполняет эту операцию.

[*Маска доступа*](/windows/desktop/SecGloss/a-gly) — это 32-разрядное значение, биты которого соответствуют правам доступа, поддерживаемым объектом. все защищаемые объекты Windows используют [формат маски доступа](access-mask-format.md) , который включает биты для следующих типов прав доступа:

-   [Универсальные права доступа](generic-access-rights.md)
-   [Стандартные права доступа](standard-access-rights.md)
-   [Право доступа к SACL](sacl-access-right.md)
-   [Права доступа к службам каталогов](directory-services-access-rights.md)

Когда поток пытается открыть обработчик для объекта, поток обычно задает маску доступа для [запроса набора прав доступа](requesting-access-rights-to-an-object.md). Например, приложение, которое должно устанавливать и запрашивать значения раздела реестра, может открыть ключ, используя маску доступа, чтобы запросить \_ \_ права доступа значения набора ключей и ключевых \_ запросов \_ .

В следующей таблице показаны функции, управляющие сведениями о безопасности для каждого типа защищаемых объектов.



| Тип объекта                                                                                                                                           | Функции дескрипторов безопасности                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Файлы или каталоги](/windows/desktop/FileIO/file-security-and-access-rights) в файловой системе NTFS                                                                     | [**Жетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**сетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**жетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**сетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Анонимные](/windows/desktop/ipc/anonymous-pipe-security-and-access-rights) каналы [именованных каналов](/windows/desktop/ipc/named-pipe-security-and-access-rights)<br/>                 | [**Жетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **сетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| Буферы экранов консоли                                                                                                                                | Не поддерживается.                                                                                                                                                                                     |
| [Обрабатывает](/windows/desktop/ProcThread/process-security-and-access-rights)[потоки](/windows/desktop/ProcThread/thread-security-and-access-rights)<br/>                                      | [**Жетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **сетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Объекты сопоставления файлов](/windows/desktop/Memory/file-mapping-security-and-access-rights)                                                                                  | [**Жетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**сетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**жетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**сетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Маркеры доступа в Azure Active Directory](access-rights-for-access-token-objects.md)                                                                                           | [**Сеткернелобжектсекурити**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity), [ **жеткернелобжектсекурити**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity)                                                                             |
| Объекты управления окнами ([оконные станции](/windows/desktop/winstation/window-station-security-and-access-rights) и [рабочие столы](/windows/desktop/winstation/desktop-security-and-access-rights)) | [**Жетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **сетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Разделы реестра](/windows/desktop/SysInfo/registry-key-security-and-access-rights)                                                                                         | [**Жетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**сетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**жетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**сетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Службы Windows](/windows/desktop/Services/service-security-and-access-rights)                                                                                           | [**Жетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**сетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**жетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**сетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Локальные или удаленные принтеры                                                                                                                              | [**Жетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**сетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**жетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**сетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Общие сетевые папки                                                                                                                                        | [**Жетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**сетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**жетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**сетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Объекты синхронизации между процессами](/windows/desktop/Sync/synchronization-object-security-and-access-rights) (события, мьютексы, семафоры и ожидающие таймеры)     | [**Жетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**сетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**жетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**сетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Объекты заданий](/windows/desktop/ProcThread/job-object-security-and-access-rights)                                                                                             | [**Жетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**сетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**жетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**сетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |



 

 

