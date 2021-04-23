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
# <a name="invoking-actions"></a><span data-ttu-id="30d60-103">Вызов действий</span><span class="sxs-lookup"><span data-stu-id="30d60-103">Invoking Actions</span></span>

<span data-ttu-id="30d60-104">Метод [**иупнпсервице:: инвокеактион**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) позволяет вызывать действия для объектов службы.</span><span class="sxs-lookup"><span data-stu-id="30d60-104">The [**IUPnPService::InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) method allows actions to be invoked on Service objects.</span></span> <span data-ttu-id="30d60-105">Этот метод имеет два входных параметра: имя действия и массив входных аргументов для этого действия.</span><span class="sxs-lookup"><span data-stu-id="30d60-105">This method has two input parameters: the name of an action and an array of input arguments to that action.</span></span> <span data-ttu-id="30d60-106">Метод имеет два параметра:</span><span class="sxs-lookup"><span data-stu-id="30d60-106">The method has two parameters:</span></span>

-   <span data-ttu-id="30d60-107">Параметр один — входной/выходной параметр — массив выходных аргументов для этого действия.</span><span class="sxs-lookup"><span data-stu-id="30d60-107">Parameter one — an input/output parameter: an array of output arguments for that action.</span></span>
-   <span data-ttu-id="30d60-108">Два параметра — выходной параметр — возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="30d60-108">Parameter two — an output parameter: a return value.</span></span>

<span data-ttu-id="30d60-109">Метод вызывает действие на устройстве.</span><span class="sxs-lookup"><span data-stu-id="30d60-109">The method causes the action to be invoked on the device.</span></span> <span data-ttu-id="30d60-110">Устройство создает уведомления о событиях, если действие вызывает изменение переменных состояния устройства.</span><span class="sxs-lookup"><span data-stu-id="30d60-110">The device generates event notifications if the action causes state variables of the device to change.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="30d60-111">Пример VBScript</span><span class="sxs-lookup"><span data-stu-id="30d60-111">VBScript Example</span></span>

<span data-ttu-id="30d60-112">Следующий пример кода VBScript вызывает два действия для объекта службы.</span><span class="sxs-lookup"><span data-stu-id="30d60-112">The following VBScript code example invokes two actions on a Service object.</span></span> <span data-ttu-id="30d60-113">Первое действие, *жеттраккинфо*, принимает один входной аргумент — номер записи.</span><span class="sxs-lookup"><span data-stu-id="30d60-113">The first action, *GetTrackInfo*, takes one input argument, a track number.</span></span> <span data-ttu-id="30d60-114">Действие *жеттраккинфо* возвращает длину пути в качестве возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="30d60-114">The *GetTrackInfo* action returns the track length as the return value.</span></span> <span data-ttu-id="30d60-115">Действие также имеет один выходной аргумент, который содержит заголовок записи, если метод возвращает значение Success.</span><span class="sxs-lookup"><span data-stu-id="30d60-115">The action also has one output argument, which contains the track title if the method returns success.</span></span>

<span data-ttu-id="30d60-116">После вызова действия *жеттраккинфо* в примере вызывается действие воспроизведение, которое не принимает аргументов.</span><span class="sxs-lookup"><span data-stu-id="30d60-116">After invoking the *GetTrackInfo* action, the example invokes the Play action, which takes no arguments.</span></span> <span data-ttu-id="30d60-117">Однако, поскольку для синтаксиса [**инвокеактион**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) требуется массив входных и выходных аргументов, в примере необходимо создать пустой массив, *емптяргс*, без элементов.</span><span class="sxs-lookup"><span data-stu-id="30d60-117">However, because the syntax of [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) requires an array of both input and output arguments, the example must create an empty array, *emptyArgs*, with no elements.</span></span> <span data-ttu-id="30d60-118">В примере этот массив передается **инвокеактион** как для входных, так и для выходных аргументов вместе с именем действия.</span><span class="sxs-lookup"><span data-stu-id="30d60-118">The example passes this array to **InvokeAction** for both the input and output arguments, along with the name of the action.</span></span>


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



## <a name="c-example"></a><span data-ttu-id="30d60-119">Пример C++</span><span class="sxs-lookup"><span data-stu-id="30d60-119">C++ Example</span></span>

<span data-ttu-id="30d60-120">В следующем примере определяется функция C++, которая вызывает действие без аргументов.</span><span class="sxs-lookup"><span data-stu-id="30d60-120">The following example defines a C++ function that invokes an action with no arguments.</span></span> <span data-ttu-id="30d60-121">Так как для [**инвокеактион**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) требуется [**массив SafeArray**](/windows/win32/api/oaidl/ns-oaidl-safearray) передаваемых аргументов, в этом примере создается пустой **массив SafeArray**.</span><span class="sxs-lookup"><span data-stu-id="30d60-121">Because [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) requires a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of arguments to be passed in, this example creates an empty **SAFEARRAY**.</span></span> <span data-ttu-id="30d60-122">Поскольку это действие не возвращает значение или имеет выходные аргументы, в этом примере пропускаются последние два значения [**типа Variant**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) , переданные в **инвокеактион**.</span><span class="sxs-lookup"><span data-stu-id="30d60-122">Since this action does not return a value or have output arguments, this example ignores the last two [**VARIANT**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) values passed to **InvokeAction**.</span></span>

<span data-ttu-id="30d60-123">Устройство создает уведомления о событиях, если действие вызывает изменение переменных состояния устройства.</span><span class="sxs-lookup"><span data-stu-id="30d60-123">The device generates event notifications if the action causes state variables of the device to change.</span></span>


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



<span data-ttu-id="30d60-124">В следующем примере вызывается фиктивное действие *жеттраккинфо* .</span><span class="sxs-lookup"><span data-stu-id="30d60-124">The following example invokes the fictitious *GetTrackInfo* action.</span></span> <span data-ttu-id="30d60-125">Он принимает номер Track в качестве аргумента, возвращает длину пути в виде возвращаемого значения и возвращает заголовок записи в выходном аргументе.</span><span class="sxs-lookup"><span data-stu-id="30d60-125">It takes a track number as an argument, returns the track length as a return value, and returns the track title in an output argument.</span></span> <span data-ttu-id="30d60-126">Код похож на предыдущий пример, за исключением того, что вместо создания пустого [**массива SafeArray**](/windows/win32/api/oaidl/ns-oaidl-safearray) входных аргументов в этом примере вставляется [**вариант**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) , содержащий номер записи.</span><span class="sxs-lookup"><span data-stu-id="30d60-126">The code is similar to the previous example, except that instead of creating an empty [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of input arguments, this example inserts a [**VARIANT**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) that contains the track number.</span></span> <span data-ttu-id="30d60-127">Если [**инвокеактион**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) возвращает значение Success, в этом примере выполняется проверка возвращаемого значения и массива выходных аргументов.</span><span class="sxs-lookup"><span data-stu-id="30d60-127">If [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) returns success, this example examines the return value and the array of output arguments.</span></span>


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



 

 