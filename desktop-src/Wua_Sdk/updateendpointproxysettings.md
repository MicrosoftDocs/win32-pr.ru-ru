---
description: Структура Упдатиндпоинтпроксисеттингс определяет параметры прокси-сервера, используемые при запросе маркера.
ms.assetid: 24AA8843-D4EE-4F17-8B96-63ED25B365D2
title: Структура Упдатиндпоинтпроксисеттингс (Упдатиндпоинтаус. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointProxySettings
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: aad6ad294baab37b7516152438dbc9fd05f7036a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072797"
---
# <a name="updateendpointproxysettings-structure"></a><span data-ttu-id="6e16d-103">Структура Упдатиндпоинтпроксисеттингс</span><span class="sxs-lookup"><span data-stu-id="6e16d-103">UpdateEndpointProxySettings structure</span></span>

<span data-ttu-id="6e16d-104">Структура **упдатиндпоинтпроксисеттингс** определяет параметры прокси-сервера, используемые при запросе маркера.</span><span class="sxs-lookup"><span data-stu-id="6e16d-104">The **UpdateEndpointProxySettings** structure defines the proxy settings used when requesting a token.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e16d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6e16d-105">Syntax</span></span>


```C++
typedef struct tagUpdateEndpointProxySettings {
  BSTR szProxyAddr;
  BSTR szBypassList;
  BSTR szUserName;
  BSTR szPassword;
} UpdateEndpointProxySettings;
```



## <a name="members"></a><span data-ttu-id="6e16d-106">Члены</span><span class="sxs-lookup"><span data-stu-id="6e16d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6e16d-107">**сзпроксяддр**</span><span class="sxs-lookup"><span data-stu-id="6e16d-107">**szProxyAddr**</span></span>
</dt> <dd>

<span data-ttu-id="6e16d-108">DNS-имя или IP-адрес прокси-сервера для использования (например, "proxy.somecorp.com" или "192.168.0.4") или пустая строка, если прокси-сервер не используется.</span><span class="sxs-lookup"><span data-stu-id="6e16d-108">The DNS name or IP address of the proxy server to use (for example, "proxy.somecorp.com" or "192.168.0.4"), or an empty string if no proxy should be used.</span></span>

</dd> <dt>

<span data-ttu-id="6e16d-109">**сзбипасслист**</span><span class="sxs-lookup"><span data-stu-id="6e16d-109">**szBypassList**</span></span>
</dt> <dd>

<span data-ttu-id="6e16d-110">Список адресов узлов, которые должны обходить прокси-сервер, или пустую строку, если все адреса узлов должны использовать прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="6e16d-110">A list of host addresses that should bypass the proxy server, or an empty string if all host addresses should use the proxy server</span></span>

<span data-ttu-id="6e16d-111">WUA не использует эти данные, если **сзпроксяддр** пуст.</span><span class="sxs-lookup"><span data-stu-id="6e16d-111">WUA does not use this data if **szProxyAddr** is empty.</span></span>

</dd> <dt>

<span data-ttu-id="6e16d-112">**сзусернаме**</span><span class="sxs-lookup"><span data-stu-id="6e16d-112">**szUserName**</span></span>
</dt> <dd>

<span data-ttu-id="6e16d-113">Имя пользователя, используемое для проверки подлинности на прокси-сервере, или пустая строка, если проверка подлинности не требуется.</span><span class="sxs-lookup"><span data-stu-id="6e16d-113">The username that is used to authenticate with the proxy server, or the empty string if no authentication is needed.</span></span>

<span data-ttu-id="6e16d-114">WUA не использует эти данные, если **сзпроксяддр** пуст.</span><span class="sxs-lookup"><span data-stu-id="6e16d-114">WUA does not use this data if **szProxyAddr** is empty.</span></span>

</dd> <dt>

<span data-ttu-id="6e16d-115">**сзпассворд**</span><span class="sxs-lookup"><span data-stu-id="6e16d-115">**szPassword**</span></span>
</dt> <dd>

<span data-ttu-id="6e16d-116">Пароль, используемый для проверки подлинности на прокси-сервере, или пустая строка, если проверка подлинности не требуется.</span><span class="sxs-lookup"><span data-stu-id="6e16d-116">The password that is used to authenticate with the proxy server, or the empty string if no authentication is needed.</span></span>

<span data-ttu-id="6e16d-117">WUA не использует эти данные, если **сзпроксяддр** пуст.</span><span class="sxs-lookup"><span data-stu-id="6e16d-117">WUA does not use this data if **szProxyAddr** is empty.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6e16d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="6e16d-118">Requirements</span></span>



| <span data-ttu-id="6e16d-119">Требование</span><span class="sxs-lookup"><span data-stu-id="6e16d-119">Requirement</span></span> | <span data-ttu-id="6e16d-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6e16d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e16d-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6e16d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6e16d-122">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6e16d-122">Windows 8 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="6e16d-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6e16d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6e16d-124">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6e16d-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="6e16d-125">Header</span><span class="sxs-lookup"><span data-stu-id="6e16d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e16d-126"><dt>Упдатиндпоинтаус. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e16d-126"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="6e16d-127">IDL</span><span class="sxs-lookup"><span data-stu-id="6e16d-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6e16d-128"><dt>Упдатиндпоинтаус. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6e16d-128"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e16d-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6e16d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e16d-130">**жетендпоинттокен**</span><span class="sxs-lookup"><span data-stu-id="6e16d-130">**GetEndpointToken**</span></span>](iupdateendpointauthprovider-getendpointtoken.md)
</dt> </dl>

 

 




