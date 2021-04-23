---
title: Структура WINBIO_EVENT (Винбио \_ types. h)
description: Содержит сведения о состоянии, отправляемые в подпрограммы обратного вызова при возникновении уведомления о событии.
ms.assetid: f46df7ff-8197-49cb-b1f8-4e7e3288e3df
keywords:
- API структуры WINBIO_EVENT биометрическая платформа Windows
- PWINBIO_EVENT API биометрическая платформа Windows указателя структуры
topic_type:
- apiref
api_name:
- WINBIO_EVENT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75b6a8301ea5dab7d860e5bd7fb32c69277bad63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661965"
---
# <a name="winbio_event-structure"></a><span data-ttu-id="9decc-105">\_Структура событий винбио</span><span class="sxs-lookup"><span data-stu-id="9decc-105">WINBIO\_EVENT structure</span></span>

<span data-ttu-id="9decc-106">Структура **\_ событий винбио** содержит сведения о состоянии, отправляемые в подпрограммы обратного вызова при возникновении уведомления о событии.</span><span class="sxs-lookup"><span data-stu-id="9decc-106">The **WINBIO\_EVENT** structure contains status information sent to the callback routine when an event notice is raised.</span></span>

## <a name="syntax"></a><span data-ttu-id="9decc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9decc-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EVENT {
  WINBIO_EVENT_TYPE Type;
  union {
    struct {
      WINBIO_UNIT_ID       UnitId;
      WINBIO_REJECT_DETAIL RejectDetail;
    } Unclaimed;
    struct {
      WINBIO_UNIT_ID           UnitId;
      WINBIO_IDENTITY          Identity;
      WINBIO_BIOMETRIC_SUBTYPE SubFactor;
      WINBIO_REJECT_DETAIL     RejectDetail;
    } UnclaimedIdentify;
    struct {
      HRESULT ErrorCode;
    } Error;
  } Parameters;
} WINBIO_EVENT, *PWINBIO_EVENT;
```



## <a name="members"></a><span data-ttu-id="9decc-108">Члены</span><span class="sxs-lookup"><span data-stu-id="9decc-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="9decc-109">**Тип**</span><span class="sxs-lookup"><span data-stu-id="9decc-109">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="9decc-110">Значение, указывающее тип вызванного уведомления о событии поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="9decc-110">A value that specifies the type of service provider event notice raised.</span></span> <span data-ttu-id="9decc-111">Единственным поставщиком, поддерживаемым в настоящее время, является датчик отпечатков пальцев.</span><span class="sxs-lookup"><span data-stu-id="9decc-111">The only provider currently supported is the fingerprint sensor.</span></span> <span data-ttu-id="9decc-112">Этот датчик поддерживает следующие флаги.</span><span class="sxs-lookup"><span data-stu-id="9decc-112">This sensor supports the following flags.</span></span>

<dl> <dt>

<span data-ttu-id="9decc-113"><span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span>**Винбио \_ \_ \_ Невостребованное событие FP** (датчик обнаружил пальца, который не запрашивался приложением или окном, которое в данный момент находится в фокусе).</span><span class="sxs-lookup"><span data-stu-id="9decc-113"><span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span>**WINBIO\_EVENT\_FP\_UNCLAIMED** (The sensor detected a finger swipe that was not requested by the application or by the window that currently has focus.</span></span> <span data-ttu-id="9decc-114">Биометрическая платформа Windows вызывает функцию обратного вызова, чтобы указать, что произошел палец, но не пытается определить отпечаток.)</span><span class="sxs-lookup"><span data-stu-id="9decc-114">The Windows Biometric Framework calls into your callback function to indicate that a finger swipe has occurred but does not try to identify the fingerprint.)</span></span>
</dt> <dt>

<span data-ttu-id="9decc-115"><span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span>**Винбио \_ Необязательное \_ \_ \_ Определение события FP** (датчик обнаружил пальца, который не запрашивался приложением или окном, которое в данный момент находится в фокусе).</span><span class="sxs-lookup"><span data-stu-id="9decc-115"><span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span>**WINBIO\_EVENT\_FP\_UNCLAIMED\_IDENTIFY** (The sensor detected a finger swipe that was not requested by the application or by the window that currently has focus.</span></span> <span data-ttu-id="9decc-116">Биометрическая платформа Windows пытается опознать отпечаток и передает результат этого процесса функции обратного вызова.)</span><span class="sxs-lookup"><span data-stu-id="9decc-116">The Windows Biometric Framework attempts to identify the fingerprint and passes the result of that process to your callback function.)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="9decc-117">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="9decc-117">**Parameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9decc-118">**Неиспользованные**</span><span class="sxs-lookup"><span data-stu-id="9decc-118">**Unclaimed**</span></span>
</dt> <dd>

<span data-ttu-id="9decc-119">Структура, возвращаемая для записи образца биометрической метрики.</span><span class="sxs-lookup"><span data-stu-id="9decc-119">Structure returned for biometric sample capture.</span></span>

<dl> <dt>

<span data-ttu-id="9decc-120">**унитид**</span><span class="sxs-lookup"><span data-stu-id="9decc-120">**UnitId**</span></span>
</dt> <dd>

<span data-ttu-id="9decc-121">Биометрическая единица, создавшая образец.</span><span class="sxs-lookup"><span data-stu-id="9decc-121">The biometric unit that generated the sample.</span></span>

</dd> <dt>

<span data-ttu-id="9decc-122">**режектдетаил**</span><span class="sxs-lookup"><span data-stu-id="9decc-122">**RejectDetail**</span></span>
</dt> <dd>

<span data-ttu-id="9decc-123">Значение типа **ulong** , содержащее дополнительные сведения о сбоях при записи образца биометрической метрики.</span><span class="sxs-lookup"><span data-stu-id="9decc-123">A **ULONG** value that contains additional information regarding failure to capture a biometric sample.</span></span> <span data-ttu-id="9decc-124">Если запись прошла удачно, этот параметр имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="9decc-124">If a capture succeeded, this parameter is set to zero.</span></span> <span data-ttu-id="9decc-125">Для записи отпечатков пальцев определены следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9decc-125">The following values are defined for fingerprint capture:</span></span>

-   <span data-ttu-id="9decc-126">\_ \_ слишком большое винбио \_ FP</span><span class="sxs-lookup"><span data-stu-id="9decc-126">WINBIO\_FP\_TOO\_HIGH</span></span>
-   <span data-ttu-id="9decc-127">\_ \_ слишком низкое винбио \_ FP</span><span class="sxs-lookup"><span data-stu-id="9decc-127">WINBIO\_FP\_TOO\_LOW</span></span>
-   <span data-ttu-id="9decc-128">ВИНБИО \_ FP \_ не \_ осталось</span><span class="sxs-lookup"><span data-stu-id="9decc-128">WINBIO\_FP\_TOO\_LEFT</span></span>
-   <span data-ttu-id="9decc-129">\_слишком винбио \_ FP \_</span><span class="sxs-lookup"><span data-stu-id="9decc-129">WINBIO\_FP\_TOO\_RIGHT</span></span>
-   <span data-ttu-id="9decc-130">\_ \_ слишком быстрое винбио \_ FP</span><span class="sxs-lookup"><span data-stu-id="9decc-130">WINBIO\_FP\_TOO\_FAST</span></span>
-   <span data-ttu-id="9decc-131">\_ \_ слишком низкое винбио \_ FP</span><span class="sxs-lookup"><span data-stu-id="9decc-131">WINBIO\_FP\_TOO\_SLOW</span></span>
-   <span data-ttu-id="9decc-132">\_ \_ низкое качество винбио \_ FP</span><span class="sxs-lookup"><span data-stu-id="9decc-132">WINBIO\_FP\_POOR\_QUALITY</span></span>
-   <span data-ttu-id="9decc-133">ВИНБИО \_ FP \_ слишком \_ наклонен</span><span class="sxs-lookup"><span data-stu-id="9decc-133">WINBIO\_FP\_TOO\_SKEWED</span></span>
-   <span data-ttu-id="9decc-134">\_ \_ слишком короткий винбио \_ FP</span><span class="sxs-lookup"><span data-stu-id="9decc-134">WINBIO\_FP\_TOO\_SHORT</span></span>
-   <span data-ttu-id="9decc-135">\_ \_ сбой слияния винбио \_ FP</span><span class="sxs-lookup"><span data-stu-id="9decc-135">WINBIO\_FP\_MERGE\_FAILURE</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9decc-136">**унклаимедидентифи**</span><span class="sxs-lookup"><span data-stu-id="9decc-136">**UnclaimedIdentify**</span></span>
</dt> <dd>

<span data-ttu-id="9decc-137">Структура, возвращаемая для биометрической записи и идентификации.</span><span class="sxs-lookup"><span data-stu-id="9decc-137">Structure returned for biometric capture and identification.</span></span> <span data-ttu-id="9decc-138">Идентификация определяет, можно ли связать образец с существующим биометрической защитным шаблоном.</span><span class="sxs-lookup"><span data-stu-id="9decc-138">Identification determines whether a sample can be associated with an existing biometric template.</span></span>

<dl> <dt>

<span data-ttu-id="9decc-139">**унитид**</span><span class="sxs-lookup"><span data-stu-id="9decc-139">**UnitId**</span></span>
</dt> <dd>

<span data-ttu-id="9decc-140">Биометрическая единица, создавшая образец.</span><span class="sxs-lookup"><span data-stu-id="9decc-140">The biometric unit that generated the sample.</span></span>

</dd> <dt>

<span data-ttu-id="9decc-141">**Удостоверение**</span><span class="sxs-lookup"><span data-stu-id="9decc-141">**Identity**</span></span>
</dt> <dd>

<span data-ttu-id="9decc-142">Структура [**\_ идентификации винбио**](winbio-identity.md) , содержащая идентификатор GUID или идентификатор безопасности пользователя, предоставляющего образец биометрической метрики.</span><span class="sxs-lookup"><span data-stu-id="9decc-142">A [**WINBIO\_IDENTITY**](winbio-identity.md) structure that contains the GUID or SID of the user providing the biometric sample.</span></span>

</dd> <dt>

<span data-ttu-id="9decc-143">**Подфакт**</span><span class="sxs-lookup"><span data-stu-id="9decc-143">**SubFactor**</span></span>
</dt> <dd>

<span data-ttu-id="9decc-144">Значение [**\_ \_ ПОДтипа БИОметрической метрики винбио**](winbio-biometric-subtype-constants.md) , указывающее вспомогательный фактор, связанный с образцом биометрических метрик.</span><span class="sxs-lookup"><span data-stu-id="9decc-144">A [**WINBIO\_BIOMETRIC\_SUBTYPE**](winbio-biometric-subtype-constants.md) value that specifies the sub-factor associated with a biometric sample.</span></span> <span data-ttu-id="9decc-145">В настоящее время биометрическая платформа Windows (ВБФ) поддерживает только запись отпечатка пальца и использует следующие константы для представления сведений о подтипах.</span><span class="sxs-lookup"><span data-stu-id="9decc-145">The Windows Biometric Framework (WBF) currently supports only fingerprint capture and uses the following constants to represent sub-type information.</span></span>

-   <span data-ttu-id="9decc-146">ВИНБИО \_ ANSI \_ 381 \_ POS \_ Unknown</span><span class="sxs-lookup"><span data-stu-id="9decc-146">WINBIO\_ANSI\_381\_POS\_UNKNOWN</span></span>
-   <span data-ttu-id="9decc-147">ВИНБИО \_ ANSI \_ 381 \_ \_ RH POS \_</span><span class="sxs-lookup"><span data-stu-id="9decc-147">WINBIO\_ANSI\_381\_POS\_RH\_THUMB</span></span>
-   <span data-ttu-id="9decc-148">ВИНБИО \_ \_ \_ \_ RH \_ указатель \_ пальца ANSI 381 POS</span><span class="sxs-lookup"><span data-stu-id="9decc-148">WINBIO\_ANSI\_381\_POS\_RH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="9decc-149">ВИНБИО \_ ANSI \_ 381 \_ \_ RH, \_ средний \_ палец</span><span class="sxs-lookup"><span data-stu-id="9decc-149">WINBIO\_ANSI\_381\_POS\_RH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="9decc-150">ВИНБИО \_ ANSI \_ 381 \_ POS \_ RH \_ Ring \_</span><span class="sxs-lookup"><span data-stu-id="9decc-150">WINBIO\_ANSI\_381\_POS\_RH\_RING\_FINGER</span></span>
-   <span data-ttu-id="9decc-151">ВИНБИО \_ ANSI \_ 381 \_ \_ RH, \_ маленький \_ палец</span><span class="sxs-lookup"><span data-stu-id="9decc-151">WINBIO\_ANSI\_381\_POS\_RH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="9decc-152">ВИНБИОный \_ \_ \_ \_ бегунок ANSI 381 POS \_</span><span class="sxs-lookup"><span data-stu-id="9decc-152">WINBIO\_ANSI\_381\_POS\_LH\_THUMB</span></span>
-   <span data-ttu-id="9decc-153">ВИНБИОный \_ палец с индексами в формате ANSI \_ 381 \_ POS \_ LH \_ \_</span><span class="sxs-lookup"><span data-stu-id="9decc-153">WINBIO\_ANSI\_381\_POS\_LH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="9decc-154">\_ \_ Средний палец винбио ANSI 381 \_ POS \_ LH \_ \_</span><span class="sxs-lookup"><span data-stu-id="9decc-154">WINBIO\_ANSI\_381\_POS\_LH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="9decc-155">ВИНБИОный \_ палец в формате ANSI \_ 381 \_ POS \_ LH \_ \_</span><span class="sxs-lookup"><span data-stu-id="9decc-155">WINBIO\_ANSI\_381\_POS\_LH\_RING\_FINGER</span></span>
-   <span data-ttu-id="9decc-156">ВИНБИО \_ ANSI \_ 381 \_ POS \_ , \_ маленький \_ палец</span><span class="sxs-lookup"><span data-stu-id="9decc-156">WINBIO\_ANSI\_381\_POS\_LH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="9decc-157">ВИНБИО \_ ANSI \_ 381 \_ RH POS с \_ \_ четырьмя \_ пальцами</span><span class="sxs-lookup"><span data-stu-id="9decc-157">WINBIO\_ANSI\_381\_POS\_RH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="9decc-158">ВИНБИО \_ ANSI \_ 381 \_ POS \_ LH \_ четыре \_ пальца</span><span class="sxs-lookup"><span data-stu-id="9decc-158">WINBIO\_ANSI\_381\_POS\_LH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="9decc-159">ВИНБИО \_ ANSI \_ 381 \_ POS \_ 2 \_ Thumbs</span><span class="sxs-lookup"><span data-stu-id="9decc-159">WINBIO\_ANSI\_381\_POS\_TWO\_THUMBS</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="9decc-160">Не пытайтесь проверить значение, заданное для *значения этого параметра* .</span><span class="sxs-lookup"><span data-stu-id="9decc-160">Do not attempt to validate the value supplied for the *SubFactor* value.</span></span> <span data-ttu-id="9decc-161">Служба биометрических систем Windows проверит переданное значение перед его передачей в реализацию.</span><span class="sxs-lookup"><span data-stu-id="9decc-161">The Windows Biometrics Service will validate the supplied value before passing it through to your implementation.</span></span> <span data-ttu-id="9decc-162">Если значение **винбио \_ подтипа \_ нет \_ данных** или **винбио \_ подтип \_ ANY**, то проверьте, где это необходимо.</span><span class="sxs-lookup"><span data-stu-id="9decc-162">If the value is **WINBIO\_SUBTYPE\_NO\_INFORMATION** or **WINBIO\_SUBTYPE\_ANY**, then validate where appropriate.</span></span>

 

</dd> <dt>

<span data-ttu-id="9decc-163">**режектдетаил**</span><span class="sxs-lookup"><span data-stu-id="9decc-163">**RejectDetail**</span></span>
</dt> <dd>

<span data-ttu-id="9decc-164">Значение типа **ulong** , содержащее дополнительные сведения о сбое записи образца биометрической метрики.</span><span class="sxs-lookup"><span data-stu-id="9decc-164">A **ULONG** value that contains additional information about the failure to capture a biometric sample.</span></span> <span data-ttu-id="9decc-165">Если запись прошла удачно, этот параметр имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="9decc-165">If the capture succeeded, this parameter is set to zero.</span></span> <span data-ttu-id="9decc-166">Для записи отпечатков пальцев определены следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9decc-166">The following values are defined for fingerprint capture:</span></span>

-   <span data-ttu-id="9decc-167">\_ \_ слишком большое винбио \_ FP</span><span class="sxs-lookup"><span data-stu-id="9decc-167">WINBIO\_FP\_TOO\_HIGH</span></span>
-   <span data-ttu-id="9decc-168">\_ \_ слишком низкое винбио \_ FP</span><span class="sxs-lookup"><span data-stu-id="9decc-168">WINBIO\_FP\_TOO\_LOW</span></span>
-   <span data-ttu-id="9decc-169">ВИНБИО \_ FP \_ не \_ осталось</span><span class="sxs-lookup"><span data-stu-id="9decc-169">WINBIO\_FP\_TOO\_LEFT</span></span>
-   <span data-ttu-id="9decc-170">\_слишком винбио \_ FP \_</span><span class="sxs-lookup"><span data-stu-id="9decc-170">WINBIO\_FP\_TOO\_RIGHT</span></span>
-   <span data-ttu-id="9decc-171">\_ \_ слишком быстрое винбио \_ FP</span><span class="sxs-lookup"><span data-stu-id="9decc-171">WINBIO\_FP\_TOO\_FAST</span></span>
-   <span data-ttu-id="9decc-172">\_ \_ слишком низкое винбио \_ FP</span><span class="sxs-lookup"><span data-stu-id="9decc-172">WINBIO\_FP\_TOO\_SLOW</span></span>
-   <span data-ttu-id="9decc-173">\_ \_ низкое качество винбио \_ FP</span><span class="sxs-lookup"><span data-stu-id="9decc-173">WINBIO\_FP\_POOR\_QUALITY</span></span>
-   <span data-ttu-id="9decc-174">ВИНБИО \_ FP \_ слишком \_ наклонен</span><span class="sxs-lookup"><span data-stu-id="9decc-174">WINBIO\_FP\_TOO\_SKEWED</span></span>
-   <span data-ttu-id="9decc-175">\_ \_ слишком короткий винбио \_ FP</span><span class="sxs-lookup"><span data-stu-id="9decc-175">WINBIO\_FP\_TOO\_SHORT</span></span>
-   <span data-ttu-id="9decc-176">\_ \_ сбой слияния винбио \_ FP</span><span class="sxs-lookup"><span data-stu-id="9decc-176">WINBIO\_FP\_MERGE\_FAILURE</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9decc-177">**Ошибка**</span><span class="sxs-lookup"><span data-stu-id="9decc-177">**Error**</span></span>
</dt> <dd>

<span data-ttu-id="9decc-178">Структура, идентифицирующая успешное или неуспешное выполнение отслеживаемой операции.</span><span class="sxs-lookup"><span data-stu-id="9decc-178">Structure that identifies the success or failure of the operation being monitored.</span></span>

<dl> <dt>

<span data-ttu-id="9decc-179">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9decc-179">**ErrorCode**</span></span>
</dt> <dd>

<span data-ttu-id="9decc-180">Значение **HRESULT** , которое содержит S \_ OK или код ошибки, полученный в результате вычислений, выполненных биометрическая платформа Windows.</span><span class="sxs-lookup"><span data-stu-id="9decc-180">**HRESULT** value that contains S\_OK or an error code that resulted from computations performed by the Windows Biometric Framework.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9decc-181">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9decc-181">Remarks</span></span>

<span data-ttu-id="9decc-182">Вызовите функцию [**винбиорегистеревентмонитор**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) , чтобы зарегистрировать подпрограммы обратного вызова для получения уведомлений о событиях из биометрическая платформа Windows.</span><span class="sxs-lookup"><span data-stu-id="9decc-182">Call the [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) function to register a callback routine to receive event notifications from the Windows Biometric Framework.</span></span> <span data-ttu-id="9decc-183">Обратный вызов — это пользовательская функция, которую необходимо определить для приложения.</span><span class="sxs-lookup"><span data-stu-id="9decc-183">The callback is a custom function that you must define for your application.</span></span>

## <a name="requirements"></a><span data-ttu-id="9decc-184">Требования</span><span class="sxs-lookup"><span data-stu-id="9decc-184">Requirements</span></span>



| <span data-ttu-id="9decc-185">Требование</span><span class="sxs-lookup"><span data-stu-id="9decc-185">Requirement</span></span> | <span data-ttu-id="9decc-186">Значение</span><span class="sxs-lookup"><span data-stu-id="9decc-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9decc-187">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9decc-187">Minimum supported client</span></span><br/> | <span data-ttu-id="9decc-188">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9decc-188">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="9decc-189">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9decc-189">Minimum supported server</span></span><br/> | <span data-ttu-id="9decc-190">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9decc-190">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="9decc-191">Header</span><span class="sxs-lookup"><span data-stu-id="9decc-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="9decc-192"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9decc-192"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9decc-193">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9decc-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9decc-194">Структуры клиентских приложений</span><span class="sxs-lookup"><span data-stu-id="9decc-194">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="9decc-195">**винбиорегистеревентмонитор**</span><span class="sxs-lookup"><span data-stu-id="9decc-195">**WinBioRegisterEventMonitor**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor)
</dt> </dl>

 

 





