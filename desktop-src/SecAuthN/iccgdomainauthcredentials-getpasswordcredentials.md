---
description: Возвращает учетные данные для проверки подлинности контейнера, не присоединенного к домену, с Active Directory.
title: 'Метод Иккгдомаинаускредентиалс:: Жетпассвордкредентиалс (ккгплугинс. h)'
ms.topic: reference
ms.date: 10/21/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- ICcgDomainAuthCredentials.GetPasswordCredentials
api_type:
- COM
api_location:
- ccgplugins.h
ms.openlocfilehash: abd70a109e491773b374ae32787760d265167baa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721031"
---
# <a name="iccgdomainauthcredentialsgetpasswordcredentials-method"></a><span data-ttu-id="1a16c-103">Метод Иккгдомаинаускредентиалс:: Жетпассвордкредентиалс</span><span class="sxs-lookup"><span data-stu-id="1a16c-103">ICcgDomainAuthCredentials::GetPasswordCredentials method</span></span>

<span data-ttu-id="1a16c-104">Возвращает учетные данные для проверки подлинности контейнера, не присоединенного к домену, с Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1a16c-104">Returns credentials to authenticate a non-domain joined container with Active Directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a16c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1a16c-105">Syntax</span></span>


```C++
HRESULT GetPasswordCredentials(
[in] LPCWSTR pluginInput, 
[out] LPWSTR* domainName, 
[out] LPWSTR* username, 
[out] LPWSTR* password);
);
```



## <a name="parameters"></a><span data-ttu-id="1a16c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a16c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a16c-107">*плугининпут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1a16c-107">*pluginInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a16c-108">Входная строка, передаваемая средой выполнения контейнера.</span><span class="sxs-lookup"><span data-stu-id="1a16c-108">An input string passed in by the container runtime.</span></span> <span data-ttu-id="1a16c-109">Реализация клиента использует предоставленную входную строку для получения учетных данных для проверки подлинности, обычно от поставщика защищенного хранилища, который возвращается в выходных параметрах.</span><span class="sxs-lookup"><span data-stu-id="1a16c-109">The client implementation uses the provided input string to retrieve authentication credentials, typically from a secure storage provider, that are returned in the output parameters.</span></span> <span data-ttu-id="1a16c-110">Входная строка предоставляется службам вычислений узла (HCS) в файле спецификации учетных данных.</span><span class="sxs-lookup"><span data-stu-id="1a16c-110">The input string is provided to the Host Compute Services (HCS) in a credential specification file.</span></span> <span data-ttu-id="1a16c-111">Дополнительные сведения см. в разделе **Примечания**.</span><span class="sxs-lookup"><span data-stu-id="1a16c-111">For more information, see the **Remarks** section.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="1a16c-112">*имя_домена* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1a16c-112">*domainName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a16c-113">Доменное имя для учетных данных.</span><span class="sxs-lookup"><span data-stu-id="1a16c-113">The domain name for the credentials.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="1a16c-114">*имя пользователя* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1a16c-114">*username* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a16c-115">Имя пользователя для учетных данных.</span><span class="sxs-lookup"><span data-stu-id="1a16c-115">The user name for the credentials.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="1a16c-116">*пароль* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1a16c-116">*password* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a16c-117">Пароль для учетных данных.</span><span class="sxs-lookup"><span data-stu-id="1a16c-117">The password for the credentials.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a16c-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1a16c-118">Return value</span></span>

<span data-ttu-id="1a16c-119">Возвращаемое значение является значением **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1a16c-119">The return value is an **HRESULT**.</span></span> <span data-ttu-id="1a16c-120">Значение S \_ ОК указывает на Успешный вызов.</span><span class="sxs-lookup"><span data-stu-id="1a16c-120">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a16c-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1a16c-121">Remarks</span></span>

<span data-ttu-id="1a16c-122">API может быть вызван параллельно.</span><span class="sxs-lookup"><span data-stu-id="1a16c-122">The API may be called concurrently.</span></span> <span data-ttu-id="1a16c-123">Поэтому разработчику необходимо убедиться, что их реализация является потокобезопасной.</span><span class="sxs-lookup"><span data-stu-id="1a16c-123">Therefore, the developer needs to ensure that their implementation is thread safe.</span></span> <span data-ttu-id="1a16c-124">Кроме того, COM-объект будет активирован вне процесса и должен быть зарегистрирован соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="1a16c-124">Additionally, the COM object will be activated out-of-proc and it must be registered appropriately.</span></span> 

<span data-ttu-id="1a16c-125">Разработчик должен добавить ключ в "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\CCG\COMClasses" для своего CLSID COM.</span><span class="sxs-lookup"><span data-stu-id="1a16c-125">The implementer must add a key under “HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\CCG\COMClasses” for their COM CLSID.</span></span> <span data-ttu-id="1a16c-126">Доступ для записи к "Ккг\комклассес" ограничен учетными записями SYSTEM и Administrator.</span><span class="sxs-lookup"><span data-stu-id="1a16c-126">Write access to “CCG\COMClasses” is restricted to SYSTEM and Administrator accounts.</span></span> 

<span data-ttu-id="1a16c-127">Ниже приведен пример файла спецификации учетных данных.</span><span class="sxs-lookup"><span data-stu-id="1a16c-127">The following is an example credential specification file.</span></span> <span data-ttu-id="1a16c-128">Сведения о предоставлении этого файла в DOCKER см. в разделе [Запуск контейнера с помощью gMSA](/virtualization/windowscontainers/manage-containers/gmsa-run-container).</span><span class="sxs-lookup"><span data-stu-id="1a16c-128">For information on supplying this file to Docker, see [Run a container with a gMSA](/virtualization/windowscontainers/manage-containers/gmsa-run-container).</span></span>

```json
{
    "CmsPlugins": [
        "ActiveDirectory"
    ],
    "DomainJoinConfig": {
        "Sid": "S-1-5-21-3700119848-2853083131-2094573802",
        "MachineAccountName": "gmsa1",
        "Guid": "630a7dd3-2d3e-4471-ae91-1d9ea2556cd5",
        "DnsTreeName": "contoso.com",
        "DnsName": "contoso.com",
        "NetBiosName": "CONTOSO"
    },
    "ActiveDirectoryConfig": {
        "GroupManagedServiceAccounts": [
            {
                "Name": "gmsa1",
                "Scope": "contoso.com"
            },
            {
                "Name": "gmsa1",
                "Scope": "CONTOSO"
            }
        ],
        "HostAccountConfig": {
            "PortableCcgVersion": "1",
            "PluginGUID": "{CFCA0441-511D-4B2A-862E-20348A78760B}",
            "PluginInput": "contoso.com:gmsaccg:<password>"
        }
    }
}

```

## <a name="examples"></a><span data-ttu-id="1a16c-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="1a16c-129">Examples</span></span>

<span data-ttu-id="1a16c-130">В следующем примере показана простая реализация **иккгдомаинаускредентиалс**.</span><span class="sxs-lookup"><span data-stu-id="1a16c-130">The following example shows a simple implementation of **ICcgDomainAuthCredentials**.</span></span> <span data-ttu-id="1a16c-131">Обратите внимание, что в целях наглядности этот пример получает учетные данные, просто анализируя входную строку.</span><span class="sxs-lookup"><span data-stu-id="1a16c-131">Note that, for illustrative purposes, this sample obtains the credentials by simply parsing the input string.</span></span> <span data-ttu-id="1a16c-132">В реальной реализации учетные данные будут храниться в защищенном хранилище данных и использовать входную строку для нахождение учетных данных.</span><span class="sxs-lookup"><span data-stu-id="1a16c-132">A real-world implementation would store the credentials in a secure data store and use the input string to locate the credential information.</span></span> <span data-ttu-id="1a16c-133">Кроме того, для краткости в этом примере опущены стандартные реализации COM-методов.</span><span class="sxs-lookup"><span data-stu-id="1a16c-133">Also, the standard COM method implementations have been omitted from this sample for brevity.</span></span>


```C++
// UUID generated by the developer
[uuid("cfca0441-511d-4b2a-862e-20348a78760b")] 
class CCGStubPlugin : public RuntimeClass<RuntimeClassFlags<RuntimeClassType::ClassicCom>, ICcgDomainAuthCredentials >
{
   public:
    CCGStubPlugin() {}

    ~CCGStubPlugin() {}

    IFACEMETHODIMP GetPasswordCredentials(
        _In_ LPCWSTR pluginInput,
        _Outptr_ LPWSTR *domainName,
        _Outptr_ LPWSTR *username,
        _Outptr_ LPWSTR *password)
    {
        std::wstring domainParsed, userParsed, passwordParsed; 
        try
        {
            if(domainName == NULL || username == NULL || password == NULL)
            {
                return STG_E_INVALIDPARAMETER;
            }
            *domainName = NULL;
            *username = NULL;
            *password = NULL;
            wstring pluginInputString(pluginInput);
            if (count(pluginInputString.begin(), pluginInputString.end(), ':') < 2)
            {
                return CO_E_NOT_SUPPORTED;
            }
            // Extract creds of this format Domain:Username:Password
            size_t sep1 = pluginInputString.find(L":");
            size_t sep2 = pluginInputString.find(L":", sep1 + 1);
            domainParsed = pluginInputString.substr(0, sep1);
            userParsed = pluginInputString.substr(sep1 + 1, sep2 - sep1 - 1);
            passwordParsed = pluginInputString.substr(sep2 + 1);
        }
        catch (...)
        {
            return EVENT_E_INTERNALERROR;
        }

        auto userCo = wil::make_cotaskmem_string_nothrow(userParsed.c_str());
        auto passwordCo = wil::make_cotaskmem_string_nothrow(passwordParsed.c_str());
        auto domainCo = wil::make_cotaskmem_string_nothrow(domainParsed.c_str());
        if (userCo == nullptr || passwordCo == nullptr || domainCo == nullptr)
        {
            return STG_E_INSUFFICIENTMEMORY;
        }

        *domainName = domainCo.release();
        *username = userCo.release();
        *password = passwordCo.release();
        return S_OK;
    }
};
CoCreatableClass(CCGStubPlugin);

```



## <a name="requirements"></a><span data-ttu-id="1a16c-134">Требования</span><span class="sxs-lookup"><span data-stu-id="1a16c-134">Requirements</span></span>




| <span data-ttu-id="1a16c-135">Требование</span><span class="sxs-lookup"><span data-stu-id="1a16c-135">Requirement</span></span> | <span data-ttu-id="1a16c-136">Значение</span><span class="sxs-lookup"><span data-stu-id="1a16c-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a16c-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1a16c-137">Minimum supported server</span></span> | <span data-ttu-id="1a16c-138">Windows Server версии 2004</span><span class="sxs-lookup"><span data-stu-id="1a16c-138">Windows Server, version 2004</span></span>                                    |
| <span data-ttu-id="1a16c-139">Header</span><span class="sxs-lookup"><span data-stu-id="1a16c-139">Header</span></span>                   | <span data-ttu-id="1a16c-140">ккгплугинс. h</span><span class="sxs-lookup"><span data-stu-id="1a16c-140">ccgplugins.h</span></span>   |
| <span data-ttu-id="1a16c-141">IID</span><span class="sxs-lookup"><span data-stu-id="1a16c-141">IID</span></span>                    | <span data-ttu-id="1a16c-142">6ecda518-2010-4437-8bc3-46e752b7b172</span><span class="sxs-lookup"><span data-stu-id="1a16c-142">6ecda518-2010-4437-8bc3-46e752b7b172</span></span>          |



 

