---
description: Чтобы использовать API платформы оценки WaaS, создайте экземпляр интерфейса Иваасассессор, а затем вызовите метод Жетосупдатеассессмент.
ms.assetid: 810D4057-8319-4B9B-9098-CD7987CB292C
title: Использование платформы оценки WaaS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08401222b11036047a6c03e98cccaa9dc65e6f6a7cf39470480479c217549d57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118884237"
---
# <a name="using-the-waas-assessment-platform"></a>Использование платформы оценки WaaS

Чтобы использовать API платформы оценки WaaS, создайте экземпляр интерфейса [**иваасассессор**](/windows/desktop/api/waasapi/nn-waasapi-iwaasassessor) , а затем вызовите метод [**жетосупдатеассессмент**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) . При успешном выполнении параметр *result* выводит объект [**осупдатеассессмент**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) , который будет содержать соответствующие сведения.

В следующем примере кода показано, как получить оценку ОС из локальной системы с помощью метода Иваасассессор. Жетосупдатеассессмент.


```C++
//
// Copyright (c) Microsoft Corporation.  All rights reserved.
//
#include <windows.h>
#include <tchar.h>
#include <oaidl.h>
#include <atlbase.h>
#include <iostream>
#include <WaaSAPI.h>
#include <WaaSAPITypes.h>

using namespace std;

void __cdecl main(int argc, char** argv)
{
    HRESULT hr = S_OK;
    CComPtr<IWaaSAssessor> assessment;
    OSUpdateAssessment result;
    hr = CoInitialize(NULL);
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(
                __uuidof(WaaSAssessor),               // rclsid
                NULL,                                   // pUnkOuter
                CLSCTX_INPROC_SERVER,                   // dwClsContext
                __uuidof(IWaaSAssessor),              // riid
                (LPVOID*)&assessment);                  // ppv
        if (SUCCEEDED(hr))
        {
            hr = assessment->GetOSUpdateAssessment(&result);
            if (SUCCEEDED(hr))
            {
                wcout << L"End of Support:" << result.isEndOfSupport << endl;
                wcout << L"Up to date:" << result.assessmentForUpToDate.status << endl;
                wcout << L"Current:" << result.assessmentForCurrent.status << endl;
                wcout << L"Up to Date Days Behind:" << result.assessmentForUpToDate.daysOutOfDate << endl;
                wcout << L"Current Days Behind:" << result.assessmentForCurrent.daysOutOfDate << endl;
                wcout << L"Up to Date Impact:" << result.assessmentForUpToDate.impact << endl;
                wcout << L"Current Impact:" << result.assessmentForCurrent.impact << endl;
            }
            else
            {
                wcout << L"Assessment Failed hr = " << hr << endl;
            }
        }
        else
        {
            wcout << L"CoCreateInstance Failed hr = " << hr << endl;
        }
    }
    else
    {
        wcout << L"CoInitialize Failed hr = " << hr << endl;
    }
}
```



 

 



