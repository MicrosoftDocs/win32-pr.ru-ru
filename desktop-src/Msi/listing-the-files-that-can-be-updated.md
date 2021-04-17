---
description: Функция Мсижетпатчфилелист и свойство Патчфилес объекта Installer получают список исправлений установщик Windows (MSP-файлы) и возвращают список файлов, которые могут быть обновлены с помощью исправлений.
ms.assetid: cc2eb506-c1fc-4125-b98c-12221b918e23
title: Список файлов, которые могут быть обновлены
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c15872cce902f5a9059d4256e9e5c30ecff213f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683730"
---
# <a name="listing-the-files-that-can-be-updated"></a>Список файлов, которые могут быть обновлены

Функция [**мсижетпатчфилелист**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista) и свойство [**патчфилес**](installer-patchfiles.md) [**объекта Installer**](installer-object.md) получают список исправлений установщик Windows (MSP-файлы) и возвращают список файлов, которые могут быть обновлены с помощью исправлений. Функция [**мсижетпатчфилелист**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista) и свойство [**патчфилес**](installer-patchfiles.md) доступны начиная с установщик Windows 4,0.

## <a name="listing-files-that-can-be-updated"></a>Перечисление файлов, которые могут быть обновлены

В следующем примере показано, как извлечь сведения о применимости для списка исправлений установщик Windows (MSP-файлы) с помощью [**мсижетпатчфилелист**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista). Функция **мсижетпатчфилелист** предоставляет код продукта для целей исправлений и список MSP-файлов, разделенных точкой с запятой. Для этого примера требуется установщик Windows 4,0, работающий в Windows Vista.


```C++
#include <windows.h>
#include <stdio.h>
#include <Shellapi.h>
#include <msi.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")
#pragma comment(lib, "shell32.lib")

void CloseMsiHandles(MSIHANDLE* phFileListRec, DWORD dwcFiles);

int __cdecl main()
{
    UINT uiRet = ERROR_SUCCESS;
    int argc;
    WCHAR** argv = CommandLineToArgvW(GetCommandLine(), &argc);
    
    MSIHANDLE *phFileListRec = NULL;
    DWORD dwcFiles = 0;
    WCHAR* szProductCode = argv[1];
    WCHAR* szPatchFileList = argv[2];
    if(ERROR_SUCCESS != (uiRet = MsiGetPatchFileList(szProductCode, szPatchFileList, &dwcFiles, &phFileListRec)))
    {
        printf("MsiGetPatchFileListW(%S, ...) Failed with:%d", szProductCode, uiRet);
        return uiRet;
    }
    
    DWORD cchBuf = 1;
    DWORD cchBufSize = 1;
    WCHAR* szBuf = new WCHAR[cchBufSize];
    if (!szBuf)
    {
        printf("Failed to allocate memory");
        CloseMsiHandles(phFileListRec, dwcFiles);
        return ERROR_OUTOFMEMORY;
    }
    memset(szBuf, 0, sizeof(WCHAR)*cchBufSize);
    
    for(unsigned int i = 0; i < dwcFiles; i++)
    {
        cchBuf = cchBufSize;
        while(ERROR_MORE_DATA == (uiRet = MsiRecordGetString(phFileListRec[i], 0, szBuf, &cchBuf)))
        {
            if (szBuf)
                delete[] szBuf;
            cchBufSize = ++cchBuf;
            szBuf = new WCHAR[cchBufSize];
            if (!szBuf)
            {
                printf("Failed to allocate memory");
                CloseMsiHandles(phFileListRec, dwcFiles);
                return ERROR_OUTOFMEMORY;
            }
        }
        
        if(uiRet != ERROR_SUCCESS)
        {
            printf("MsiRecordGetString(phFileListRec[%d] with %d", i, uiRet);
            CloseMsiHandles(phFileListRec, dwcFiles);
            if (szBuf)
                delete[] szBuf;
            return uiRet;
        }
        else
        {
            printf("File %d:%S\n", i, szBuf);
        }            
    }

    CloseMsiHandles(phFileListRec, dwcFiles);
    if (szBuf)
        delete[] szBuf;
    return 0;
}

void CloseMsiHandles(MSIHANDLE* phFileListRec, DWORD dwcFiles)
{
    if (!phFileListRec)
        return;
    
    for (unsigned int i = 0; i < dwcFiles; i++)
    {
        if (phFileListRec[i])
            MsiCloseHandle(phFileListRec[i]);
    }    
}
//
```



В следующем примере показано, как извлечь сведения о применимости для списка исправлений установщик Windows (MSP-файлы) с помощью свойства [**Патчфилес**](installer-patchfiles.md) [**объекта установщика**](installer-object.md). Свойство **патчфилес** предоставляет код продукта для целей исправлений и список MSP-файлов, разделенных точкой с запятой. Для этого примера требуется установщик Windows 4,0, работающий в Windows Vista.


```VB
Dim FileList
Dim installer : Set installer = Nothing
Dim argCount:argCount = Wscript.Arguments.Count

Set installer = Wscript.CreateObject("WindowsInstaller.Installer")

If (argCount > 0) Then
    sProdCode = Wscript.Arguments(0)
    sPatchPckgPath = Wscript.Arguments(1)
    Set FileList = installer.PatchFiles (sProdCode, sPatchPckgPath)
    For each File in FileList
           Wscript.Echo "Affected file: " & File
    Next
Else
    Usage
End If

Sub Usage
    Wscript.Echo "Windows Installer utility to list files updated by a patch for an installed product" &_
    vbNewLine & " 1st argument is the product code (GUID) of an installed product" &_
    vbNewLine & " 2nd argument is the list of patches" &_
    vbNewLine &_
    vbNewLine & "Copyright (C) Microsoft. All rights reserved."
    Wscript.Quit 1
End Sub
```



 

 



