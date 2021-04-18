---
description: Возвращает список наборов ЦП в наборе процессов по умолчанию, который был установлен с помощью Сетпроцессдефаулткпусетс. Если для данного процесса не заданы наборы ЦП по умолчанию, то для Рекуиредидкаунт устанавливается значение 0, а функция выполняется.
ms.assetid: 85DC5331-9EC0-4603-94FD-B49E725301B1
title: Функция Жетпроцессдефаулткпусетс (Процесссреадапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProcessDefaultCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: a5bd7c27b76efbbac923317837ac82b3a6700197
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673767"
---
# <a name="getprocessdefaultcpusets-function"></a><span data-ttu-id="aecb1-104">Функция Жетпроцессдефаулткпусетс</span><span class="sxs-lookup"><span data-stu-id="aecb1-104">GetProcessDefaultCpuSets function</span></span>

<span data-ttu-id="aecb1-105">Возвращает список наборов ЦП в наборе процессов по умолчанию, который был установлен с помощью [**сетпроцессдефаулткпусетс**](setprocessdefaultcpusets.md).</span><span class="sxs-lookup"><span data-stu-id="aecb1-105">Retrieves the list of CPU Sets in the process default set that was set by [**SetProcessDefaultCpuSets**](setprocessdefaultcpusets.md).</span></span> <span data-ttu-id="aecb1-106">Если для данного процесса не заданы наборы ЦП по умолчанию, то для **рекуиредидкаунт** устанавливается значение 0, а функция выполняется.</span><span class="sxs-lookup"><span data-stu-id="aecb1-106">If no default CPU Sets are set for a given process, then the **RequiredIdCount** is set to 0 and the function succeeds.</span></span>

## <a name="syntax"></a><span data-ttu-id="aecb1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aecb1-107">Syntax</span></span>


```C++
BOOL WINAPI GetProcessDefaultCpuSets(
  _In_      HANDLE Process,
  _Out_opt_ PULONG CpuSetIds,
  _In_      ULONG  CpuSetIdCount,
  _Out_     PULONG RequiredIdCount
);
```



## <a name="parameters"></a><span data-ttu-id="aecb1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="aecb1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aecb1-109">*Обработка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aecb1-109">*Process* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aecb1-110">Задает обработчик процесса для запроса.</span><span class="sxs-lookup"><span data-stu-id="aecb1-110">Specifies a process handle for the process to query.</span></span> <span data-ttu-id="aecb1-111">Этот обработчик должен иметь право на \_ \_ доступ к ограниченным данным Process \_ .</span><span class="sxs-lookup"><span data-stu-id="aecb1-111">This handle must have the PROCESS\_QUERY\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="aecb1-112">Значение, возвращаемое функцией [**жеткуррентпроцесс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) , также можно указать здесь.</span><span class="sxs-lookup"><span data-stu-id="aecb1-112">The value returned by [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) can also be specified here.</span></span>

</dd> <dt>

<span data-ttu-id="aecb1-113">*Кпусетидс* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="aecb1-113">*CpuSetIds* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="aecb1-114">Задает необязательный буфер для получения списка идентификаторов набора ЦП.</span><span class="sxs-lookup"><span data-stu-id="aecb1-114">Specifies an optional buffer to retrieve the list of CPU Set identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="aecb1-115">*Кпусетидкаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aecb1-115">*CpuSetIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aecb1-116">Указывает Емкость буфера, указанного в **кпусетидс**.</span><span class="sxs-lookup"><span data-stu-id="aecb1-116">Specifies the capacity of the buffer specified in **CpuSetIds**.</span></span> <span data-ttu-id="aecb1-117">Если буфер равен NULL, это значение должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="aecb1-117">If the buffer is NULL, this must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="aecb1-118">*Рекуиредидкаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="aecb1-118">*RequiredIdCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aecb1-119">Указывает требуемую Емкость буфера для хранения всего списка наборов ЦП по умолчанию процесса.</span><span class="sxs-lookup"><span data-stu-id="aecb1-119">Specifies the required capacity of the buffer to hold the entire list of process default CPU Sets.</span></span> <span data-ttu-id="aecb1-120">При успешном возвращении этот параметр указывает количество идентификаторов, заполняемых в буфер.</span><span class="sxs-lookup"><span data-stu-id="aecb1-120">On successful return, this specifies the number of IDs filled into the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aecb1-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aecb1-121">Return value</span></span>

<span data-ttu-id="aecb1-122">Этот API возвращает значение TRUE в случае успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="aecb1-122">This API returns TRUE on success.</span></span> <span data-ttu-id="aecb1-123">Если буфер недостаточно велик, API возвращает значение FALSE, а значением **GetLastError** является ошибка \_ недостаточно \_ буфера.</span><span class="sxs-lookup"><span data-stu-id="aecb1-123">If the buffer is not large enough the API returns FALSE, and the **GetLastError** value is ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="aecb1-124">Этот API не может завершиться ошибкой, если переданы допустимые параметры, и буфер возврата достаточно большой.</span><span class="sxs-lookup"><span data-stu-id="aecb1-124">This API cannot fail when passed valid parameters and the return buffer is large enough.</span></span>

## <a name="requirements"></a><span data-ttu-id="aecb1-125">Требования</span><span class="sxs-lookup"><span data-stu-id="aecb1-125">Requirements</span></span>



| <span data-ttu-id="aecb1-126">Требование</span><span class="sxs-lookup"><span data-stu-id="aecb1-126">Requirement</span></span> | <span data-ttu-id="aecb1-127">Значение</span><span class="sxs-lookup"><span data-stu-id="aecb1-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="aecb1-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aecb1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="aecb1-129">\[Приложения UWP для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="aecb1-129">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="aecb1-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aecb1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="aecb1-131">\[Приложения UWP для классических приложений Windows Server 2016 \|\]</span><span class="sxs-lookup"><span data-stu-id="aecb1-131">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="aecb1-132">Header</span><span class="sxs-lookup"><span data-stu-id="aecb1-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="aecb1-133"><dt>Процесссреадсапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="aecb1-133"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="aecb1-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="aecb1-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="aecb1-135"><dt>Windows. h</dt></span><span class="sxs-lookup"><span data-stu-id="aecb1-135"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="aecb1-136">DLL</span><span class="sxs-lookup"><span data-stu-id="aecb1-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aecb1-137"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aecb1-137"><dt>Kernel32.dll</dt></span></span> </dl>       |



 

