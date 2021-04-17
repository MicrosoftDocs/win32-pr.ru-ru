---
description: Начиная с установщик Windows 3,0, можно применить исправления к приложению, которое было установлено в контексте, управляемом пользователем, после того как исправление будет зарегистрировано с повышенными привилегиями.
ms.assetid: ebe5f447-9b74-48dc-8192-f2ac90dca490
title: Исправление управляемых пользователем приложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa6a19933e5c8ab409d510d980b8ed634a630e1
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105664838"
---
# <a name="patching-per-user-managed-applications"></a>Исправление управляемых пользователем приложений

Начиная с установщик Windows 3,0, можно применить исправления к приложению, которое было установлено в контексте, управляемом пользователем, после того как исправление будет зарегистрировано с повышенными привилегиями.

**Установщик Windows 2,0:** Не поддерживается. Вы не можете применить исправления к приложениям, которые установлены в контексте, управляемом пользователем, с использованием более ранних версий установщик Windows, чем установщик Windows 3,0.

В следующих случаях приложение устанавливается в состояние, управляемое для каждого пользователя.

-   Установка приложения на уровне пользователя выполнялась с помощью развертывания и [Групповая политика](/previous-versions/windows/desktop/Policy/group-policy-start-page).
-   Приложение было объявлено указанному пользователю и установлено методом, описанным в статье [объявление Per-User приложения для установки с повышенными привилегиями](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md).

Для установки приложения в контексте, управляемом пользователем, требуются права доступа. Таким образом, последующие установщик Windows переустановки или восстановления приложения также выполняются установщиком с повышенными привилегиями. Это означает, что в приложение можно применить только исправления из доверенных источников.

Начиная с установщик Windows 3,0, можно применить исправление к управляемому пользователем приложению после регистрации исправления с повышенными привилегиями. Чтобы зарегистрировать исправление с повышенными привилегиями, используйте функцию [**мсисаурцелистаддсаурцеекс**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) или метод [**саурцелистаддсаурце**](patch-sourcelistaddsource.md) объекта [**Patch**](patch-object.md) с повышенными привилегиями. После регистрации исправления можно применить его с помощью функций [**мсиапплипатч**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) или [**мсиапплимултиплепатчес**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) , [**Апплипатч**](installer-applypatch.md) или [**апплимултиплепатчес**](installer-applymultiplepatches.md) методов [**объекта установщика**](installer-object.md)или [параметра командной строки](command-line-options.md)/p.

> [!Note]
> Перед установкой приложения можно зарегистрировать исправление с повышенными привилегиями. После регистрации исправления оно остается зарегистрированным до тех пор, пока не будет удалено Последнее зарегистрированное приложение для этого исправления.
> 
> Исправления, примененные к управляемому пользователем приложению, не могут быть удалены без удаления всего приложения. Регистрация исправлений для приложения, управляемого пользователем, удаляется при удалении приложения.

Этот метод также можно использовать, чтобы разрешить пользователям без прав администратора исправлять приложения для конкретного компьютера, или можно использовать исправление с минимальными правами доступа, описанное в статье [исправление контроля учетных записей пользователей (UAC)](user-account-control--uac--patching.md).

## <a name="example-1"></a>Пример 1

В следующем примере сценария используется метод [**саурцелистаддсаурце**](patch-sourcelistaddsource.md) для регистрации пакета исправлений, который находится на странице \\ \\ Server \\ Share \\ Products patchs \\ \\ example. MSP с повышенными привилегиями. Затем это исправление готово к применению к продукту, управляемому пользователем.

``` syntax
const msiInstallContextUserManaged = 1
const msiInstallSourceTypeNetwork = 1

const PatchCode = "{XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}"
const UserSid = "S-X-X-XX-XXXXXXXXX-XXXXXXXXX-XXXXXXXXX-XXXXXXX"
const PatchPath = "\\server\share\products\patches\"
const PatchPackageName = "example.msp"

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

Set patch = installer.Patch(PatchCode, "", UserSid, msiInstallContextUserManaged)

patch.SourceListAddSource msiInstallSourceTypeNetwork, PatchPath, 0

patch.SourceListInfo("PackageName") = PatchPackageName
```

## <a name="example-2"></a>Пример 2

В следующем примере кода функция [**мсисаурцелистаддсаурцеекс**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) используется для регистрации пакета исправлений, расположенного на странице \\ \\ Server \\ Share \\ Products patchs \\ \\ example. MSP с повышенными привилегиями. Затем это исправление готово к применению к продукту, управляемому пользователем.


```C++
#ifndef UNICODE
#define UNICODE
#endif    // UNICODE

#ifndef _WIN32_MSI
#define _WIN32_MSI
#endif    // _WIN32_MSI

#include <windows.h>
#include <msi.h>


/////////////////////////////////////////////////////////////////
// RegisterElevatedPatch
//
// Purpose: register a patch elevated from a network location
//
// Arguments:
//    wszPatchCode <entity type="ndash"/> GUID of patch to be registered
//    wszUserSid   - String SID that specifies the user account
//    wszPatchPath <entity type="ndash"/> Network location of patch
//    wszPatchPackageName <entity type="ndash"/> Package name of patch
//
/////////////////////////////////////////////////////////////////
UINT RegisterElevatedPatch(LPCWSTR wszPatchCode, 
LPCWSTR wszUserSid, 
LPCWSTR wszPatchPath, 
LPCWSTR wszPatchPackageName)
{
// wszUserSid can be NULL
// when wszUserSid is NULL, register patch for current user
// current user must be administrator
if (!wszPatchCode || !wszPatchPath || !wszPatchPackageName)
    return ERROR_INVALID_PARAMETER;

UINT uiReturn = ERROR_SUCCESS;

uiReturn = MsiSourceListAddSourceEx(
/*szPatchCode*/ wszPatchCode,
/*szUserSid*/ wszUserSid,
/*dwContext*/ MSIINSTALLCONTEXT_USERMANAGED,
/*dwOptions*/ MSISOURCETYPE_NETWORK+MSICODE_PATCH,
/*szSource*/ wszPatchPath,
/*dwIndex*/ 0);
if (ERROR_SUCCESS == uiReturn)
{
uiReturn = MsiSourceListSetInfo(
/*szPatchCode*/ wszPatchCode,
/*szUserSid*/ wszUserSid,
/*dwContext*/ MSIINSTALLCONTEXT_USERMANAGED,
/*dwOptions*/ MSISOURCETYPE_NETWORK+MSICODE_PATCH,
/*szProperty*/ L"PackageName",
/*szValue*/ wszPatchPackageName);
if (ERROR_SUCCESS != uiReturn)
{
// Function call failed, return error code
    return uiReturn;
}
}
else
{
// Function call failed, return error code
    return uiReturn;
}

return ERROR_SUCCESS;
}


```



 

 
