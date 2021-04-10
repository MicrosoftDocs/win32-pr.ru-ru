---
title: Обозреватель контейнеров
description: Приложение может использовать функцию Дсбровсефорконтаинер для вывода диалогового окна, которое можно использовать для просмотра контейнеров в службе домен Active Directory.
ms.assetid: aa88d565-ff25-4082-964a-9a230d2607f2
ms.tgt_platform: multiple
keywords:
- Active Directory в браузере контейнеров
- контейнеры Active Directory, браузер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 964c67873cc7936a75e2b9c1cdf331d0fa1fdae1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069804"
---
# <a name="container-browser"></a>Обозреватель контейнеров

Приложение может использовать функцию [**дсбровсефорконтаинер**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) для вывода диалогового окна, которое можно использовать для просмотра контейнеров в службе домен Active Directory. Диалоговое окно отображает контейнеры в формате дерева и позволяет пользователю перемещаться по дереву с помощью клавиатуры и мыши. Когда пользователь выбирает элемент в диалоговом окне, предоставляется путь к контейнеру, выбранному пользователем.

[**Дсбровсефорконтаинер**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) принимает указатель на структуру [**дсбровсеинфо**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) , содержащую данные о диалоговом окне, и возвращает путь к выбранному элементу.

Элемент **псзрут** является указателем на строку в Юникоде, содержащую корневой контейнер дерева. Если **псзрут** имеет **значение NULL**, дерево будет содержать все дерево.

Элемент **псзпас** получает путь к выбранному объекту. Можно указать конкретный контейнер, который должен быть видимым и выбранным при первом отображении диалогового окна. Это достигается путем установки для **псзпас** значения ADsPath для выбранного элемента и установки флага **\_ експандонопен ДСБИ** в **dwFlags**.

Содержимое и поведение диалогового окна также можно контролировать во время выполнения путем реализации функции [**бффкаллбакк**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) . Функция **бффкаллбакк** реализуется приложением и вызывается при возникновении определенных событий. Приложение может использовать эти события для управления отображением элементов диалогового окна, а также фактическим содержимым диалогового окна. Например, приложение может отфильтровать элементы, отображаемые в диалоговом окне, путем реализации функции **бффкаллбакк** , которая может управлять уведомлением **\_ куеринсерт ДСБМ** . При получении уведомления **ДСБМ \_ куеринсерт** используйте элемент **псзадспас** структуры [**дсбитем**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) , чтобы определить, какой элемент будет вставлен. Если приложение определяет, что элемент не должен отображаться, он может скрыть элемент, выполнив следующие действия.

1.  Добавьте флаг **\_ состояния дсбф** в элемент **двмаск** структуры [**дсбитем**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) .
2.  Добавьте флаг **дсбс \_ Hidden** в элемент **двстатемаск** структуры [**дсбитем**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) .
3.  Добавьте флаг **дсбс \_ Hidden** в элемент **двстате** структуры [**дсбитем**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) .
4.  Возврат ненулевого значения из функции [**бффкаллбакк**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) .

В дополнение к скрытию определенных элементов приложение может изменить текст и значок, отображаемые для элемента, обрабатывая уведомление **ДСБМ \_ куеринсерт** . Дополнительные сведения см. в разделе [**дсбитем**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema).

Функция [**бффкаллбакк**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) может использовать **\_ инициализированное уведомление бффм** для получения маркера диалогового окна. Приложение может использовать этот обработчик для отправки сообщений, например **бффм \_ енаблеок**, в диалоговое окно. Дополнительные сведения о сообщениях, которые могут быть отправлены в диалоговое окно, см. в разделе [**бффкаллбакк**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback).

Чтобы получить прямой доступ к элементам управления в диалоговом окне, можно также использовать обработчик диалогового окна. **Дсбид \_ БАННЕР** — это идентификатор элемента управления "статический текст", в котором отображается элемент **Псзтитле** структуры [**дсбровсеинфо**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) . **Дсбид \_ КОНТАИНЕРЛИСТ** — это идентификатор элемента управления иерархического представления, используемого для отображения содержимого дерева. По возможности следует избегать использования этих элементов, чтобы предотвратить будущие проблемы совместимости приложений.

В следующем примере кода C++ показано, как использовать функцию [**дсбровсефорконтаинер**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) для создания диалогового окна "Обозреватель контейнеров" и реализации функции [**бффкаллбакк**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) . [**Бффкаллбакк**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) использует уведомление **\_ куеринсерт ДСБМ** , чтобы изменить отображаемое имя каждого элемента на различающееся имя элемента.


```C++
#include <shlobj.h>
#include <dsclient.h>
#include <atlbase.h>

/**********

    WideCharToLocal()
   
***********/

int WideCharToLocal(LPTSTR pLocal, LPWSTR pWide, DWORD dwChars)
{
    *pLocal = NULL;
    size_t nWideLength = 0;
    wchar_t *pwszSubstring;

    nWideLength = wcslen(pWide);

#ifdef UNICODE
    if(nWideLength < dwChars)
    {
        wcsncpy_s(pLocal, pWide, dwChars);
    }
    else
    {
        wcsncpy_s(pLocal, pWide, dwChars-1);
        pLocal[dwChars-1] = NULL;
    }
#else
    if(nWideLength < dwChars)
    {
        WideCharToMultiByte(    CP_ACP, 
                                0, 
                                pWide, 
                                -1, 
                                pLocal, 
                                dwChars, 
                                NULL, 
                                NULL);
    }
    else
    {
        pwszSubstring = new WCHAR[dwChars];
        wcsncpy_s(pwszSubstring,pWide,dwChars-1);
        pwszSubstring[dwChars-1] = NULL;

        WideCharToMultiByte(    CP_ACP, 
                                0, 
                                pwszSubstring, 
                                -1, 
                                pLocal, 
                                dwChars, 
                                NULL, 
                                NULL);

    delete [] pwszSubstring;
    }
#endif

    return lstrlen(pLocal);
}

/**********

    BrowseCallback()

***********/

int CALLBACK BrowseCallback(HWND hWnd, 
                            UINT uMsg, 
                            LPARAM lParam, 
                            LPARAM lpData)
{
    switch(uMsg)
    {
    case DSBM_QUERYINSERT:
        {
            BOOL fReturn = FALSE;
            DSBITEM *pItem = (DSBITEM*)lParam;

            /*
            If this is to the root item, get the distinguished name 
            for the object and set the display name to the 
            distinguished name.
            */
            if(!(pItem->dwState & DSBS_ROOT))
            {
                HRESULT hr;
                IADs    *pads;

                hr = ADsGetObject(pItem->pszADsPath , 
                    IID_IADs, (LPVOID*)&pads);
                if(SUCCEEDED(hr))
                {
                    VARIANT var;

                    VariantInit(&var);
                    hr = pads->Get(CComBSTR("distinguishedName"), 
                        &var);
                    if(SUCCEEDED(hr))
                    {
                        if(VT_BSTR == var.vt)
                        {
                            WideCharToLocal(pItem->szDisplayName, 
                                var.bstrVal, 
                                DSB_MAX_DISPLAYNAME_CHARS);
                            pItem->dwMask |= DSBF_DISPLAYNAME;
                            fReturn = TRUE;
                        }
                        
                        VariantClear(&var);
                    }
                    
                    pads->Release();
                }
            }

            return fReturn;
        }

        break;
    }
    
    return FALSE;
}

/***********

    BrowseForContainer()

************/

HRESULT BrowseForContainer(HWND hwndParent, 
    LPOLESTR *ppContainerADsPath)
{
    HRESULT hr = E_FAIL;
    DSBROWSEINFO dsbi;
    OLECHAR wszPath[MAX_PATH * 2];
    DWORD result;
 
    if(!ppContainerADsPath)
    {
        return E_INVALIDARG;
    }
 
    ZeroMemory(&dsbi, sizeof(dsbi));
    dsbi.hwndOwner = hwndParent;
    dsbi.cbStruct = sizeof (DSBROWSEINFO);
    dsbi.pszCaption = TEXT("Browse for a Container");
    dsbi.pszTitle = TEXT("Select an Active Directory container.");
    dsbi.pszRoot = NULL;
    dsbi.pszPath = wszPath;
    dsbi.cchPath = sizeof(wszPath)/sizeof(OLECHAR);
    dsbi.dwFlags = DSBI_INCLUDEHIDDEN |
                    DSBI_IGNORETREATASLEAF|
                    DSBI_RETURN_FORMAT;
    dsbi.pfnCallback = BrowseCallback;
    dsbi.lParam = 0;
    dsbi.dwReturnFormat = ADS_FORMAT_X500;
 
    // Display the browse dialog box.
    // Returns -1, 0, IDOK, or IDCANCEL.
    result = DsBrowseForContainer(&dsbi); 
    if(IDOK == result)
    {
        // Allocate memory for the string.
        *ppContainerADsPath = (OLECHAR*)CoTaskMemAlloc(
            sizeof(OLECHAR)*(wcslen(wszPath) + 1));
        if(*ppContainerADsPath)
        {
            wcscpy_s(*ppContainerADsPath, wszPath);
            // Caller must free using CoTaskMemFree. 
            hr = S_OK;
        }
        else
        {
            hr = E_FAIL;
        }
    }
    else
    {
        hr = E_FAIL;
    }
 
    return hr;
}
```



 

 