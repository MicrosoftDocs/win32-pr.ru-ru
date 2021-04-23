---
description: Завершает настройку буфера трассировки с необязательными полями для трассировок в стиле sprintf.
ms.assetid: 6c23e61c-0285-47ba-b614-b73bd001d552
title: Функция Сетасинктрацепарамсекс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetAsyncTraceParamsEx
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: e5f99af2e6226e39ecc06a1c4c2bb7f2ad3c3b8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648117"
---
# <a name="setasynctraceparamsex-function"></a><span data-ttu-id="e31a2-103">Функция Сетасинктрацепарамсекс</span><span class="sxs-lookup"><span data-stu-id="e31a2-103">SetAsyncTraceParamsEx function</span></span>

<span data-ttu-id="e31a2-104">Завершает настройку буфера трассировки с необязательными полями для трассировок в стиле **sprintf**.</span><span class="sxs-lookup"><span data-stu-id="e31a2-104">Finishes setting up a trace buffer with optional fields for **sprintf**-style traces.</span></span>

## <a name="syntax"></a><span data-ttu-id="e31a2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e31a2-105">Syntax</span></span>


```C++
int SetAsyncTraceParamsEx(
   LPSTR pszModule,
   LPSTR pszFile,
   int   lLine,
   LPSTR pszFunction,
   DWORD dwTraceMask
);
```



## <a name="parameters"></a><span data-ttu-id="e31a2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e31a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e31a2-107">*псзмодуле*</span><span class="sxs-lookup"><span data-stu-id="e31a2-107">*pszModule*</span></span> 
</dt> <dd>

<span data-ttu-id="e31a2-108">Имя модуля, связанного с трассировкой.</span><span class="sxs-lookup"><span data-stu-id="e31a2-108">The name of the module that is associated with the trace.</span></span>

</dd> <dt>

<span data-ttu-id="e31a2-109">*псзфиле*</span><span class="sxs-lookup"><span data-stu-id="e31a2-109">*pszFile*</span></span> 
</dt> <dd>

<span data-ttu-id="e31a2-110">Имя исходного файла, содержащего исключение.</span><span class="sxs-lookup"><span data-stu-id="e31a2-110">The name of the source file that contains the exception.</span></span>

</dd> <dt>

<span data-ttu-id="e31a2-111">*ллине*</span><span class="sxs-lookup"><span data-stu-id="e31a2-111">*lLine*</span></span> 
</dt> <dd>

<span data-ttu-id="e31a2-112">Номер строки исключения в исходном файле.</span><span class="sxs-lookup"><span data-stu-id="e31a2-112">The line number of the exception in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="e31a2-113">*псзфунктион*</span><span class="sxs-lookup"><span data-stu-id="e31a2-113">*pszFunction*</span></span> 
</dt> <dd>

<span data-ttu-id="e31a2-114">Имя функции для исключения.</span><span class="sxs-lookup"><span data-stu-id="e31a2-114">The function name of the exception.</span></span>

</dd> <dt>

<span data-ttu-id="e31a2-115">*двтрацемаск*</span><span class="sxs-lookup"><span data-stu-id="e31a2-115">*dwTraceMask*</span></span> 
</dt> <dd>

<span data-ttu-id="e31a2-116">Константа флага трассировки, представляющая один из доступных типов трассировки.</span><span class="sxs-lookup"><span data-stu-id="e31a2-116">A trace flag constant that represents one of the available trace types.</span></span> <span data-ttu-id="e31a2-117">Этот параметр может принимать любое из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e31a2-117">This parameter can be any of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e31a2-118"><span id="FATAL_TRACE_MASK"></span><span id="fatal_trace_mask"></span>**Неустранимая \_ Ошибка \_Маска трассировки** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="e31a2-118"><span id="FATAL_TRACE_MASK"></span><span id="fatal_trace_mask"></span>**FATAL\_TRACE\_MASK** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="e31a2-119"><span id="ERROR_TRACE_MASK"></span><span id="error_trace_mask"></span>**Ошибка при \_ \_Маска трассировки** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="e31a2-119"><span id="ERROR_TRACE_MASK"></span><span id="error_trace_mask"></span>**ERROR\_TRACE\_MASK** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="e31a2-120"><span id="DEBUG_TRACE_MASK"></span><span id="debug_trace_mask"></span>**Отладка \_ \_Маска трассировки** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="e31a2-120"><span id="DEBUG_TRACE_MASK"></span><span id="debug_trace_mask"></span>**DEBUG\_TRACE\_MASK** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="e31a2-121"><span id="STATE_TRACE_MASK"></span><span id="state_trace_mask"></span>**Состояние \_ \_Маска трассировки** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="e31a2-121"><span id="STATE_TRACE_MASK"></span><span id="state_trace_mask"></span>**STATE\_TRACE\_MASK** (0x00000008)</span></span>
</dt> <dt>

<span data-ttu-id="e31a2-122"><span id="FUNCT_TRACE_MASK"></span><span id="funct_trace_mask"></span>**Функция \_ Func \_Маска трассировки** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="e31a2-122"><span id="FUNCT_TRACE_MASK"></span><span id="funct_trace_mask"></span>**FUNCT\_TRACE\_MASK** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="e31a2-123"><span id="MESSAGE_TRACE_MASK"></span><span id="message_trace_mask"></span>**Сообщение об ошибке \_ \_Маска трассировки** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="e31a2-123"><span id="MESSAGE_TRACE_MASK"></span><span id="message_trace_mask"></span>**MESSAGE\_TRACE\_MASK** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="e31a2-124"><span id="ALL_TRACE_MASK"></span><span id="all_trace_mask"></span>**Все \_ \_Маска трассировки** (0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="e31a2-124"><span id="ALL_TRACE_MASK"></span><span id="all_trace_mask"></span>**ALL\_TRACE\_MASK** (0xFFFFFFFF)</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e31a2-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e31a2-125">Return value</span></span>

<span data-ttu-id="e31a2-126">Эта функция возвращает значение 1, если функция выполнена. в противном случае возвращается значение 0.</span><span class="sxs-lookup"><span data-stu-id="e31a2-126">This function returns 1 if the function succeeds; otherwise, it returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="e31a2-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e31a2-127">Remarks</span></span>

<span data-ttu-id="e31a2-128">Exstrace.dll является необязательным компонентом, который устанавливается с протоколом SMTP и протоколом NNTP.</span><span class="sxs-lookup"><span data-stu-id="e31a2-128">Exstrace.dll is an optional component that installs with the Simple Mail Transfer Protocol (SMTP) and the Network News Transfer Protocol (NNTP).</span></span>

<span data-ttu-id="e31a2-129">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="e31a2-129">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="e31a2-130">Требования</span><span class="sxs-lookup"><span data-stu-id="e31a2-130">Requirements</span></span>



| <span data-ttu-id="e31a2-131">Требование</span><span class="sxs-lookup"><span data-stu-id="e31a2-131">Requirement</span></span> | <span data-ttu-id="e31a2-132">Значение</span><span class="sxs-lookup"><span data-stu-id="e31a2-132">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e31a2-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e31a2-133">DLL</span></span><br/> | <dl> <span data-ttu-id="e31a2-134"><dt>Exstrace.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e31a2-134"><dt>Exstrace.dll</dt></span></span> </dl> |



 

 
