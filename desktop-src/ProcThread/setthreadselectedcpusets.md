---
description: Задает назначение выбранных наборов ЦП для указанного потока. Это назначение переопределяет назначение процесса по умолчанию, если оно задано.
ms.assetid: A73F7118-CC4A-45E6-869A-DFF6924D10C8
title: Функция Сетсреадселектедкпусетс (Процесссреадапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetThreadSelectedCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: b8b1f7c382d034e804d4ac7e63d58b8ec5853620
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909676"
---
# <a name="setthreadselectedcpusets-function"></a><span data-ttu-id="6d3fb-104">Функция Сетсреадселектедкпусетс</span><span class="sxs-lookup"><span data-stu-id="6d3fb-104">SetThreadSelectedCpuSets function</span></span>

<span data-ttu-id="6d3fb-105">Задает назначение выбранных наборов ЦП для указанного потока.</span><span class="sxs-lookup"><span data-stu-id="6d3fb-105">Sets the selected CPU Sets assignment for the specified thread.</span></span> <span data-ttu-id="6d3fb-106">Это назначение переопределяет назначение процесса по умолчанию, если оно задано.</span><span class="sxs-lookup"><span data-stu-id="6d3fb-106">This assignment overrides the process default assignment, if one is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d3fb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d3fb-107">Syntax</span></span>


```C++
BOOL WINAPI SetThreadSelectedCpuSets(
  _In_       HANDLE Thread,
  _In_ const ULONG  *CpuSetIds,
  _In_       ULONG  CpuSetIdCount
);
```



## <a name="parameters"></a><span data-ttu-id="6d3fb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d3fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d3fb-109">*Поток команд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d3fb-109">*Thread* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d3fb-110">Указывает поток, в котором следует задать назначение набора ЦП.</span><span class="sxs-lookup"><span data-stu-id="6d3fb-110">Specifies the thread on which to set the CPU Set assignment.</span></span> <span data-ttu-id="6d3fb-111">Этот обработчик должен иметь право на \_ \_ доступ к ограниченным данным в наборе потоков \_ .</span><span class="sxs-lookup"><span data-stu-id="6d3fb-111">This handle must have the THREAD\_SET\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="6d3fb-112">Можно также использовать значение, возвращаемое функцией [**жеткуррентсреад**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) .</span><span class="sxs-lookup"><span data-stu-id="6d3fb-112">The value returned by [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) can also be used.</span></span>

</dd> <dt>

<span data-ttu-id="6d3fb-113">*Кпусетидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d3fb-113">*CpuSetIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d3fb-114">Указывает список идентификаторов наборов ЦП, которые должны быть заданы в качестве выбранного в потоке набора ЦП.</span><span class="sxs-lookup"><span data-stu-id="6d3fb-114">Specifies the list of CPU Set IDs to set as the thread selected CPU set.</span></span> <span data-ttu-id="6d3fb-115">Если это значение равно NULL, API удаляет любое назначение, при этом возвращается к обработке назначения по умолчанию, если оно задано.</span><span class="sxs-lookup"><span data-stu-id="6d3fb-115">If this is NULL, the API clears out any assignment, reverting to process default assignment if one is set.</span></span>

</dd> <dt>

<span data-ttu-id="6d3fb-116">*Кпусетидкаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d3fb-116">*CpuSetIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d3fb-117">Указывает количество идентификаторов в списке, переданном в аргументе **кпусетидс** .</span><span class="sxs-lookup"><span data-stu-id="6d3fb-117">Specifies the number of IDs in the list passed in the **CpuSetIds** argument.</span></span> <span data-ttu-id="6d3fb-118">Если это значение равно NULL, то оно должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="6d3fb-118">If that value is NULL, this should be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d3fb-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6d3fb-119">Return value</span></span>

<span data-ttu-id="6d3fb-120">Эта функция не может завершиться ошибкой, если переданы допустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="6d3fb-120">This function cannot fail when passed valid parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d3fb-121">Требования</span><span class="sxs-lookup"><span data-stu-id="6d3fb-121">Requirements</span></span>



| <span data-ttu-id="6d3fb-122">Требование</span><span class="sxs-lookup"><span data-stu-id="6d3fb-122">Requirement</span></span> | <span data-ttu-id="6d3fb-123">Значение</span><span class="sxs-lookup"><span data-stu-id="6d3fb-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d3fb-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6d3fb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6d3fb-125">\[Приложения UWP для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="6d3fb-125">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="6d3fb-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6d3fb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6d3fb-127">\[Приложения UWP для классических приложений Windows Server 2016 \|\]</span><span class="sxs-lookup"><span data-stu-id="6d3fb-127">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="6d3fb-128">Header</span><span class="sxs-lookup"><span data-stu-id="6d3fb-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d3fb-129"><dt>Процесссреадсапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d3fb-129"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="6d3fb-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6d3fb-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="6d3fb-131"><dt>Windows. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d3fb-131"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="6d3fb-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6d3fb-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d3fb-133"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d3fb-133"><dt>Kernel32.dll</dt></span></span> </dl>       |



 

 
