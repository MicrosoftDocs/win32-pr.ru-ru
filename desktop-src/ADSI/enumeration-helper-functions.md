---
title: Вспомогательные функции перечисления
description: Существует три вспомогательных функции перечислителя, которые можно использовать из C/C++ для облегчения навигации по Active Directoryным объектам. Это Адсбуилденумератор, Адсенумератенекст и Адсфриенумератор.
ms.assetid: 019958c8-5bf5-45eb-871c-796ff3750cdc
ms.tgt_platform: multiple
keywords:
- Адсбуилденумератор ADSI, использование
- Адсенумератенекст ADSI, использование
- Адсфриенумератор ADSI, использование
- ADSI ADSI, пример кода C/C++, использование Адсбуилденумератор Адсенумератенекст и Адсфриенумератор
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c110fbc4fddd420bf8205d6c2d894c7d4f4daf8287312c2d0d86002f5520310b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082658"
---
# <a name="enumeration-helper-functions"></a>Вспомогательные функции перечисления

Существует три вспомогательных функции перечислителя, которые можно использовать из C/C++ для облегчения навигации по Active Directoryным объектам. Это [**адсбуилденумератор**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator), [**адсенумератенекст**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext)и [**адсфриенумератор**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator).

## <a name="adsbuildenumerator"></a>адсбуилденумератор

Вспомогательная функция [**адсбуилденумератор**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) инкапсулирует код, необходимый для создания объекта перечислителя. Он вызывает метод [**иадсконтаинер:: Get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) , чтобы создать объект перечислителя, а затем вызывает метод [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , чтобы получить указатель на интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) для этого объекта. Объект перечисления — это механизм автоматизации для перечисления контейнеров. Чтобы освободить этот объект перечислителя, используйте функцию [**адсфриенумератор**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator) .

## <a name="adsenumeratenext"></a>адсенумератенекст

Вспомогательная функция [**адсенумератенекст**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) заполняет массив Variant с элементами, полученными из объекта перечислителя. Число извлекаемых элементов может быть меньше запрошенного числа.

## <a name="adsfreeenumerator"></a>адсфриенумератор

Освобождает объект перечислителя, созданный ранее с помощью функции [**адсбуилденумератор**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) .

В следующем примере кода показана функция, которая использует вспомогательные функции перечислителя в C++.


```C++
/*****************************************************************************
  Function:    TestEnumObject
  Arguments:   pszADsPath - ADsPath of the container to be enumerated (WCHAR*).
  Return:      S_OK if successful, an error code otherwise.
  Purpose:     Example using ADsBuildEnumerator, ADsEnumerateNext and
               ADsFreeEnumerator.
******************************************************************************/
#define MAX_ENUM      100  
 
HRESULT
TestEnumObject( LPWSTR pszADsPath )
{
    ULONG cElementFetched = 0L;
    IEnumVARIANT * pEnumVariant = NULL;
    VARIANT VariantArray[MAX_ENUM];
    HRESULT hr = S_OK;
    IADsContainer * pADsContainer =  NULL;
    DWORD dwObjects = 0, dwEnumCount = 0, i = 0;
    BOOL  fContinue = TRUE;
 
 
    hr = ADsGetObject(
                pszADsPath,
                IID_IADsContainer,
                (void **)&pADsContainer
                );
 
 
    if (FAILED(hr)) {
 
        printf("\"%S\" is not a valid container object.\n", pszADsPath) ;
        goto exitpoint ;
    }
 
    hr = ADsBuildEnumerator(
            pADsContainer,
            &pEnumVariant
            );
 
    if( FAILED( hr ) )
    {
      printf("ADsBuildEnumerator failed with %lx\n", hr ) ;
      goto exitpoint ;
    }
 
    fContinue  = TRUE;
    while (fContinue) {
 
        IADs *pObject ;
 
        hr = ADsEnumerateNext(
                    pEnumVariant,
                    MAX_ENUM,
                    VariantArray,
                    &cElementFetched
                    );

        if ( FAILED( hr ) )
        {
            printf("ADsEnumerateNext failed with %lx\n",hr);
            goto exitpoint;
        }
 
        if (hr == S_FALSE) {
            fContinue = FALSE;
        }
 
        dwEnumCount++;
 
        for (i = 0; i < cElementFetched; i++ ) {
 
            IDispatch *pDispatch    = NULL;
            BSTR        bstrADsPath = NULL;
 
            pDispatch = VariantArray[i].pdispVal;
 
            hr = V_DISPATCH( VariantArray + i )->QueryInterface(IID_IADs, (void **) &pObject) ;
 
            if( SUCCEEDED( hr ) )
            {
               pObject->get_ADsPath( &bstrADsPath );
               printf( "%S\n", bstrADsPath );
            }
            pObject->Release();
            VariantClear( VariantArray + i );
            SysFreeString( bstrADsPath );
        }
 
        dwObjects += cElementFetched;
    }
 
    printf("Total Number of Objects enumerated is %d\n", dwObjects);
 
exitpoint:
    if (pEnumVariant) {
        ADsFreeEnumerator( pEnumVariant );
    }
 
    if (pADsContainer) {
        pADsContainer->Release();
    }
 
    return(hr);
}
```



 

 