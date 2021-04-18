---
description: Использование кэша учетных данных
ms.assetid: b58d0a6e-ecae-48a1-a3af-d4246caa272b
title: Использование кэша учетных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d512d0bab8f45f50a587e3c8eda2a73c4832685f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719420"
---
# <a name="using-the-credential-cache"></a>Использование кэша учетных данных

Media Foundation предоставляет реализацию интерфейса [**имфнеткредентиалкаче**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) по умолчанию. Приложение, реализующее интерфейс [**имфнеткредентиалманажер**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) , может использовать объект кэша учетных данных по умолчанию для хранения учетных данных пользователя.

Чтобы создать объект кэша учетных данных по умолчанию, вызовите функцию [**мфкреатекредентиалкаче**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) .


```C++
HRESULT hr = S_OK;
IMFNetCredentialCache *pCredentialCache = NULL;
hr = MFCreateCredentialCache(&pCredentialCache);
```



После создания кэша учетных данных приложение может использовать следующие методы для получения объекта учетных данных, установки учетных данных пользователя и указания параметров кэширования.

-   Чтобы получить объект учетных данных для URL-адреса, вызовите [**имфнеткредентиалкаче:: Credential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential).

    ```C++
    hr = pCredentialCache-> GetCredential(
            pszUrl,
            pszRealm,
            dwAuthenticationFlags,
            &pCredential,
            &dwRequirementsFlags);
    ```

    

    Если учетные данные для указанного URL-адреса не существуют в кэше учетных данных, то при выполнении инструкции [**Credential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) создается новый объект учетных данных с пустыми значениями имени пользователя и пароля.

-   Чтобы задать имя пользователя и пароль для объекта учетных данных, вызовите метод [**имфнеткредентиал:: SetUser**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) и [**Имфнеткредентиал:: SetPassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword).
-   Чтобы задать параметры кэширования для объекта учетных данных, вызовите метод [**имфнеткредентиалкаче:: сетусероптионс**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions).

    ```C++
    hr = pCredentialCache-> SetUserOptions( 
            pCredentialCache,
            MFNET_CREDENTIAL_SAVE);
    ```

    

    Значения параметров *двоптионсфлагс* определены в перечислении [**мфнеткредентиалоптионс**](/windows/desktop/api/mfidl/ne-mfidl-mfnetcredentialoptions) . Чтобы сохранить учетные данные пользователя для URL-адреса в постоянном хранилище, установите \_ флаг сохранения учетных данных мфнет \_ . Если вызов [**сетусероптионс**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) завершается успешно, то при последующем вызове метода [**Credential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) выполняется поиск учетных данных в постоянном хранилище. Если совпадение найдено, этот метод возвращает указатель на объект учетных данных, содержащий сведения.

    По умолчанию учетные данные пользователя, передаваемые по сети, шифруются. Чтобы изменить это значение на незашифрованный текст, установите \_ флаг мфнет Credentials \_ allow \_ clear \_ Text.

    Чтобы удалить сведения из реестра, вызовите метод [**Credential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) , чтобы получить объект учетных данных, а затем вызовите [**сетусероптион**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) и задайте для *двоптионсфлагс* мфнет \_ Credential \_ не \_ Cache.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Проверка подлинности источника сети](network-source-authentication.md)
</dt> </dl>

 

 



