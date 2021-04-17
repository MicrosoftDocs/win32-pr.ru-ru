---
description: Приложение может вызывать функции Мсиенумпродуктс или Мсиенумпродуктсекс для перечисления продуктов, установленных или объявленных в системе.
ms.assetid: 162bda20-0c62-4eac-8c1f-fd107e42c528
title: Определение контекста установки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24367e2367f845dfef2e4947a32d9dec84d644cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663712"
---
# <a name="determining-installation-context"></a>Определение контекста установки

Приложение может вызывать функции [**мсиенумпродуктс**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) или [**мсиенумпродуктсекс**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) для перечисления продуктов, установленных или объявленных в системе. Эта функция может перечислить все продукты, установленные в [контексте установки](installation-context.md)на компьютере. Он может перечислить продукты, установленные в контексте "на пользователя" для текущего пользователя. Приложение может получить сведения о контексте этих продуктов, вызвав функции [**мсижетпродуктинфоекс**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) или [**мсижетпродуктинфо**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) .

Установщик Windows может устанавливать продукты для запуска с повышенными правами (System) для пользователей без прав администратора. Для этого требуется разрешение пользователя администратора. Продукт, устанавливаемый с повышенными привилегиями, называется "управляемым". Управление всеми продуктами, установленными для каждого компьютера, осуществляется. Продукты, установленные для каждого пользователя, управляются только в том случае, если локальный системный агент выполняет объявление при олицетворении пользователя. Это метод, используемый развертыванием программного обеспечения с помощью [Групповая политика](/previous-versions/windows/desktop/Policy/group-policy-start-page). Приложения на уровне пользователя, установленные, пока не установлены политики [AlwaysInstallElevated](alwaysinstallelevated.md) , не считаются управляемыми. Вызывая [**мсииспродуктелеватед**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda), приложение может проверить, является ли определенный продукт управляемым.

В следующем примере показано, как приложение определяет контекст с помощью [**мсиенумпродуктс**](/windows/desktop/api/Msi/nf-msi-msienumproductsa), [**мсижетпродуктинфо**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)и [**мсииспродуктелеватед**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda).


```C++
#ifndef UNICODE
#define UNICODE
#endif //UNICODE

#ifndef _WIN32_MSI
#define _WIN32_MSI 200
#endif //_WIN32_MSI

#include <stdio.h>
#include <windows.h>
#include <msi.h>
#pragma comment(lib, "msi.lib")

const int cchGUID = 38;

UINT DetermineContextForAllProducts()
{
    WCHAR wszProductCode[cchGUID+1] = {0};
    WCHAR wszAssignmentType[10] = {0};
    DWORD cchAssignmentType = 
            sizeof(wszAssignmentType)/sizeof(wszAssignmentType[0]);
    DWORD dwIndex = 0;

    DWORD cchProductName = MAX_PATH;
    WCHAR* lpProductName = new WCHAR[cchProductName];
    if (!lpProductName)
    {
        return ERROR_OUTOFMEMORY;
    }

    UINT uiStatus = ERROR_SUCCESS;

    // enumerate all visible products
    do
    {
        uiStatus = MsiEnumProducts(dwIndex,
                          wszProductCode);
        if (ERROR_SUCCESS == uiStatus)
        {
            cchAssignmentType = 
                sizeof(wszAssignmentType)/sizeof(wszAssignmentType[0]);
            BOOL fPerMachine = FALSE;
            BOOL fManaged = FALSE;

            // Determine assignment type of product
            // This indicates whether the product
            // instance is per-user or per-machine
            if (ERROR_SUCCESS == 
                MsiGetProductInfo(wszProductCode,INSTALLPROPERTY_ASSIGNMENTTYPE,wszAssignmentType,&cchAssignmentType))
            {
                if (L'1' == wszAssignmentType[0])
                    fPerMachine = TRUE;
            }
            else
            {
                // This halts the enumeration and fails. Alternatively the error
                // could be logged and enumeration continued for the
                // remainder of the products
                uiStatus = ERROR_FUNCTION_FAILED;
                break;
            }

            // determine the "managed" status of the product.
            // If fManaged is TRUE, product is installed managed
            // and runs with elevated privileges.
            // If fManaged is FALSE, product installation operations
            // run as the user.
            if (ERROR_SUCCESS != MsiIsProductElevated(wszProductCode,
                                         &fManaged))
            {
                // This halts the enumeration and fails. Alternatively the error
                // could be logged and enumeration continued for the
                // remainder of the products
                uiStatus = ERROR_FUNCTION_FAILED;
                break;
            }

            // obtain the user friendly name of the product
            UINT uiReturn = MsiGetProductInfo(wszProductCode,INSTALLPROPERTY_PRODUCTNAME,lpProductName,&cchProductName);
            if (ERROR_MORE_DATA == uiReturn)
            {
                // try again, but with a larger product name buffer
                delete [] lpProductName;

                // returned character count does not include
                // terminating NULL
                ++cchProductName;

                lpProductName = new WCHAR[cchProductName];
                if (!lpProductName)
                {
                    uiStatus = ERROR_OUTOFMEMORY;
                    break;
                }

                uiReturn = MsiGetProductInfo(wszProductCode,INSTALLPROPERTY_PRODUCTNAME,lpProductName,&cchProductName);
            }

            if (ERROR_SUCCESS != uiReturn)
            {
                // This halts the enumeration and fails. Alternatively the error
                // could be logged and enumeration continued for the
                // remainder of the products
                uiStatus = ERROR_FUNCTION_FAILED;
                break;
            }

            // output information
            wprintf(L" Product %s:\n", lpProductName);
            wprintf(L"\t%s\n", wszProductCode);
                        wprintf(L"\tInstalled %s %s\n", 
                fPerMachine ? L"per-machine" : L"per-user",
                fManaged ? L"managed" : L"non-managed");
        }
        dwIndex++;
    }
    while (ERROR_SUCCESS == uiStatus);

    if (lpProductName)
    {
        delete [] lpProductName;
        lpProductName = NULL;
    }

    return (ERROR_NO_MORE_ITEMS == uiStatus) ? ERROR_SUCCESS : uiStatus;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**мсиенумпродуктс**](/windows/desktop/api/Msi/nf-msi-msienumproductsa)
</dt> <dt>

[**мсижетпродуктинфо**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)
</dt> <dt>

[**мсижетпродуктинфоекс**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa)
</dt> <dt>

[**мсииспродуктелеватед**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda)
</dt> <dt>

[Установка пакета с повышенными привилегиями для без прав администратора](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
</dt> <dt>

[Объявление приложения Per-User для установки с повышенными привилегиями](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
</dt> <dt>

[Контекст установки](installation-context.md)
</dt> </dl>

 

 
