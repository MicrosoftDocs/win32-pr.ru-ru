---
title: Интерфейсы ADSI и управление учетными записями пользователей
description: Windows и Windows Server имеют контроль учетных записей, который имеет последствия для приложений, использующих интерфейсы служб Active Directory (ADSI).
ms.assetid: 0b286252-8c24-4a18-9dc6-063ca158a8ff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1d0163348356f83b64522c9b05607d0d094ceb8f0ad530a798e546021433ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023972"
---
# <a name="adsi-and-user-account-control"></a>Интерфейсы ADSI и управление учетными записями пользователей

Windows и Windows Server имеют [контроль учетных записей](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10)), который имеет последствия для приложений, использующих [интерфейсы служб Active Directory](active-directory-service-interfaces-adsi.md) (ADSI). В частности, эти интерфейсы были созданы для запуска с учетной записью пользователя с правами администратора на локальном компьютере.

**Проблема.**

Каждый раз, когда приложение подключается к каталогу и пытается создать объект ADSI, [Active Directoryная схема](/windows/desktop/ADSchema/active-directory-schema) проверяется на наличие изменений. Если с момента последнего подключения он изменился, схема загружается и сохраняется в кэше на локальном компьютере. в версиях Windows до Windows Vista расположением по умолчанию для этого кэша было

`%systemroot%\SchCache\`

Однако приложения, работающие с учетными записями Standard (то есть без прав администратора), не будут иметь доступа к этому каталогу, поэтому приложения, использующие интерфейсы ADSI, которые выполняются в этом режиме, будут скачивать схему при каждом подключении, что повлияет на пропускную способность и производительность.

**Решения**

*Один пользователь* . для устранения этой проблемы существуют новые ключи управления реестром поставщика ADSI, которые определяют расположения реестра и расположения файлов для кэшированных [Active Directory объектов схемы](/windows/desktop/ADSchema/active-directory-schema) . Если раздел реестра

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\adsi\Cache\PerMachine`

имеет значение 0 (ноль), каждый пользователь будет иметь другое место хранения для ADSI; разделы реестра будут храниться в

`HKEY_CURRENT_USER\Software\Microsoft\ADs\Providers\LDAP\`

файлы кэша будут храниться в

`%LOCALAPPDATA%\Microsoft\Windows\SchCache`

эти параметры являются параметрами по умолчанию на компьютерах с Windows Server 2008 или Windows Vista.

*Несколько пользователей* . Если приложения ADSI выполняются на компьютере с несколькими учетными записями пользователей (например, на веб-сервере), предпочтительнее не иметь большого количества копий кэша [Active Directory схемы](/windows/desktop/ADSchema/active-directory-schema) , используя большие объемы дискового пространства. Настройка раздела реестра

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\adsi\Cache\PerMachine`

в 1 (один) вернет ADSI к предыдущему поведению; все объекты [схемы Active Directory](/windows/desktop/ADSchema/active-directory-schema) будут храниться в их предыдущих расположениях. раздел реестра будет находиться в

`HKEY_LOCAL_MACHINE\Software\Microsoft\ADs\Providers\LDAP`

и файл кэша будет находиться в

`%systemroot%\SchCache`

В этом случае учетные записи администратора должны запустить приложение, что приведет к кэшированию файла схемы в глобальном расположении для будущего использования пользователями с меньшими правами.

 

 