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
ms.openlocfilehash: af9597787202adf183435262eab9341957e19457
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104134571"
---
# <a name="enumeration-helper-functions"></a><span data-ttu-id="2c4cd-108">Вспомогательные функции перечисления</span><span class="sxs-lookup"><span data-stu-id="2c4cd-108">Enumeration Helper Functions</span></span>

<span data-ttu-id="2c4cd-109">Существует три вспомогательных функции перечислителя, которые можно использовать из C/C++ для облегчения навигации по Active Directoryным объектам.</span><span class="sxs-lookup"><span data-stu-id="2c4cd-109">There are three enumerator helper functions that can be used from C/C++ to aid in the navigation of Active Directory objects.</span></span> <span data-ttu-id="2c4cd-110">Это [**адсбуилденумератор**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator), [**адсенумератенекст**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext)и [**адсфриенумератор**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator).</span><span class="sxs-lookup"><span data-stu-id="2c4cd-110">They are [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator), [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext), and [**ADsFreeEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator).</span></span>

## <a name="adsbuildenumerator"></a><span data-ttu-id="2c4cd-111">адсбуилденумератор</span><span class="sxs-lookup"><span data-stu-id="2c4cd-111">ADsBuildEnumerator</span></span>

<span data-ttu-id="2c4cd-112">Вспомогательная функция [**адсбуилденумератор**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) инкапсулирует код, необходимый для создания объекта перечислителя.</span><span class="sxs-lookup"><span data-stu-id="2c4cd-112">The [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) helper function encapsulates the code required to create an enumerator object.</span></span> <span data-ttu-id="2c4cd-113">Он вызывает метод [**иадсконтаинер:: Get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) , чтобы создать объект перечислителя, а затем вызывает метод [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , чтобы получить указатель на интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="2c4cd-113">It calls the [**IADsContainer::get\_\_NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) method to create an enumerator object and then calls the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method of [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) to get a pointer to the [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface for that object.</span></span> <span data-ttu-id="2c4cd-114">Объект перечисления — это механизм автоматизации для перечисления контейнеров.</span><span class="sxs-lookup"><span data-stu-id="2c4cd-114">The enumeration object is the Automation mechanism to enumerate over containers.</span></span> <span data-ttu-id="2c4cd-115">Чтобы освободить этот объект перечислителя, используйте функцию [**адсфриенумератор**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator) .</span><span class="sxs-lookup"><span data-stu-id="2c4cd-115">Use the [**ADsFreeEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator) function to release this enumerator object.</span></span>

## <a name="adsenumeratenext"></a><span data-ttu-id="2c4cd-116">адсенумератенекст</span><span class="sxs-lookup"><span data-stu-id="2c4cd-116">ADsEnumerateNext</span></span>

<span data-ttu-id="2c4cd-117">Вспомогательная функция [**адсенумератенекст**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) заполняет массив Variant с элементами, полученными из объекта перечислителя.</span><span class="sxs-lookup"><span data-stu-id="2c4cd-117">The [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) helper function populates a VARIANT array with elements fetched from an enumerator object.</span></span> <span data-ttu-id="2c4cd-118">Число извлекаемых элементов может быть меньше запрошенного числа.</span><span class="sxs-lookup"><span data-stu-id="2c4cd-118">The number of elements retrieved can be smaller than the number requested.</span></span>

## <a name="adsfreeenumerator"></a><span data-ttu-id="2c4cd-119">адсфриенумератор</span><span class="sxs-lookup"><span data-stu-id="2c4cd-119">ADsFreeEnumerator</span></span>

<span data-ttu-id="2c4cd-120">Освобождает объект перечислителя, созданный ранее с помощью функции [**адсбуилденумератор**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) .</span><span class="sxs-lookup"><span data-stu-id="2c4cd-120">Frees an enumerator object previously created through the [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) function.</span></span>

<span data-ttu-id="2c4cd-121">В следующем примере кода показана функция, которая использует вспомогательные функции перечислителя в C++.</span><span class="sxs-lookup"><span data-stu-id="2c4cd-121">The following code example shows a function that uses enumerator helper functions in C++.</span></span>


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



 

 