---
description: Начиная с установщик Windows 3,0, некоторые исправления можно удалить из приложений.
ms.assetid: 11e995b7-30c7-4992-b436-3af289ac3966
title: Удаление исправлений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff9418704bdeeb5ccc57839cbe2416faa5692265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272939"
---
# <a name="uninstalling-patches"></a><span data-ttu-id="676be-103">Удаление исправлений</span><span class="sxs-lookup"><span data-stu-id="676be-103">Uninstalling Patches</span></span>

<span data-ttu-id="676be-104">Начиная с установщик Windows 3,0, некоторые исправления можно удалить из приложений.</span><span class="sxs-lookup"><span data-stu-id="676be-104">Beginning with Windows Installer 3.0, it is possible to uninstall some patches from applications.</span></span> <span data-ttu-id="676be-105">Исправление должно быть [неудаляемым исправлением](uninstallable-patches.md).</span><span class="sxs-lookup"><span data-stu-id="676be-105">The patch must be an [uninstallable patch](uninstallable-patches.md).</span></span> <span data-ttu-id="676be-106">При использовании установщик Windows версии, отличной от версии 3,0, [Удаление исправлений требует удаления](removing-patches.md) продукта исправления и переустановки продукта без применения исправления.</span><span class="sxs-lookup"><span data-stu-id="676be-106">When using a Windows Installer version less than version 3.0, [removing patches](removing-patches.md) requires uninstalling the patch product and reinstalling the product without applying the patch.</span></span>

<span data-ttu-id="676be-107">**Установщик Windows 2,0:** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="676be-107">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="676be-108">Исправления, примененные с помощью более ранней версии установщик Windows, чем установщик Windows 3,0, не могут быть удалены.</span><span class="sxs-lookup"><span data-stu-id="676be-108">Patches applied using a version of Windows Installer that is earlier than Windows Installer 3.0 are not uninstallable.</span></span>

<span data-ttu-id="676be-109">При вызове удаления исправления любым из следующих методов установщик пытается удалить исправление из первого продукта, видимого для приложения или пользователя, запрашивающего удаление.</span><span class="sxs-lookup"><span data-stu-id="676be-109">When you invoke an uninstallation of a patch by any of the following methods, the installer attempts to remove the patch from the first product visible to the application or user requesting the uninstallation.</span></span> <span data-ttu-id="676be-110">Установщик ищет продукты с исправлениями в следующем порядке: управляемый пользователем, неуправляемый для каждого пользователя, на компьютер.</span><span class="sxs-lookup"><span data-stu-id="676be-110">The installer searches for patched products in the following order: per-user managed, per-user unmanaged, per-machine.</span></span>

## <a name="uninstalling-a-patch-using-msipatchremove-on-a-command-line"></a><span data-ttu-id="676be-111">Удаление исправления с помощью МСИПАТЧРЕМОВЕ в командной строке</span><span class="sxs-lookup"><span data-stu-id="676be-111">Uninstalling a patch using MSIPATCHREMOVE on a command line</span></span>

<span data-ttu-id="676be-112">Вы можете удалить исправления из команды с помощью msiexec.exe и [параметров командной строки](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="676be-112">You can uninstall patches from a command by using msiexec.exe and the [Command Line Options](command-line-options.md).</span></span> <span data-ttu-id="676be-113">В приведенном ниже примере командная строка удаляет [исправление](uninstallable-patches.md), например MSP, из приложения example.msi с помощью свойства [**мсипатчремове**](msipatchremove.md) и параметра командной строки/i.</span><span class="sxs-lookup"><span data-stu-id="676be-113">The following sample command line removes an [uninstallable patch](uninstallable-patches.md), example.msp, from an application, example.msi, using the [**MSIPATCHREMOVE**](msipatchremove.md) property and the /i command line option.</span></span> <span data-ttu-id="676be-114">При использовании параметра/i исправленное приложение может быть идентифицировано по пути к пакету приложения (MSI-файлу) или [коду продукта](product-codes.md)приложения.</span><span class="sxs-lookup"><span data-stu-id="676be-114">When using /i, the patched application can be identified by the path to the application's package (.msi file) or the application's [product code](product-codes.md).</span></span> <span data-ttu-id="676be-115">В этом примере пакет установки приложения находится в папке " \\ \\ Server \\ Share \\ Products \\ example \\example.msi", а свойство [**ProductCode**](productcode.md) приложения — "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span><span class="sxs-lookup"><span data-stu-id="676be-115">In this example, the application's installation package is located at "\\\\server\\share\\products\\example\\example.msi" and the application's [**ProductCode**](productcode.md) property is "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span></span> <span data-ttu-id="676be-116">Пакет исправлений находится в папке " \\ \\ Server \\ Share \\ Products example patchs example \\ \\ \\ . MSP", а код исправления GUID — "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span><span class="sxs-lookup"><span data-stu-id="676be-116">The patch package is located at "\\\\server\\share\\products\\example\\patches\\example.msp" and the patch code GUID is "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span></span>

<span data-ttu-id="676be-117">**Msiexec/I {0C9840E7-7F0B-C648-10F0-4641926FE463} МСИПАТЧРЕМОВЕ = {EB8C947C-78B2-85A0-644D-86CEEF8E07C0}/QB**</span><span class="sxs-lookup"><span data-stu-id="676be-117">**Msiexec /I {0C9840E7-7F0B-C648-10F0-4641926FE463} MSIPATCHREMOVE={EB8C947C-78B2-85A0-644D-86CEEF8E07C0} /qb**</span></span>

## <a name="uninstalling-a-patch-using-the-standard-command-line-options"></a><span data-ttu-id="676be-118">Удаление исправления с помощью стандартных параметров командной строки</span><span class="sxs-lookup"><span data-stu-id="676be-118">Uninstalling a patch using the standard command line options</span></span>

<span data-ttu-id="676be-119">Начиная с версии установщик Windows 3,0 можно использовать [стандартные параметры командной строки](standard-installer-command-line-options.md) , используемые обновлениями операционной системы Microsoft Windows (update.exe), чтобы удалить установщик Windows исправления из командной строки.</span><span class="sxs-lookup"><span data-stu-id="676be-119">Beginning with Windows Installer version 3.0, you can use the [standard command line options](standard-installer-command-line-options.md) used by Microsoft Windows Operating System Updates (update.exe) to uninstall Windows Installer patches from a command line.</span></span>

<span data-ttu-id="676be-120">Следующая командная строка представляет собой стандартную командную строку, эквивалентную командной строке установщик Windows, используемой для удаления исправления с помощью свойства [**мсипатчремове**](msipatchremove.md) .</span><span class="sxs-lookup"><span data-stu-id="676be-120">The following command line is the standard command line equivalent of the Windows Installer command line used to uninstall a patch using the [**MSIPATCHREMOVE**](msipatchremove.md) property.</span></span> <span data-ttu-id="676be-121">Параметр/uninstall, используемый с параметром/Package, обозначает удаление исправления.</span><span class="sxs-lookup"><span data-stu-id="676be-121">The /uninstall option used with the /package option denotes the uninstallation of a patch.</span></span> <span data-ttu-id="676be-122">На исправление может ссылаться полный путь к исправлению или идентификатор GUID кода исправления.</span><span class="sxs-lookup"><span data-stu-id="676be-122">The patch can be referenced by the full path to the patch or by the patch code GUID.</span></span>

<span data-ttu-id="676be-123">**Msiexec/Package {0C9840E7-7F0B-C648-10F0-4641926FE463}/uninstall {EB8C947C-78B2-85A0-644D-86CEEF8E07C0}/passive**</span><span class="sxs-lookup"><span data-stu-id="676be-123">**Msiexec /package {0C9840E7-7F0B-C648-10F0-4641926FE463} /uninstall {EB8C947C-78B2-85A0-644D-86CEEF8E07C0} /passive**</span></span>

> [!Note]  
> <span data-ttu-id="676be-124">Параметр/passive Standard не является точным эквивалентом параметра установщик Windows/QB.</span><span class="sxs-lookup"><span data-stu-id="676be-124">The /passive standard option is not an exact equivalent of the Windows Installer /qb option.</span></span>

 

## <a name="uninstalling-a-patch-using-the-removepatches-method"></a><span data-ttu-id="676be-125">Удаление исправления с помощью метода Ремовепатчес</span><span class="sxs-lookup"><span data-stu-id="676be-125">Uninstalling a patch using the RemovePatches method</span></span>

<span data-ttu-id="676be-126">Вы можете удалить исправления из скрипта с помощью установщик Windows [интерфейса автоматизации](automation-interface.md).</span><span class="sxs-lookup"><span data-stu-id="676be-126">You can uninstall patches from script by using the Windows Installer [Automation Interface](automation-interface.md).</span></span> <span data-ttu-id="676be-127">Приведенный ниже пример сценария удаляет [исправление](uninstallable-patches.md), например MSP, из приложения example.msi с помощью метода [**ремовепатчес**](installer-removepatches.md) объекта [установщика](installer-object.md) .</span><span class="sxs-lookup"><span data-stu-id="676be-127">The following scripting sample removes an [uninstallable patch](uninstallable-patches.md), example.msp, from an application, example.msi, using the [**RemovePatches**](installer-removepatches.md) method of the [Installer](installer-object.md) object.</span></span> <span data-ttu-id="676be-128">Каждое удаляемое исправление может быть представлено полным путем к пакету исправлений или идентификатором GUID кода исправления.</span><span class="sxs-lookup"><span data-stu-id="676be-128">Each patch being uninstalled can be represented by either the full path to the patch package or the patch code GUID.</span></span> <span data-ttu-id="676be-129">В этом примере пакет установки приложения находится в папке " \\ \\ Server \\ Share \\ Products \\ example \\example.msi", а свойство [**ProductCode**](productcode.md) приложения — "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span><span class="sxs-lookup"><span data-stu-id="676be-129">In this example, the application's installation package is located at "\\\\server\\share\\products\\example\\example.msi" and the application's [**ProductCode**](productcode.md) property is "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span></span> <span data-ttu-id="676be-130">Пакет исправлений находится в папке " \\ \\ Server \\ Share \\ Products example patchs example \\ \\ \\ . MSP", а код исправления GUID — "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span><span class="sxs-lookup"><span data-stu-id="676be-130">The patch package is located at "\\\\server\\share\\products\\example\\patches\\example.msp" and the patch code GUID is "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span></span>


```VB
const msiInstallTypeSingleInstance = 2
const PatchList = "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}"
const Product = "{0C9840E7-7F0B-C648-10F0-4641926FE463}"

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

installer.RemovePatches(PatchList, Product, msiInstallTypeSingleInstance, "")
```



## <a name="uninstalling-a-patch-using-addremove-programs"></a><span data-ttu-id="676be-131">Удаление исправления с помощью компонента "Установка и удаление программ"</span><span class="sxs-lookup"><span data-stu-id="676be-131">Uninstalling a patch using Add/Remove Programs</span></span>

<span data-ttu-id="676be-132">Windows XP позволяет удалять исправления с помощью компонента "Установка и удаление программ".</span><span class="sxs-lookup"><span data-stu-id="676be-132">With Windows XP, you can uninstall patches using Add/Remove programs.</span></span>

## <a name="uninstalling-a-patch-using-the-msiremovepatches-function"></a><span data-ttu-id="676be-133">Удаление исправления с помощью функции Мсиремовепатчес</span><span class="sxs-lookup"><span data-stu-id="676be-133">Uninstalling a patch using the MsiRemovePatches function</span></span>

<span data-ttu-id="676be-134">Приложения могут удалять исправления из других приложений с помощью [функций установщик Windows](installer-functions.md).</span><span class="sxs-lookup"><span data-stu-id="676be-134">Your applications can uninstall patches from other applications by using the [Windows Installer Functions](installer-functions.md).</span></span> <span data-ttu-id="676be-135">В следующем примере кода удаляется [удаляемое исправление](uninstallable-patches.md), например, MSP, из приложения example.msi с помощью функции [**мсиремовепатчес**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) .</span><span class="sxs-lookup"><span data-stu-id="676be-135">The following code example removes an [uninstallable patch](uninstallable-patches.md), example.msp, from an application, example.msi, using the [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) function.</span></span> <span data-ttu-id="676be-136">На исправление может ссылаться полный путь к пакету исправлений или GUID кода исправления.</span><span class="sxs-lookup"><span data-stu-id="676be-136">A patch can be referenced by the full path to the patch package or the patch code GUID.</span></span> <span data-ttu-id="676be-137">В этом примере пакет установки приложения находится в папке " \\ \\ Server \\ Share \\ Products \\ example \\example.msi", а свойство [**ProductCode**](productcode.md) приложения — "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span><span class="sxs-lookup"><span data-stu-id="676be-137">In this example, the application's installation package is located at "\\\\server\\share\\products\\example\\example.msi" and the application's [**ProductCode**](productcode.md) property is "{0C9840E7-7F0B-C648-10F0-4641926FE463}".</span></span> <span data-ttu-id="676be-138">Пакет исправлений находится в папке " \\ \\ Server \\ Share \\ Products example patchs example \\ \\ \\ . MSP", а код исправления GUID — "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span><span class="sxs-lookup"><span data-stu-id="676be-138">The patch package is located at "\\\\server\\share\\products\\example\\patches\\example.msp" and the patch code GUID is "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".</span></span>


```C++
    UINT uiReturn = MsiRemovePatches(
          /*szPatchList=*/TEXT("\\server\\share\\products\\example\\patches\\example.msp"),
          /*szProductCode=*/  TEXT("{0C9840E7-7F0B-C648-10F0-4641926FE463}"),
          /*eUninstallType=*/ INSTALLTYPE_SINGLE_INSTANCE,
          /*szPropertyList=*/ NULL);
```



## <a name="uninstalling-a-patch-from-all-applications-using-msiremovepatches-function"></a><span data-ttu-id="676be-139">Удаление исправления из всех приложений с помощью функции Мсиремовепатчес</span><span class="sxs-lookup"><span data-stu-id="676be-139">Uninstalling a patch from all applications using MsiRemovePatches function</span></span>

<span data-ttu-id="676be-140">Одно исправление может обновлять более одного продукта на компьютере.</span><span class="sxs-lookup"><span data-stu-id="676be-140">A single patch can update more than one product on the computer.</span></span> <span data-ttu-id="676be-141">Приложение может использовать [**мсиенумпродуктсекс**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) для перечисления всех продуктов на компьютере и определения того, применено ли исправление к конкретному экземпляру продукта.</span><span class="sxs-lookup"><span data-stu-id="676be-141">An application can use [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) to enumerate all the products on the computer and determine whether a patch has been applied to a particular instance of the product.</span></span> <span data-ttu-id="676be-142">Затем приложение может удалить исправление с помощью [**мсиремовепатчес**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa).</span><span class="sxs-lookup"><span data-stu-id="676be-142">The application can then uninstall the patch using [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa).</span></span> <span data-ttu-id="676be-143">Например, одно исправление может обновить несколько продуктов, если исправление обновляет файл в компоненте, который является общим для нескольких продуктов, а исправление распространяется на обновление обоих продуктов.</span><span class="sxs-lookup"><span data-stu-id="676be-143">For example, a single patch can update multiple products if the patch updates a file in a component that is shared by multiple products and the patch is distributed to update both products.</span></span>

<span data-ttu-id="676be-144">В следующем примере показано, как приложение может использовать установщик Windows для удаления исправления из всех приложений, доступных пользователю.</span><span class="sxs-lookup"><span data-stu-id="676be-144">The following example demonstrates how an application can use the Windows Installer to remove a patch from all applications that are available to the user.</span></span> <span data-ttu-id="676be-145">Это обновление не удаляется из приложений, установленных для каждого пользователя для другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="676be-145">It does not remove the patch from applications installed per-user for another user.</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif //UNICODE

#ifndef _WIN32_MSI
#define _WIN32_MSI 300
#endif //_WIN32_MSI

#include <stdio.h>
#include <windows.h>
#include <msi.h>

#pragma comment(lib, "msi.lib")

const int cchGUID = 38;

///////////////////////////////////////////////////////////////////
// RemovePatchFromAllVisibleapplications:
//
// Arguments:
//    wszPatchToRemove - GUID of patch to remove
//
///////////////////////////////////////////////////////////////////
//
UINT RemovePatchFromAllVisibleapplications(LPCWSTR wszPatchToRemove)
{
    if (!wszPatchToRemove)
        return ERROR_INVALID_PARAMETER;

    UINT uiStatus = ERROR_SUCCESS;
    DWORD dwIndex = 0;
    WCHAR wszapplicationCode[cchGUID+1] = {0};

    DWORD dwapplicationSearchContext = MSIINSTALLCONTEXT_ALL;
    MSIINSTALLCONTEXT dwInstallContext = MSIINSTALLCONTEXT_NONE;

    do
    {
        // Enumerate all visible applications in all contexts for the caller.
        // NULL for szUserSid defaults to using the caller's SID
        uiStatus = MsiEnumProductsEx(/*szapplicationCode*/NULL,
         /*szUserSid*/NULL,
         dwapplicationSearchContext,
         dwIndex,
         wszapplicationCode,
         &dwInstallContext,
         /*szSid*/NULL,
         /*pcchSid*/NULL);

        if (ERROR_SUCCESS == uiStatus)
        {
            // check to see if the provided patch is
            // registered for this application instance
            UINT uiPatchStatus = MsiGetPatchInfoEx(wszPatchToRemove,
             wszapplicationCode,
             /*szUserSid*/NULL,
             dwInstallContext,
             INSTALLPROPERTY_PATCHSTATE,
             NULL,
             NULL);

            if (ERROR_SUCCESS == uiPatchStatus)
            {
                // patch is registered to this application; remove patch
                wprintf(L"Removing patch %s from application %s...\n",
                 wszPatchToRemove, wszapplicationCode);
                                
                UINT uiRemoveStatus = MsiRemovePatches(
                 wszPatchToRemove,
                 wszapplicationCode,
                 INSTALLTYPE_SINGLE_INSTANCE,
                 L"");

                if (ERROR_SUCCESS != uiRemoveStatus)
                {
                    // This halts the enumeration and fails. Alternatively
                    // you could output an error and continue the
                    // enumeration
                     return ERROR_FUNCTION_FAILED;
                }
            }
            else if (ERROR_UNKNOWN_PATCH != uiPatchStatus)
            {
                // Some other error occurred during processing. This
                // halts the enumeration and fails. Alternatively you
                // could output an error and continue the enumeration
                 return ERROR_FUNCTION_FAILED;
            }
            // else patch was not applied to this application
            // (ERROR_UNKNOWN_PATCH returned)
        }

        dwIndex++;
    }
    while (uiStatus == ERROR_SUCCESS);

    if (ERROR_NO_MORE_ITEMS != uiStatus)
        return ERROR_FUNCTION_FAILED;

    return ERROR_SUCCESS;
}
```



## <a name="related-topics"></a><span data-ttu-id="676be-146">См. также</span><span class="sxs-lookup"><span data-stu-id="676be-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="676be-147">Последовательность исправлений</span><span class="sxs-lookup"><span data-stu-id="676be-147">Patch Sequencing</span></span>](sequencing-patches.md)
</dt> <dt>

[<span data-ttu-id="676be-148">Удаление исправлений</span><span class="sxs-lookup"><span data-stu-id="676be-148">Removing Patches</span></span>](removing-patches.md)
</dt> <dt>

[<span data-ttu-id="676be-149">Неустанавливаемые исправления</span><span class="sxs-lookup"><span data-stu-id="676be-149">Uninstallable Patches</span></span>](uninstallable-patches.md)
</dt> <dt>

[<span data-ttu-id="676be-150">Настраиваемые действия при удалении исправлений</span><span class="sxs-lookup"><span data-stu-id="676be-150">Patch Uninstall Custom Actions</span></span>](patch-uninstall-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="676be-151">**мсипатчремове**</span><span class="sxs-lookup"><span data-stu-id="676be-151">**MSIPATCHREMOVE**</span></span>](msipatchremove.md)
</dt> <dt>

[<span data-ttu-id="676be-152">**мсиенумаппликатионсекс**</span><span class="sxs-lookup"><span data-stu-id="676be-152">**MsiEnumapplicationsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[<span data-ttu-id="676be-153">**мсижетпатчинфоекс**</span><span class="sxs-lookup"><span data-stu-id="676be-153">**MsiGetPatchInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[<span data-ttu-id="676be-154">**мсиремовепатчес**</span><span class="sxs-lookup"><span data-stu-id="676be-154">**MsiRemovePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 



