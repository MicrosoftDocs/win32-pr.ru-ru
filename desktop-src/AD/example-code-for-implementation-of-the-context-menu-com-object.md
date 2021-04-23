---
title: Пример кода для реализации COM-объекта контекстного меню
description: Следующий пример кода можно использовать для реализации расширения контекстного меню Active Directory. В одном элементе контекстного меню отображается окно сообщения, содержащее путь к каждому выбранному элементу.
ms.assetid: dc8f2c31-6031-4c7d-a173-5cedcedbfb26
ms.tgt_platform: multiple
keywords:
- Active Directory AD, пример кода C/C++, реализация COM-объекта контекстного меню
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99402606b21f3b91e0511a4baf4ca18e8a2e8c23
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069767"
---
# <a name="example-code-for-implementation-of-the-context-menu-com-object"></a><span data-ttu-id="0d524-105">Пример кода для реализации COM-объекта контекстного меню</span><span class="sxs-lookup"><span data-stu-id="0d524-105">Example Code for Implementation of the Context Menu COM Object</span></span>

<span data-ttu-id="0d524-106">Следующий пример кода можно использовать для реализации расширения контекстного меню Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0d524-106">The following code example can be used to implement an Active Directory context menu extension.</span></span> <span data-ttu-id="0d524-107">В одном элементе контекстного меню отображается окно сообщения, содержащее путь к каждому выбранному элементу.</span><span class="sxs-lookup"><span data-stu-id="0d524-107">The single context menu item will display a message box that contains the ADsPath of each item selected.</span></span>

## <a name="ishellextinit-implementation"></a><span data-ttu-id="0d524-108">Реализация Ишеллекстинит</span><span class="sxs-lookup"><span data-stu-id="0d524-108">IShellExtInit Implementation</span></span>

<span data-ttu-id="0d524-109">Следующий пример кода можно использовать для реализации методов [**ишеллекстинит**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) .</span><span class="sxs-lookup"><span data-stu-id="0d524-109">The following code example can be used to implement the [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) methods.</span></span>


```C++
///////////////////////////////////////////////////////////////////////////
//
// IShellExtInit Implementation
//

/**************************************************************************

   CContMenuExt::Initialize()

**************************************************************************/

STDMETHODIMP CContMenuExt::Initialize(  LPCITEMIDLIST pidlFolder,
                                        LPDATAOBJECT pDataObj,
                                        HKEY  hKeyProgId)
{
    STGMEDIUM   stm;
    FORMATETC   fe;
    HRESULT     hr;

    if(NULL == pDataObj)
    {
        return E_INVALIDARG;
    }

    fe.cfFormat = RegisterClipboardFormat(CFSTR_DSOBJECTNAMES);
    fe.ptd = NULL;
    fe.dwAspect = DVASPECT_CONTENT;
    fe.lindex = -1;
    fe.tymed = TYMED_HGLOBAL;
    hr = pDataObj->GetData(&fe, &stm);
    if(SUCCEEDED(hr))
    {
        LPDSOBJECTNAMES pdson = (LPDSOBJECTNAMES)GlobalLock(stm.hGlobal);

        if(pdson)
        {
            DWORD   dwBytes = GlobalSize(stm.hGlobal);

            m_pObjectNames = (DSOBJECTNAMES*)GlobalAlloc(GPTR, dwBytes);
            if(m_pObjectNames)
            {
                CopyMemory(m_pObjectNames, pdson, dwBytes);
            }
            
            GlobalUnlock(stm.hGlobal);
        }
        
        ReleaseStgMedium(&stm);
    }

    fe.cfFormat = RegisterClipboardFormat(CFSTR_DS_DISPLAY_SPEC_OPTIONS);
    fe.ptd = NULL;
    fe.dwAspect = DVASPECT_CONTENT;
    fe.lindex = -1;
    fe.tymed = TYMED_HGLOBAL;
    hr = pDataObj->GetData(&fe, &stm);
    if(SUCCEEDED(hr))
    {
        PDSDISPLAYSPECOPTIONS   pdso;
        
        pdso = (PDSDISPLAYSPECOPTIONS)GlobalLock(stm.hGlobal);
        if(pdso)
        {
            DWORD   dwBytes = GlobalSize(stm.hGlobal);

            m_pDispSpecOpts = (PDSDISPLAYSPECOPTIONS)GlobalAlloc(GPTR, dwBytes);
            if(m_pDispSpecOpts)
            {
                CopyMemory(m_pDispSpecOpts, pdso, dwBytes);
            }
            
            GlobalUnlock(stm.hGlobal);
        }

        ReleaseStgMedium(&stm);
    }

    return hr;
}

```



## <a name="icontextmenu-implementation"></a><span data-ttu-id="0d524-110">Реализация IContextMenu</span><span class="sxs-lookup"><span data-stu-id="0d524-110">IContextMenu Implementation</span></span>

<span data-ttu-id="0d524-111">Следующий пример кода можно использовать для реализации методов [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) .</span><span class="sxs-lookup"><span data-stu-id="0d524-111">The following code example can be used to implement the [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) methods.</span></span>


```C++
///////////////////////////////////////////////////////////////////////////
//
// IContextMenu Implementation
//

/**************************************************************************

   CContMenuExt::QueryContextMenu()

**************************************************************************/

STDMETHODIMP CContMenuExt::QueryContextMenu(    HMENU hMenu,
                                                UINT indexMenu,
                                                UINT idCmdFirst,
                                                UINT idCmdLast,
                                                UINT uFlags)
{
    if(m_pObjectNames && !(CMF_DEFAULTONLY & uFlags))
    {
        InsertMenu( hMenu, 
                    indexMenu, 
                    MF_STRING | MF_BYPOSITION, 
                    idCmdFirst + IDM_CONTMENU, 
                    TEXT("AD Sample Context Menu"));

        return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(IDM_CONTMENU + 1));
    }

    return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(0));
}

/**************************************************************************

   CContMenuExt::InvokeCommand()

**************************************************************************/

STDMETHODIMP CContMenuExt::InvokeCommand(LPCMINVOKECOMMANDINFO lpcmi)
{
    if(LOWORD(lpcmi->lpVerb) > IDM_CONTMENU)
    {
        return E_INVALIDARG;
    }

    switch (LOWORD(lpcmi->lpVerb))
    {
    case IDM_CONTMENU:
        {
            LPWSTR  pwszName;
            DWORD   dwBytes;
            UINT    i;

            for(i = 0, dwBytes = 0; i < m_pObjectNames->cItems; i++)
            {
                pwszName = (LPWSTR)((LPBYTE)m_pObjectNames + m_pObjectNames->aObjects[i].offsetName);
                dwBytes += (lstrlenW(pwszName) + 2) * sizeof(WCHAR);
            }

            LPWSTR  pwszText = (LPWSTR)GlobalAlloc(GPTR, dwBytes);

            if(pwszText)
            {
                pwszText[0] = 0;
                for(i = 0; i < m_pObjectNames->cItems; i++)
                {
                    pwszName = (LPWSTR)((LPBYTE)m_pObjectNames + m_pObjectNames->aObjects[i].offsetName);
                    wcscat_s(pwszText, pwszName);
                    wcscat_s(pwszText, L"\n");
                }
                
                MessageBoxW(lpcmi->hwnd, 
                            pwszText, 
                            L"Sample Command", 
                            MB_OK | MB_ICONINFORMATION);

                GlobalFree(pwszText);
            }
        }
        break;
    }

    return NOERROR;
}

/**************************************************************************

   CContMenuExt::GetCommandString()

**************************************************************************/

STDMETHODIMP CContMenuExt::GetCommandString(    UINT idCommand,
                                                UINT uFlags,
                                                LPUINT lpReserved,
                                                LPSTR lpszName,
                                                UINT uMaxNameLen)
{
    HRESULT hr = E_INVALIDARG;
    TCHAR   szHelp[] = TEXT("Sample Context Menu Command");
    TCHAR   szVerb[] = TEXT("adcontmenu");

    switch(uFlags)
    {
    case GCS_HELPTEXTA:
        switch(idCommand)
        {
        case IDM_CONTMENU:
            LocalToAnsi((LPSTR)lpszName, szHelp, uMaxNameLen);
            hr = S_OK;
            break;
         }
        break;
   
    case GCS_HELPTEXTW:
        switch(idCommand)
        {
        case IDM_CONTMENU:
            LocalToWideChar((LPWSTR)lpszName, szHelp, uMaxNameLen);
            hr = S_OK;
            break;
         }
        break;
   
    case GCS_VERBA:
        switch(idCommand)
        {
        case IDM_CONTMENU:
            LocalToAnsi((LPSTR)lpszName, szVerb, uMaxNameLen);
            hr = S_OK;
            break;
        }
        break;
   
    case GCS_VERBW:
        switch(idCommand)
        {
        case IDM_CONTMENU:
            LocalToWideChar((LPWSTR)lpszName, szVerb, uMaxNameLen);
            hr = S_OK;
            break;
        }
        break;
   
    case GCS_VALIDATE:
        hr = S_OK;
        break;
    }

    return hr;
}

```



 

 