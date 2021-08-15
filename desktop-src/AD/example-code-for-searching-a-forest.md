---
title: Пример кода для поиска в лесу
description: В этом разделе содержится пример кода, который выполняет поиск в лесу.
ms.assetid: 56740e95-548a-4e84-ab2e-2bb7a51b7e1e
ms.tgt_platform: multiple
keywords:
- Active Directory примеры Active Directory, поиск в лесу
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92c71afeecebf96ba123e909ad408835de083b8d45cb259a7b371b8214cc5b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118190291"
---
# <a name="example-code-for-searching-a-forest"></a>Пример кода для поиска в лесу

В этом разделе содержится пример кода, который выполняет поиск в лесу.

Следующий пример кода C/C++ привязывается к корню глобального каталога и перечисляет один объект, который является корнем леса, чтобы его можно было использовать для поиска в целом лесу.


```C++
Set gc = GetObject("GC:")
For each child in gc
    Set entpr = child
Next
' Now entpr is an object that can be used
' to search the entire forest.
```



Следующий пример кода C/C++ содержит функцию, которая возвращает указатель [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) , используемый для поиска в целом лесу.

Функция выполняет бессерверную привязку к корню глобального каталога, перечисляет один элемент, который является корнем леса и может использоваться для поиска в целом лесу, вызывает [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для получения указателя [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) на объект и возвращает этот указатель для использования вызывающим объектом для поиска в лесу.


```C++
HRESULT GetGC(IDirectorySearch **ppDS)
{
HRESULT hr;
IEnumVARIANT *pEnum = NULL;
IADsContainer *pCont = NULL;
VARIANT var;
IDispatch *pDisp = NULL;
ULONG lFetch;
 
// Set IDirectorySearch pointer to NULL.
*ppDS = NULL;
 
// First, bind to the GC: namespace container object. 
hr = ADsOpenObject(TEXT("GC:"),
                NULL,
                NULL,
                ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                IID_IADsContainer,
                (void**)&pCont);
if (FAILED(hr)) {
    _tprintf(TEXT("ADsOpenObject failed: 0x%x\n"), hr);
    goto cleanup;
} 
 
// Get an enumeration interface for the GC container to enumerate the 
// contents. The actual GC is the only child of the GC container.
hr = ADsBuildEnumerator(pCont, &pEnum);
if (FAILED(hr)) {
    _tprintf(TEXT("ADsBuildEnumerator failed: 0x%x\n"), hr);
    goto cleanup;
} 
 
// Now enumerate. There is only one child of the GC: object.
hr = pEnum->Next(1, &var, &lFetch);
if (FAILED(hr)) {
    _tprintf(TEXT("ADsEnumerateNext failed: 0x%x\n"), hr);
    goto cleanup;
} 
 
// Get the IDirectorySearch pointer.
if (( hr == S_OK ) && ( lFetch == 1 ) )     
{    
    pDisp = V_DISPATCH(&var);
    hr = pDisp->QueryInterface( IID_IDirectorySearch, (void**)ppDS); 
}
 
cleanup:
 
if (pEnum)
    ADsFreeEnumerator(pEnum);
if (pCont)
    pCont->Release();
if (pDisp)
    (pDisp)->Release();
return hr;
}
```



 

 