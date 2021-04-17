---
description: Функция Аусзжетцентралакцессполицикаллбакк — это определяемая приложением функция, которая получает централизованную политику доступа. Аусзжетцентралакцессполицикаллбакк — это заполнитель для имени определяемой приложением функции.
ms.assetid: 1D5831EF-ACA8-4EE9-A7C1-E1A3CB74CEC0
title: Функция обратного вызова Аусзжетцентралакцессполицикаллбакк
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzGetCentralAccessPolicyCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: b96832fa647fde920a70ac3d6608c8ebb0048892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651211"
---
# <a name="authzgetcentralaccesspolicycallback-callback-function"></a><span data-ttu-id="b03a1-104">Функция обратного вызова Аусзжетцентралакцессполицикаллбакк</span><span class="sxs-lookup"><span data-stu-id="b03a1-104">AuthzGetCentralAccessPolicyCallback callback function</span></span>

<span data-ttu-id="b03a1-105">Функция *аусзжетцентралакцессполицикаллбакк* — это определяемая приложением функция, которая получает централизованную политику доступа.</span><span class="sxs-lookup"><span data-stu-id="b03a1-105">The *AuthzGetCentralAccessPolicyCallback* function is an application-defined function that retrieves the central access policy.</span></span> <span data-ttu-id="b03a1-106">*Аусзжетцентралакцессполицикаллбакк* — это заполнитель для имени определяемой приложением функции.</span><span class="sxs-lookup"><span data-stu-id="b03a1-106">*AuthzGetCentralAccessPolicyCallback* is a placeholder for the application-defined function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="b03a1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b03a1-107">Syntax</span></span>


```C++
BOOL CALLBACK AuthzGetCentralAccessPolicyCallback (
  _In_     AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_     PSID                        capid,
  _In_opt_ PVOID                       pArgs,
  _Out_    PBOOL                       pCentralAccessPolicyApplicable,
  _Out_    PVOID                       ppCentralAccessPolicy
);
```



## <a name="parameters"></a><span data-ttu-id="b03a1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b03a1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b03a1-109">*хаусзклиентконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b03a1-109">*hAuthzClientContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b03a1-110">Обработчик контекста клиента.</span><span class="sxs-lookup"><span data-stu-id="b03a1-110">Handle to the client context.</span></span>

</dd> <dt>

<span data-ttu-id="b03a1-111">*капид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b03a1-111">*capid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b03a1-112">Идентификатор извлекаемой централизованной политики доступа.</span><span class="sxs-lookup"><span data-stu-id="b03a1-112">ID of the central access policy to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="b03a1-113">*паргс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b03a1-113">*pArgs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b03a1-114">Необязательные аргументы, которые были переданы функции [**аусзакцессчекк**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) через элемент **оптионаларгументс** структуры [**\_ \_ запроса на доступ к авторизации**](/windows/desktop/api/Authz/ns-authz-authz_access_request) .</span><span class="sxs-lookup"><span data-stu-id="b03a1-114">Optional arguments that were passed to the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function through the **OptionalArguments** member of the [**AUTHZ\_ACCESS\_REQUEST**](/windows/desktop/api/Authz/ns-authz-authz_access_request) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b03a1-115">*пцентралакцессполициаппликабле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b03a1-115">*pCentralAccessPolicyApplicable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b03a1-116">Указатель на логическое значение, используемое диспетчером ресурсов, чтобы указать, следует ли использовать централизованную политику доступа во время оценки доступа.</span><span class="sxs-lookup"><span data-stu-id="b03a1-116">Pointer to a Boolean value that the resource manager uses to indicate whether a central access policy should be used during access evaluation.</span></span>

</dd> <dt>

<span data-ttu-id="b03a1-117">*ппцентралакцессполици* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b03a1-117">*ppCentralAccessPolicy* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b03a1-118">Указатель на централизованную политику доступа (CAP), используемую для оценки доступа.</span><span class="sxs-lookup"><span data-stu-id="b03a1-118">Pointer to the central access policy (CAP) to be used for evaluating access.</span></span> <span data-ttu-id="b03a1-119">Если это значение равно **null**, применяется ограничение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b03a1-119">If this value is **NULL**, the default CAP is applied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b03a1-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b03a1-120">Return value</span></span>

<span data-ttu-id="b03a1-121">Если функция завершается с ошибкой, функция возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="b03a1-121">If the function succeeds, the function returns **TRUE**.</span></span>

<span data-ttu-id="b03a1-122">Если функция не может выполнить вычисление, она возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="b03a1-122">If the function is unable to perform the evaluation, it returns **FALSE**.</span></span> <span data-ttu-id="b03a1-123">Используйте [**сетластеррор**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) , чтобы вернуть ошибку в функцию проверки доступа.</span><span class="sxs-lookup"><span data-stu-id="b03a1-123">Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to return an error to the access check function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b03a1-124">Требования</span><span class="sxs-lookup"><span data-stu-id="b03a1-124">Requirements</span></span>



| <span data-ttu-id="b03a1-125">Требование</span><span class="sxs-lookup"><span data-stu-id="b03a1-125">Requirement</span></span> | <span data-ttu-id="b03a1-126">Значение</span><span class="sxs-lookup"><span data-stu-id="b03a1-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="b03a1-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b03a1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b03a1-128">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b03a1-128">Windows 8 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b03a1-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b03a1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b03a1-130">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b03a1-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="b03a1-131">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="b03a1-131">Redistributable</span></span><br/>          | <span data-ttu-id="b03a1-132">Пакет средств администрирования Windows Server 2003 в Windows XP</span><span class="sxs-lookup"><span data-stu-id="b03a1-132">Windows Server 2003 Administration Tools Pack on Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b03a1-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b03a1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b03a1-134">**\_запрос на доступ к AUTHZ \_**</span><span class="sxs-lookup"><span data-stu-id="b03a1-134">**AUTHZ\_ACCESS\_REQUEST**</span></span>](/windows/desktop/api/Authz/ns-authz-authz_access_request)
</dt> <dt>

[<span data-ttu-id="b03a1-135">**\_ \_ сведения о инициализации AUTHZ**</span><span class="sxs-lookup"><span data-stu-id="b03a1-135">**AUTHZ\_INIT\_INFO**</span></span>](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[<span data-ttu-id="b03a1-136">**аусзакцессчекк**</span><span class="sxs-lookup"><span data-stu-id="b03a1-136">**AuthzAccessCheck**</span></span>](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> </dl>

 

