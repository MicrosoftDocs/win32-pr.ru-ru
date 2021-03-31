---
description: Извлекает маркер объекта для указанного объекта, связанного с указанным процессом.
ms.assetid: c7b371c3-02c0-4137-ad9d-dd07a74fe2a5
title: Функция Обфиндхандлефоробжект (Нтосп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObFindHandleForObject
api_type:
- LibDef
api_location:
- Ntoskrnl.lib
- Ntoskrnl.dll
ms.openlocfilehash: 7ba87d05d4264f3bb160bae16053a338e38e2145
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895557"
---
# <a name="obfindhandleforobject-function"></a><span data-ttu-id="49fdf-103">Функция Обфиндхандлефоробжект</span><span class="sxs-lookup"><span data-stu-id="49fdf-103">ObFindHandleForObject function</span></span>

<span data-ttu-id="49fdf-104">\[Эта функция устарела и может быть изменена или недоступна в будущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="49fdf-104">\[This function is obsolete and may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="49fdf-105">Старайтесь не использовать эту функцию.\]</span><span class="sxs-lookup"><span data-stu-id="49fdf-105">Avoid using this function.\]</span></span>

<span data-ttu-id="49fdf-106">Извлекает маркер объекта для указанного объекта, связанного с указанным процессом.</span><span class="sxs-lookup"><span data-stu-id="49fdf-106">Retrieves an object handle for the specified object associated with the specified process.</span></span>

## <a name="syntax"></a><span data-ttu-id="49fdf-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="49fdf-107">Syntax</span></span>


```C++
BOOLEAN WINAPI ObFindHandleForObject(
  _In_     PEPROCESS Process,
  _In_     PVOID     Object,
  _In_opt_ PVOID     Reserved1,
  _In_opt_ PVOID     Reserved2,
  _Out_    PHANDLE   Handle
);
```



## <a name="parameters"></a><span data-ttu-id="49fdf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="49fdf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49fdf-109">*Обработка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="49fdf-109">*Process* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49fdf-110">Процесс.</span><span class="sxs-lookup"><span data-stu-id="49fdf-110">The process.</span></span> <span data-ttu-id="49fdf-111">Этот маркер возвращается функцией **иожеткуррентпроцесс** или **псжеткуррентпроцесс** .</span><span class="sxs-lookup"><span data-stu-id="49fdf-111">This handle is returned by the **IoGetCurrentProcess** or **PsGetCurrentProcess** function.</span></span>

</dd> <dt>

<span data-ttu-id="49fdf-112">*Объект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="49fdf-112">*Object* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49fdf-113">Указатель на объект.</span><span class="sxs-lookup"><span data-stu-id="49fdf-113">A pointer to the object.</span></span>

</dd> <dt>

<span data-ttu-id="49fdf-114">*Reserved1* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="49fdf-114">*Reserved1* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="49fdf-115">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="49fdf-115">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="49fdf-116">*Reserved2* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="49fdf-116">*Reserved2* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="49fdf-117">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="49fdf-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="49fdf-118">*Обработчик* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="49fdf-118">*Handle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49fdf-119">Объектный обработчик.</span><span class="sxs-lookup"><span data-stu-id="49fdf-119">The object handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49fdf-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="49fdf-120">Return value</span></span>

<span data-ttu-id="49fdf-121">Функция возвращает **значение true** , если найдено совпадение, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="49fdf-121">The function returns **TRUE** if a match is found and **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="49fdf-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="49fdf-122">Remarks</span></span>

<span data-ttu-id="49fdf-123">Эта функция доступна в Ntoskrnl.exe и может вызываться только из режима ядра.</span><span class="sxs-lookup"><span data-stu-id="49fdf-123">This function is available in Ntoskrnl.exe and can be called only from kernel mode.</span></span> <span data-ttu-id="49fdf-124">Соответствующая библиотека импорта доступна в комплекте драйверов Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="49fdf-124">The corresponding import library is available through the Windows Driver Kit (WDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="49fdf-125">Требования</span><span class="sxs-lookup"><span data-stu-id="49fdf-125">Requirements</span></span>



| <span data-ttu-id="49fdf-126">Требование</span><span class="sxs-lookup"><span data-stu-id="49fdf-126">Requirement</span></span> | <span data-ttu-id="49fdf-127">Значение</span><span class="sxs-lookup"><span data-stu-id="49fdf-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49fdf-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="49fdf-128">Minimum supported client</span></span><br/> | <span data-ttu-id="49fdf-129">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="49fdf-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="49fdf-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="49fdf-130">Minimum supported server</span></span><br/> | <span data-ttu-id="49fdf-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="49fdf-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="49fdf-132">Header</span><span class="sxs-lookup"><span data-stu-id="49fdf-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="49fdf-133"><dt>Нтосп. h</dt></span><span class="sxs-lookup"><span data-stu-id="49fdf-133"><dt>Ntosp.h</dt></span></span> </dl>      |
| <span data-ttu-id="49fdf-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="49fdf-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="49fdf-135"><dt>Ntoskrnl. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49fdf-135"><dt>Ntoskrnl.lib</dt></span></span> </dl> |



 

 




