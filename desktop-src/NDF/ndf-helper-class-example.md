---
title: Расширение класса поддержки NDF
description: В этом примере показано, как реализовать функции диагностики и восстановления NDF.
ms.assetid: 18e66d09-e565-4b86-8bc3-600f2159a4bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1fd8fd7683aded0573034ffec56097256093c61e2bb0f9ec2e7bcd353ff8d3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802114"
---
# <a name="ndf-helper-class-extension"></a>Расширение класса поддержки NDF

В этом примере показано, как реализовать функции диагностики и восстановления NDF. В этом примере для поддержания работоспособности системы должен существовать важный файл конфигурации. Таким образом, проблема заключается в том, чтобы определить, существует ли файл. В противном случае система будет неработоспособна, и диагностика проблемы будет устранена с помощью NDF. Восстановление предназначено для повторного создания отсутствующего файла.

Для диагностики и устранения проблемы необходимо использовать четыре метода [**инетдиагхелпер**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) : [**Initialize**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-initialize), [**ловхеалс**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth), [**жетрепаиринфо**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getrepairinfo)и [**Repair**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-repair).

## <a name="initializing-the-helper-class"></a>Инициализация вспомогательного класса

Инициализируйте и извлеките имя файла для поиска. Это имя файла передается во время диагностики в качестве вспомогательного атрибута с именем filename.


```C++
#include <windows.h>
//utility function to simplify string allocation and copies, user throughout example
HRESULT 
StringCchCopyWithAlloc (
    PWSTR* Dest, 
    size_t cchMaxLen,
    in PCWSTR Src)
{
    if (NULL == Dest || NULL == Src || cchMaxLen > USHRT_MAX)
    {
        return E_INVALIDARG;
    }
    size_t cchSize = 0;

    HRESULT hr = StringCchLength(Src, cchMaxLen - 1, &cchSize); 
    if (FAILED(hr))
    {
        return hr;
    }

    size_t cbSize = (cchSize + 1)*sizeof(WCHAR);
    *Dest = (PWSTR) CoTaskMemAlloc(cbSize);
    if (NULL == *Dest)
    {
        return E_OUTOFMEMORY;
    }
    SecureZeroMemory(*Dest, cbSize);

    return StringCchCopy((STRSAFE_LPWSTR)*Dest, cchSize + 1, Src);    
}

HRESULT SimpleFileHelperClass::Initialize(
        /* [in] */ ULONG celt,
        /* [size_is][in] */ HELPER_ATTRIBUTE rgAttributes[  ])
{
    if(celt < 1)
    {
        return E_INVALIDARG;
    }
    if(rgAttributes == NULL)
    {
        return E_INVALIDARG; 
    }
    else
    {
        //verify the attribute is named as expected
        if (wcscmp(rgAttributes[0].pwszName, L"filename")==0)
        {
            //copy the attribute to member variable
            return StringCchCopyWithAlloc(&m_pwszTestFile, MAX_PATH, 
                    rgAttributes[0].PWStr);
        } else {
            //the attribute isn't named as expected
            return E_INVALIDARG;
        }
    }
}

```



## <a name="checking-on-the-files-existence"></a>Проверка существования файла

Метод [**ловхеалс**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) используется для проверки существования файла. Если файл существует, состояние диагностики — " **DS \_ отклонено**", что означает, что ничего не происходит. Если файл не найден, состояние диагностики — " **DS \_ подтверждено**".


```C++
#include <windows.h>

HRESULT SimpleFileHelperClass::LowHealth( 
            /* [unique][string][in] */ LPCWSTR pwszInstanceDescription,
            /* [string][out] */ LPWSTR *ppwszDescription,
            /* [out] */ long *pDeferredTime,
            /* [out] */ DIAGNOSIS_STATUS *pStatus) 

{
    HANDLE hFile = NULL;
    LPWSTR pwszDiagString=NULL;
    // does the file already exist?
    hFile = CreateFile(
        m_pwszTestFile, 
        GENERIC_READ, 
        0, 
        NULL, 
        OPEN_EXISTING, 
        FILE_ATTRIBUTE_NORMAL, 
        NULL);

    if(INVALID_HANDLE_VALUE == hFile)
    { 
        // alloc and set the diagnosis description and status
        HRESULT hr = StringCchCopyWithAlloc(&pwszDiagString, MAX_PATH, 
                    L"The file was deleted.");
        if (FAILED(hr))
        {
            return hr;
        }
  
        *ppwszDescription = pwszDiagString;
        *pStatus = DS_CONFIRMED;
        return S_OK;
    }
    CloseHandle(hFile); 
    
    //the file exists
    *pStatus = DS_REJECTED;
    return S_OK;
}
```



## <a name="determining-the-repair-action"></a>Определение действия по восстановлению

Если [**ловхеалс**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) возвращает **DS \_**, [**жетрепаиринфо**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getrepairinfo) реализуется для определения соответствующего действия по восстановлению. В этом примере это означает повторное создание файла.


```C++
#include <windows.h>

HRESULT  
SimpleFileHelperClass::GetRepairInfo( 
            /* [in] */ PROBLEM_TYPE problem,
            /* [out] */ ULONG *pcelt,
            /* [size_is][size_is][out] */ RepairInfo **ppInfo)
{
    HRESULT hr=S_OK;
    RepairInfo* pRepair = (RepairInfo *)CoTaskMemAlloc(sizeof(RepairInfo));
    if (pRepair == NULL) {
        return E_OUTOFMEMORY;
    }
    SecureZeroMemory(pRepair,sizeof(RepairInfo));

    // set the repair description and class name
    hr = StringCchCopyWithAlloc(&pRepair->pwszClassName, MAX_PATH,
                L"SimpleFileHelperClass");
    if (FAILED(hr))
    {
        goto Error;
    }

    hr = StringCchCopyWithAlloc(&pRepair->pwszDescription, MAX_PATH, 
                L"Low Health Repair");
    if (FAILED(hr))
    {
        goto Error;
    }
  
    // set the resolution GUID and cost
    pRepair->guid = ID_LowHealthRepair;
    pRepair->cost = 0;
    // set repair status flags
    pRepair->sidType = WinWorldSid;
    pRepair->scope = RS_SYSTEM;
    pRepair->risk = RR_NORISK;
    pRepair->flags |= DF_IMPERSONATION; //impersonate the user when repairing
    pRepair->UiInfo.type = UIT_NONE;
    
    //pass back the repair
    *ppInfo = pRepair; 
    *pcelt = 1; //number of repairs

    return S_OK;

Error:
    if(pRepair){
        if(pRepair->pwszClassName){
            CoTaskMemFree(pRepair->pwszClassName);
        }
        if(pRepair->pwszDescription){
            CoTaskMemFree(pRepair->pwszDescription);
        }
    }
    return hr;
}

```



## <a name="repairing-the-problem"></a>Устранение проблемы

Пользователю предоставляются параметры исправления, возвращаемые [**жетрепаиринфо**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getrepairinfo), если только не существует только один вариант восстановления. в этом случае он выполняется автоматически. Метод [**Repair**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-repair) вызывается с соответствующей структурой [**репаиринфо**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) , чтобы можно было восстановить файл конфигурации.


```C++
#include <windows.h>

HRESULT  
SimpleFileHelperClass::Repair( 
            /* [in] */ RepairInfo *pInfo,
            /* [out] */ long *pDeferredTime,
            /* [out] */ REPAIR_STATUS *pStatus)
{
    //verify expected repair was requested
    if(IsEqualGUID(ID_LowHealthRepair, pInfo->guid)){
        HANDLE hFile = NULL;
        hFile = CreateFile(m_pwszTestFile, 
                                GENERIC_WRITE, 
                                0, 
                                NULL, 
                                CREATE_ALWAYS,
                                FILE_ATTRIBUTE_NORMAL, 
                                NULL);
        if(INVALID_HANDLE_VALUE == hFile)
        {
            // repair failed
            *pStatus = RS_UNREPAIRED;
            return HRESULT_FROM_WIN32(GetLastError());
        }
        CloseHandle(hFile);
        
        // repair succeeded
        *pStatus = RS_REPAIRED;
    } else {
        return E_INVALIDARG; //unkown repair passed in
    }
    return S_OK;
}
```



 

 




