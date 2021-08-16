---
description: Защищаемый объект — это объект, который может иметь дескриптор безопасности.
ms.assetid: 32f2ec06-822f-4d1e-bf51-5ae1d7355e60
title: Защищаемые объекты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93af0153082a5e94577e96e3b3f85c30ced8775aa8617bff84db37c96904d814
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780509"
---
# <a name="securable-objects"></a>Защищаемые объекты

Защищаемый объект — это объект, который может иметь [дескриптор безопасности](security-descriptors.md). все именованные объекты Windows являются защищаемыми. Некоторые неименованные объекты, такие как [*процессы*](/windows/desktop/SecGloss/p-gly) и объекты потоков, могут также иметь дескрипторы безопасности. Для большинства защищаемых объектов можно указать [*дескриптор безопасности*](/windows/desktop/SecGloss/s-gly) объекта в вызове функции, который создает объект. Например, можно указать дескриптор безопасности в функциях [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) и [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .

кроме того, функции безопасности Windows позволяют получать и задавать сведения о безопасности защищаемых объектов, созданных в операционных системах, отличных от Windows. функции безопасности Windows также обеспечивают поддержку использования дескрипторов безопасности с частными объектами, определяемыми приложением. Дополнительные сведения о закрытых защищаемых объектах см. в разделе [Управление доступом на клиент/сервер](client-server-access-control.md).

Каждый тип защищаемого объекта определяет собственный набор конкретных [прав доступа](access-rights-and-access-masks.md) и собственное [Сопоставление общих прав доступа](generic-access-rights.md). Сведения о конкретных и универсальных правах доступа для каждого типа защищаемого объекта см. в обзоре для этого типа объекта.

В следующей таблице показаны функции, используемые для управления сведениями о безопасности для некоторых распространенных защищаемых объектов.



| Тип объекта                                                                                                                                           | Функции дескрипторов безопасности                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Файлы или каталоги](/windows/desktop/FileIO/file-security-and-access-rights) в файловой системе NTFS                                                                     | [**Жетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**сетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**жетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**сетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Именованные каналы](/windows/desktop/ipc/named-pipe-security-and-access-rights)<br/> [Анонимные каналы](/windows/desktop/ipc/anonymous-pipe-security-and-access-rights)<br/>     | [**Жетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **сетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Процессы](/windows/desktop/ProcThread/process-security-and-access-rights)<br/> [Потоки](/windows/desktop/ProcThread/thread-security-and-access-rights)<br/>                          | [**Жетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **сетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Объекты сопоставления файлов](/windows/desktop/Memory/file-mapping-security-and-access-rights)                                                                                  | [**Жетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**сетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**жетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**сетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Маркеры доступа в Azure Active Directory](access-rights-for-access-token-objects.md)                                                                                           | [**Сеткернелобжектсекурити**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity), [ **жеткернелобжектсекурити**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity)                                                                             |
| Объекты управления окнами ([оконные станции](/windows/desktop/winstation/window-station-security-and-access-rights) и [рабочие столы](/windows/desktop/winstation/desktop-security-and-access-rights)) | [**Жетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **сетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Разделы реестра](/windows/desktop/SysInfo/registry-key-security-and-access-rights)                                                                                         | [**Жетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**сетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**жетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**сетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Службы Windows](/windows/desktop/Services/service-security-and-access-rights)                                                                                           | [**Жетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**сетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**жетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**сетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Локальные или удаленные принтеры                                                                                                                              | [**Жетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**сетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**жетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**сетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Общие сетевые папки                                                                                                                                        | [**Жетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**сетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**жетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**сетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Объекты синхронизации между процессами](/windows/desktop/Sync/synchronization-object-security-and-access-rights) (события, мьютексы, семафоры и ожидающие таймеры)     | [**Жетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**сетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**жетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**сетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Объекты заданий](/windows/desktop/ProcThread/job-object-security-and-access-rights)                                                                                             | [**Жетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**сетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**жетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**сетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Объекты службы каталогов                                                                                                                             | Эти объекты обрабатываются Active Directoryными объектами. Дополнительные сведения см. в разделе [интерфейсы службы Active Directory](/windows/desktop/ADSI/active-directory-service-interfaces-adsi).                             |



 

 

