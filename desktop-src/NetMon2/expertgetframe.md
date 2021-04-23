---
description: Возвращает запрошенный кадр из загруженной записи.
ms.assetid: efd1cff5-a3a1-4910-b003-25b6e10dad6e
title: Функция Експертжетфраме (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertGetFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2bd02bde8caf157b6df6b1dd772a8f7574df0e57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896789"
---
# <a name="expertgetframe-function"></a><span data-ttu-id="e1695-103">Функция Експертжетфраме</span><span class="sxs-lookup"><span data-stu-id="e1695-103">ExpertGetFrame function</span></span>

<span data-ttu-id="e1695-104">Функция **експертжетфраме** возвращает запрошенный кадр из загруженной записи.</span><span class="sxs-lookup"><span data-stu-id="e1695-104">The **ExpertGetFrame** function returns the requested frame from a loaded capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1695-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1695-105">Syntax</span></span>


```C++
DWORD WINAPI ExpertGetFrame(
  _In_  HEXPERTKEY              hExpertKey,
  _In_  DWORD                   Direction,
  _In_  DWORD                   RequestFlags,
  _In_  DWORD                   RequestedFrameNumber,
  _In_  HFILTER                 hFilter,
  _Out_ LPEXPERTFRAMEDESCRIPTOR pEFrameDescriptor
);
```



## <a name="parameters"></a><span data-ttu-id="e1695-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1695-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1695-107">*хексперткэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e1695-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1695-108">Уникальный идентификатор эксперта.</span><span class="sxs-lookup"><span data-stu-id="e1695-108">A unique expert identifier.</span></span> <span data-ttu-id="e1695-109">Сетевой монитор передает идентификатор *хексперткэй* эксперту при вызове функции [**Run**](run.md) .</span><span class="sxs-lookup"><span data-stu-id="e1695-109">Network Monitor passes the *hExpertKey* identifier to the expert when it calls the [**Run**](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="e1695-110">*Направление письма* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e1695-110">*Direction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1695-111">Значение, определяющее, как сетевой монитор ищет кадр.</span><span class="sxs-lookup"><span data-stu-id="e1695-111">A value that identifies how Network Monitor searches for the frame.</span></span>



| <span data-ttu-id="e1695-112">Значение</span><span class="sxs-lookup"><span data-stu-id="e1695-112">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="e1695-113">Значение</span><span class="sxs-lookup"><span data-stu-id="e1695-113">Meaning</span></span>                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="GET_SPECIFIED_FRAME"></span><span id="get_specified_frame"></span><dl> <span data-ttu-id="e1695-114"><dt>**ПОЛУЧИТЬ \_ указанный \_ кадр**</dt></span><span class="sxs-lookup"><span data-stu-id="e1695-114"><dt>**GET\_SPECIFIED\_FRAME**</dt></span></span> </dl>              | <span data-ttu-id="e1695-115">Возврат запрошенного кадра.</span><span class="sxs-lookup"><span data-stu-id="e1695-115">Return the requested frame.</span></span><br/> |
| <span id="GET_FRAME_NEXT_FORWARD"></span><span id="get_frame_next_forward"></span><dl> <span data-ttu-id="e1695-116"><dt>**ПОЛУЧИТЬ \_ кадр \_ Далее \_ вперед**</dt></span><span class="sxs-lookup"><span data-stu-id="e1695-116"><dt>**GET\_FRAME\_NEXT\_FORWARD**</dt></span></span> </dl>    | <span data-ttu-id="e1695-117">Возвратить следующий кадр.</span><span class="sxs-lookup"><span data-stu-id="e1695-117">Return the next frame.</span></span><br/>      |
| <span id="GET_FRAME_NEXT_BACKWARD"></span><span id="get_frame_next_backward"></span><dl> <span data-ttu-id="e1695-118"><dt>**ПОЛУЧИТЬ \_ кадр на \_ следующий \_ задний план**</dt></span><span class="sxs-lookup"><span data-stu-id="e1695-118"><dt>**GET\_FRAME\_NEXT\_BACKWARD**</dt></span></span> </dl> | <span data-ttu-id="e1695-119">Возврат предыдущего кадра.</span><span class="sxs-lookup"><span data-stu-id="e1695-119">Return the previous frame.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="e1695-120">*Рекуестфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e1695-120">*RequestFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1695-121">Флаги, указывающие, как сетевой монитор должен выполнять запрос.</span><span class="sxs-lookup"><span data-stu-id="e1695-121">The flags that specify how Network Monitor should handle the request.</span></span> <span data-ttu-id="e1695-122">Укажите один или несколько следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="e1695-122">Specify one or more of the following flags.</span></span>



| <span data-ttu-id="e1695-123">Значение</span><span class="sxs-lookup"><span data-stu-id="e1695-123">Value</span></span>                                                                                                                                                                                             | <span data-ttu-id="e1695-124">Значение</span><span class="sxs-lookup"><span data-stu-id="e1695-124">Meaning</span></span>                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAGS_DEFER_TO_UI_FILTER"></span><span id="flags_defer_to_ui_filter"></span><dl> <span data-ttu-id="e1695-125"><dt>**ФЛАГи \_ откладываются \_ на \_ Фильтр пользовательского интерфейса \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e1695-125"><dt>**FLAGS\_DEFER\_TO\_UI\_FILTER**</dt></span></span> </dl> | <span data-ttu-id="e1695-126">Перед применением параметра фильтра экрана эксперта, указанного в *хфилтер*, примените фильтр просмотра, который сетевой монитор использует при запуске эксперта.</span><span class="sxs-lookup"><span data-stu-id="e1695-126">Before applying the display filter parameter of the expert which is specified in *hFilter*, apply the display filter that Network Monitor is using when the expert starts.</span></span><br/>                                                                                                                              |
| <span id="FLAGS_ATTACH_PROPERTIES"></span><span id="flags_attach_properties"></span><dl> <span data-ttu-id="e1695-127"><dt>**ФЛАГ \_ присоединения \_ свойств**</dt></span><span class="sxs-lookup"><span data-stu-id="e1695-127"><dt>**FLAGS\_ATTACH\_PROPERTIES**</dt></span></span> </dl>      | <span data-ttu-id="e1695-128">Свойства, которые все парсеры протоколов находят с запрошенными разделами этого кадра, присоединяются к кадру.</span><span class="sxs-lookup"><span data-stu-id="e1695-128">The properties that all protocol parsers find with claimed sections of this frame are attached to the frame.</span></span> <span data-ttu-id="e1695-129">Если флаг не установлен, поле **лппропертитабле** структуры [**експертфрамедескриптор**](expertframedescriptor.md) (возвращаемое **Пефрамедескриптор**) будет иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e1695-129">If the flag is not set, the **lpPropertyTable** field of the [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) structure (returned by **pEFrameDescriptor**) will be set to **NULL**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e1695-130">*Рекуестедфраменумбер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e1695-130">*RequestedFrameNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1695-131">Номер запрошенного кадра.</span><span class="sxs-lookup"><span data-stu-id="e1695-131">The number of the requested frame.</span></span>

</dd> <dt>

<span data-ttu-id="e1695-132">*хфилтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e1695-132">*hFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1695-133">Маркер фильтра экрана эксперта.</span><span class="sxs-lookup"><span data-stu-id="e1695-133">A handle to the expert display filter.</span></span> <span data-ttu-id="e1695-134">Если у эксперта нет фильтра экрана, установите для параметра значение **null**.</span><span class="sxs-lookup"><span data-stu-id="e1695-134">If the expert does not have a display filter, set the parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e1695-135">*пефрамедескриптор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e1695-135">*pEFrameDescriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1695-136">Структура [**експертфрамедескриптор**](expertframedescriptor.md) , которая возвращает, описывает кадр.</span><span class="sxs-lookup"><span data-stu-id="e1695-136">The [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) structure that, on return, describes the frame.</span></span> <span data-ttu-id="e1695-137">Эксперт должен выделить и освободить память, которую использует эта структура.</span><span class="sxs-lookup"><span data-stu-id="e1695-137">The expert must allocate and free the memory that this structure uses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1695-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e1695-138">Return value</span></span>

<span data-ttu-id="e1695-139">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="e1695-139">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="e1695-140">Если функция завершается неудачно, возвращаемое значение указывает причину сбоя.</span><span class="sxs-lookup"><span data-stu-id="e1695-140">If the function is unsuccessful, the return value indicates the reason for the failure.</span></span> <span data-ttu-id="e1695-141">Если возвращаемое значение — НМЕРР \_ \_ , то эксперт должен немедленно очистить и вернуться; пользователь прервал запуск эксперта.</span><span class="sxs-lookup"><span data-stu-id="e1695-141">If the return value is NMERR\_EXPERT\_TERMINATE, the expert must immediately clean up and return; the user has aborted the expert run.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1695-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e1695-142">Remarks</span></span>

<span data-ttu-id="e1695-143">Если задать ФЛАГи \_ присоединения \_ свойств, вызов требует больше ресурсов, чем если бы флаг не был установлен.</span><span class="sxs-lookup"><span data-stu-id="e1695-143">If you set FLAGS\_ATTACH\_PROPERTIES, the call requires more resources than if you do not set the flag.</span></span> <span data-ttu-id="e1695-144">Если флаг не установлен, указатель указывает на необработанный кадр и на данные о кадре.</span><span class="sxs-lookup"><span data-stu-id="e1695-144">If the flag is not set, a pointer points to the raw frame and to data about the frame.</span></span> <span data-ttu-id="e1695-145">Если этот флаг установлен, сетевой монитор присоединяет все свойства к кадру путем вызова каждого средства синтаксического анализа, которое заявляет часть кадра.</span><span class="sxs-lookup"><span data-stu-id="e1695-145">If this flag is set, Network Monitor attaches all properties to the frame by calling every parser that claims a portion of the frame.</span></span> <span data-ttu-id="e1695-146">Это может быть очень длительный процесс.</span><span class="sxs-lookup"><span data-stu-id="e1695-146">This can be a slow process.</span></span>

<span data-ttu-id="e1695-147">Эксперты не должны устанавливать \_ флаг присоединения флагов, \_ Если для экспертов не требуются свойства, присоединяемые к фрейму анализаторами.</span><span class="sxs-lookup"><span data-stu-id="e1695-147">Experts should not set the FLAGS\_ATTACH\_PROPERTIES flag unless the experts require the properties that parsers attach to the frame.</span></span> <span data-ttu-id="e1695-148">Если это возможно, эксперты должны вызвать функцию **експертжетфраме** без флага, а затем извлечь необходимые данные непосредственно из фрейма.</span><span class="sxs-lookup"><span data-stu-id="e1695-148">If possible, experts should call the **ExpertGetFrame** function without the flag, and then extract the required data directly from the frame.</span></span>

<span data-ttu-id="e1695-149">Если эксперт вызывает **експертжетфраме** без флагов \_ присоединить \_ Свойства и требует свойства, связанные с этим кадром (например, событие), эксперт вызывает **експертжетфраме** с теми же параметрами, за исключением следующих:</span><span class="sxs-lookup"><span data-stu-id="e1695-149">If the expert calls **ExpertGetFrame** without the FLAGS\_ATTACH\_PROPERTIES flag and requires the properties associated with that frame (an event, for example), the expert calls **ExpertGetFrame** with the same parameters except for the following:</span></span>

``` syntax
Direction = EXPERT_GET_SPECIFIED_FRAME;
RequestFlags &= (~EXPERT_DEFER_TO_UI_FILTER) | EXPERT_ATTACH_PROPERTIES;
RequestedFrameNumber= (The actual frame number you want);
hFilter = NULL;
pEFrameDescriptor = (The same one as last time);
```

<span data-ttu-id="e1695-150">Использование приведенного выше кода гарантирует, что эксперт получает необходимый кадр без необходимости повторного вызова кода фильтра.</span><span class="sxs-lookup"><span data-stu-id="e1695-150">Using the preceding code ensures that the expert gets the required frame without having to call filter code again.</span></span>

<span data-ttu-id="e1695-151">Параметр *хфилтер* можно задать как **лпвоид**.</span><span class="sxs-lookup"><span data-stu-id="e1695-151">You can set the *hFilter* parameter as an **LPVOID**.</span></span> <span data-ttu-id="e1695-152">Если он существует, возвращаемый кадр передает этот фильтр.</span><span class="sxs-lookup"><span data-stu-id="e1695-152">If it exists, the returned frame passes this filter.</span></span> <span data-ttu-id="e1695-153">Если у эксперта нет фильтра для передачи функции (если *хфилтер* имеет **значение NULL** ), то возвращаемый кадр не фильтруется.</span><span class="sxs-lookup"><span data-stu-id="e1695-153">If the expert does not have a display filter to pass to the function (if *hFilter* is **NULL** ), then the frame returned is not filtered.</span></span>

<span data-ttu-id="e1695-154">Функция **експертжетфраме** может вызываться экспертами, реализующими функцию [**запуска**](run.md) или [**настройки**](configure.md) экспорта.</span><span class="sxs-lookup"><span data-stu-id="e1695-154">The **ExpertGetFrame** function can only be called by experts that implement the [**Run**](run.md) or [**Configure**](configure.md) export function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1695-155">Требования</span><span class="sxs-lookup"><span data-stu-id="e1695-155">Requirements</span></span>



| <span data-ttu-id="e1695-156">Требование</span><span class="sxs-lookup"><span data-stu-id="e1695-156">Requirement</span></span> | <span data-ttu-id="e1695-157">Значение</span><span class="sxs-lookup"><span data-stu-id="e1695-157">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e1695-158">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e1695-158">Minimum supported client</span></span><br/> | <span data-ttu-id="e1695-159">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e1695-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e1695-160">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e1695-160">Minimum supported server</span></span><br/> | <span data-ttu-id="e1695-161">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e1695-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e1695-162">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e1695-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1695-163"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1695-163"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="e1695-164">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e1695-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="e1695-165"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1695-165"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="e1695-166">DLL</span><span class="sxs-lookup"><span data-stu-id="e1695-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1695-167"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1695-167"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




