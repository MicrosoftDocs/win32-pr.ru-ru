---
description: Задает назначение наборов ЦП по умолчанию для потоков в указанном процессе. Создаваемые потоки, не имеющие наборов ЦП, явно заданные с помощью Сетсреадселектедкпусетс, будут наследовать наборы, заданные Сетпроцессдефаулткпусетс, автоматически.
ms.assetid: 7A510A8D-B06C-4B7B-9A87-BCFE0DE4D17B
title: Функция Сетпроцессдефаулткпусетс (Процесссреадапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetProcessDefaultCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 7998b20815529b41c5e29204c0ef50fbc15e6288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673737"
---
# <a name="setprocessdefaultcpusets-function"></a><span data-ttu-id="816c5-104">Функция Сетпроцессдефаулткпусетс</span><span class="sxs-lookup"><span data-stu-id="816c5-104">SetProcessDefaultCpuSets function</span></span>

<span data-ttu-id="816c5-105">Задает назначение наборов ЦП по умолчанию для потоков в указанном процессе.</span><span class="sxs-lookup"><span data-stu-id="816c5-105">Sets the default CPU Sets assignment for threads in the specified process.</span></span> <span data-ttu-id="816c5-106">Создаваемые потоки, не имеющие наборов ЦП, явно заданные с помощью [**сетсреадселектедкпусетс**](setthreadselectedcpusets.md), будут наследовать наборы, заданные **сетпроцессдефаулткпусетс** , автоматически.</span><span class="sxs-lookup"><span data-stu-id="816c5-106">Threads that are created, which don’t have CPU Sets explicitly set using [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md), will inherit the sets specified by **SetProcessDefaultCpuSets** automatically.</span></span>

## <a name="syntax"></a><span data-ttu-id="816c5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="816c5-107">Syntax</span></span>


```C++
BOOL WINAPI SetProcessDefaultCpuSets(
  _In_     HANDLE Process,
  _In_opt_ ULONG  CpuSetIds,
  _In_     ULONG  CpuSetIdCound
);
```



## <a name="parameters"></a><span data-ttu-id="816c5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="816c5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="816c5-109">*Обработка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="816c5-109">*Process* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="816c5-110">Указывает процесс, для которого задаются наборы ЦП по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="816c5-110">Specifies the process for which to set the default CPU Sets.</span></span> <span data-ttu-id="816c5-111">Этот обработчик должен иметь право на \_ \_ \_ доступ к ограниченным сведениям.</span><span class="sxs-lookup"><span data-stu-id="816c5-111">This handle must have the PROCESS\_SET\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="816c5-112">Значение, возвращаемое функцией [**жеткуррентпроцесс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) , также можно указать здесь.</span><span class="sxs-lookup"><span data-stu-id="816c5-112">The value returned by [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) can also be specified here.</span></span>

</dd> <dt>

<span data-ttu-id="816c5-113">*Кпусетидс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="816c5-113">*CpuSetIds* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="816c5-114">Указывает список идентификаторов наборов ЦП, которые необходимо задать в качестве набора ЦП процесса по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="816c5-114">Specifies the list of CPU Set IDs to set as the process default CPU set.</span></span> <span data-ttu-id="816c5-115">Если это значение равно NULL, **сетпроцессдефаулткпусетс** удаляет любое назначение.</span><span class="sxs-lookup"><span data-stu-id="816c5-115">If this is NULL, the **SetProcessDefaultCpuSets** clears out any assignment.</span></span>

</dd> <dt>

<span data-ttu-id="816c5-116">*Кпусетидкаунд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="816c5-116">*CpuSetIdCound* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="816c5-117">Указывает количество идентификаторов в списке, переданном в аргументе **кпусетидс** .</span><span class="sxs-lookup"><span data-stu-id="816c5-117">Specifies the number of IDs in the list passed in the **CpuSetIds** argument.</span></span> <span data-ttu-id="816c5-118">Если это значение равно NULL, то оно должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="816c5-118">If that value is NULL, this should be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="816c5-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="816c5-119">Return value</span></span>

<span data-ttu-id="816c5-120">Эта функция не может завершиться ошибкой, если переданы допустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="816c5-120">This function cannot fail when passed valid parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="816c5-121">Требования</span><span class="sxs-lookup"><span data-stu-id="816c5-121">Requirements</span></span>



| <span data-ttu-id="816c5-122">Требование</span><span class="sxs-lookup"><span data-stu-id="816c5-122">Requirement</span></span> | <span data-ttu-id="816c5-123">Значение</span><span class="sxs-lookup"><span data-stu-id="816c5-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="816c5-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="816c5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="816c5-125">\[Приложения UWP для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="816c5-125">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="816c5-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="816c5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="816c5-127">\[Приложения UWP для классических приложений Windows Server 2016 \|\]</span><span class="sxs-lookup"><span data-stu-id="816c5-127">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="816c5-128">Header</span><span class="sxs-lookup"><span data-stu-id="816c5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="816c5-129"><dt>Процесссреадсапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="816c5-129"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="816c5-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="816c5-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="816c5-131"><dt>Windows. h</dt></span><span class="sxs-lookup"><span data-stu-id="816c5-131"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="816c5-132">DLL</span><span class="sxs-lookup"><span data-stu-id="816c5-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="816c5-133"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="816c5-133"><dt>Kernel32.dll</dt></span></span> </dl>       |



 

 
