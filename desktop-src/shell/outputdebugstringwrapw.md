---
description: Отправляет в отладчик строку в Юникоде для вывода.
ms.assetid: 26cf4750-8ca1-4a9a-8378-d65ed288b358
title: Функция Аутпутдебугстрингврапв (Шлвапип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OutputDebugStringWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: e8213aee48a90a816e2968aac115159472ed7b8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997778"
---
# <a name="outputdebugstringwrapw-function"></a><span data-ttu-id="2532b-103">Функция Аутпутдебугстрингврапв</span><span class="sxs-lookup"><span data-stu-id="2532b-103">OutputDebugStringWrapW function</span></span>

<span data-ttu-id="2532b-104">\[Эта функция доступна для использования в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2532b-104">\[This function is available for use in Windows XP.</span></span> <span data-ttu-id="2532b-105">Она может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="2532b-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="2532b-106">Используйте [**аутпутдебугстрингв**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) на своем месте.\]</span><span class="sxs-lookup"><span data-stu-id="2532b-106">Use [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) in its place.\]</span></span>

<span data-ttu-id="2532b-107">Отправляет в отладчик строку в Юникоде для вывода.</span><span class="sxs-lookup"><span data-stu-id="2532b-107">Sends a Unicode string to the debugger for display.</span></span>

> [!Note]  
> <span data-ttu-id="2532b-108">**Аутпутдебугстрингврапв** — это оболочка для функции **аутпутдебугстрингв** .</span><span class="sxs-lookup"><span data-stu-id="2532b-108">**OutputDebugStringWrapW** is a wrapper for the **OutputDebugStringW** function.</span></span> <span data-ttu-id="2532b-109">Дополнительные сведения об использовании см. на странице [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) .</span><span class="sxs-lookup"><span data-stu-id="2532b-109">See the [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="2532b-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2532b-110">Syntax</span></span>


```C++
void OutputDebugStringWrapW(
  _In_ LPCWSTR lpOutputString
);
```



## <a name="parameters"></a><span data-ttu-id="2532b-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="2532b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2532b-112">*лпаутпутстринг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2532b-112">*lpOutputString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2532b-113">Тип: **лпквстр**</span><span class="sxs-lookup"><span data-stu-id="2532b-113">Type: **LPCWSTR**</span></span>

<span data-ttu-id="2532b-114">Указатель на строку в Юникоде, заканчивающуюся нулем и отображаемую.</span><span class="sxs-lookup"><span data-stu-id="2532b-114">A pointer to the null-terminated Unicode string to be displayed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2532b-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2532b-115">Return value</span></span>

<span data-ttu-id="2532b-116">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2532b-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2532b-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="2532b-117">Remarks</span></span>

<span data-ttu-id="2532b-118">**Аутпутдебугстрингврапв** предоставляет возможность использования строк Юникода в операционных системах до Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2532b-118">**OutputDebugStringWrapW** provides the ability to use Unicode strings in operating systems prior to Windows XP.</span></span> <span data-ttu-id="2532b-119">Предпочтительным методом является использование [**аутпутдебугстрингв**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) в сочетании с уровнем Майкрософт для Юникода (мслу).</span><span class="sxs-lookup"><span data-stu-id="2532b-119">The preferred method is to use [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="2532b-120">**Аутпутдебугстрингврапв** должен вызываться напрямую из Shlwapi.dll с использованием порядкового номера 115.</span><span class="sxs-lookup"><span data-stu-id="2532b-120">**OutputDebugStringWrapW** must be called directly from Shlwapi.dll, using ordinal 115.</span></span>

<span data-ttu-id="2532b-121">Если в приложении нет отладчика, системный отладчик отображает строку.</span><span class="sxs-lookup"><span data-stu-id="2532b-121">If the application has no debugger, the system debugger displays the string.</span></span> <span data-ttu-id="2532b-122">Если в приложении нет отладчика, а системный отладчик неактивен, **аутпутдебугстрингврапв** не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="2532b-122">If the application has no debugger and the system debugger is not active, **OutputDebugStringWrapW** does nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="2532b-123">Требования</span><span class="sxs-lookup"><span data-stu-id="2532b-123">Requirements</span></span>



| <span data-ttu-id="2532b-124">Требование</span><span class="sxs-lookup"><span data-stu-id="2532b-124">Requirement</span></span> | <span data-ttu-id="2532b-125">Значение</span><span class="sxs-lookup"><span data-stu-id="2532b-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2532b-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2532b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2532b-127">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2532b-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2532b-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2532b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2532b-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2532b-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2532b-130">Header</span><span class="sxs-lookup"><span data-stu-id="2532b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="2532b-131"><dt>Шлвапип. h</dt></span><span class="sxs-lookup"><span data-stu-id="2532b-131"><dt>Shlwapip.h</dt></span></span> </dl>                         |
| <span data-ttu-id="2532b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2532b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2532b-133"><dt>Shlwapi.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="2532b-133"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2532b-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2532b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2532b-135">**OutputDebugString**</span><span class="sxs-lookup"><span data-stu-id="2532b-135">**OutputDebugString**</span></span>](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)
</dt> </dl>

 

 
