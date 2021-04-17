---
description: Поддержка регистрации новых функций в системном реестре должна быть указана в новой библиотеке DLL вместе с новой функцией.
ms.assetid: 7a6af325-4891-40db-8d33-c9782bd438e5
title: Регистрация новых функций
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 470541ed9b832ad5eaa914c1a35805dbd861a843
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684328"
---
# <a name="registering-the-new-functionality"></a>Регистрация новых функций

Поддержка регистрации новых функций в системном реестре должна быть указана в новой библиотеке DLL вместе с новой функцией. [Функции поддержки OID](cryptography-functions.md) обеспечивают помощь при регистрации. Regsvr32.exe регистрирует новые функции. Это средство входит в состав Windows.

Новая библиотека DLL должна предоставлять точки входа [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) и [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) для использования Regsvr32.exe. Функции [*CryptoAPI*](../secgloss/c-gly.md) , такие как [**криптрегистероидфунктион**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) или [**криптунрегистероидфунктион**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidfunction), можно использовать в этих точках входа, как показано в следующем примере.


```C++
//  The DllRegisterServer Entry Point
STDAPI DllRegisterServer(void)
{
    if(!CryptRegisterOIDFunction(
         X509_ASN_ENCODING,                  // Encoding type
         CRYPT_OID_ENCODE_OBJECT_FUNC,       // Function name
         szOID_NEW_CERTIFICATE_TYPE,         // OID
         L"NewCert.dll",                     // Dll name
         L"NewCertificateTypeEncodeObject"   // Override function
         ))                                  //   name
       {
         return E_FAIL;
       }
    else
       {
         return S_OK;
       }
}

// The DllUnregisterServer Entry Point
STDAPI DllUnregisterServer(void)
{
    HRESULT     hr = S_OK;

    if(!CryptUnregisterOIDFunction(
          X509_ASN_ENCODING,             // Encoding type
          CRYPT_OID_ENCODE_OBJECT_FUNC,  // Function name
          szOID_NEW_CERTIFICATE_TYPE     // OID
          ))
    {
       if(ERROR_FILE_NOT_FOUND != GetLastError())
               hr = E_FAIL;
    }
    return hr;
}
```



Этот пример должен быть скомпилирован и связан с новой библиотекой DLL. Эти две точки входа вместе с точкой входа функции должны быть экспортированы.

Чтобы установить новые функции на компьютере, запустите Regsvr32.exe из командной строки, указав имя и путь к новой библиотеке DLL. Regsvr32.exe обращается к функции [**криптрегистероидфунктион**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) через точку входа функции [**DllRegisterServer**](/previous-versions/windows/desktop/legacy/aa369359(v=vs.85)) и регистрирует новую функцию и библиотеку DLL.

 

 
