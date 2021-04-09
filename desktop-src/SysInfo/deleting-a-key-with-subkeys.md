---
description: В примере в этом разделе используются функции RegOpenKeyEx, Реженумкэйекс и Регделетекэй для удаления раздела реестра с подразделами.
ms.assetid: 1cf6db95-85a4-4416-b17e-e14f45804503
title: Удаление ключа с подразделами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490020ff5a7bc6ea44f83b729bcbad4491aaa62e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081635"
---
# <a name="deleting-a-key-with-subkeys"></a>Удаление ключа с подразделами

В примере в этом разделе используются функции [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa), [**реженумкэйекс**](/windows/desktop/api/Winreg/nf-winreg-regenumkeyexa)и [**регделетекэй**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeya) для удаления раздела реестра с подразделами.

Чтобы протестировать этот пример, создайте следующий раздел реестра с помощью Regedt32.exe, а затем добавьте несколько значений и подразделов:

**HKey \_ Текущее \_ пользовательское** \\ **программное обеспечение** \\ **тестдир**

После выполнения кода используйте клавишу F5 для обновления данных реестра и обратите внимание, что ключ **тестдир** удаляется.


```C++
#include <windows.h>
#include <stdio.h>
#include <strsafe.h>

//*************************************************************
//
//  RegDelnodeRecurse()
//
//  Purpose:    Deletes a registry key and all its subkeys / values.
//
//  Parameters: hKeyRoot    -   Root key
//              lpSubKey    -   SubKey to delete
//
//  Return:     TRUE if successful.
//              FALSE if an error occurs.
//
//*************************************************************

BOOL RegDelnodeRecurse (HKEY hKeyRoot, LPTSTR lpSubKey)
{
    LPTSTR lpEnd;
    LONG lResult;
    DWORD dwSize;
    TCHAR szName[MAX_PATH];
    HKEY hKey;
    FILETIME ftWrite;

    // First, see if we can delete the key without having
    // to recurse.

    lResult = RegDeleteKey(hKeyRoot, lpSubKey);

    if (lResult == ERROR_SUCCESS) 
        return TRUE;

    lResult = RegOpenKeyEx (hKeyRoot, lpSubKey, 0, KEY_READ, &hKey);

    if (lResult != ERROR_SUCCESS) 
    {
        if (lResult == ERROR_FILE_NOT_FOUND) {
            printf("Key not found.\n");
            return TRUE;
        } 
        else {
            printf("Error opening key.\n");
            return FALSE;
        }
    }

    // Check for an ending slash and add one if it is missing.

    lpEnd = lpSubKey + lstrlen(lpSubKey);

    if (*(lpEnd - 1) != TEXT('\\')) 
    {
        *lpEnd =  TEXT('\\');
        lpEnd++;
        *lpEnd =  TEXT('\0');
    }

    // Enumerate the keys

    dwSize = MAX_PATH;
    lResult = RegEnumKeyEx(hKey, 0, szName, &dwSize, NULL,
                           NULL, NULL, &ftWrite);

    if (lResult == ERROR_SUCCESS) 
    {
        do {

            *lpEnd = TEXT('\0');
            StringCchCat(lpSubKey, MAX_PATH * 2, szName);

            if (!RegDelnodeRecurse(hKeyRoot, lpSubKey)) {
                break;
            }

            dwSize = MAX_PATH;

            lResult = RegEnumKeyEx(hKey, 0, szName, &dwSize, NULL,
                                   NULL, NULL, &ftWrite);

        } while (lResult == ERROR_SUCCESS);
    }

    lpEnd--;
    *lpEnd = TEXT('\0');

    RegCloseKey (hKey);

    // Try again to delete the key.

    lResult = RegDeleteKey(hKeyRoot, lpSubKey);

    if (lResult == ERROR_SUCCESS) 
        return TRUE;

    return FALSE;
}

//*************************************************************
//
//  RegDelnode()
//
//  Purpose:    Deletes a registry key and all its subkeys / values.
//
//  Parameters: hKeyRoot    -   Root key
//              lpSubKey    -   SubKey to delete
//
//  Return:     TRUE if successful.
//              FALSE if an error occurs.
//
//*************************************************************

BOOL RegDelnode (HKEY hKeyRoot, LPCTSTR lpSubKey)
{
    TCHAR szDelKey[MAX_PATH*2];

    StringCchCopy (szDelKey, MAX_PATH*2, lpSubKey);
    return RegDelnodeRecurse(hKeyRoot, szDelKey);

}

int __cdecl main()
{
   BOOL bSuccess;

   bSuccess = RegDelnode(HKEY_CURRENT_USER, TEXT("Software\\TestDir"));

   if(bSuccess)
      printf("Success!\n");
   else printf("Failure.\n");

   return 0;
}
```



 

 



