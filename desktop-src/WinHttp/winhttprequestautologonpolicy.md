---
description: Включает возможные параметры для политики автоматического входа в систему.
ms.assetid: dad4f6a7-8e84-4f4f-b962-4189e3dc01f7
title: Перечисление Винхттпрекуестаутологонполици
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequestAutoLogonPolicy
api_type:
- IDLDef
api_location:
- HttpRequest.idl
ms.openlocfilehash: dab3dc14dd194e36b9b4d1225f77161005b9d21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711066"
---
# <a name="winhttprequestautologonpolicy-enumeration"></a><span data-ttu-id="29e94-103">Перечисление Винхттпрекуестаутологонполици</span><span class="sxs-lookup"><span data-stu-id="29e94-103">WinHttpRequestAutoLogonPolicy enumeration</span></span>

<span data-ttu-id="29e94-104">Перечисление **винхттпрекуестаутологонполици** включает возможные параметры для [политики автоматического входа в систему](authentication-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="29e94-104">The **WinHttpRequestAutoLogonPolicy** enumeration includes possible settings for the [Automatic Logon Policy](authentication-in-winhttp.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="29e94-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="29e94-105">Syntax</span></span>


```C++
typedef enum WinHttpRequestAutoLogonPolicy { 
  AutoLogonPolicy_Always             = 0,
  AutoLogonPolicy_OnlyIfBypassProxy  = 1,
  AutoLogonPolicy_Never              = 2
} WinHttpRequestAutoLogonPolicy;
```



## <a name="constants"></a><span data-ttu-id="29e94-106">Константы</span><span class="sxs-lookup"><span data-stu-id="29e94-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="29e94-107"><span id="AutoLogonPolicy_Always"></span><span id="autologonpolicy_always"></span><span id="AUTOLOGONPOLICY_ALWAYS"></span>**Аутологонполици \_ всегда**</span><span class="sxs-lookup"><span data-stu-id="29e94-107"><span id="AutoLogonPolicy_Always"></span><span id="autologonpolicy_always"></span><span id="AUTOLOGONPOLICY_ALWAYS"></span>**AutoLogonPolicy\_Always**</span></span>
</dt> <dd>

<span data-ttu-id="29e94-108">Вход с проверкой подлинности с использованием учетных данных по умолчанию выполняется для всех запросов.</span><span class="sxs-lookup"><span data-stu-id="29e94-108">An authenticated log on, using the default credentials, is performed for all requests.</span></span>

</dd> <dt>

<span data-ttu-id="29e94-109"><span id="AutoLogonPolicy_OnlyIfBypassProxy"></span><span id="autologonpolicy_onlyifbypassproxy"></span><span id="AUTOLOGONPOLICY_ONLYIFBYPASSPROXY"></span>**Аутологонполици \_ онлифбипасспрокси**</span><span class="sxs-lookup"><span data-stu-id="29e94-109"><span id="AutoLogonPolicy_OnlyIfBypassProxy"></span><span id="autologonpolicy_onlyifbypassproxy"></span><span id="AUTOLOGONPOLICY_ONLYIFBYPASSPROXY"></span>**AutoLogonPolicy\_OnlyIfBypassProxy**</span></span>
</dt> <dd>

<span data-ttu-id="29e94-110">Вход с проверкой подлинности с использованием учетных данных по умолчанию выполняется только для запросов в локальной интрасети.</span><span class="sxs-lookup"><span data-stu-id="29e94-110">An authenticated log on, using the default credentials, is performed only for requests on the local intranet.</span></span> <span data-ttu-id="29e94-111">Локальная интрасеть считается любым сервером в списке обхода прокси-сервера в текущей конфигурации прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="29e94-111">The local intranet is considered to be any server on the proxy bypass list in the current proxy configuration.</span></span>

</dd> <dt>

<span data-ttu-id="29e94-112"><span id="AutoLogonPolicy_Never"></span><span id="autologonpolicy_never"></span><span id="AUTOLOGONPOLICY_NEVER"></span>**Аутологонполици \_ никогда**</span><span class="sxs-lookup"><span data-stu-id="29e94-112"><span id="AutoLogonPolicy_Never"></span><span id="autologonpolicy_never"></span><span id="AUTOLOGONPOLICY_NEVER"></span>**AutoLogonPolicy\_Never**</span></span>
</dt> <dd>

<span data-ttu-id="29e94-113">Проверка подлинности не используется автоматически.</span><span class="sxs-lookup"><span data-stu-id="29e94-113">Authentication is not used automatically.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29e94-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="29e94-114">Remarks</span></span>

<span data-ttu-id="29e94-115">Чтобы задать политику автоматического входа в систему, вызовите метод [**сетаутологонполици**](iwinhttprequest-setautologonpolicy.md) и укажите одну из приведенных выше констант.</span><span class="sxs-lookup"><span data-stu-id="29e94-115">To set the automatic logon policy, call the [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md) method and specify one of the preceding constants.</span></span>

> [!Note]  
> <span data-ttu-id="29e94-116">Для Windows XP и Windows 2000 см. раздел [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="29e94-116">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP start page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="29e94-117">Требования</span><span class="sxs-lookup"><span data-stu-id="29e94-117">Requirements</span></span>



| <span data-ttu-id="29e94-118">Требование</span><span class="sxs-lookup"><span data-stu-id="29e94-118">Requirement</span></span> | <span data-ttu-id="29e94-119">Значение</span><span class="sxs-lookup"><span data-stu-id="29e94-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="29e94-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="29e94-120">Minimum supported client</span></span><br/> | <span data-ttu-id="29e94-121">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="29e94-121">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="29e94-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="29e94-122">Minimum supported server</span></span><br/> | <span data-ttu-id="29e94-123">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="29e94-123">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="29e94-124">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="29e94-124">Redistributable</span></span><br/>          | <span data-ttu-id="29e94-125">WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="29e94-125">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="29e94-126">IDL</span><span class="sxs-lookup"><span data-stu-id="29e94-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="29e94-127"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="29e94-127"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29e94-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="29e94-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29e94-129">Версии WinHTTP</span><span class="sxs-lookup"><span data-stu-id="29e94-129">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




