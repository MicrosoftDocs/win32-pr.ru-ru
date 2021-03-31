---
description: Следующая процедура содержит краткий обзор процесса сборки.
ms.assetid: a369d4d7-bd4b-4b4d-846e-ad85251e9ffb
title: Создание команды КАТЕГОРИЯХ APDU ISO7816-4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63987f27e74dd30b4520e6e09f27ae716d793d40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263471"
---
# <a name="building-an-iso7816-4-apdu-command"></a>Создание команды КАТЕГОРИЯХ APDU ISO7816-4

Чтобы добавить функциональные возможности для поставщика услуг, необходимо знать, как будет создаваться [*блок данных протокола приложения*](/windows/desktop/SecGloss/a-gly) ISO7816-4 (категориях APDU) в базовых библиотеках DLL поставщика служб. Следующая процедура содержит краткий обзор процесса сборки.

> [!Note]  
> Представленный здесь пример не обязательно должен быть полным. Дополнительные сведения см. в примерах приложений и библиотек DLL.

 

**Создание команды ISO7816-4 КАТЕГОРИЯХ APDU**

1.  Создайте объект [**искардкмд**](iscardcmd.md) и объект [**ISCardISO7816**](iscardiso7816.md) .

    ```C++
    //  Create an ISCardCmd object.
    HRESULT hresult = CoCreateInstance(CLSID_CSCardCmd,
                               NULL,
                               CLSCTX_ALL,
                               IID_ISCardCmd,
                               (LPVOID*) &g_pISCardCmd);
    //  Create an ISCardISO7816 object.
    HRESULT hresult = CoCreateInstance(CLSID_CSCardISO7816,
                               NULL,
                               CLSCTX_ALL,
                               IID_ISCardISO7816,
                               (LPVOID*) &g_pISCardISO7816);
    ```

    

    Интерфейс [**искардкмд**](iscardcmd.md) содержит два буфера **ибитебуффер** . Один буфер содержит собственно командную строку КАТЕГОРИЯХ APDU (а также любые данные для отправки с помощью команды). Другой содержит все сведения ответа, возвращаемые картой после выполнения команды.

2.  Используя эти объекты, создайте допустимую команду ISO7816-4 следующим образом:

    ```C++
    //  Do challenge.
    HRESULT hresult = g_pISCardISO7816->GetChallenge(dwLengthOfChallenge,
                                             &g_pISCardCmd);
    ```

    

    Ниже приведен [**код, используемый в методе**](iscardiso7816-getchallenge.md) метода WebMethod:

    ```C++
    #include <windows.h>

    STDMETHODIMP CSCardISO7816::GetChallenge(IN DWORD dwBytesExpected /*= 0*/,
                                IN OUT LPSCARDCMD *ppCmd)
    {
        //  Locals.
        HRESULT hr = S_OK;
        
        try
        {
            //  Is the ISCardCmd object okay?
            hr = IsSCardCmdValid(ppCmd);
            if (FAILED(hr))
                throw (hr);

            //  Do it.
            hr = (*ppCmd)->BuildCmd(m_byClassId,
                                    (BYTE) INS_GET_CHALLENGE,
                                    (BYTE) INS_NULL,  // P1 = 0x00
                                    (BYTE) INS_NULL,  // P2 = 0x00
                                    NULL,
                                    &dwBytesExpected);
            if (FAILED(hr))
                throw (hr);
        }
    }
    ```

    

    Метод [**ISCardISO7816:: unchallenge**](iscardiso7816-getchallenge.md) использует метод [**Искардкмд:: буилдкмд**](iscardcmd-buildcmd.md) для создания запрошенного категориях APDU. Это делается путем записи соответствующей информации в буфер категориях APDU [**искардкмд**](iscardcmd.md) в следующей инструкции:

    ```C++
    hr = (*ppCmd)->BuildCmd;
    ```

    

3.  С помощью созданного объекта [**искардкмд**](iscardcmd.md) выполните транзакцию с картой, воспримете результаты и продолжайте.

## <a name="expanding-beyond-iso7816-4"></a>Расширение за пределами ISO7816-4

Чтобы расширить процесс сборки или выполнения поставщика услуг, описанный выше, рекомендуется создать новый COM-объект. Этот COM-объект должен поддерживать новый интерфейс, который позволяет создавать команды, отличные от ISO7816-4, и выполнять статистическую обработку интерфейса [**ISCardISO7816**](iscardiso7816.md) .

## <a name="example-of-building-an-iso7816-4-apdu-command"></a>Пример создания команды КАТЕГОРИЯХ APDU ISO7816-4

В следующем примере показан код, используемый в процедуре выше.


```C++
//  Create an ISCardCmd object.
hresult = CoCreateInstance(CLSID_CSCardCmd,
                           NULL,
                           CLSCTX_ALL,
                           IID_ISCardCmd,
                           (LPVOID*) &g_pISCardCmd);
//  Create an ISCardISO7816 object.
hresult = CoCreateInstance(CLSID_CSCardISO7816,
                           NULL,
                           CLSCTX_ALL,
                           IID_ISCardISO7816,
                           (LPVOID*) &g_pISCardISO7816);
//  Do challenge.
hresult = g_pISCardISO7816->GetChallenge(dwLengthOfChallenge,
                                         &g_pISCardCmd);

STDMETHODIMP
CSCardISO7816::GetChallenge(IN DWORD dwBytesExpected /*= 0*/,
                            IN OUT LPSCARDCMD *ppCmd)
{
    //  Locals.
    HRESULT hr = S_OK;
    
    try
    {
        //  Is the ISCardCmd object okay?
        hr = IsSCardCmdValid(ppCmd);
        if (FAILED(hr))
            throw (hr);

        //  Do it.
        hr = (*ppCmd)->BuildCmd(m_byClassId,
                                (BYTE) INS_GET_CHALLENGE,
                                (BYTE) INS_NULL,  // P1 = 0x00
                                (BYTE) INS_NULL,  // P2 = 0x00
                                NULL,
                                &dwBytesExpected);
        if (FAILED(hr))
            throw (hr);
    }
}
```



 

 
