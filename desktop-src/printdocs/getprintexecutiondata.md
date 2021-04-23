---
description: Жетпринтексекутиондата извлекает текущий контекст печати.
ms.assetid: bb9506aa-a0da-46bc-a86a-84a79587cd50
title: Функция Жетпринтексекутиондата (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintExecutionData
api_type:
- DllExport
api_location:
- winspool.drv
ms.openlocfilehash: a1b2f2674c9ef186338c91ed2e4500d8408964d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693601"
---
# <a name="getprintexecutiondata-function"></a><span data-ttu-id="a8e55-103">Функция Жетпринтексекутиондата</span><span class="sxs-lookup"><span data-stu-id="a8e55-103">GetPrintExecutionData function</span></span>

<span data-ttu-id="a8e55-104">**Жетпринтексекутиондата** извлекает текущий контекст печати.</span><span class="sxs-lookup"><span data-stu-id="a8e55-104">The **GetPrintExecutionData** retrieves the current print context.</span></span>

> [!Note]  
> <span data-ttu-id="a8e55-105">Эта функция предназначена для использования драйверами принтеров, которые выполняются в контексте диспетчера очереди печати.</span><span class="sxs-lookup"><span data-stu-id="a8e55-105">This function is intended for use by printer drivers that are running in the context of the print spooler.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a8e55-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a8e55-106">Syntax</span></span>


```C++
BOOL WINAPI GetPrintExecutionData(
  _Out_ PRINT_EXECUTION_DATA *pData
);
```



## <a name="parameters"></a><span data-ttu-id="a8e55-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a8e55-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8e55-108">*pData* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a8e55-108">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8e55-109">Указатель на переменную, которая получает адрес структуры [**\_ \_ данных выполнения печати**](print-execution-data.md) .</span><span class="sxs-lookup"><span data-stu-id="a8e55-109">A pointer to a variable that receives the address of the [**PRINT\_EXECUTION\_DATA**](print-execution-data.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8e55-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a8e55-110">Return value</span></span>

<span data-ttu-id="a8e55-111">Возвращает **значение true** , если функция выполнена. в противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="a8e55-111">Returns **TRUE** if the function succeeds; otherwise **FALSE**.</span></span> <span data-ttu-id="a8e55-112">Если возвращаемое значение равно **false**, вызовите [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) , чтобы получить состояние ошибки.</span><span class="sxs-lookup"><span data-stu-id="a8e55-112">If the return value is **FALSE**, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get the error status.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8e55-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a8e55-113">Remarks</span></span>

<span data-ttu-id="a8e55-114">Драйверы принтера должны вызывать [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) в модуле винспул. drv для получения адреса функции **жетпринтексекутиондата** , так как **Жетпринтексекутиондата** не поддерживается в Windows Vista и более ранних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="a8e55-114">Printer drivers should call [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) on the winspool.drv module to get the address of the **GetPrintExecutionData** function because **GetPrintExecutionData** is not supported on Windows Vista or earlier versions of Windows.</span></span>

<span data-ttu-id="a8e55-115">**Жетпринтексекутиондата** не выполняется, только если значение *pData* равно **null**.</span><span class="sxs-lookup"><span data-stu-id="a8e55-115">**GetPrintExecutionData** only fails if the value of *pData* is **NULL**.</span></span>

<span data-ttu-id="a8e55-116">Значение элемента **клиентапппид** [**\_ \_ данных выполнения печати**](print-execution-data.md) имеет смысл только в том случае, если значение **context** является **\_ контекстом выполнения печати \_ \_ WOW64**.</span><span class="sxs-lookup"><span data-stu-id="a8e55-116">The value of the **clientAppPID** member of [**PRINT\_EXECUTION\_DATA**](print-execution-data.md) is only meaningful if the value of **context** is **PRINT\_EXECUTION\_CONTEXT\_WOW64**.</span></span> <span data-ttu-id="a8e55-117">Если значение **context** не является **\_ контекстом выполнения вывода \_ \_ WOW64**, значение **клиентапппид** равно 0.</span><span class="sxs-lookup"><span data-stu-id="a8e55-117">If the value of **context** is not **PRINT\_EXECUTION\_CONTEXT\_WOW64**, the value of **clientAppPID** is 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8e55-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a8e55-118">Requirements</span></span>



| <span data-ttu-id="a8e55-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a8e55-119">Requirement</span></span> | <span data-ttu-id="a8e55-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a8e55-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8e55-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a8e55-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a8e55-122">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a8e55-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="a8e55-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a8e55-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a8e55-124">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a8e55-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="a8e55-125">Header</span><span class="sxs-lookup"><span data-stu-id="a8e55-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8e55-126"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8e55-126"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a8e55-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a8e55-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8e55-128"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="a8e55-128"><dt>Winspool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="a8e55-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8e55-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8e55-130">**Функция**</span><span class="sxs-lookup"><span data-stu-id="a8e55-130">**GetLastError**</span></span>](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="a8e55-131">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="a8e55-131">**GetProcAddress**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="a8e55-132">**\_контекст выполнения \_ печати**</span><span class="sxs-lookup"><span data-stu-id="a8e55-132">**PRINT\_EXECUTION\_CONTEXT**</span></span>](print-execution-context.md)
</dt> <dt>

[<span data-ttu-id="a8e55-133">**Печать \_ \_ данных выполнения**</span><span class="sxs-lookup"><span data-stu-id="a8e55-133">**PRINT\_EXECUTION\_DATA**</span></span>](print-execution-data.md)
</dt> </dl>

 

