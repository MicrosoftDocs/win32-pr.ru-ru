---
title: Пример перенаправления реестра в эмуляторе WOW64
description: В следующем примере кода демонстрируются отдельные представления реестра, предоставляемые перенаправитель реестра в 64-разрядной версии Windows.
ms.assetid: b3ca2a47-402d-4e91-88bc-ddda6c776468
keywords:
- Примеры в 64-разрядном программировании Windows
- 64-разрядное руководством по программированию для Windows. примеры 64-разрядного программирования Windows
- 64-разрядное руководством по программированию для Windows. примеры использования 64-разрядного программирования для Windows, перенаправление реестра в WOW64
- Пример перенаправления реестра 64-разрядное программирование для Windows
- 64-разрядное руководством по программированию Windows 64-разрядное программирование для Windows, примеры см. в статье примеры программного кода для Windows 64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff37b077137e9802e6716319623fe8e372941500
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "104414020"
---
# <a name="example-of-registry-redirection-on-wow64"></a>Пример перенаправления реестра в эмуляторе WOW64

В следующем примере кода демонстрируются отдельные представления реестра, предоставляемые перенаправитель реестра в 64-разрядной версии Windows. Здесь также показано, как задаются значения ключей в зависимости от того, является ли ключ общим или перенаправленным. Дополнительные сведения см. в разделе [разделы реестра, затрагиваемые WOW64](shared-registry-keys.md).

Скомпилируйте следующий код отдельно для 32-разрядных и 64-разрядных Windows. Запустите каждый полученный исполняемый файл в 64-разрядной системе Windows и сравните выходные данные. Пример выходных данных для обеих версий приведен ниже исходного кода.


```C++
#include <windows.h>
#include <stdio.h>

#pragma comment(lib, "advapi32.lib")

// Define application constants.
#if defined(_WIN64)

#define VIEW_DATA L"Hello! 64-bit World"
#define ALT_VIEW_DATA L"Hello! 32-bit World"
#define CROSS_ACCESS KEY_WOW64_32KEY

#else

#define VIEW_DATA L"Hello! 32-bit World"
#define ALT_VIEW_DATA L"Hello! 64-bit World"
#define CROSS_ACCESS KEY_WOW64_64KEY

#endif

// Create a registry key and set its value.
// Return TRUE if the function succeeds, FALSE if it fails.
BOOL
    CreateRegistryKeyValue(
        HKEY hKeyParent,
        PWCHAR KeyName,
        REGSAM rsAccessMask,
        REGSAM rsSamViewFlag,
        PBYTE pValue,
        DWORD dwValueSize
        )
{
    DWORD dwDisposition;
    HKEY  hKey;
    DWORD dwRet;

    dwRet = 
        RegCreateKeyEx(
            hKeyParent,
            KeyName,
            0,
            NULL,
            REG_OPTION_NON_VOLATILE,
            rsAccessMask | rsSamViewFlag,
            NULL,
            &hKey,
            &dwDisposition);

    if (dwRet != ERROR_SUCCESS)
    {
        printf("Error opening or creating key.\n");
        return FALSE;
    }

    // Attempt to set the value of the key.
    // If the call fails, close the key and return.
    if (ERROR_SUCCESS !=
            RegSetValueEx(
                hKey,
                NULL,
                0,
                REG_SZ,
                pValue,
                dwValueSize))
    {
        printf("Could not set registry value.\n");
        RegCloseKey(hKey);
        return FALSE;
    }

    RegCloseKey(hKey);
    return TRUE;
}

// Access a registry key and print its value.
// Return TRUE if the function succeeds, FALSE if it fails.
BOOL
    AccessRegistryKeyValue(
        HKEY hKeyParent,
        PWCHAR KeyName,
        REGSAM rsAccessMask,
        REGSAM rsSamViewFlag
        )
{
    HKEY hKey;
    WCHAR Buffer[MAX_PATH];
    DWORD dwSize = sizeof(Buffer);
    DWORD dwType;
    DWORD dwRet;

    dwRet =
        RegOpenKeyEx(
            hKeyParent,
            KeyName,
            0,
            rsAccessMask | rsSamViewFlag,
            &hKey);

    if (dwRet != ERROR_SUCCESS)
    {
        printf("Error opening key!\n");
        return FALSE;
    }

    if (ERROR_SUCCESS !=
            RegQueryValueEx(
                hKey,
                NULL,
                0,
                &dwType,
                (PBYTE)Buffer,
                &dwSize))
    {
        printf("Could not read registry value.\n");
        RegCloseKey(hKey);
        return FALSE;
    }

    if (rsSamViewFlag != 0)
    {
        printf("Alternate view:   %S\n", Buffer);
    }
    else
    {
        printf("Default view:     %S\n", Buffer);
    }

    RegCloseKey(hKey);
    return TRUE;
}

int
main()
{
    BOOL Res;

    // Define the list of keys to work with.
    typedef struct {
        HKEY hkRoot;
        LPWSTR szRootName;
        LPWSTR szName;
    }KEYDATA;

    KEYDATA Keys[] =
    {
        { HKEY_LOCAL_MACHINE, L"HKLM", L"Software\\Hello World" },
        { HKEY_CLASSES_ROOT,  L"HKCR", L"Hello" },
        { HKEY_CLASSES_ROOT,  L"HKCR", L"CLSID\\{00000000-0000-0000-0000-ABCD00000000}" },
        { HKEY_CLASSES_ROOT,  L"HKCR", L"CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\InprocServer32" },
        { HKEY_CLASSES_ROOT,  L"HKCR", L"CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\LocalServer32" }
    };

    // Now create the keys.
    for (int i = 0; i < _countof(Keys); i++)
    {
        // Create the keys in the alternate view of the registry.
        Res = 
            CreateRegistryKeyValue(
                Keys[i].hkRoot,
                Keys[i].szName,
                KEY_READ | KEY_WRITE,
                CROSS_ACCESS,
                (PBYTE)ALT_VIEW_DATA,
                sizeof(ALT_VIEW_DATA));
        if (Res == FALSE)
        {
            printf("Could not create keys in alternate view of the registry.\n");
            return 1; 
       }

        // Create the keys in the default view of the registry.
        Res = 
            CreateRegistryKeyValue(
                Keys[i].hkRoot,
                Keys[i].szName,
                KEY_READ | KEY_WRITE,
                0,
                (PBYTE)VIEW_DATA,
                sizeof(VIEW_DATA));
        if (Res == FALSE)
        {
            printf("Could not create keys in default view of the registry.\n");
            return 1;
        }
    }

    // Access the registry and print key values.
    printf("Application string: %S\n", VIEW_DATA);

    for (int i = 0; i < _countof(Keys); i++)
    {
        printf("%S\\%S\n", Keys[i].szRootName, Keys[i].szName);
        Res = 
            AccessRegistryKeyValue(
                Keys[i].hkRoot,
                Keys[i].szName,
                KEY_READ, 
                0);
        if (Res == FALSE)
        {
            printf("Unable to access default view of registry.\n");
            return 1;
        }

        // Calls with CROSS_ACCESS explicitly access the alternate registry view.
        Res =
            AccessRegistryKeyValue(
                Keys[i].hkRoot,
                Keys[i].szName,
                KEY_READ,
                CROSS_ACCESS);
        if (Res == FALSE)
        {
            printf("Unable to access alternate view of registry.\n");
            return 1;
        }
    }
    return 0;
}
```



При выполнении 64-разрядной версии примера выдается следующий результат. Значения по умолчанию и альтернативные представления **HKCR \\ Hello** одинаковы, так как этот ключ является общим. Значения других ключей отличаются, так как они перенаправлены.

Windows **server 2008, Windows Vista, Windows server 2003 и Windows XP:** Если этот пример выполняется в этих операционных системах, то значения по умолчанию и альтернативные представления ключа LocalServer32 имеют одинаковое значение. Это связано с тем, что ключ LocalServer32 перенаправляется и *отражается*, что вызывает синхронизацию его значения между 64-разрядными и 32-битовыми представлениями реестра сразу после закрытия маркера для ключа. Отражение реестра удалено начиная с Windows 7. Дополнительные сведения см. в разделе [отражение реестра](registry-reflection.md).

``` syntax
Application string: Hello! 64-bit World
HKLM\Software\Hello World
Default view:     Hello! 64-bit World
Alternate view:   Hello! 32-bit World
HKCR\Hello
Default view:     Hello! 64-bit World
Alternate view:   Hello! 64-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}
Default view:     Hello! 64-bit World
Alternate view:   Hello! 32-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}\InprocServer32
Default view:     Hello! 64-bit World
Alternate view:   Hello! 32-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}\LocalServer32
Default view:     Hello! 64-bit World
Alternate view:   Hello! 32-bit World
```

При выполнении 32-разрядной версии примера выдается следующий результат. Для 32-разрядного приложения 64-разрядное представление реестра является альтернативным представлением, поэтому значения реверсируются, за исключением \\ ключа HKCR Hello, который является общим ключом.

``` syntax
Application string: Hello! 32-bit World
HKLM\Software\Hello World
Default view:     Hello! 32-bit World
Alternate view:   Hello! 64-bit World
HKCR\Hello
Default view:     Hello! 32-bit World
Alternate view:   Hello! 32-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}
Default view:     Hello! 32-bit World
Alternate view:   Hello! 64-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}\InprocServer32
Default view:     Hello! 32-bit World
Alternate view:   Hello! 64-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}\LocalServer32
Default view:     Hello! 32-bit World
Alternate view:   Hello! 64-bit World
```

Чтобы проверить результат выполнения этого примера с помощью Regedit, проверьте значения следующих ключей. Обратите внимание, что приложения должны избегать использования Wow6432Node в жестко запрограммированных путях реестра.

**\\Hello World HKLM Software \\**  
**HKLM \\ Software \\ WOW6432Node \\ Hello World**  
**Раздел HKCR \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000}**  
**Раздел HKCR \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\ InprocServer32**  
**\\LocalServer32 CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\**  
**HKCR \\ Hello HKCR \\ WOW6432Node \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000}**  
**Раздел HKCR \\ WOW6432Node \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\ InprocServer32**  
**Раздел HKCR \\ WOW6432Node \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\ LocalServer32**  
**HKCR \\ WOW6432Node \\ Hello**  


## <a name="related-topics"></a>См. также

<dl> <dt>

[Перенаправитель реестра](registry-redirector.md)
</dt> <dt>

[Отражение реестра](registry-reflection.md)
</dt> </dl>

 

 




