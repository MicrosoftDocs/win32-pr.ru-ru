---
description: Определяемая приложением функция, которая обрабатывает записи контроля доступа (ACE) обратного вызова во время проверки доступа.
ms.assetid: e8a510e6-0739-4765-ad07-3bcb1b9c905c
title: Функция обратного вызова Аусзакцессчекккаллбакк
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzAccessCheckCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 82e100092dd7c59e9cc689aa8723365fae8bed29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104273100"
---
# <a name="authzaccesscheckcallback-callback-function"></a><span data-ttu-id="7f64f-103">Функция обратного вызова Аусзакцессчекккаллбакк</span><span class="sxs-lookup"><span data-stu-id="7f64f-103">AuthzAccessCheckCallback callback function</span></span>

<span data-ttu-id="7f64f-104">Функция **аусзакцессчекккаллбакк** — это определяемая приложением функция, которая обрабатывает [*записи контроля доступа*](/windows/desktop/SecGloss/a-gly) (ACE) обратного вызова во время проверки доступа.</span><span class="sxs-lookup"><span data-stu-id="7f64f-104">The **AuthzAccessCheckCallback** function is an application-defined function that handles callback [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) during an access check.</span></span> <span data-ttu-id="7f64f-105">**Аусзакцессчекккаллбакк** — это заполнитель для имени определяемой приложением функции.</span><span class="sxs-lookup"><span data-stu-id="7f64f-105">**AuthzAccessCheckCallback** is a placeholder for the application-defined function name.</span></span> <span data-ttu-id="7f64f-106">Приложение регистрирует этот обратный вызов, вызвав [**аусзинитиализересаурцеманажер**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager).</span><span class="sxs-lookup"><span data-stu-id="7f64f-106">The application registers this callback by calling [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager).</span></span>

## <a name="syntax"></a><span data-ttu-id="7f64f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f64f-107">Syntax</span></span>


```C++
BOOL CALLBACK AuthzAccessCheckCallback(
  _In_     AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_     PACE_HEADER                 pAce,
  _In_opt_ PVOID                       pArgs,
  _Inout_  PBOOL                       pbAceApplicable
);
```



## <a name="parameters"></a><span data-ttu-id="7f64f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f64f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f64f-109">*хаусзклиентконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7f64f-109">*hAuthzClientContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f64f-110">Маркер контекста клиента.</span><span class="sxs-lookup"><span data-stu-id="7f64f-110">A handle to a client context.</span></span>

</dd> <dt>

<span data-ttu-id="7f64f-111">*скорость* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7f64f-111">*pAce* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f64f-112">Указатель на запись ACE для проверки включения в вызов функции [**аусзакцессчекк**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) .</span><span class="sxs-lookup"><span data-stu-id="7f64f-112">A pointer to the ACE to evaluate for inclusion in the call to the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function.</span></span>

</dd> <dt>

<span data-ttu-id="7f64f-113">*паргс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="7f64f-113">*pArgs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7f64f-114">Данные, передаваемые в параметре *динамикграупаргс* вызова [**аусзакцессчекк**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) или [**аусзкачедакцессчекк**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck).</span><span class="sxs-lookup"><span data-stu-id="7f64f-114">Data passed in the *DynamicGroupArgs* parameter of the call to [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) or [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck).</span></span>

</dd> <dt>

<span data-ttu-id="7f64f-115">*пбацеаппликабле* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="7f64f-115">*pbAceApplicable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f64f-116">Указатель на логическую переменную, которая получает результаты вычисления логики, определенной приложением.</span><span class="sxs-lookup"><span data-stu-id="7f64f-116">A pointer to a Boolean variable that receives the results of the evaluation of the logic defined by the application.</span></span>

<span data-ttu-id="7f64f-117">Результаты имеют **значение true** , если логика определяет, что элемент ACE применим и будет включен в вызов [**аусзакцессчекк**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck); в противном случае результат будет **ложным**.</span><span class="sxs-lookup"><span data-stu-id="7f64f-117">The results are **TRUE** if the logic determines that the ACE is applicable and will be included in the call to [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck); otherwise, the results are **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f64f-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f64f-118">Return value</span></span>

<span data-ttu-id="7f64f-119">Если функция завершается с ошибкой, функция возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="7f64f-119">If the function succeeds, the function returns **TRUE**.</span></span>

<span data-ttu-id="7f64f-120">Если функция не может выполнить вычисление, она возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="7f64f-120">If the function is unable to perform the evaluation, it returns **FALSE**.</span></span> <span data-ttu-id="7f64f-121">Используйте [**сетластеррор**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) , чтобы вернуть ошибку в функцию проверки доступа.</span><span class="sxs-lookup"><span data-stu-id="7f64f-121">Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to return an error to the access check function.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f64f-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7f64f-122">Remarks</span></span>

<span data-ttu-id="7f64f-123">Переменные атрибутов безопасности должны присутствовать в контексте клиента, если они ссылаются на условное выражение, в противном случае термин условного выражения, ссылающийся на них, будет считаться неизвестным.</span><span class="sxs-lookup"><span data-stu-id="7f64f-123">Security attribute variables must be present in the client context if referred to in a conditional expression, otherwise the conditional expression term referencing them will evaluate to unknown.</span></span>

<span data-ttu-id="7f64f-124">Дополнительные сведения см. в статьях [как работают методы AccessCheck](how-dacls-control-access-to-an-object.md) и [централизованные политики авторизации](centralized-authorization-policy.md) .</span><span class="sxs-lookup"><span data-stu-id="7f64f-124">For more information, see the [How AccessCheck Works](how-dacls-control-access-to-an-object.md) and [Centralized Authorization Policy](centralized-authorization-policy.md) overviews.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f64f-125">Требования</span><span class="sxs-lookup"><span data-stu-id="7f64f-125">Requirements</span></span>



| <span data-ttu-id="7f64f-126">Требование</span><span class="sxs-lookup"><span data-stu-id="7f64f-126">Requirement</span></span> | <span data-ttu-id="7f64f-127">Значение</span><span class="sxs-lookup"><span data-stu-id="7f64f-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="7f64f-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7f64f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7f64f-129">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7f64f-129">Windows XP \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="7f64f-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7f64f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7f64f-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7f64f-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="7f64f-132">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="7f64f-132">Redistributable</span></span><br/>          | <span data-ttu-id="7f64f-133">Пакет средств администрирования Windows Server 2003 в Windows XP</span><span class="sxs-lookup"><span data-stu-id="7f64f-133">Windows Server 2003 Administration Tools Pack on Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7f64f-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f64f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f64f-135">Основные функции контроля доступа</span><span class="sxs-lookup"><span data-stu-id="7f64f-135">Basic Access Control Functions</span></span>](authorization-functions.md)
</dt> <dt>

[<span data-ttu-id="7f64f-136">Централизованная политика авторизации</span><span class="sxs-lookup"><span data-stu-id="7f64f-136">Centralized Authorization Policy</span></span>](centralized-authorization-policy.md)
</dt> <dt>

[<span data-ttu-id="7f64f-137">Как работает AccessCheck</span><span class="sxs-lookup"><span data-stu-id="7f64f-137">How AccessCheck Works</span></span>](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="7f64f-138">**аусзакцессчекк**</span><span class="sxs-lookup"><span data-stu-id="7f64f-138">**AuthzAccessCheck**</span></span>](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> <dt>

[<span data-ttu-id="7f64f-139">**аусзкачедакцессчекк**</span><span class="sxs-lookup"><span data-stu-id="7f64f-139">**AuthzCachedAccessCheck**</span></span>](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)
</dt> <dt>

[<span data-ttu-id="7f64f-140">**аусзинитиализеремотересаурцеманажер**</span><span class="sxs-lookup"><span data-stu-id="7f64f-140">**AuthzInitializeRemoteResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[<span data-ttu-id="7f64f-141">**аусзинитиализересаурцеманажер**</span><span class="sxs-lookup"><span data-stu-id="7f64f-141">**AuthzInitializeResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

