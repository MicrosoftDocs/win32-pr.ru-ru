---
description: Сообщает службе диспетчера очереди печати, находится ли задание печати XPS в очереди печати или на этапе отрисовки и какая часть обработки в данный момент выполняется.
ms.assetid: 66f7483d-be98-410d-b0c7-430743397de2
title: Функция Репортжобпроцессингпрогресс (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReportJobProcessingProgress
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 327d2f7cffe2f90a5719de38cef4cd3fde17e086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998949"
---
# <a name="reportjobprocessingprogress-function"></a><span data-ttu-id="00ca5-103">Функция Репортжобпроцессингпрогресс</span><span class="sxs-lookup"><span data-stu-id="00ca5-103">ReportJobProcessingProgress function</span></span>

<span data-ttu-id="00ca5-104">Сообщает службе диспетчера очереди печати, находится ли задание печати XPS в очереди печати или на этапе отрисовки и какая часть обработки в данный момент выполняется.</span><span class="sxs-lookup"><span data-stu-id="00ca5-104">Reports to the Print Spooler service whether an XPS print job is in the spooling or the rendering phase and what part of the processing is currently underway.</span></span>

## <a name="syntax"></a><span data-ttu-id="00ca5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="00ca5-105">Syntax</span></span>


```C++
HRESULT ReportJobProcessingProgress(
  _In_ HANDLE                printerHandle,
  _In_ ULONG                 jobId,
       EPrintXPSJobOperation jobOperation,
       EPrintXPSJobProgress  jobProgress
);
```



## <a name="parameters"></a><span data-ttu-id="00ca5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="00ca5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00ca5-107">*принтерхандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="00ca5-107">*printerHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00ca5-108">Маркер принтера, для которого функция возвращает сведения.</span><span class="sxs-lookup"><span data-stu-id="00ca5-108">A printer handle for which the function is to retrieve information.</span></span> <span data-ttu-id="00ca5-109">Используйте функцию [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="00ca5-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="00ca5-110">Идентификатор *задания* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="00ca5-110">*jobId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00ca5-111">Определяет задание печати, для которого извлекаются данные.</span><span class="sxs-lookup"><span data-stu-id="00ca5-111">Identifies the print job for which to retrieve data.</span></span> <span data-ttu-id="00ca5-112">Чтобы получить идентификатор задания печати, используйте функцию [**AddJob**](addjob.md) или функцию [**стартдок**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) .</span><span class="sxs-lookup"><span data-stu-id="00ca5-112">Use the [**AddJob**](addjob.md) function or [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) function to get a print job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="00ca5-113">*жобоператион*</span><span class="sxs-lookup"><span data-stu-id="00ca5-113">*jobOperation*</span></span> 
</dt> <dd>

<span data-ttu-id="00ca5-114">Указывает, находится ли задание на этапе постановки в очередь или на этапе отрисовки.</span><span class="sxs-lookup"><span data-stu-id="00ca5-114">Specifies whether the job is in the spooling phase or the rendering phase.</span></span>

</dd> <dt>

<span data-ttu-id="00ca5-115">*жобпрогресс*</span><span class="sxs-lookup"><span data-stu-id="00ca5-115">*jobProgress*</span></span> 
</dt> <dd>

<span data-ttu-id="00ca5-116">Указывает, какая часть обработки в данный момент выполняется.</span><span class="sxs-lookup"><span data-stu-id="00ca5-116">Specifies what part of the processing is currently underway.</span></span> <span data-ttu-id="00ca5-117">Это значение относится к событиям в фазе буферизации или подготовки к просмотру в зависимости от значения *жобоператион*.</span><span class="sxs-lookup"><span data-stu-id="00ca5-117">This value refers to events in either the spooling or rendering phase depending on the value of *jobOperation*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00ca5-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="00ca5-118">Return value</span></span>

<span data-ttu-id="00ca5-119">Если операция выполнена успешно, возвращается значение S \_ ОК, в противном случае **HRESULT** будет содержать код ошибки.</span><span class="sxs-lookup"><span data-stu-id="00ca5-119">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="00ca5-120">Дополнительные сведения о кодах ошибок COM см. в разделе [Обработка ошибок](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="00ca5-120">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="00ca5-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="00ca5-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="00ca5-122">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="00ca5-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="00ca5-123">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="00ca5-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="00ca5-124">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="00ca5-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

> [!Note]  
> <span data-ttu-id="00ca5-125">**Репортжобпроцессингпрогресс** будет сообщать о ходе выполнения задания печати XPS только в том случае, если задание печати находится на этапе буферизации или подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="00ca5-125">**ReportJobProcessingProgress** will only report the progress of the XPS print job if the print job is in the spooling or rendering phase.</span></span> <span data-ttu-id="00ca5-126">**Репортжобпроцессингпрогресс** завершится ошибкой, если он вызывается, когда задание печати XPS не находится на этапе буферизации или подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="00ca5-126">**ReportJobProcessingProgress** will fail if it is called when the XPS print job is not in the spooling or rendering phase.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="00ca5-127">Требования</span><span class="sxs-lookup"><span data-stu-id="00ca5-127">Requirements</span></span>



| <span data-ttu-id="00ca5-128">Требование</span><span class="sxs-lookup"><span data-stu-id="00ca5-128">Requirement</span></span> | <span data-ttu-id="00ca5-129">Значение</span><span class="sxs-lookup"><span data-stu-id="00ca5-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00ca5-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="00ca5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="00ca5-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="00ca5-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="00ca5-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="00ca5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="00ca5-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="00ca5-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="00ca5-134">Header</span><span class="sxs-lookup"><span data-stu-id="00ca5-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="00ca5-135"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00ca5-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="00ca5-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="00ca5-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="00ca5-137"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00ca5-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="00ca5-138">DLL</span><span class="sxs-lookup"><span data-stu-id="00ca5-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00ca5-139"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00ca5-139"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="00ca5-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="00ca5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00ca5-141">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="00ca5-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="00ca5-142">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="00ca5-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="00ca5-143">**епринткспсжобоператион**</span><span class="sxs-lookup"><span data-stu-id="00ca5-143">**EPrintXPSJobOperation**</span></span>](eprintxpsjoboperation.md)
</dt> <dt>

[<span data-ttu-id="00ca5-144">**епринткспсжобпрогресс**</span><span class="sxs-lookup"><span data-stu-id="00ca5-144">**EPrintXPSJobProgress**</span></span>](eprintxpsjobprogress.md)
</dt> </dl>

 

