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
# <a name="patching-per-user-managed-applications"></a><span data-ttu-id="78ee2-103">Исправление управляемых пользователем приложений</span><span class="sxs-lookup"><span data-stu-id="78ee2-103">Patching Per-User Managed Applications</span></span>

<span data-ttu-id="78ee2-104">Начиная с установщик Windows 3,0, можно применить исправления к приложению, которое было установлено в контексте, управляемом пользователем, после того как исправление будет зарегистрировано с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="78ee2-104">Beginning with Windows Installer 3.0, it is possible to apply patches to an application that has been installed in a per-user-managed context after the patch has been registered as having elevated privileges.</span></span>

<span data-ttu-id="78ee2-105">**Установщик Windows 2,0:** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="78ee2-105">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="78ee2-106">Вы не можете применить исправления к приложениям, которые установлены в контексте, управляемом пользователем, с использованием более ранних версий установщик Windows, чем установщик Windows 3,0.</span><span class="sxs-lookup"><span data-stu-id="78ee2-106">You cannot apply patches to applications that are installed in a per-user managed context using versions of Windows Installer earlier than Windows Installer 3.0.</span></span>

<span data-ttu-id="78ee2-107">В следующих случаях приложение устанавливается в состояние, управляемое для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="78ee2-107">An application is installed in the per-user-managed state in the following cases.</span></span>

-   <span data-ttu-id="78ee2-108">Установка приложения на уровне пользователя выполнялась с помощью развертывания и [Групповая политика](/previous-versions/windows/desktop/Policy/group-policy-start-page).</span><span class="sxs-lookup"><span data-stu-id="78ee2-108">The per-user installation of the application was performed using deployment and [Group Policy](/previous-versions/windows/desktop/Policy/group-policy-start-page).</span></span>
-   <span data-ttu-id="78ee2-109">Приложение было объявлено указанному пользователю и установлено методом, описанным в статье [объявление Per-User приложения для установки с повышенными привилегиями](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md).</span><span class="sxs-lookup"><span data-stu-id="78ee2-109">The application was advertised to a specified user and installed by the method described in [Advertising a Per-User Application To Be Installed with Elevated Privileges](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md).</span></span>

<span data-ttu-id="78ee2-110">Для установки приложения в контексте, управляемом пользователем, требуются права доступа. Таким образом, последующие установщик Windows переустановки или восстановления приложения также выполняются установщиком с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="78ee2-110">Privileges are required to install an application in the per-user-managed context; therefore, future Windows Installer reinstallations or repairs of the application are also performed by the installer using elevated privileges.</span></span> <span data-ttu-id="78ee2-111">Это означает, что в приложение можно применить только исправления из доверенных источников.</span><span class="sxs-lookup"><span data-stu-id="78ee2-111">This means that only patches from trusted sources can be applied to the application.</span></span>

<span data-ttu-id="78ee2-112">Начиная с установщик Windows 3,0, можно применить исправление к управляемому пользователем приложению после регистрации исправления с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="78ee2-112">Beginning with Windows Installer 3.0, you can apply a patch to a per-user managed application after the patch has been registered as having elevated privileges.</span></span> <span data-ttu-id="78ee2-113">Чтобы зарегистрировать исправление с повышенными привилегиями, используйте функцию [**мсисаурцелистаддсаурцеекс**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) или метод [**саурцелистаддсаурце**](patch-sourcelistaddsource.md) объекта [**Patch**](patch-object.md) с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="78ee2-113">To register a patch as having elevated privileges, use the [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) function or the [**SourceListAddSource**](patch-sourcelistaddsource.md) method of the [**Patch**](patch-object.md) object, with elevated privileges.</span></span> <span data-ttu-id="78ee2-114">После регистрации исправления можно применить его с помощью функций [**мсиапплипатч**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) или [**мсиапплимултиплепатчес**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) , [**Апплипатч**](installer-applypatch.md) или [**апплимултиплепатчес**](installer-applymultiplepatches.md) методов [**объекта установщика**](installer-object.md)или [параметра командной строки](command-line-options.md)/p.</span><span class="sxs-lookup"><span data-stu-id="78ee2-114">After registering the patch, you can apply the patch using the [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) functions, [**ApplyPatch**](installer-applypatch.md) or [**ApplyMultiplePatches**](installer-applymultiplepatches.md) methods of the [**Installer Object**](installer-object.md), or the /p [command-line option](command-line-options.md).</span></span>

> [!Note]
> <span data-ttu-id="78ee2-115">Перед установкой приложения можно зарегистрировать исправление с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="78ee2-115">A patch can be registered as having elevated privileges before the application is installed.</span></span> <span data-ttu-id="78ee2-116">После регистрации исправления оно остается зарегистрированным до тех пор, пока не будет удалено Последнее зарегистрированное приложение для этого исправления.</span><span class="sxs-lookup"><span data-stu-id="78ee2-116">When a patch has been registered, it remains registered until the last registered application for this patch is removed.</span></span>
> 
> <span data-ttu-id="78ee2-117">Исправления, примененные к управляемому пользователем приложению, не могут быть удалены без удаления всего приложения.</span><span class="sxs-lookup"><span data-stu-id="78ee2-117">Patches that have been applied to a per-user managed application cannot be removed without removing the entire application.</span></span> <span data-ttu-id="78ee2-118">Регистрация исправлений для приложения, управляемого пользователем, удаляется при удалении приложения.</span><span class="sxs-lookup"><span data-stu-id="78ee2-118">The patch registrations for a per-user managed application are removed on the removal of the application.</span></span>

<span data-ttu-id="78ee2-119">Этот метод также можно использовать, чтобы разрешить пользователям без прав администратора исправлять приложения для конкретного компьютера, или можно использовать исправление с минимальными правами доступа, описанное в статье [исправление контроля учетных записей пользователей (UAC)](user-account-control--uac--patching.md).</span><span class="sxs-lookup"><span data-stu-id="78ee2-119">You can also use this method to enable a non-administrator to patch a per-machine application, or you can use least-privilege patching described in [User Account Control (UAC) Patching](user-account-control--uac--patching.md).</span></span>

## <a name="example-1"></a><span data-ttu-id="78ee2-120">Пример 1</span><span class="sxs-lookup"><span data-stu-id="78ee2-120">Example 1</span></span>

<span data-ttu-id="78ee2-121">В следующем примере сценария используется метод [**саурцелистаддсаурце**](patch-sourcelistaddsource.md) для регистрации пакета исправлений, который находится на странице \\ \\ Server \\ Share \\ Products patchs \\ \\ example. MSP с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="78ee2-121">The following scripting sample uses the [**SourceListAddSource**](patch-sourcelistaddsource.md) method to register a patch package located at \\\\server\\share\\products\\patches\\example.msp as having elevated privileges.</span></span> <span data-ttu-id="78ee2-122">Затем это исправление готово к применению к продукту, управляемому пользователем.</span><span class="sxs-lookup"><span data-stu-id="78ee2-122">That patch is then ready to be applied to a per-user managed product.</span></span>

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

## <a name="example-2"></a><span data-ttu-id="78ee2-123">Пример 2</span><span class="sxs-lookup"><span data-stu-id="78ee2-123">Example 2</span></span>

<span data-ttu-id="78ee2-124">В следующем примере кода функция [**мсисаурцелистаддсаурцеекс**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) используется для регистрации пакета исправлений, расположенного на странице \\ \\ Server \\ Share \\ Products patchs \\ \\ example. MSP с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="78ee2-124">The following code sample uses the [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) function to register a patch package located at \\\\server\\share\\products\\patches\\example.msp as having elevated privileges.</span></span> <span data-ttu-id="78ee2-125">Затем это исправление готово к применению к продукту, управляемому пользователем.</span><span class="sxs-lookup"><span data-stu-id="78ee2-125">That patch is then ready to be applied to a per-user managed product.</span></span>


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



 

 
