---
title: Пример Стгкреатепропсетстг
description: Показывает, как можно использовать функцию Стгкреатепропсетстг для создания интерфейса IPropertySetStorage поверх любого заданного интерфейса IStorage.
ms.assetid: f0d0664a-2cfd-4eb0-b1d5-47d1545394fd
keywords:
- структурированные служба хранилища стрктд Stg, примеры, стгкреатепропсетстг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7820563adbd165a620fadca29e4d75aefd2b33a81291f54ebdfeaadb5bbf6829
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117960294"
---
# <a name="stgcreatepropsetstg-sample"></a>Пример Стгкреатепропсетстг

В примере Стгкреатепропсетстг. cpp показано, как можно использовать функцию [**стгкреатепропсетстг**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg) для создания интерфейса [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) поверх любого заданного интерфейса [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) .


```C++
//+===================================================================
//
// To Build:   cl /GX StgCreatePropSetStg.cpp
//
//+===================================================================

#define UNICODE
#define _UNICODE
#define WIN32_LEAN_AND_MEAN

#include <stdio.h>
#include <windows.h>
#include <ole2.h>

#pragma comment( lib, "ole32.lib" )

IPropertyStorage*
CreatePropertySetInStorage( IStorage *pStg, const FMTID &fmtid )
{
    HRESULT hr = S_OK;
    IPropertySetStorage *pPropSetStg = NULL;
    IPropertyStorage *pPropStg = NULL;

    try
    {
        hr = StgCreatePropSetStg( pStg, 0 /*reserved*/, 
                                  &pPropSetStg );
        if( FAILED(hr) ) 
            throw L"Failed StgCreatePropSetStg (%08x)";

        hr = pPropSetStg->Create( fmtid, NULL,
            PROPSETFLAG_DEFAULT,
            STGM_CREATE | STGM_READWRITE | STGM_SHARE_EXCLUSIVE,
            &pPropStg );
        if( FAILED(hr) ) 
            throw L"Failed IPropertySetStorage::Create (%08x)";

        // Success. The caller must now call Release on both
        // pPropSetStg and pStg.

    }
    catch( const WCHAR *pwszError )
    {
        wprintf( L"Error: %s (%08x)\n", pwszError, hr );
    }

    if( NULL != pPropSetStg )
        pPropSetStg->Release();

    return( pPropStg );
}


extern "C" void wmain()
{
    HRESULT hr = S_OK;
    IStorage *pStg = NULL;
    IPropertyStorage *pPropStg = NULL;

    try
    {
        // Create an object with an IStorage interface. It is not 
        // necessary that it be a system-provided storage, such as 
        // that obtained by this call.  Any object that implements 
        // IStorage can be used.

        hr = StgCreateStorageEx( NULL,  // Create a temporary storage.
                                 STGM_CREATE
                                    | STGM_READWRITE
                                    | STGM_SHARE_EXCLUSIVE,
                                 STGFMT_STORAGE,
                                 0, NULL, NULL,
                                 IID_IStorage,
                                 reinterpret_cast<void**>(&pStg) );
        if( FAILED(hr) ) throw L"Failed StgCreateStorageEx";

        // Get and use an IPropertySetStorage that represents this 
        // IStorage.

        pPropStg = CreatePropertySetInStorage( pStg, 
                                        FMTID_SummaryInformation );
        if( NULL == pPropStg ) 
           throw L"Failed CreatePropertySetInStorage";

        // Here you could call IPropertyStorage methods, such as 
        // WriteMultiple andReadMultiple, using the pPropStg pointer.

        printf( "Success\n" );
    }
    catch( const WCHAR *pwszError )
    {
        wprintf( L"Error: %s (%08x)\n", pwszError, hr );
    }

    if( NULL != pPropStg )
        pPropStg->Release();
    if( NULL != pStg )
        pStg->Release();

}
```



 

 




