---
description: Возвращает явное назначение набора ЦП указанного потока, если какое-либо назначение было задано с помощью API Сетсреадселектедкпусетс. Если явное присваивание не задано, Рекуиредидкаунт имеет значение 0, а функция возвращает значение TRUE.
ms.assetid: 9ACF72F8-A64C-4FFF-B340-C920E80238CA
title: Функция Жетсреадселектедкпусетс (Процесссреадапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetThreadSelectedCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 26530b1fbb9694ed7ecc8c4e457ad023e971a470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080788"
---
# <a name="getthreadselectedcpusets-function"></a><span data-ttu-id="eb776-104">Функция Жетсреадселектедкпусетс</span><span class="sxs-lookup"><span data-stu-id="eb776-104">GetThreadSelectedCpuSets function</span></span>

<span data-ttu-id="eb776-105">Возвращает явное назначение набора ЦП указанного потока, если какое-либо назначение было задано с помощью API [**сетсреадселектедкпусетс**](setthreadselectedcpusets.md) .</span><span class="sxs-lookup"><span data-stu-id="eb776-105">Returns the explicit CPU Set assignment of the specified thread, if any assignment was set using the [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md) API.</span></span> <span data-ttu-id="eb776-106">Если явное присваивание не задано, **рекуиредидкаунт** имеет значение 0, а функция возвращает значение true.</span><span class="sxs-lookup"><span data-stu-id="eb776-106">If no explicit assignment is set, **RequiredIdCount** is set to 0 and the function returns TRUE.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb776-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eb776-107">Syntax</span></span>


```C++
BOOL WINAPI GetThreadSelectedCpuSets(
  _In_      HANDLE Thread,
  _Out_opt_ PULONG CpuSetIds,
  _In_      ULONG  CpuSetIdCount,
  _Out_     PULONG RequiredIdCount
);
```



## <a name="parameters"></a><span data-ttu-id="eb776-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="eb776-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb776-109">*Поток команд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eb776-109">*Thread* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb776-110">Указывает поток, для которого запрашиваются выбранные наборы ЦП.</span><span class="sxs-lookup"><span data-stu-id="eb776-110">Specifies the thread for which to query the selected CPU Sets.</span></span> <span data-ttu-id="eb776-111">Этот обработчик должен иметь \_ \_ право доступа к ограниченным данным в запросе потока \_ .</span><span class="sxs-lookup"><span data-stu-id="eb776-111">This handle must have the THREAD\_QUERY\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="eb776-112">Значение, возвращаемое функцией [**жеткуррентсреад**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) , также можно указать здесь.</span><span class="sxs-lookup"><span data-stu-id="eb776-112">The value returned by [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) can also be specified here.</span></span>

</dd> <dt>

<span data-ttu-id="eb776-113">*Кпусетидс* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="eb776-113">*CpuSetIds* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb776-114">Задает необязательный буфер для получения списка идентификаторов набора ЦП.</span><span class="sxs-lookup"><span data-stu-id="eb776-114">Specifies an optional buffer to retrieve the list of CPU Set identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="eb776-115">*Кпусетидкаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eb776-115">*CpuSetIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb776-116">Указывает Емкость буфера, указанного в **кпусетидс**.</span><span class="sxs-lookup"><span data-stu-id="eb776-116">Specifies the capacity of the buffer specified in **CpuSetIds**.</span></span> <span data-ttu-id="eb776-117">Если буфер равен NULL, это значение должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="eb776-117">If the buffer is NULL, this must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="eb776-118">*Рекуиредидкаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="eb776-118">*RequiredIdCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb776-119">Указывает требуемую Емкость буфера для хранения всего списка наборов ЦП, выбранных в потоке.</span><span class="sxs-lookup"><span data-stu-id="eb776-119">Specifies the required capacity of the buffer to hold the entire list of thread selected CPU Sets.</span></span> <span data-ttu-id="eb776-120">При успешном возвращении этот параметр указывает количество идентификаторов, заполняемых в буфер.</span><span class="sxs-lookup"><span data-stu-id="eb776-120">On successful return, this specifies the number of IDs filled into the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb776-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eb776-121">Return value</span></span>

<span data-ttu-id="eb776-122">Этот API возвращает значение TRUE в случае успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="eb776-122">This API returns TRUE on success.</span></span> <span data-ttu-id="eb776-123">Если буфер недостаточно велик, значение **GetLastError** не является ошибкой \_ \_ buffer.</span><span class="sxs-lookup"><span data-stu-id="eb776-123">If the buffer is not large enough, the **GetLastError** value is ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="eb776-124">Этот API не может завершиться ошибкой, если переданы допустимые параметры, и буфер возврата достаточно большой.</span><span class="sxs-lookup"><span data-stu-id="eb776-124">This API cannot fail when passed valid parameters and the return buffer is large enough.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb776-125">Требования</span><span class="sxs-lookup"><span data-stu-id="eb776-125">Requirements</span></span>



| <span data-ttu-id="eb776-126">Требование</span><span class="sxs-lookup"><span data-stu-id="eb776-126">Requirement</span></span> | <span data-ttu-id="eb776-127">Значение</span><span class="sxs-lookup"><span data-stu-id="eb776-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb776-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eb776-128">Minimum supported client</span></span><br/> | <span data-ttu-id="eb776-129">\[Приложения UWP для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="eb776-129">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="eb776-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eb776-130">Minimum supported server</span></span><br/> | <span data-ttu-id="eb776-131">\[Приложения UWP для классических приложений Windows Server 2016 \|\]</span><span class="sxs-lookup"><span data-stu-id="eb776-131">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="eb776-132">Header</span><span class="sxs-lookup"><span data-stu-id="eb776-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb776-133"><dt>Процесссреадсапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb776-133"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="eb776-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="eb776-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="eb776-135"><dt>Windows. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb776-135"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="eb776-136">DLL</span><span class="sxs-lookup"><span data-stu-id="eb776-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb776-137"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb776-137"><dt>Kernel32.dll</dt></span></span> </dl>       |



 

