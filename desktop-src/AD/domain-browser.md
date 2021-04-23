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
# <a name="domain-browser"></a><span data-ttu-id="ab765-104">Браузер домена</span><span class="sxs-lookup"><span data-stu-id="ab765-104">Domain Browser</span></span>

<span data-ttu-id="ab765-105">С помощью интерфейса [**идсбровседомаинтри**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) приложение может отобразить диалоговое окно обозреватель домена и получить DNS-имя домена, выбранного пользователем.</span><span class="sxs-lookup"><span data-stu-id="ab765-105">Using the [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) interface, an application can display a domain browser dialog box and obtain the DNS name of the domain selected by the user.</span></span> <span data-ttu-id="ab765-106">Приложение также может использовать интерфейс **идсбровседомаинтри** для получения данных обо всех деревьях доменов и доменах в лесу.</span><span class="sxs-lookup"><span data-stu-id="ab765-106">An application can also use the **IDsBrowseDomainTree** interface to obtain data about all domain trees and domains within a forest.</span></span>

<span data-ttu-id="ab765-107">Экземпляр интерфейса [**идсбровседомаинтри**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) создается путем вызова [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) с идентификатором класса **CLSID \_ дсдомаинтрибровсер** , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="ab765-107">An instance of the [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) interface is created by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the **CLSID\_DsDomainTreeBrowser** class identifier as shown below.</span></span>

<span data-ttu-id="ab765-108">Метод [**идсбровседомаинтри:: сеткомпутер**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-setcomputer) можно использовать для указания того, какой компьютер и учетные данные используются в качестве основания для получения данных домена.</span><span class="sxs-lookup"><span data-stu-id="ab765-108">The [**IDsBrowseDomainTree::SetComputer**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-setcomputer) method can be used to specify which computer and credentials are used as the basis for retrieving the domain data.</span></span> <span data-ttu-id="ab765-109">Когда **сеткомпутер** вызывается в определенном экземпляре [**идсбровседомаинтри**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) , [**идсбровседомаинтри:: флушкачеддомаинс**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-flushcacheddomains) должен вызываться до повторного вызова **сеткомпутер** .</span><span class="sxs-lookup"><span data-stu-id="ab765-109">When **SetComputer** is called on a particular [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) instance, [**IDsBrowseDomainTree::FlushCachedDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-flushcacheddomains) must be called before **SetComputer** is called again.</span></span>

<span data-ttu-id="ab765-110">Метод [**идсбровседомаинтри:: бровсето**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-browseto) используется для вывода диалогового окна "обозреватель домена".</span><span class="sxs-lookup"><span data-stu-id="ab765-110">The [**IDsBrowseDomainTree::BrowseTo**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-browseto) method is used to display the domain browser dialog box.</span></span> <span data-ttu-id="ab765-111">Когда пользователь выбирает домен и нажимает кнопку **ОК** , **Идсбровседомаинтри:: бровсето** возвращает **S \_ OK** , а параметр *ппсзтаржетпас* содержит имя выбранного домена.</span><span class="sxs-lookup"><span data-stu-id="ab765-111">When the user selects a domain and clicks the **OK** button, the **IDsBrowseDomainTree::BrowseTo** returns **S\_OK** and the *ppszTargetPath* parameter contains the name of the selected domain.</span></span> <span data-ttu-id="ab765-112">Если строка имени больше не требуется, вызывающий объект должен освободить строку, вызвав [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="ab765-112">When the name string is no longer required, the caller must free the string by calling [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

<span data-ttu-id="ab765-113">В следующем примере кода показано, как использовать интерфейс [**идсбровседомаинтри**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) для отображения диалогового окна "обозреватель домена".</span><span class="sxs-lookup"><span data-stu-id="ab765-113">The following code example shows how to use the [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) interface to display the domain browser dialog box.</span></span>


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



<span data-ttu-id="ab765-114">Для получения данных из дерева доменов используется метод [**идсбровседомаинтри::-«Domains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) ».</span><span class="sxs-lookup"><span data-stu-id="ab765-114">The [**IDsBrowseDomainTree::GetDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) method is used to obtain domain tree data.</span></span> <span data-ttu-id="ab765-115">Данные домена передаются в структуру [**домаинтри**](/windows/desktop/api/Dsclient/ns-dsclient-domain_tree) .</span><span class="sxs-lookup"><span data-stu-id="ab765-115">The domain data is supplied in a [**DOMAINTREE**](/windows/desktop/api/Dsclient/ns-dsclient-domain_tree) structure.</span></span> <span data-ttu-id="ab765-116">Структура **домаинтри** содержит размер структуры и число элементов домена в дереве.</span><span class="sxs-lookup"><span data-stu-id="ab765-116">The **DOMAINTREE** structure contains the size of the structure and the number of domain elements in the tree.</span></span> <span data-ttu-id="ab765-117">Структура **домаинтри** также содержит одну или несколько структур [**домаиндеск**](/windows/desktop/api/Dsclient/ns-dsclient-domaindesc) .</span><span class="sxs-lookup"><span data-stu-id="ab765-117">The **DOMAINTREE** structure also contains one or more [**DOMAINDESC**](/windows/desktop/api/Dsclient/ns-dsclient-domaindesc) structures.</span></span> <span data-ttu-id="ab765-118">**Домаиндеск** содержит данные об одном элементе в дереве доменов, включая дочерние и родственные данные.</span><span class="sxs-lookup"><span data-stu-id="ab765-118">The **DOMAINDESC** contains data about a single element in the domain tree, including child and sibling data.</span></span> <span data-ttu-id="ab765-119">Одноуровневые элементы домена можно перечислить путем доступа к элементу **пднекстсиблинг** каждой последующей структуры **домаиндеск** .</span><span class="sxs-lookup"><span data-stu-id="ab765-119">The siblings of a domain can be enumerated by accessing the **pdNextSibling** member of each subsequent **DOMAINDESC** structure.</span></span> <span data-ttu-id="ab765-120">Дочерние домены могут быть получены аналогичным образом путем доступа к элементу **пдчилдлист** каждой последующей структуры **домаиндеск** .</span><span class="sxs-lookup"><span data-stu-id="ab765-120">The children of the domain can be retrieved in a similar manner by accessing the **pdChildList** member of each subsequent **DOMAINDESC** structure.</span></span>

<span data-ttu-id="ab765-121">В следующем примере кода показано, как получить данные дерева доменов и получить к ним доступ с помощью метода [**идсбровседомаинтри::.**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains)</span><span class="sxs-lookup"><span data-stu-id="ab765-121">The following code example shows how to obtain and access the domain tree data using the [**IDsBrowseDomainTree::GetDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) method.</span></span>


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



 

 