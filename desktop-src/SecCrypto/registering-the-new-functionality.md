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
# <a name="registering-the-new-functionality"></a><span data-ttu-id="f7df9-103">Регистрация новых функций</span><span class="sxs-lookup"><span data-stu-id="f7df9-103">Registering the New Functionality</span></span>

<span data-ttu-id="f7df9-104">Поддержка регистрации новых функций в системном реестре должна быть указана в новой библиотеке DLL вместе с новой функцией.</span><span class="sxs-lookup"><span data-stu-id="f7df9-104">Support for registering the new functionality in a system registry must be provided in the new DLL along with the new function.</span></span> <span data-ttu-id="f7df9-105">[Функции поддержки OID](cryptography-functions.md) обеспечивают помощь при регистрации.</span><span class="sxs-lookup"><span data-stu-id="f7df9-105">[OID Support Functions](cryptography-functions.md) provide assistance with this registration.</span></span> <span data-ttu-id="f7df9-106">Regsvr32.exe регистрирует новые функции.</span><span class="sxs-lookup"><span data-stu-id="f7df9-106">Regsvr32.exe registers new functions.</span></span> <span data-ttu-id="f7df9-107">Это средство входит в состав Windows.</span><span class="sxs-lookup"><span data-stu-id="f7df9-107">This tool is included with Windows.</span></span>

<span data-ttu-id="f7df9-108">Новая библиотека DLL должна предоставлять точки входа [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) и [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) для использования Regsvr32.exe.</span><span class="sxs-lookup"><span data-stu-id="f7df9-108">The new DLL must provide [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) entry points for use by Regsvr32.exe.</span></span> <span data-ttu-id="f7df9-109">Функции [*CryptoAPI*](../secgloss/c-gly.md) , такие как [**криптрегистероидфунктион**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) или [**криптунрегистероидфунктион**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidfunction), можно использовать в этих точках входа, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="f7df9-109">[*CryptoAPI*](../secgloss/c-gly.md) functions, such as [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) or [**CryptUnregisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidfunction), can be used within these entry points, as shown in the following example.</span></span>


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



<span data-ttu-id="f7df9-110">Этот пример должен быть скомпилирован и связан с новой библиотекой DLL.</span><span class="sxs-lookup"><span data-stu-id="f7df9-110">This example must be compiled and linked into the new DLL.</span></span> <span data-ttu-id="f7df9-111">Эти две точки входа вместе с точкой входа функции должны быть экспортированы.</span><span class="sxs-lookup"><span data-stu-id="f7df9-111">These two entry points, along with the function entry point, must be exported.</span></span>

<span data-ttu-id="f7df9-112">Чтобы установить новые функции на компьютере, запустите Regsvr32.exe из командной строки, указав имя и путь к новой библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="f7df9-112">To install the new functionality on a computer, run Regsvr32.exe from a command prompt, specifying the name and path of the new DLL.</span></span> <span data-ttu-id="f7df9-113">Regsvr32.exe обращается к функции [**криптрегистероидфунктион**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) через точку входа функции [**DllRegisterServer**](/previous-versions/windows/desktop/legacy/aa369359(v=vs.85)) и регистрирует новую функцию и библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="f7df9-113">Regsvr32.exe accesses the [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) function through the [**DllRegisterServer**](/previous-versions/windows/desktop/legacy/aa369359(v=vs.85)) function entry point and registers the new function and DLL.</span></span>

 

 
