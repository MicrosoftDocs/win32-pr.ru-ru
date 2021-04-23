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
# <a name="navigating-the-namespace"></a><span data-ttu-id="86252-103">Навигация по пространству имен</span><span class="sxs-lookup"><span data-stu-id="86252-103">Navigating the Namespace</span></span>

<span data-ttu-id="86252-104">Теперь у вас есть все необходимые элементы, необходимые для навигации в любом месте пространства имен.</span><span class="sxs-lookup"><span data-stu-id="86252-104">You now have all the essential elements needed to navigate anywhere in the namespace.</span></span> <span data-ttu-id="86252-105">Самый простой способ начать с того, чтобы приложение вызывало [**шжетдесктопфолдер**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder) для получения интерфейса [**ишеллфолдер**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="86252-105">The simplest way to start is to have your application call [**SHGetDesktopFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder) to retrieve the desktop's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface.</span></span> <span data-ttu-id="86252-106">Затем, чтобы переместиться вниз по пространству имен, приложение может выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="86252-106">Then, to navigate downward through the namespace, your application can follow these steps:</span></span>

1.  <span data-ttu-id="86252-107">Перечисление содержимого папки.</span><span class="sxs-lookup"><span data-stu-id="86252-107">Enumerate the folder's contents.</span></span>
2.  <span data-ttu-id="86252-108">Определите, какие объекты являются вложенными папками, и выберите один из них.</span><span class="sxs-lookup"><span data-stu-id="86252-108">Determine which objects are subfolders, and select one.</span></span>
3.  <span data-ttu-id="86252-109">Выполните привязку к вложенной папке, чтобы получить интерфейс [**ишеллфолдер**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) .</span><span class="sxs-lookup"><span data-stu-id="86252-109">Bind to the subfolder to retrieve its [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface.</span></span>

<span data-ttu-id="86252-110">Повторите эти шаги так часто, как это необходимо для достижения целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="86252-110">Repeat these steps as often as necessary to reach the target.</span></span>

## <a name="a-simple-example-of-namespace-navigation"></a><span data-ttu-id="86252-111">Простой пример навигации по пространству имен</span><span class="sxs-lookup"><span data-stu-id="86252-111">A Simple Example of Namespace Navigation</span></span>

<span data-ttu-id="86252-112">Следующий фрагмент кода — это простое консольное приложение, которое иллюстрирует ряд процедур, описанных в предыдущих разделах.</span><span class="sxs-lookup"><span data-stu-id="86252-112">The following piece of sample code is a simple console application that illustrates a number of the procedures discussed in the preceding sections.</span></span> <span data-ttu-id="86252-113">Для ясности пропущена проверка ошибок.</span><span class="sxs-lookup"><span data-stu-id="86252-113">Error checking has been omitted for clarity.</span></span> <span data-ttu-id="86252-114">Приложение выполняет такие задачи:</span><span class="sxs-lookup"><span data-stu-id="86252-114">The application performs the following tasks:</span></span>

1.  <span data-ttu-id="86252-115">Получает интерфейс [**ишеллфолдер**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) папки Program Files ([с помощью интерфейса ишеллфолдер](folder-info.md)).</span><span class="sxs-lookup"><span data-stu-id="86252-115">Retrieves the Program Files folder's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface ([Using the IShellFolder Interface](folder-info.md)).</span></span>
2.  <span data-ttu-id="86252-116">Перечисляет содержимое папки ([Перечисление содержимого папки](folder-info.md)).</span><span class="sxs-lookup"><span data-stu-id="86252-116">Enumerates the contents of the folder ([Enumerating the Contents of a Folder](folder-info.md)).</span></span>
3.  <span data-ttu-id="86252-117">Определяет все отображаемые имена и выводит их на печать ([определяя отображаемые имена и другие свойства](folder-info.md)).</span><span class="sxs-lookup"><span data-stu-id="86252-117">Determines all the display names and prints them ([Determining Display Names and Other Properties](folder-info.md)).</span></span>
4.  <span data-ttu-id="86252-118">Ищет вложенную папку ([Получение указателя на интерфейс Ишеллфолдер вложенной папки](folder-info.md)).</span><span class="sxs-lookup"><span data-stu-id="86252-118">Looks for a subfolder ([Getting a Pointer to a Subfolder's IShellFolder Interface](folder-info.md)).</span></span>
5.  <span data-ttu-id="86252-119">Выполняет привязку к первой найденной вложенной папке (путем[получения указателя на интерфейс Ишеллфолдер вложенной папки](folder-info.md)).</span><span class="sxs-lookup"><span data-stu-id="86252-119">Binds to the first subfolder it finds ([Getting a Pointer to a Subfolder's IShellFolder Interface](folder-info.md)).</span></span>
6.  <span data-ttu-id="86252-120">Выводит отображаемые имена объектов во вложенной папке.</span><span class="sxs-lookup"><span data-stu-id="86252-120">Prints the display names of the objects in the subfolder.</span></span>


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



 

 
