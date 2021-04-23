---
description: Определяемая приложением функция, которая освобождает память, выделенную функцией Аусзкомпутеграупскаллбакк. Аусзфриграупскаллбакк — это заполнитель для имени определяемой приложением функции.
ms.assetid: 5563311c-2bd1-4e96-ba0a-5a4225050f77
title: Функция обратного вызова Аусзфриграупскаллбакк
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzFreeGroupsCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 7d8942acbc67f122ea79f0b9e98793628b5f21f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819457"
---
# <a name="authzfreegroupscallback-callback-function"></a><span data-ttu-id="2eb6a-104">Функция обратного вызова Аусзфриграупскаллбакк</span><span class="sxs-lookup"><span data-stu-id="2eb6a-104">AuthzFreeGroupsCallback callback function</span></span>

<span data-ttu-id="2eb6a-105">Функция **аусзфриграупскаллбакк** является определяемой приложением функцией, которая освобождает память, выделенную функцией [**аусзкомпутеграупскаллбакк**](authzcomputegroupscallback.md) .</span><span class="sxs-lookup"><span data-stu-id="2eb6a-105">The **AuthzFreeGroupsCallback** function is an application-defined function that frees memory allocated by the [**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md) function.</span></span> <span data-ttu-id="2eb6a-106">**Аусзфриграупскаллбакк** — это заполнитель для имени определяемой приложением функции.</span><span class="sxs-lookup"><span data-stu-id="2eb6a-106">**AuthzFreeGroupsCallback** is a placeholder for the application-defined function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="2eb6a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2eb6a-107">Syntax</span></span>


```C++
void CALLBACK AuthzFreeGroupsCallback(
  _In_ PSID_AND_ATTRIBUTES pSidAttrArray
);
```



## <a name="parameters"></a><span data-ttu-id="2eb6a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2eb6a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2eb6a-109">*псидаттраррай* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2eb6a-109">*pSidAttrArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2eb6a-110">Указатель на память, выделенную [**аусзкомпутеграупскаллбакк**](authzcomputegroupscallback.md).</span><span class="sxs-lookup"><span data-stu-id="2eb6a-110">A pointer to memory allocated by [**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2eb6a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2eb6a-111">Return value</span></span>

<span data-ttu-id="2eb6a-112">Эта функция обратного вызова не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2eb6a-112">This callback function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2eb6a-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2eb6a-113">Remarks</span></span>

<span data-ttu-id="2eb6a-114">Переменные атрибутов должны быть выражены в виде выражения при использовании с логическими операторами. в противном случае они оцениваются как неизвестные.</span><span class="sxs-lookup"><span data-stu-id="2eb6a-114">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="requirements"></a><span data-ttu-id="2eb6a-115">Требования</span><span class="sxs-lookup"><span data-stu-id="2eb6a-115">Requirements</span></span>



| <span data-ttu-id="2eb6a-116">Требование</span><span class="sxs-lookup"><span data-stu-id="2eb6a-116">Requirement</span></span> | <span data-ttu-id="2eb6a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="2eb6a-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="2eb6a-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2eb6a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2eb6a-119">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2eb6a-119">Windows XP \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="2eb6a-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2eb6a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2eb6a-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2eb6a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="2eb6a-122">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="2eb6a-122">Redistributable</span></span><br/>          | <span data-ttu-id="2eb6a-123">Пакет средств администрирования Windows Server 2003 в Windows XP</span><span class="sxs-lookup"><span data-stu-id="2eb6a-123">Windows Server 2003 Administration Tools Pack on Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2eb6a-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2eb6a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eb6a-125">Основные функции контроля доступа</span><span class="sxs-lookup"><span data-stu-id="2eb6a-125">Basic Access Control Functions</span></span>](authorization-functions.md)
</dt> <dt>

[<span data-ttu-id="2eb6a-126">**аусзкомпутеграупскаллбакк**</span><span class="sxs-lookup"><span data-stu-id="2eb6a-126">**AuthzComputeGroupsCallback**</span></span>](authzcomputegroupscallback.md)
</dt> </dl>

 

 




