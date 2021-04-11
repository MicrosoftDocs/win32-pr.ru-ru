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
# <a name="uninstalling-patches"></a>Удаление исправлений

Начиная с установщик Windows 3,0, некоторые исправления можно удалить из приложений. Исправление должно быть [неудаляемым исправлением](uninstallable-patches.md). При использовании установщик Windows версии, отличной от версии 3,0, [Удаление исправлений требует удаления](removing-patches.md) продукта исправления и переустановки продукта без применения исправления.

**Установщик Windows 2,0:** Не поддерживается. Исправления, примененные с помощью более ранней версии установщик Windows, чем установщик Windows 3,0, не могут быть удалены.

При вызове удаления исправления любым из следующих методов установщик пытается удалить исправление из первого продукта, видимого для приложения или пользователя, запрашивающего удаление. Установщик ищет продукты с исправлениями в следующем порядке: управляемый пользователем, неуправляемый для каждого пользователя, на компьютер.

## <a name="uninstalling-a-patch-using-msipatchremove-on-a-command-line"></a>Удаление исправления с помощью МСИПАТЧРЕМОВЕ в командной строке

Вы можете удалить исправления из команды с помощью msiexec.exe и [параметров командной строки](command-line-options.md). В приведенном ниже примере командная строка удаляет [исправление](uninstallable-patches.md), например MSP, из приложения example.msi с помощью свойства [**мсипатчремове**](msipatchremove.md) и параметра командной строки/i. При использовании параметра/i исправленное приложение может быть идентифицировано по пути к пакету приложения (MSI-файлу) или [коду продукта](product-codes.md)приложения. В этом примере пакет установки приложения находится в папке " \\ \\ Server \\ Share \\ Products \\ example \\example.msi", а свойство [**ProductCode**](productcode.md) приложения — "{0C9840E7-7F0B-C648-10F0-4641926FE463}". Пакет исправлений находится в папке " \\ \\ Server \\ Share \\ Products example patchs example \\ \\ \\ . MSP", а код исправления GUID — "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".

**Msiexec/I {0C9840E7-7F0B-C648-10F0-4641926FE463} МСИПАТЧРЕМОВЕ = {EB8C947C-78B2-85A0-644D-86CEEF8E07C0}/QB**

## <a name="uninstalling-a-patch-using-the-standard-command-line-options"></a>Удаление исправления с помощью стандартных параметров командной строки

Начиная с версии установщик Windows 3,0 можно использовать [стандартные параметры командной строки](standard-installer-command-line-options.md) , используемые обновлениями операционной системы Microsoft Windows (update.exe), чтобы удалить установщик Windows исправления из командной строки.

Следующая командная строка представляет собой стандартную командную строку, эквивалентную командной строке установщик Windows, используемой для удаления исправления с помощью свойства [**мсипатчремове**](msipatchremove.md) . Параметр/uninstall, используемый с параметром/Package, обозначает удаление исправления. На исправление может ссылаться полный путь к исправлению или идентификатор GUID кода исправления.

**Msiexec/Package {0C9840E7-7F0B-C648-10F0-4641926FE463}/uninstall {EB8C947C-78B2-85A0-644D-86CEEF8E07C0}/passive**

> [!Note]  
> Параметр/passive Standard не является точным эквивалентом параметра установщик Windows/QB.

 

## <a name="uninstalling-a-patch-using-the-removepatches-method"></a>Удаление исправления с помощью метода Ремовепатчес

Вы можете удалить исправления из скрипта с помощью установщик Windows [интерфейса автоматизации](automation-interface.md). Приведенный ниже пример сценария удаляет [исправление](uninstallable-patches.md), например MSP, из приложения example.msi с помощью метода [**ремовепатчес**](installer-removepatches.md) объекта [установщика](installer-object.md) . Каждое удаляемое исправление может быть представлено полным путем к пакету исправлений или идентификатором GUID кода исправления. В этом примере пакет установки приложения находится в папке " \\ \\ Server \\ Share \\ Products \\ example \\example.msi", а свойство [**ProductCode**](productcode.md) приложения — "{0C9840E7-7F0B-C648-10F0-4641926FE463}". Пакет исправлений находится в папке " \\ \\ Server \\ Share \\ Products example patchs example \\ \\ \\ . MSP", а код исправления GUID — "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".


```VB
const msiInstallTypeSingleInstance = 2
const PatchList = "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}"
const Product = "{0C9840E7-7F0B-C648-10F0-4641926FE463}"

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

installer.RemovePatches(PatchList, Product, msiInstallTypeSingleInstance, "")
```



## <a name="uninstalling-a-patch-using-addremove-programs"></a>Удаление исправления с помощью компонента "Установка и удаление программ"

Windows XP позволяет удалять исправления с помощью компонента "Установка и удаление программ".

## <a name="uninstalling-a-patch-using-the-msiremovepatches-function"></a>Удаление исправления с помощью функции Мсиремовепатчес

Приложения могут удалять исправления из других приложений с помощью [функций установщик Windows](installer-functions.md). В следующем примере кода удаляется [удаляемое исправление](uninstallable-patches.md), например, MSP, из приложения example.msi с помощью функции [**мсиремовепатчес**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) . На исправление может ссылаться полный путь к пакету исправлений или GUID кода исправления. В этом примере пакет установки приложения находится в папке " \\ \\ Server \\ Share \\ Products \\ example \\example.msi", а свойство [**ProductCode**](productcode.md) приложения — "{0C9840E7-7F0B-C648-10F0-4641926FE463}". Пакет исправлений находится в папке " \\ \\ Server \\ Share \\ Products example patchs example \\ \\ \\ . MSP", а код исправления GUID — "{EB8C947C-78B2-85A0-644D-86CEEF8E07C0}".


```C++
    UINT uiReturn = MsiRemovePatches(
          /*szPatchList=*/TEXT("\\server\\share\\products\\example\\patches\\example.msp"),
          /*szProductCode=*/  TEXT("{0C9840E7-7F0B-C648-10F0-4641926FE463}"),
          /*eUninstallType=*/ INSTALLTYPE_SINGLE_INSTANCE,
          /*szPropertyList=*/ NULL);
```



## <a name="uninstalling-a-patch-from-all-applications-using-msiremovepatches-function"></a>Удаление исправления из всех приложений с помощью функции Мсиремовепатчес

Одно исправление может обновлять более одного продукта на компьютере. Приложение может использовать [**мсиенумпродуктсекс**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) для перечисления всех продуктов на компьютере и определения того, применено ли исправление к конкретному экземпляру продукта. Затем приложение может удалить исправление с помощью [**мсиремовепатчес**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa). Например, одно исправление может обновить несколько продуктов, если исправление обновляет файл в компоненте, который является общим для нескольких продуктов, а исправление распространяется на обновление обоих продуктов.

В следующем примере показано, как приложение может использовать установщик Windows для удаления исправления из всех приложений, доступных пользователю. Это обновление не удаляется из приложений, установленных для каждого пользователя для другого пользователя.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Последовательность исправлений](sequencing-patches.md)
</dt> <dt>

[Удаление исправлений](removing-patches.md)
</dt> <dt>

[Неустанавливаемые исправления](uninstallable-patches.md)
</dt> <dt>

[Настраиваемые действия при удалении исправлений](patch-uninstall-custom-actions.md)
</dt> <dt>

[**мсипатчремове**](msipatchremove.md)
</dt> <dt>

[**мсиенумаппликатионсекс**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**мсижетпатчинфоекс**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[**мсиремовепатчес**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 



