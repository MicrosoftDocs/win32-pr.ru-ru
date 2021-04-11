---
description: Функция Експертиндикатестатус указывает процент завершения анализа экспертов файла записи.
ms.assetid: 6dbaa6d3-6068-4a28-9d9f-bcc7a25da407
title: Функция Експертиндикатестатус (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertIndicateStatus
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ac707a774b667b96a4d612e9eaf7da2c779c0327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143810"
---
# <a name="expertindicatestatus-function"></a><span data-ttu-id="bf9ee-103">Функция Експертиндикатестатус</span><span class="sxs-lookup"><span data-stu-id="bf9ee-103">ExpertIndicateStatus function</span></span>

<span data-ttu-id="bf9ee-104">Функция **експертиндикатестатус** указывает процент завершения анализа файла записи экспертом.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-104">The **ExpertIndicateStatus** function indicates the percentage of completion of the expert's analysis of the capture file.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf9ee-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf9ee-105">Syntax</span></span>


```C++
DWORD WINAPI ExpertIndicateStatus(
  _In_  HEXPERTKEY              hExpertKey,
  _In_  EXPERTSTATUSENUMERATION Status,
  _In_  DWORD                   SubStatus,
  _In_  char                    *sztext,
  _Out_ long                    PercentDone
);
```



## <a name="parameters"></a><span data-ttu-id="bf9ee-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf9ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf9ee-107">*хексперткэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf9ee-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf9ee-108">Уникальный идентификатор эксперта.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-108">Unique expert identifier.</span></span> <span data-ttu-id="bf9ee-109">Сетевой монитор передает *хексперткэй* эксперту при вызове функции [Run](run.md) .</span><span class="sxs-lookup"><span data-stu-id="bf9ee-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="bf9ee-110">*Состояние* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf9ee-110">*Status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf9ee-111">Текущее состояние анализа.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-111">Current status of the analysis.</span></span> <span data-ttu-id="bf9ee-112">Укажите одно из следующих значений [експертстатусенумератион](expertstatusenumeration.md) .</span><span class="sxs-lookup"><span data-stu-id="bf9ee-112">Specify one of the following [EXPERTSTATUSENUMERATION](expertstatusenumeration.md) values.</span></span>



| <span data-ttu-id="bf9ee-113">Значение</span><span class="sxs-lookup"><span data-stu-id="bf9ee-113">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="bf9ee-114">Значение</span><span class="sxs-lookup"><span data-stu-id="bf9ee-114">Meaning</span></span>                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span><dl> <span data-ttu-id="bf9ee-115"><dt>**ЕКСПЕРТСТАТУС \_ неактивен**</dt></span><span class="sxs-lookup"><span data-stu-id="bf9ee-115"><dt>**EXPERTSTATUS\_INACTIVE**</dt></span></span> </dl> | <span data-ttu-id="bf9ee-116">Эксперт никогда не начал работу.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-116">The expert never started.</span></span> <br/>                                          |
| <span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span><dl> <span data-ttu-id="bf9ee-117"><dt>**ЕКСПЕРТСТАТУС \_ Запуск**</dt></span><span class="sxs-lookup"><span data-stu-id="bf9ee-117"><dt>**EXPERTSTATUS\_STARTING**</dt></span></span> </dl> | <span data-ttu-id="bf9ee-118">Эксперт начинает работу.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-118">The expert is starting.</span></span> <br/>                                            |
| <span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span><dl> <span data-ttu-id="bf9ee-119"><dt>**ЕКСПЕРТСТАТУС \_ работает**</dt></span><span class="sxs-lookup"><span data-stu-id="bf9ee-119"><dt>**EXPERTSTATUS\_RUNNING**</dt></span></span> </dl>    | <span data-ttu-id="bf9ee-120">Эксперт работает нормально.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-120">The expert is running normally.</span></span> <br/>                                    |
| <span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span><dl> <span data-ttu-id="bf9ee-121"><dt>**\_проблема експертстатус**</dt></span><span class="sxs-lookup"><span data-stu-id="bf9ee-121"><dt>**EXPERTSTATUS\_PROBLEM**</dt></span></span> </dl>    | <span data-ttu-id="bf9ee-122">Проблема, указанная в параметре подсостояния, прекратила работу эксперта.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-122">A problem specified in the SubStatus parameter stopped the expert.</span></span> <br/> |
| <span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span><dl> <span data-ttu-id="bf9ee-123"><dt>**ЕКСПЕРТСТАТУС \_ прервана**</dt></span><span class="sxs-lookup"><span data-stu-id="bf9ee-123"><dt>**EXPERTSTATUS\_ABORTED**</dt></span></span> </dl>    | <span data-ttu-id="bf9ee-124">Сетевой монитор был остановлен эксперт.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-124">Network Monitor stopped the expert.</span></span> <br/>                                |
| <span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span><dl> <span data-ttu-id="bf9ee-125"><dt>**ЕКСПЕРТСТАТУС \_ Готово**</dt></span><span class="sxs-lookup"><span data-stu-id="bf9ee-125"><dt>**EXPERTSTATUS\_DONE**</dt></span></span> </dl>             | <span data-ttu-id="bf9ee-126">Эксперт успешно завершил анализ.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-126">The expert finished the analysis successfully.</span></span> <br/>                     |



 

</dd> <dt>

<span data-ttu-id="bf9ee-127">*Подсостояние* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf9ee-127">*SubStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf9ee-128">Расширение или уточнение сведений, предоставленных параметром *Status* .</span><span class="sxs-lookup"><span data-stu-id="bf9ee-128">Extension or clarification of information provided by the *Status* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="bf9ee-129">*сзтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf9ee-129">*sztext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf9ee-130">Необязательный индикатор состояния текста.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-130">Optional text status indicator.</span></span>

<span data-ttu-id="bf9ee-131">Значение этого параметра может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-131">This parameter value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bf9ee-132">*PercentDone* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bf9ee-132">*PercentDone* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf9ee-133">Процент данных записи, обработанных экспертом.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-133">Percentage of the capture data that the expert has processed.</span></span>

<span data-ttu-id="bf9ee-134">Когда эксперт успешно завершает анализ файла записи, система устанавливает в процентах значение 100.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-134">When the expert successfully completes analysis of a capture file, the system sets the percentage to 100.</span></span> <span data-ttu-id="bf9ee-135">Любое число больше 99 будет игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-135">Any number greater than 99 will be ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf9ee-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf9ee-136">Return value</span></span>

<span data-ttu-id="bf9ee-137">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-137">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="bf9ee-138">Если функция завершается неудачно, возвращается значение НМЕРР Expert ( \_ эксперт). \_ эксперт должен немедленно очистить и вернуться, не выполняя захват.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-138">If the function is unsuccessful, the return value is NMERR\_EXPERT\_TERMINATE; the expert must immediately clean up and return without completing the capture.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf9ee-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bf9ee-139">Remarks</span></span>

<span data-ttu-id="bf9ee-140">Функция **експертиндикатестатус** может вызываться экспертами, реализующими функцию [запуска](run.md) или [настройки](configure.md) экспорта.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-140">The **ExpertIndicateStatus** function can only be called by experts that implement the [Run](run.md) or [Configure](configure.md) export function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf9ee-141">Требования</span><span class="sxs-lookup"><span data-stu-id="bf9ee-141">Requirements</span></span>



| <span data-ttu-id="bf9ee-142">Требование</span><span class="sxs-lookup"><span data-stu-id="bf9ee-142">Requirement</span></span> | <span data-ttu-id="bf9ee-143">Значение</span><span class="sxs-lookup"><span data-stu-id="bf9ee-143">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bf9ee-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bf9ee-144">Minimum supported client</span></span><br/> | <span data-ttu-id="bf9ee-145">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bf9ee-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="bf9ee-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bf9ee-146">Minimum supported server</span></span><br/> | <span data-ttu-id="bf9ee-147">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bf9ee-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bf9ee-148">Заголовок</span><span class="sxs-lookup"><span data-stu-id="bf9ee-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf9ee-149"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf9ee-149"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="bf9ee-150">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bf9ee-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="bf9ee-151"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf9ee-151"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="bf9ee-152">DLL</span><span class="sxs-lookup"><span data-stu-id="bf9ee-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf9ee-153"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf9ee-153"><dt>Nmapi.dll</dt></span></span> </dl> |
