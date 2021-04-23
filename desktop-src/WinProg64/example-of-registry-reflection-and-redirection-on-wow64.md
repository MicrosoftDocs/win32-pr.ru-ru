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
# <a name="example-of-registry-redirection-on-wow64"></a><span data-ttu-id="a93e4-108">Пример перенаправления реестра в эмуляторе WOW64</span><span class="sxs-lookup"><span data-stu-id="a93e4-108">Example of Registry Redirection on WOW64</span></span>

<span data-ttu-id="a93e4-109">В следующем примере кода демонстрируются отдельные представления реестра, предоставляемые перенаправитель реестра в 64-разрядной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="a93e4-109">The following example code demonstrates the separate views of the registry provided by the registry redirector on 64-bit Windows.</span></span> <span data-ttu-id="a93e4-110">Здесь также показано, как задаются значения ключей в зависимости от того, является ли ключ общим или перенаправленным.</span><span class="sxs-lookup"><span data-stu-id="a93e4-110">It also demonstrates how the values of keys are set depending on whether a key is shared or redirected.</span></span> <span data-ttu-id="a93e4-111">Дополнительные сведения см. в разделе [разделы реестра, затрагиваемые WOW64](shared-registry-keys.md).</span><span class="sxs-lookup"><span data-stu-id="a93e4-111">For more information, see [Registry Keys Affected by WOW64](shared-registry-keys.md).</span></span>

<span data-ttu-id="a93e4-112">Скомпилируйте следующий код отдельно для 32-разрядных и 64-разрядных Windows.</span><span class="sxs-lookup"><span data-stu-id="a93e4-112">Compile the following code separately for both 32-bit and 64-bit Windows.</span></span> <span data-ttu-id="a93e4-113">Запустите каждый полученный исполняемый файл в 64-разрядной системе Windows и сравните выходные данные.</span><span class="sxs-lookup"><span data-stu-id="a93e4-113">Run each resulting executable file on 64-bit Windows and compare the output.</span></span> <span data-ttu-id="a93e4-114">Пример выходных данных для обеих версий приведен ниже исходного кода.</span><span class="sxs-lookup"><span data-stu-id="a93e4-114">Sample output for both versions is listed below the source code.</span></span>


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



<span data-ttu-id="a93e4-115">При выполнении 64-разрядной версии примера выдается следующий результат.</span><span class="sxs-lookup"><span data-stu-id="a93e4-115">When the 64-bit version of the example is run, it produces the following output.</span></span> <span data-ttu-id="a93e4-116">Значения по умолчанию и альтернативные представления **HKCR \\ Hello** одинаковы, так как этот ключ является общим.</span><span class="sxs-lookup"><span data-stu-id="a93e4-116">The values of both the default and alternate views of **HKCR\\Hello** are the same because this key is shared.</span></span> <span data-ttu-id="a93e4-117">Значения других ключей отличаются, так как они перенаправлены.</span><span class="sxs-lookup"><span data-stu-id="a93e4-117">The values of the other keys differ because they are redirected.</span></span>

<span data-ttu-id="a93e4-118">Windows **server 2008, Windows Vista, Windows server 2003 и Windows XP:** Если этот пример выполняется в этих операционных системах, то значения по умолчанию и альтернативные представления ключа LocalServer32 имеют одинаковое значение.</span><span class="sxs-lookup"><span data-stu-id="a93e4-118">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** When this example is run on these operating systems, the default and alternate views of the LocalServer32 key have the same value.</span></span> <span data-ttu-id="a93e4-119">Это связано с тем, что ключ LocalServer32 перенаправляется и *отражается*, что вызывает синхронизацию его значения между 64-разрядными и 32-битовыми представлениями реестра сразу после закрытия маркера для ключа.</span><span class="sxs-lookup"><span data-stu-id="a93e4-119">This is because the LocalServer32 key is redirected and *reflected*, which causes its value to be synchronized between the 64-bit and 32-bit views of the registry as soon as the handle to the key is closed.</span></span> <span data-ttu-id="a93e4-120">Отражение реестра удалено начиная с Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a93e4-120">Registry reflection was removed starting with Windows 7.</span></span> <span data-ttu-id="a93e4-121">Дополнительные сведения см. в разделе [отражение реестра](registry-reflection.md).</span><span class="sxs-lookup"><span data-stu-id="a93e4-121">For more information, see [Registry Reflection](registry-reflection.md).</span></span>

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

<span data-ttu-id="a93e4-122">При выполнении 32-разрядной версии примера выдается следующий результат.</span><span class="sxs-lookup"><span data-stu-id="a93e4-122">When the 32-bit version of the example is run, it produces the following output.</span></span> <span data-ttu-id="a93e4-123">Для 32-разрядного приложения 64-разрядное представление реестра является альтернативным представлением, поэтому значения реверсируются, за исключением \\ ключа HKCR Hello, который является общим ключом.</span><span class="sxs-lookup"><span data-stu-id="a93e4-123">For a 32-bit application, the 64-bit view of the registry is the alternate view so the values are reversed, except for HKCR\\Hello, which is a shared key.</span></span>

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

<span data-ttu-id="a93e4-124">Чтобы проверить результат выполнения этого примера с помощью Regedit, проверьте значения следующих ключей.</span><span class="sxs-lookup"><span data-stu-id="a93e4-124">To examine the effect of running this example with regedit, inspect the values of the following keys.</span></span> <span data-ttu-id="a93e4-125">Обратите внимание, что приложения должны избегать использования Wow6432Node в жестко запрограммированных путях реестра.</span><span class="sxs-lookup"><span data-stu-id="a93e4-125">Note that applications should avoid using Wow6432Node in hard-coded registry paths.</span></span>

<span data-ttu-id="a93e4-126">**\\Hello World HKLM Software \\**</span><span class="sxs-lookup"><span data-stu-id="a93e4-126">**HKLM\\SOFTWARE\\Hello World**</span></span>  
<span data-ttu-id="a93e4-127">**HKLM \\ Software \\ WOW6432Node \\ Hello World**</span><span class="sxs-lookup"><span data-stu-id="a93e4-127">**HKLM\\SOFTWARE\\Wow6432Node\\Hello World**</span></span>  
<span data-ttu-id="a93e4-128">**Раздел HKCR \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000}**</span><span class="sxs-lookup"><span data-stu-id="a93e4-128">**HKCR\\CLSID\\{00000000-0000-0000-0000-ABCD00000000}**</span></span>  
<span data-ttu-id="a93e4-129">**Раздел HKCR \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\ InprocServer32**</span><span class="sxs-lookup"><span data-stu-id="a93e4-129">**HKCR\\CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\InprocServer32**</span></span>  
<span data-ttu-id="a93e4-130">**\\LocalServer32 CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\**</span><span class="sxs-lookup"><span data-stu-id="a93e4-130">**HKCR\\CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\LocalServer32**</span></span>  
<span data-ttu-id="a93e4-131">**HKCR \\ Hello HKCR \\ WOW6432Node \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000}**</span><span class="sxs-lookup"><span data-stu-id="a93e4-131">**HKCR\\Hello HKCR\\Wow6432Node\\CLSID\\{00000000-0000-0000-0000-ABCD00000000}**</span></span>  
<span data-ttu-id="a93e4-132">**Раздел HKCR \\ WOW6432Node \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\ InprocServer32**</span><span class="sxs-lookup"><span data-stu-id="a93e4-132">**HKCR\\Wow6432Node\\CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\InprocServer32**</span></span>  
<span data-ttu-id="a93e4-133">**Раздел HKCR \\ WOW6432Node \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\ LocalServer32**</span><span class="sxs-lookup"><span data-stu-id="a93e4-133">**HKCR\\Wow6432Node\\CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\LocalServer32**</span></span>  
<span data-ttu-id="a93e4-134">**HKCR \\ WOW6432Node \\ Hello**</span><span class="sxs-lookup"><span data-stu-id="a93e4-134">**HKCR\\Wow6432Node\\Hello**</span></span>  


## <a name="related-topics"></a><span data-ttu-id="a93e4-135">См. также</span><span class="sxs-lookup"><span data-stu-id="a93e4-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a93e4-136">Перенаправитель реестра</span><span class="sxs-lookup"><span data-stu-id="a93e4-136">Registry Redirector</span></span>](registry-redirector.md)
</dt> <dt>

[<span data-ttu-id="a93e4-137">Отражение реестра</span><span class="sxs-lookup"><span data-stu-id="a93e4-137">Registry Reflection</span></span>](registry-reflection.md)
</dt> </dl>

 

 




