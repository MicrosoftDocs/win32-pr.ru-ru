---
description: Регистрация подключаемого терминала может быть вызвана функцией DllRegisterServer компонента, который реализует терминал. Следующий пример кода можно вставить в код для DllRegisterServer.
ms.assetid: d88a8d2c-4b05-4c31-928f-0baf1dbc218c
title: Регистрация подключаемого терминала
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7be84d9e2063c28a320c49d5249ea6434094b9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674471"
---
# <a name="register-a-pluggable-terminal"></a><span data-ttu-id="2c04e-104">Регистрация подключаемого терминала</span><span class="sxs-lookup"><span data-stu-id="2c04e-104">Register a Pluggable Terminal</span></span>

<span data-ttu-id="2c04e-105">Регистрация подключаемого терминала может быть вызвана функцией **DllRegisterServer** компонента, который реализует терминал.</span><span class="sxs-lookup"><span data-stu-id="2c04e-105">The registration of a pluggable terminal can be called into the **DllRegisterServer** function of the component that implements the terminal.</span></span> <span data-ttu-id="2c04e-106">Следующий пример кода можно вставить в код для **DllRegisterServer**.</span><span class="sxs-lookup"><span data-stu-id="2c04e-106">The following code example can be put into the code for **DllRegisterServer**.</span></span>

``` syntax
ITPluggableTerminalClassRegistration* pTerminal;
BSTR bstrTerminalSuperclass = SysAllocString(L"{F7438990-D6EB-11d0-82A6-00AA00B5CA1B}");

// If (NULL == bstrTerminalSuperclass) process the error here.

BSTR bstrTerminalClass = SysAllocString(L"{AED6483E-3304-11d2-86F1-006008B0E5D2}");

// If (NULL == bstrTerminalClass) process the error here.

BSTR bstrTerminalCLSID = SysAllocString(L"{E2F7AEF7-4971-11D1-A671-006097C9A2E8}");

// If (NULL == bstrTerminalCLSID) process the error here.

HRESULT hr;
hr = CoCreateInstance( 
    CLSID_PluggableTerminalRegistration,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_ITPluggableTerminalClassRegistration,
    (void**)&pTerminal);

hr = pTerminal->put_TerminalClass( bstrTerminalClass );
// If (hr != S_OK) process the error here. 
pTerminal->put_CLSID( bstrTerminalCLSID );
// If (hr != S_OK) process the error here.
pTerminal->put_Name( ... );
// If (hr != S_OK) process the error here.
pTerminal->put_Company( ... );
// If (hr != S_OK) process the error here.
pTerminal->put_Version( ... );
// If (hr != S_OK) process the error here.
pTerminal->put_Direction( ... );
// If (hr != S_OK) process the error here.
pTerminal->put_MediaTypes( ... );
// If (hr != S_OK) process the error here.
pTerminal->Add( bstrTerminalSuperclass );
// If (hr != S_OK) process the error here.

// Free the memory created by SysAllocString().
SysFreeString(bstrTerminalSuperclass);
SysFreeString(bstrTerminalClass);
SysFreeString(bstrTerminalCLSID);
```

 

 



