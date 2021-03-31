---
description: Пароль автоматического входа должен быть защищен с помощью функции Лсастореприватедата.
ms.assetid: 7bd4d725-de17-4801-bd06-8d47a777409d
title: Защита пароля автоматического входа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25508af4de64554e664426db3e786a1eca34579b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999235"
---
# <a name="protecting-the-automatic-logon-password"></a>Защита пароля автоматического входа

Пароль автоматического входа должен быть защищен с помощью функции [**лсастореприватедата**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) .

В следующем примере показано, как защитить пароль автоматического входа. Пример извлекает маркер объекта [**политики**](../secmgmt/policy-object.md) , вызывая функцию [**лсаопенполици**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopenpolicy) . Дополнительные сведения об объекте **политики** и дескрипторах объектов **политики** см. в разделе объект **политики** и [Открытие дескриптора объекта политики](../secmgmt/opening-a-policy-object-handle.md)соответственно. Затем в примере задается защищенный пароль путем вызова функции [**лсастореприватедата**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) . Обратите внимание, что если вызывающий объект передает значение **null** для защищенного пароля, код очищает существующий защищенный пароль. Перед выходом код закрывает маркер объекта **политики** .


```C++
#include <windows.h>
#include <stdio.h>

DWORD UpdateDefaultPassword(WCHAR * pwszSecret)
{

    LSA_OBJECT_ATTRIBUTES ObjectAttributes;
    LSA_HANDLE LsaPolicyHandle = NULL;

    LSA_UNICODE_STRING lusSecretName;
    LSA_UNICODE_STRING lusSecretData;
    USHORT SecretNameLength;
    USHORT SecretDataLength;

    NTSTATUS ntsResult = STATUS_SUCCESS;
    DWORD dwRetCode = ERROR_SUCCESS;

    //  Object attributes are reserved, so initialize to zeros.
    ZeroMemory(&ObjectAttributes, sizeof(ObjectAttributes));

    //  Get a handle to the Policy object.
    ntsResult = LsaOpenPolicy(
        NULL,    // local machine
        &ObjectAttributes, 
        POLICY_CREATE_SECRET,
        &LsaPolicyHandle);

    if( STATUS_SUCCESS != ntsResult )
    {
        //  An error occurred. Display it as a win32 error code.
        dwRetCode = LsaNtStatusToWinError(ntsResult);
        wprintf(L"Failed call to LsaOpenPolicy %lu\n", dwRetCode);
        return dwRetCode;
    } 

    //  Initialize an LSA_UNICODE_STRING for the name of the
    //  private data ("DefaultPassword").
    SecretNameLength = (USHORT)wcslen(L"DefaultPassword");
    lusSecretName.Buffer = L"DefaultPassword";
    lusSecretName.Length = SecretNameLength * sizeof(WCHAR);
    lusSecretName.MaximumLength =
        (SecretNameLength+1) * sizeof(WCHAR);

    //  If the pwszSecret parameter is NULL, then clear the secret.
    if( NULL == pwszSecret )
    {
        wprintf(L"Clearing the secret...\n");
        ntsResult = LsaStorePrivateData(
            LsaPolicyHandle,
            &lusSecretName,
            NULL);
        dwRetCode = LsaNtStatusToWinError(ntsResult);
    }
    else
    {
        wprintf(L"Setting the secret...\n");
        //  Initialize an LSA_UNICODE_STRING for the value
        //  of the private data. 
        SecretDataLength = (USHORT)wcslen(pwszSecret);
        lusSecretData.Buffer = pwszSecret;
        lusSecretData.Length = SecretDataLength * sizeof(WCHAR);
        lusSecretData.MaximumLength =
            (SecretDataLength+1) * sizeof(WCHAR);
        ntsResult = LsaStorePrivateData(
            LsaPolicyHandle,
            &lusSecretName,
            &lusSecretData);
        dwRetCode = LsaNtStatusToWinError(ntsResult);
    }

    LsaClose(LsaPolicyHandle);

    if (dwRetCode != ERROR_SUCCESS)
        wprintf(L"Failed call to LsaStorePrivateData %lu\n",
            dwRetCode);
    
    return dwRetCode;

}

```



Обратите внимание, что если Winlogon не может найти пароль, хранящийся в функции [**лсастореприватедата**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) , он будет использовать значение **DefaultPassword** ключа Winlogon (если оно существует) для пароля автоматического входа.

Дополнительные сведения об автоматическом входе и разделе реестра Winlogon см. в разделе [MSGina.dll Features](msgina-dll-features.md).

Дополнительные сведения о защите паролей см. в разделе [обработка паролей](../secbp/handling-passwords.md).

 

 
