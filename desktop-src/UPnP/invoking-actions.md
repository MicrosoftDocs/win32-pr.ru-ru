---
title: Вызов действий
description: Метод Иупнпсервице Инвокеактион позволяет вызывать действия для объектов службы.
ms.assetid: 671e9280-5ead-43f2-bb6b-12792a6a4487
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc7550575281681f3f533db90ef1c1034dbaa085
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413405"
---
# <a name="invoking-actions"></a>Вызов действий

Метод [**иупнпсервице:: инвокеактион**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) позволяет вызывать действия для объектов службы. Этот метод имеет два входных параметра: имя действия и массив входных аргументов для этого действия. Метод имеет два параметра:

-   Параметр один — входной/выходной параметр — массив выходных аргументов для этого действия.
-   Два параметра — выходной параметр — возвращаемое значение.

Метод вызывает действие на устройстве. Устройство создает уведомления о событиях, если действие вызывает изменение переменных состояния устройства.

## <a name="vbscript-example"></a>Пример VBScript

Следующий пример кода VBScript вызывает два действия для объекта службы. Первое действие, *жеттраккинфо*, принимает один входной аргумент — номер записи. Действие *жеттраккинфо* возвращает длину пути в качестве возвращаемого значения. Действие также имеет один выходной аргумент, который содержит заголовок записи, если метод возвращает значение Success.

После вызова действия *жеттраккинфо* в примере вызывается действие воспроизведение, которое не принимает аргументов. Однако, поскольку для синтаксиса [**инвокеактион**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) требуется массив входных и выходных аргументов, в примере необходимо создать пустой массив, *емптяргс*, без элементов. В примере этот массив передается **инвокеактион** как для входных, так и для выходных аргументов вместе с именем действия.


```VB
Dim returnVal
Dim outArgs(1)
Dim args(1)
args(0) = 3
returnVal = service.InvokeAction("GetTrackInfo", args, outArgs)
'return Val now contains the track length
'and outArgs(0) contains the track title
Dim emptyArgs(0)
returnVal = service.InvokeAction("Play", emptyArgs, emptyArgs)
'returnVal indicates if the action was successful
```



## <a name="c-example"></a>Пример C++

В следующем примере определяется функция C++, которая вызывает действие без аргументов. Так как для [**инвокеактион**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) требуется [**массив SafeArray**](/windows/win32/api/oaidl/ns-oaidl-safearray) передаваемых аргументов, в этом примере создается пустой **массив SafeArray**. Поскольку это действие не возвращает значение или имеет выходные аргументы, в этом примере пропускаются последние два значения [**типа Variant**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) , переданные в **инвокеактион**.

Устройство создает уведомления о событиях, если действие вызывает изменение переменных состояния устройства.


```C++
#include <windows.h>
#include <upnp.h>
#include <iostream>
#include <iomanip>

#pragma comment(lib, "oleaut32.lib")

using namespace std;

void InvokePlay(IUPnPService * pService)
{
    HRESULT hr;
    BSTR bstrActionName;

    bstrActionName = SysAllocString(L"Play");

    if (bstrActionName)
    {
        SAFEARRAYBOUND  rgsaBound[1];
        SAFEARRAY       * psa = NULL;

        rgsaBound[0].lLbound = 0;
        rgsaBound[0].cElements = 0;

        psa = SafeArrayCreate(VT_VARIANT, 1, rgsaBound);

        if (psa)
        {
            LONG    lStatus;
            VARIANT varInArgs;

            VariantInit(&varInArgs);

            varInArgs.vt = VT_VARIANT | VT_ARRAY;

            V_ARRAY(&varInArgs) = psa;

            hr = pService->InvokeAction(bstrActionName,
                                        varInArgs,
                                        NULL,
                                        NULL);

            if (SUCCEEDED(hr))
            {
                wcout << L"Action invoked successfully\n"; 
            }
            else
            {
                wcerr << L"Failed to invoke action - HRESULT 0x" 
                      << setbase(16)
                      << hr << L"\n";                        

            }                                   

            SafeArrayDestroy(psa);
        }
        else
        {
            wcerr << L"Failed to create safe array\n";
        }   

        SysFreeString(bstrActionName);
    }
    else
    {
        wcerr << L"Failed to allocate action name string\n";
    }
}
```



В следующем примере вызывается фиктивное действие *жеттраккинфо* . Он принимает номер Track в качестве аргумента, возвращает длину пути в виде возвращаемого значения и возвращает заголовок записи в выходном аргументе. Код похож на предыдущий пример, за исключением того, что вместо создания пустого [**массива SafeArray**](/windows/win32/api/oaidl/ns-oaidl-safearray) входных аргументов в этом примере вставляется [**вариант**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) , содержащий номер записи. Если [**инвокеактион**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) возвращает значение Success, в этом примере выполняется проверка возвращаемого значения и массива выходных аргументов.


```C++
#include <windows.h>
#include <upnp.h>
#include <iostream>
#include <iomanip>

#pragma comment(lib, "oleaut32.lib")

using namespace std;

void InvokeGetTrackInfo(IUPnPService * pService)
{
    HRESULT hr;
    BSTR bstrActionName;

    bstrActionName = SysAllocString(L"GetTrackInfo");

    if (bstrActionName)
    {
        SAFEARRAYBOUND  rgsaBound[1];
        SAFEARRAY       * psa = NULL;

        rgsaBound[0].lLbound = 0;
        rgsaBound[0].cElements = 1;

        psa = SafeArrayCreate(VT_VARIANT, 1, rgsaBound);

        if (psa)
        {
            long rgIndices[1];
            VARIANT varTrackNum;

            rgIndices[0] = 0;
            VariantInit(&varTrackNum);

            varTrackNum.vt = VT_I4;
            // An arbitrary track is chosen (track 3)
            V_I4(&varTrackNum) = 3;

            hr = SafeArrayPutElement(psa,
                                     rgIndices,
                                     (void *) &varTrackNum);

            VariantClear(&varTrackNum);

            if (SUCCEEDED(hr))
            {            
                LONG    lStatus;
                VARIANT varInArgs;
                VARIANT varOutArgs;
                VARIANT varReturnVal;

                VariantInit(&varInArgs);
                VariantInit(&varOutArgs);
                VariantInit(&varReturnVal);

                varInArgs.vt = VT_VARIANT | VT_ARRAY;

                V_ARRAY(&varInArgs) = psa;

                hr = pService->InvokeAction(bstrActionName,
                                            varInArgs,
                                            &varOutArgs,
                                            &varReturnVal);

                if (SUCCEEDED(hr))
                {
                    SAFEARRAY * psaOutArgs = NULL;
                    VARIANT   varTrackTitle;

                    psaOutArgs = V_ARRAY(&varOutArgs);
                    VariantInit(&varTrackTitle);

                    rgIndices[0] = 0;
                    hr = SafeArrayGetElement(psaOutArgs,
                                             rgIndices,
                                             (void *)&varTrackTitle);                    

                    if (SUCCEEDED(hr))
                    {                    
                        wcout << L"Action invoked successfully\n"
                              << L"\tTrack Length == " 
                              << V_I4(&varReturnVal) << L"\n"
                              << L"\tTrack Title == " 
                              << V_BSTR(&varTrackTitle) << L"\n";
                    }
                    else
                    {
                        wcerr << L"Failed to get array element -"
                              << L" HRESULT 0x" 
                              << setbase(16)
                              << hr << L"\n";                        
                    }

                    VariantClear(&varTrackTitle);
                    VariantClear(&varReturnVal);
                    VariantClear(&varOutArgs);
                }
                else
                {
                    wcerr << L"Failed to invoke action - HRESULT 0x" 
                          << setbase(16)
                          << hr << L"\n";                        
                }                                   
            }
            else
            {
                wcerr << L"Failed to insert argument into array - "
                      << L"HRESULT 0x" 
                      << setbase(16)
                      << hr << L"\n";                        
            }

            SafeArrayDestroy(psa);
        }
        else
        {
            wcerr << L"Failed to create safe array\n";
        }   

        SysFreeString(bstrActionName);
    }
    else
    {
        wcerr << L"Failed to allocate action name string\n";
    }
}
```



 

 