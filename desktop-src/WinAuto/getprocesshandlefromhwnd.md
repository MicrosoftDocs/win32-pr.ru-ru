---
title: Функция Жетпроцесшандлефромхвнд
description: Извлекает маркер процесса из маркера окна.
ms.assetid: 173579d2-c930-402c-81c7-761b063b5b51
keywords:
- Специальные возможности Windows для функции Жетпроцесшандлефромхвнд
topic_type:
- apiref
api_name:
- GetProcessHandleFromHwnd
api_location:
- Oleacc.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bee00f36f236396816e7bb54cadbe6914f3437e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135991"
---
# <a name="getprocesshandlefromhwnd-function"></a><span data-ttu-id="eebaa-104">Функция Жетпроцесшандлефромхвнд</span><span class="sxs-lookup"><span data-stu-id="eebaa-104">GetProcessHandleFromHwnd function</span></span>

<span data-ttu-id="eebaa-105">Извлекает маркер процесса из маркера окна.</span><span class="sxs-lookup"><span data-stu-id="eebaa-105">Retrieves a process handle from a window handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="eebaa-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eebaa-106">Syntax</span></span>


```C++
HANDLE WINAPI GetProcessHandleFromHwnd(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="eebaa-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="eebaa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eebaa-108">*HWND* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eebaa-108">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eebaa-109">Тип: **[ **HWND**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eebaa-109">Type: **[**HWND**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="eebaa-110">Дескриптор окна.</span><span class="sxs-lookup"><span data-stu-id="eebaa-110">The window handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eebaa-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eebaa-111">Return value</span></span>

<span data-ttu-id="eebaa-112">Тип: **[ **Handle**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eebaa-112">Type: **[**HANDLE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="eebaa-113">В случае успеха возвращает маркер процесса, владеющего окном.</span><span class="sxs-lookup"><span data-stu-id="eebaa-113">If successful, returns the handle of the process that owns the window.</span></span>

<span data-ttu-id="eebaa-114">Если это не удалось, возвращает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="eebaa-114">If not successful, returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="eebaa-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eebaa-115">Remarks</span></span>

<span data-ttu-id="eebaa-116">В предыдущих версиях операционной системы процесс мог открыть другой процесс (например, для доступа к его памяти) с помощью [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess).</span><span class="sxs-lookup"><span data-stu-id="eebaa-116">In previous versions of the operating system, a process could open another process (to access its memory, for example) using [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess).</span></span> <span data-ttu-id="eebaa-117">Эта функция будет выполнена успешно, если вызывающая сторона имеет соответствующие привилегии. как правило, вызывающий и целевой процессы должны быть одного пользователя.</span><span class="sxs-lookup"><span data-stu-id="eebaa-117">This function succeeds if the caller has appropriate privileges; usually the caller and target process must be the same user.</span></span>

<span data-ttu-id="eebaa-118">Однако в Windows Vista [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) завершается ошибкой в сценарии, где вызывающий объект имеет UIAccess, и целевой процесс повышается.</span><span class="sxs-lookup"><span data-stu-id="eebaa-118">On Windows Vista, however, [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) fails in the scenario where the caller has UIAccess, and the target process is elevated.</span></span> <span data-ttu-id="eebaa-119">В этом случае владелец целевого процесса находится в группе Администраторы, но вызывающий процесс выполняется с маркером с ограниченным доступом, поэтому не имеет членства в этой группе и запрещает доступ к процессу с повышенными правами.</span><span class="sxs-lookup"><span data-stu-id="eebaa-119">In this case, the owner of the target process is in the Administrators group, but the calling process is running with the restricted token, so does not have membership in this group, and is denied access to the elevated process.</span></span> <span data-ttu-id="eebaa-120">Однако если вызывающий объект имеет UIAccess, то он может использовать обработчик Windows для внедрения кода в целевой процесс, а в рамках целевого процесса отправить его обратно вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="eebaa-120">If the caller has UIAccess, however, they can use a windows hook to inject code into the target process, and from within the target process, send a handle back to the caller.</span></span>

<span data-ttu-id="eebaa-121">**Жетпроцесшандлефромхвнд** — это удобная функция, которая использует этот метод для получения дескриптора процесса, владеющего указанным HWND.</span><span class="sxs-lookup"><span data-stu-id="eebaa-121">**GetProcessHandleFromHwnd** is a convenience function that uses this technique to obtain the handle of the process that owns the specified HWND.</span></span> <span data-ttu-id="eebaa-122">Обратите внимание, что она выполняется только в тех случаях, когда вызывающий и целевой процессы выполняются как один и тот же пользователь.</span><span class="sxs-lookup"><span data-stu-id="eebaa-122">Note that it only succeeds in cases where the caller and target process are running as the same user.</span></span> <span data-ttu-id="eebaa-123">Возвращенный обработчик имеет следующие привилегии: Process \_ DUP обработка операции виртуальной машины обработка виртуальной машины процесс \_ \| чтения виртуальной \_ \_ \| \_ \_ \| \_ машины \_ запись \| Синхронизация.</span><span class="sxs-lookup"><span data-stu-id="eebaa-123">The returned handle has the following privileges: PROCESS\_DUP\_HANDLE \| PROCESS\_VM\_OPERATION \| PROCESS\_VM\_READ \| PROCESS\_VM\_WRITE \| SYNCHRONIZE.</span></span> <span data-ttu-id="eebaa-124">Если требуются другие привилегии, то вместо использования этой функции может потребоваться реализовать методику привязки явным образом.</span><span class="sxs-lookup"><span data-stu-id="eebaa-124">If other privileges are required, it may be necessary to implement the hooking technique explicitly instead of using this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="eebaa-125">Требования</span><span class="sxs-lookup"><span data-stu-id="eebaa-125">Requirements</span></span>



| <span data-ttu-id="eebaa-126">Требование</span><span class="sxs-lookup"><span data-stu-id="eebaa-126">Requirement</span></span> | <span data-ttu-id="eebaa-127">Значение</span><span class="sxs-lookup"><span data-stu-id="eebaa-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eebaa-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eebaa-128">Minimum supported client</span></span><br/> | <span data-ttu-id="eebaa-129">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="eebaa-129">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="eebaa-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eebaa-130">Minimum supported server</span></span><br/> | <span data-ttu-id="eebaa-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eebaa-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eebaa-132">DLL</span><span class="sxs-lookup"><span data-stu-id="eebaa-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eebaa-133"><dt>Oleacc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eebaa-133"><dt>Oleacc.dll</dt></span></span> </dl> |



 

