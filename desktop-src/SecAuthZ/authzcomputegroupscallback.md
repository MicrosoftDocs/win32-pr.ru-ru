---
description: Определяемая приложением функция, которая создает список идентификаторов безопасности (SID), которые применяются к клиенту. Аусзкомпутеграупскаллбакк — это заполнитель для имени определяемой приложением функции.
ms.assetid: c20a02a0-5303-4433-a484-5a89999b32b9
title: Функция обратного вызова Аусзкомпутеграупскаллбакк
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzComputeGroupsCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 3728f8114d87d07ddb33dd77a6fda5db30d07cf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819464"
---
# <a name="authzcomputegroupscallback-callback-function"></a><span data-ttu-id="04fab-104">Функция обратного вызова Аусзкомпутеграупскаллбакк</span><span class="sxs-lookup"><span data-stu-id="04fab-104">AuthzComputeGroupsCallback callback function</span></span>

<span data-ttu-id="04fab-105">Функция **аусзкомпутеграупскаллбакк** — это определяемая приложением функция, которая создает список [*идентификаторов безопасности*](/windows/desktop/SecGloss/s-gly) (SID), которые применяются к клиенту.</span><span class="sxs-lookup"><span data-stu-id="04fab-105">The **AuthzComputeGroupsCallback** function is an application-defined function that creates a list of [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) that apply to a client.</span></span> <span data-ttu-id="04fab-106">**Аусзкомпутеграупскаллбакк** — это заполнитель для имени определяемой приложением функции.</span><span class="sxs-lookup"><span data-stu-id="04fab-106">**AuthzComputeGroupsCallback** is a placeholder for the application-defined function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="04fab-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="04fab-107">Syntax</span></span>


```C++
BOOL CALLBACK AuthzComputeGroupsCallback(
  _In_  AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_  PVOID                       Args,
  _Out_ PSID_AND_ATTRIBUTES         *pSidAttrArray,
  _Out_ PDWORD                      pSidCount,
  _Out_ PSID_AND_ATTRIBUTES         *pRestrictedSidAttrArray,
  _Out_ PDWORD                      pRestrictedSidCount
);
```



## <a name="parameters"></a><span data-ttu-id="04fab-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="04fab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04fab-109">*хаусзклиентконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="04fab-109">*hAuthzClientContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04fab-110">Маркер контекста клиента.</span><span class="sxs-lookup"><span data-stu-id="04fab-110">A handle to a client context.</span></span>

</dd> <dt>

<span data-ttu-id="04fab-111">*Args* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="04fab-111">*Args* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04fab-112">Данные, передаваемые в параметре *динамикграупаргс* вызова функции [**аусзинитиализеконтекстфромаусзконтекст**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext), [**аусзинитиализеконтекстфромсид**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)или [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) .</span><span class="sxs-lookup"><span data-stu-id="04fab-112">Data passed in the *DynamicGroupArgs* parameter of a call to the [**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext), [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid), or [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) function.</span></span>

</dd> <dt>

<span data-ttu-id="04fab-113">*псидаттраррай* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="04fab-113">*pSidAttrArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04fab-114">Указатель на переменную указателя, которая получает адрес массива структур [**SID \_ и \_ атрибутов**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) .</span><span class="sxs-lookup"><span data-stu-id="04fab-114">A pointer to a pointer variable that receives the address of an array of [**SID\_AND\_ATTRIBUTES**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) structures.</span></span> <span data-ttu-id="04fab-115">Эти структуры представляют группы, к которым принадлежит клиент.</span><span class="sxs-lookup"><span data-stu-id="04fab-115">These structures represent the groups to which the client belongs.</span></span>

</dd> <dt>

<span data-ttu-id="04fab-116">*псидкаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="04fab-116">*pSidCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04fab-117">Количество структур в *псидаттраррай*.</span><span class="sxs-lookup"><span data-stu-id="04fab-117">The number of structures in *pSidAttrArray*.</span></span>

</dd> <dt>

<span data-ttu-id="04fab-118">*престриктедсидаттраррай* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="04fab-118">*pRestrictedSidAttrArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04fab-119">Указатель на переменную указателя, которая получает адрес массива структур [**SID \_ и \_ атрибутов**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) .</span><span class="sxs-lookup"><span data-stu-id="04fab-119">A pointer to a pointer variable that receives the address of an array of [**SID\_AND\_ATTRIBUTES**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) structures.</span></span> <span data-ttu-id="04fab-120">Эти структуры представляют группы, из которых клиент ограничен.</span><span class="sxs-lookup"><span data-stu-id="04fab-120">These structures represent the groups from which the client is restricted.</span></span>

</dd> <dt>

<span data-ttu-id="04fab-121">*престриктедсидкаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="04fab-121">*pRestrictedSidCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04fab-122">Количество структур в *псидрестриктедаттраррай*.</span><span class="sxs-lookup"><span data-stu-id="04fab-122">The number of structures in *pSidRestrictedAttrArray*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04fab-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="04fab-123">Return value</span></span>

<span data-ttu-id="04fab-124">Если функция успешно возвращает список идентификаторов безопасности, возвращается значение **true**.</span><span class="sxs-lookup"><span data-stu-id="04fab-124">If the function successfully returns a list of SIDs, the return value is **TRUE**.</span></span>

<span data-ttu-id="04fab-125">Если функция завершается ошибкой, возвращается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="04fab-125">If the function fails, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="04fab-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="04fab-126">Remarks</span></span>

<span data-ttu-id="04fab-127">Приложения также могут добавлять идентификаторы безопасности в контекст клиента путем вызова [**аусзаддсидстоконтекст**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext).</span><span class="sxs-lookup"><span data-stu-id="04fab-127">Applications can also add SIDs to the client context by calling [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext).</span></span>

<span data-ttu-id="04fab-128">Переменные атрибутов должны быть выражены в виде выражения при использовании с логическими операторами. в противном случае они оцениваются как неизвестные.</span><span class="sxs-lookup"><span data-stu-id="04fab-128">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="requirements"></a><span data-ttu-id="04fab-129">Требования</span><span class="sxs-lookup"><span data-stu-id="04fab-129">Requirements</span></span>



| <span data-ttu-id="04fab-130">Требование</span><span class="sxs-lookup"><span data-stu-id="04fab-130">Requirement</span></span> | <span data-ttu-id="04fab-131">Значение</span><span class="sxs-lookup"><span data-stu-id="04fab-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="04fab-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="04fab-132">Minimum supported client</span></span><br/> | <span data-ttu-id="04fab-133">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="04fab-133">Windows XP \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="04fab-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="04fab-134">Minimum supported server</span></span><br/> | <span data-ttu-id="04fab-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="04fab-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="04fab-136">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="04fab-136">Redistributable</span></span><br/>          | <span data-ttu-id="04fab-137">Пакет средств администрирования Windows Server 2003 в Windows XP</span><span class="sxs-lookup"><span data-stu-id="04fab-137">Windows Server 2003 Administration Tools Pack on Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="04fab-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="04fab-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04fab-139">Основные функции контроля доступа</span><span class="sxs-lookup"><span data-stu-id="04fab-139">Basic Access Control Functions</span></span>](authorization-functions.md)
</dt> <dt>

[<span data-ttu-id="04fab-140">**аусзаддсидстоконтекст**</span><span class="sxs-lookup"><span data-stu-id="04fab-140">**AuthzAddSidsToContext**</span></span>](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext)
</dt> <dt>

[<span data-ttu-id="04fab-141">**аусзкачедакцессчекк**</span><span class="sxs-lookup"><span data-stu-id="04fab-141">**AuthzCachedAccessCheck**</span></span>](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)
</dt> <dt>

[<span data-ttu-id="04fab-142">**аусзинитиализеконтекстфромаусзконтекст**</span><span class="sxs-lookup"><span data-stu-id="04fab-142">**AuthzInitializeContextFromAuthzContext**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext)
</dt> <dt>

[<span data-ttu-id="04fab-143">**аусзинитиализеконтекстфромсид**</span><span class="sxs-lookup"><span data-stu-id="04fab-143">**AuthzInitializeContextFromSid**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)
</dt> <dt>

[<span data-ttu-id="04fab-144">**аусзинитиализеконтекстфромтокен**</span><span class="sxs-lookup"><span data-stu-id="04fab-144">**AuthzInitializeContextFromToken**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken)
</dt> <dt>

[<span data-ttu-id="04fab-145">**аусзинитиализересаурцеманажер**</span><span class="sxs-lookup"><span data-stu-id="04fab-145">**AuthzInitializeResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> <dt>

[<span data-ttu-id="04fab-146">**Идентификатор безопасности \_ и \_ атрибуты**</span><span class="sxs-lookup"><span data-stu-id="04fab-146">**SID\_AND\_ATTRIBUTES**</span></span>](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes)
</dt> </dl>

 

