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
# <a name="using-the-credential-cache"></a><span data-ttu-id="234a5-103">Использование кэша учетных данных</span><span class="sxs-lookup"><span data-stu-id="234a5-103">Using the Credential Cache</span></span>

<span data-ttu-id="234a5-104">Media Foundation предоставляет реализацию интерфейса [**имфнеткредентиалкаче**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="234a5-104">Media Foundation provides a default implementation of the [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) interface.</span></span> <span data-ttu-id="234a5-105">Приложение, реализующее интерфейс [**имфнеткредентиалманажер**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) , может использовать объект кэша учетных данных по умолчанию для хранения учетных данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="234a5-105">An application that implements the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface can use the default credential cache object to store the user's credentials.</span></span>

<span data-ttu-id="234a5-106">Чтобы создать объект кэша учетных данных по умолчанию, вызовите функцию [**мфкреатекредентиалкаче**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) .</span><span class="sxs-lookup"><span data-stu-id="234a5-106">To create the default credential cache object, call the [**MFCreateCredentialCache**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) function.</span></span>


```C++
HRESULT hr = S_OK;
IMFNetCredentialCache *pCredentialCache = NULL;
hr = MFCreateCredentialCache(&pCredentialCache);
```



<span data-ttu-id="234a5-107">После создания кэша учетных данных приложение может использовать следующие методы для получения объекта учетных данных, установки учетных данных пользователя и указания параметров кэширования.</span><span class="sxs-lookup"><span data-stu-id="234a5-107">After the credential cache is created, the application can use the following methods to get a credential object, set user credentials, and specify the caching options.</span></span>

-   <span data-ttu-id="234a5-108">Чтобы получить объект учетных данных для URL-адреса, вызовите [**имфнеткредентиалкаче:: Credential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential).</span><span class="sxs-lookup"><span data-stu-id="234a5-108">To get the credential object for a URL, call [**IMFNetCredentialCache::GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential).</span></span>

    ```C++
    hr = pCredentialCache-> GetCredential(
            pszUrl,
            pszRealm,
            dwAuthenticationFlags,
            &pCredential,
            &dwRequirementsFlags);
    ```

    

    <span data-ttu-id="234a5-109">Если учетные данные для указанного URL-адреса не существуют в кэше учетных данных, то при выполнении инструкции [**Credential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) создается новый объект учетных данных с пустыми значениями имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="234a5-109">If the credentials for the specified URL do not exist in the credential cache, [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) creates a new credential object with empty user name and password values.</span></span>

-   <span data-ttu-id="234a5-110">Чтобы задать имя пользователя и пароль для объекта учетных данных, вызовите метод [**имфнеткредентиал:: SetUser**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) и [**Имфнеткредентиал:: SetPassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword).</span><span class="sxs-lookup"><span data-stu-id="234a5-110">To set the user name and password on the credential object, call [**IMFNetCredential::SetUser**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) and [**IMFNetCredential::SetPassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword).</span></span>
-   <span data-ttu-id="234a5-111">Чтобы задать параметры кэширования для объекта учетных данных, вызовите метод [**имфнеткредентиалкаче:: сетусероптионс**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions).</span><span class="sxs-lookup"><span data-stu-id="234a5-111">To set the caching options on the credential object, call [**IMFNetCredentialCache::SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions).</span></span>

    ```C++
    hr = pCredentialCache-> SetUserOptions( 
            pCredentialCache,
            MFNET_CREDENTIAL_SAVE);
    ```

    

    <span data-ttu-id="234a5-112">Значения параметров *двоптионсфлагс* определены в перечислении [**мфнеткредентиалоптионс**](/windows/desktop/api/mfidl/ne-mfidl-mfnetcredentialoptions) .</span><span class="sxs-lookup"><span data-stu-id="234a5-112">The *dwOptionsFlags* parameter values are defined in the [**MFNetCredentialOptions**](/windows/desktop/api/mfidl/ne-mfidl-mfnetcredentialoptions) enumeration.</span></span> <span data-ttu-id="234a5-113">Чтобы сохранить учетные данные пользователя для URL-адреса в постоянном хранилище, установите \_ флаг сохранения учетных данных мфнет \_ .</span><span class="sxs-lookup"><span data-stu-id="234a5-113">To save user credentials for a URL in a persistent storage, set the MFNET\_CREDENTIAL\_SAVE flag.</span></span> <span data-ttu-id="234a5-114">Если вызов [**сетусероптионс**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) завершается успешно, то при последующем вызове метода [**Credential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) выполняется поиск учетных данных в постоянном хранилище.</span><span class="sxs-lookup"><span data-stu-id="234a5-114">If the [**SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) call completes successfully, then the subsequent call to [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) searches for the credentials in the persistent storage.</span></span> <span data-ttu-id="234a5-115">Если совпадение найдено, этот метод возвращает указатель на объект учетных данных, содержащий сведения.</span><span class="sxs-lookup"><span data-stu-id="234a5-115">If a match is found, this method returns a pointer to the credential object that contains the information.</span></span>

    <span data-ttu-id="234a5-116">По умолчанию учетные данные пользователя, передаваемые по сети, шифруются.</span><span class="sxs-lookup"><span data-stu-id="234a5-116">By default, user credentials sent over the network are encrypted.</span></span> <span data-ttu-id="234a5-117">Чтобы изменить это значение на незашифрованный текст, установите \_ флаг мфнет Credentials \_ allow \_ clear \_ Text.</span><span class="sxs-lookup"><span data-stu-id="234a5-117">To change this to clear text, set the MFNET\_CREDENTIAL\_ALLOW\_CLEAR\_TEXT flag.</span></span>

    <span data-ttu-id="234a5-118">Чтобы удалить сведения из реестра, вызовите метод [**Credential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) , чтобы получить объект учетных данных, а затем вызовите [**сетусероптион**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) и задайте для *двоптионсфлагс* мфнет \_ Credential \_ не \_ Cache.</span><span class="sxs-lookup"><span data-stu-id="234a5-118">To remove information from the registry, call [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) to get the credential object, and then call [**SetUserOption**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) and set *dwOptionsFlags* to MFNET\_CREDENTIAL\_DONT\_CACHE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="234a5-119">См. также</span><span class="sxs-lookup"><span data-stu-id="234a5-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="234a5-120">Проверка подлинности источника сети</span><span class="sxs-lookup"><span data-stu-id="234a5-120">Network Source Authentication</span></span>](network-source-authentication.md)
</dt> </dl>

 

 



