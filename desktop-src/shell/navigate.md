---
description: Теперь у вас есть все необходимые элементы, необходимые для навигации в любом месте пространства имен.
ms.assetid: bd9f903d-bea6-494f-af81-d90457dc2647
title: Навигация по пространству имен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d24993369222fb32f9de6c79a0c998b1d7be9f2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080374"
---
# <a name="navigating-the-namespace"></a>Навигация по пространству имен

Теперь у вас есть все необходимые элементы, необходимые для навигации в любом месте пространства имен. Самый простой способ начать с того, чтобы приложение вызывало [**шжетдесктопфолдер**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder) для получения интерфейса [**ишеллфолдер**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) рабочего стола. Затем, чтобы переместиться вниз по пространству имен, приложение может выполнить следующие действия:

1.  Перечисление содержимого папки.
2.  Определите, какие объекты являются вложенными папками, и выберите один из них.
3.  Выполните привязку к вложенной папке, чтобы получить интерфейс [**ишеллфолдер**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) .

Повторите эти шаги так часто, как это необходимо для достижения целевого объекта.

## <a name="a-simple-example-of-namespace-navigation"></a>Простой пример навигации по пространству имен

Следующий фрагмент кода — это простое консольное приложение, которое иллюстрирует ряд процедур, описанных в предыдущих разделах. Для ясности пропущена проверка ошибок. Приложение выполняет такие задачи:

1.  Получает интерфейс [**ишеллфолдер**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) папки Program Files ([с помощью интерфейса ишеллфолдер](folder-info.md)).
2.  Перечисляет содержимое папки ([Перечисление содержимого папки](folder-info.md)).
3.  Определяет все отображаемые имена и выводит их на печать ([определяя отображаемые имена и другие свойства](folder-info.md)).
4.  Ищет вложенную папку ([Получение указателя на интерфейс Ишеллфолдер вложенной папки](folder-info.md)).
5.  Выполняет привязку к первой найденной вложенной папке (путем[получения указателя на интерфейс Ишеллфолдер вложенной папки](folder-info.md)).
6.  Выводит отображаемые имена объектов во вложенной папке.


```
#include <shlobj.h>
#include <shlwapi.h>
#include <iostream.h>

main()
{
    LPITEMIDLIST pidlProgFiles = NULL;
    LPITEMIDLIST pidlItems = NULL;
    IShellFolder *psfFirstFolder = NULL;
    IShellFolder *psfDeskTop = NULL;
    IShellFolder *psfProgFiles = NULL;
    LPENUMIDLIST ppenum = NULL;
    ULONG celtFetched;
    HRESULT hr;
    STRRET strDispName;
    TCHAR pszDisplayName[MAX_PATH];
    ULONG uAttr;
   
    CoInitialize( NULL );
    
    hr = SHGetFolderLocation(NULL, CSIDL_PROGRAM_FILES, NULL, 0, &pidlProgFiles);

    hr = SHGetDesktopFolder(&psfDeskTop);

    hr = psfDeskTop->BindToObject(pidlProgFiles, NULL, IID_IShellFolder, (LPVOID *) &psfProgFiles);
    psfDeskTop->Release();

    hr = psfProgFiles->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, &ppenum);

    while( hr = ppenum->Next(1,&pidlItems, &celtFetched) == S_OK && (celtFetched) == 1)
    {
        psfProgFiles->GetDisplayNameOf(pidlItems, SHGDN_INFOLDER, &strDispName);
        StrRetToBuf(&strDispName, pidlItems, pszDisplayName, MAX_PATH);
        cout << pszDisplayName << '\n';
        if(!psfFirstFolder)
        {
            uAttr = SFGAO_FOLDER;
            psfProgFiles->GetAttributesOf(1, (LPCITEMIDLIST *) &pidlItems, &uAttr);
            if(uAttr & SFGAO_FOLDER)
            {
                hr = psfProgFiles->BindToObject(pidlItems, NULL, IID_IShellFolder, (LPVOID *) &psfFirstFolder);
            }
        }
        CoTaskMemFree(pidlItems);
    }

    cout << "\n\n";

    ppenum->Release();

    if(psfFirstFolder)
    {
        hr = psfFirstFolder->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, &ppenum);

        while( hr = ppenum->Next(1,&pidlItems, &celtFetched) == S_OK && (celtFetched) == 1)
        {
            psfFirstFolder->GetDisplayNameOf(pidlItems, SHGDN_INFOLDER, &strDispName);
            StrRetToBuf(&strDispName, pidlItems, pszDisplayName, MAX_PATH);
            cout << pszDisplayName << '\n';
            CoTaskMemFree(pidlItems);
        }
    }

    ppenum->Release();
    CoTaskMemFree(pidlProgFiles);
    psfProgFiles->Release();
    psfFirstFolder->Release();

    CoUninitialize();
    return 0;
}
```



 

 
