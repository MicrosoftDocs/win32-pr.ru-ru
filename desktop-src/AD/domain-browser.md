---
title: Браузер домена
description: С помощью интерфейса Идсбровседомаинтри приложение может отобразить диалоговое окно обозреватель домена и получить DNS-имя домена, выбранного пользователем.
ms.assetid: 26793c61-469e-4e99-9056-b9fc04336b69
ms.tgt_platform: multiple
keywords:
- Active Directory в браузере доменов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b16bb932f14544902ab24e8fc1f50daa327bb705
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069777"
---
# <a name="domain-browser"></a>Браузер домена

С помощью интерфейса [**идсбровседомаинтри**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) приложение может отобразить диалоговое окно обозреватель домена и получить DNS-имя домена, выбранного пользователем. Приложение также может использовать интерфейс **идсбровседомаинтри** для получения данных обо всех деревьях доменов и доменах в лесу.

Экземпляр интерфейса [**идсбровседомаинтри**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) создается путем вызова [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) с идентификатором класса **CLSID \_ дсдомаинтрибровсер** , как показано ниже.

Метод [**идсбровседомаинтри:: сеткомпутер**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-setcomputer) можно использовать для указания того, какой компьютер и учетные данные используются в качестве основания для получения данных домена. Когда **сеткомпутер** вызывается в определенном экземпляре [**идсбровседомаинтри**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) , [**идсбровседомаинтри:: флушкачеддомаинс**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-flushcacheddomains) должен вызываться до повторного вызова **сеткомпутер** .

Метод [**идсбровседомаинтри:: бровсето**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-browseto) используется для вывода диалогового окна "обозреватель домена". Когда пользователь выбирает домен и нажимает кнопку **ОК** , **Идсбровседомаинтри:: бровсето** возвращает **S \_ OK** , а параметр *ппсзтаржетпас* содержит имя выбранного домена. Если строка имени больше не требуется, вызывающий объект должен освободить строку, вызвав [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).

В следующем примере кода показано, как использовать интерфейс [**идсбровседомаинтри**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) для отображения диалогового окна "обозреватель домена".


```C++
#include <shlobj.h>
#include <dsclient.h>

void main(void)
{
    HRESULT     hr;

    hr = CoInitialize(NULL);
    if(FAILED(hr)) 
    {
        return;
    }

    IDsBrowseDomainTree *pDsDomains = NULL;

    hr = ::CoCreateInstance(    CLSID_DsDomainTreeBrowser,
                                NULL,
                                CLSCTX_INPROC_SERVER,
                                IID_IDsBrowseDomainTree,
                                (void **)(&pDsDomains));
    
    if(SUCCEEDED(hr))
    {
        LPOLESTR    pstr;        

        hr = pDsDomains->BrowseTo(  GetDesktopWindow(),
                                    &pstr,
                                    0);
        
        if(S_OK == hr)
        {
            wprintf(pstr);
            wprintf(L"\n");
            CoTaskMemFree(pstr);
        }

        pDsDomains->Release();
    }

    CoUninitialize();
}
```



Для получения данных из дерева доменов используется метод [**идсбровседомаинтри::-«Domains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) ». Данные домена передаются в структуру [**домаинтри**](/windows/desktop/api/Dsclient/ns-dsclient-domain_tree) . Структура **домаинтри** содержит размер структуры и число элементов домена в дереве. Структура **домаинтри** также содержит одну или несколько структур [**домаиндеск**](/windows/desktop/api/Dsclient/ns-dsclient-domaindesc) . **Домаиндеск** содержит данные об одном элементе в дереве доменов, включая дочерние и родственные данные. Одноуровневые элементы домена можно перечислить путем доступа к элементу **пднекстсиблинг** каждой последующей структуры **домаиндеск** . Дочерние домены могут быть получены аналогичным образом путем доступа к элементу **пдчилдлист** каждой последующей структуры **домаиндеск** .

В следующем примере кода показано, как получить данные дерева доменов и получить к ним доступ с помощью метода [**идсбровседомаинтри::.**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains)


```C++
//  Add dsuiext.lib to the project.

#include "stdafx.h"
#include <shlobj.h>
#include <dsclient.h>

//The PrintDomain() function displays the domain name
void PrintDomain(DOMAINDESC *pDomainDesc, DWORD dwIndentLevel)
{
    DWORD i;

    // Display the domain name.
    for(i = 0; i < dwIndentLevel; i++)
    {
        wprintf(L"  ");
    }
    wprintf(pDomainDesc->pszName);
    wprintf(L"\n");
}

//The WalkDomainTree() function traverses the domain tree and prints the current domain name
void WalkDomainTree(DOMAINDESC *pDomainDesc, DWORD dwIndentLevel = 0)
{
    DOMAINDESC  *pCurrent;

    // Walk through the current item and any siblings it may have.
    for(pCurrent = pDomainDesc; 
        NULL != pCurrent; 
        pCurrent = pCurrent->pdNextSibling)
    {
        // Print the current domain name.
        PrintDomain(pCurrent, dwIndentLevel);

        // Walk the child tree, if one exists.
        if(NULL != pCurrent->pdChildList)
        {
            WalkDomainTree(pCurrent->pdChildList, 
                           dwIndentLevel + 1);
        }
    }
}

//  Entry point for application
int main(void)
{
    HRESULT hr;
    IDsBrowseDomainTree *pBrowseTree;
    CoInitialize(NULL);

    hr = CoCreateInstance(CLSID_DsDomainTreeBrowser,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IDsBrowseDomainTree,
                          (void**)&pBrowseTree);

    if(SUCCEEDED(hr))
    {
        DOMAINTREE  *pDomTreeStruct;
        hr = pBrowseTree->GetDomains(&pDomTreeStruct, 
                                     DBDTF_RETURNFQDN);
        if(SUCCEEDED(hr))
        {
            WalkDomainTree(&pDomTreeStruct->aDomains[0]);
            hr = pBrowseTree->FreeDomains(&pDomTreeStruct);
        }
        pBrowseTree->Release();
    }
    CoUninitialize();
}
```



 

 