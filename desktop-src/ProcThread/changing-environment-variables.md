---
description: С каждым процессом связан блок среды.
ms.assetid: b428688c-7b16-48c7-8d89-55d066496d1c
title: Изменение переменных среды
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e13054afff996c4f8128fdc58f9d6dfadc35cc84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673780"
---
# <a name="changing-environment-variables"></a>Изменение переменных среды

С каждым процессом связан блок среды. Блок среды состоит из завершающего нуль блока строк, заканчивающихся нулем (т. е. в конце блока есть два байта, равных NULL), где каждая строка имеет вид:

*имя* = *значение*

Все строки в блоке среды должны быть отсортированы в алфавитном порядке по имени. При сортировке регистр не учитывается, порядок Юникода без учета языка. Так как знак равенства является разделителем, он не должен использоваться в имени переменной среды.

## <a name="example-1"></a>Пример 1

По умолчанию дочерний процесс наследует копию блока среды родительского процесса. В следующем примере показано, как создать новый блок среды для передачи в дочерний процесс с помощью [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).

В этом примере код в примере 3 используется в качестве дочернего процесса Ex3.exe.


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <strsafe.h>

#define BUFSIZE 4096

int _tmain()
{
    TCHAR chNewEnv[BUFSIZE];
    LPTSTR lpszCurrentVariable; 
    DWORD dwFlags=0;
    TCHAR szAppName[]=TEXT("ex3.exe");
    STARTUPINFO si;
    PROCESS_INFORMATION pi;
    BOOL fSuccess; 
 
    // Copy environment strings into an environment block. 
 
    lpszCurrentVariable = (LPTSTR) chNewEnv;
    if (FAILED(StringCchCopy(lpszCurrentVariable, BUFSIZE, TEXT("MySetting=A"))))
    {
        printf("String copy failed\n"); 
        return FALSE;
    }

    lpszCurrentVariable += lstrlen(lpszCurrentVariable) + 1; 
    if (FAILED(StringCchCopy(lpszCurrentVariable, BUFSIZE, TEXT("MyVersion=2")))) 
    {
        printf("String copy failed\n"); 
        return FALSE;
    }
 
    // Terminate the block with a NULL byte. 
 
    lpszCurrentVariable += lstrlen(lpszCurrentVariable) + 1; 
    *lpszCurrentVariable = (TCHAR)0; 

    // Create the child process, specifying a new environment block. 
 
    SecureZeroMemory(&si, sizeof(STARTUPINFO));
    si.cb = sizeof(STARTUPINFO);

#ifdef UNICODE
    dwFlags = CREATE_UNICODE_ENVIRONMENT;
#endif

    fSuccess = CreateProcess(szAppName, NULL, NULL, NULL, TRUE, dwFlags,
        (LPVOID) chNewEnv,   // new environment block
        NULL, &si, &pi); 
 
    if (! fSuccess) 
    {
        printf("CreateProcess failed (%d)\n", GetLastError());
        return FALSE;
    }
    WaitForSingleObject(pi.hProcess, INFINITE);
    return TRUE;
}
```



## <a name="example-2"></a>Пример 2

Изменение переменных среды дочернего процесса во время создания процесса — единственный способ, которым один процесс может напрямую изменить переменные среды другого процесса. Процесс не может напрямую изменять переменные среды другого процесса, который не является дочерним для этого процесса.

Если необходимо, чтобы дочерний процесс наследовал большую часть среды родителя только с небольшими изменениями, извлеките текущие значения с помощью [**GetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable), сохраните эти значения, создайте обновленный блок для наследуемого дочернего процесса, создайте дочерний процесс, а затем восстановите сохраненные значения с помощью [**SetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable), как показано в следующем примере.

В этом примере код в примере 3 используется в качестве дочернего процесса Ex3.exe.


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#define BUFSIZE 4096
#define VARNAME TEXT("MyVariable")

int _tmain()
{
    DWORD dwRet, dwErr;
    LPTSTR pszOldVal; 
    TCHAR szAppName[]=TEXT("ex3.exe");
    DWORD dwFlags=0;
    STARTUPINFO si;
    PROCESS_INFORMATION pi;
    BOOL fExist, fSuccess; 
 
    // Retrieves the current value of the variable if it exists.
    // Sets the variable to a new value, creates a child process,
    // then uses SetEnvironmentVariable to restore the original
    // value or delete it if it did not exist previously. 
 
    pszOldVal = (LPTSTR) malloc(BUFSIZE*sizeof(TCHAR));
    if(NULL == pszOldVal)
    {
        printf("Out of memory\n");
        return FALSE;
    }

    dwRet = GetEnvironmentVariable(VARNAME, pszOldVal, BUFSIZE);

    if(0 == dwRet)
    {
        dwErr = GetLastError();
        if( ERROR_ENVVAR_NOT_FOUND == dwErr )
        {
            printf("Environment variable does not exist.\n");
            fExist=FALSE;
        }
    }
    else if(BUFSIZE < dwRet)
    {
        pszOldVal = (LPTSTR) realloc(pszOldVal, dwRet*sizeof(TCHAR));   
        if(NULL == pszOldVal)
        {
            printf("Out of memory\n");
            return FALSE;
        }
        dwRet = GetEnvironmentVariable(VARNAME, pszOldVal, dwRet);
        if(!dwRet)
        {
            printf("GetEnvironmentVariable failed (%d)\n", GetLastError());
            return FALSE;
        }
        else fExist=TRUE;
    }
    else fExist=TRUE;

    // Set a value for the child process to inherit. 
 
    if (! SetEnvironmentVariable(VARNAME, TEXT("Test"))) 
    {
        printf("SetEnvironmentVariable failed (%d)\n", GetLastError()); 
        return FALSE;
    }
 
    // Create a child process. 

    SecureZeroMemory(&si, sizeof(STARTUPINFO));
    si.cb = sizeof(STARTUPINFO);
 
#ifdef UNICODE
    dwFlags = CREATE_UNICODE_ENVIRONMENT;
#endif

    fSuccess = CreateProcess(szAppName, NULL, NULL, NULL, TRUE, dwFlags, 
        NULL,     // inherit parent's environment 
        NULL, &si, &pi); 
    if (! fSuccess) 
    {
        printf("CreateProcess failed (%d)\n", GetLastError()); 
    }
    WaitForSingleObject(pi.hProcess, INFINITE);

    // Restore the original environment variable. 
 
    if(fExist)
    {
        if (! SetEnvironmentVariable(VARNAME, pszOldVal)) 
        {
            printf("SetEnvironmentVariable failed (%d)\n", GetLastError()); 
            return FALSE;
        }
    }
    else SetEnvironmentVariable(VARNAME, NULL);

    free(pszOldVal);
    
    return fSuccess;
}
```



## <a name="example-3"></a>Пример 3

В следующем примере извлекается блок среды процесса с помощью [**жетенвиронментстрингс**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings) и выводится содержимое на консоль.


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

int _tmain()
{
    LPTSTR lpszVariable; 
    LPTCH lpvEnv; 
 
    // Get a pointer to the environment block. 
 
    lpvEnv = GetEnvironmentStrings();

    // If the returned pointer is NULL, exit.
    if (lpvEnv == NULL)
    {
        printf("GetEnvironmentStrings failed (%d)\n", GetLastError()); 
        return 0;
    }
 
    // Variable strings are separated by NULL byte, and the block is 
    // terminated by a NULL byte. 

    lpszVariable = (LPTSTR) lpvEnv;

    while (*lpszVariable)
    {
        _tprintf(TEXT("%s\n"), lpszVariable);
        lpszVariable += lstrlen(lpszVariable) + 1;
    }
    FreeEnvironmentStrings(lpvEnv);
    return 1;
}
```



 

 
