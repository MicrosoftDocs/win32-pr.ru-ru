---
description: Описывает статистику имеющуюся цепочку буферов, связанную с вызовами Пресентекс.
ms.assetid: aa100b83-6fbf-442d-9891-7fc034a5b1d5
title: Структура D3DPRESENTSTATS (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRESENTSTATS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b49a589fa1702f61e5a5daef806a5b36d464d0ec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273830"
---
# <a name="d3dpresentstats-structure"></a><span data-ttu-id="75425-103">Структура D3DPRESENTSTATS</span><span class="sxs-lookup"><span data-stu-id="75425-103">D3DPRESENTSTATS structure</span></span>

<span data-ttu-id="75425-104">Описывает статистику имеющуюся цепочку буферов, связанную с вызовами [**пресентекс**](/windows/win32/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) .</span><span class="sxs-lookup"><span data-stu-id="75425-104">Describes swapchain statistics relating to [**PresentEx**](/windows/win32/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) calls.</span></span>

## <a name="syntax"></a><span data-ttu-id="75425-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="75425-105">Syntax</span></span>


```C++
typedef struct _D3DPRESENTSTATS {
  UINT          PresentCount;
  UINT          PresentRefreshCount;
  UINT          SyncRefreshCount;
  LARGE_INTEGER SyncQPCTime;
  LARGE_INTEGER SyncGPUTime;
} D3DPRESENTSTATS;
```



## <a name="members"></a><span data-ttu-id="75425-106">Члены</span><span class="sxs-lookup"><span data-stu-id="75425-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="75425-107">**пресенткаунт**</span><span class="sxs-lookup"><span data-stu-id="75425-107">**PresentCount**</span></span>
</dt> <dd>

<span data-ttu-id="75425-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75425-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="75425-109">Текущее число успешных вызовов, выполненных отображаемым устройством, которое в настоящий момент переводится на экран.</span><span class="sxs-lookup"><span data-stu-id="75425-109">Running count of successful Present calls made by a display device that is currently outputting to screen.</span></span> <span data-ttu-id="75425-110">Этот параметр является фактически ИДЕНТИФИКАТОРом последнего текущего вызова и не обязательно является общим числом выполненных вызовов API.</span><span class="sxs-lookup"><span data-stu-id="75425-110">This parameter is really the Present ID of the last Present call and is not necessarily the total number of Present API calls made.</span></span>

</dd> <dt>

<span data-ttu-id="75425-111">**пресентрефрешкаунт**</span><span class="sxs-lookup"><span data-stu-id="75425-111">**PresentRefreshCount**</span></span>
</dt> <dd>

<span data-ttu-id="75425-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75425-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="75425-113">Счетчик вбланк, в котором на экране отображается последнее представление, число вбланк увеличивается после каждого интервала вбланк.</span><span class="sxs-lookup"><span data-stu-id="75425-113">The vblank count at which the last Present was displayed on screen, the vblank count increments once every vblank interval.</span></span>

</dd> <dt>

<span data-ttu-id="75425-114">**синкрефрешкаунт**</span><span class="sxs-lookup"><span data-stu-id="75425-114">**SyncRefreshCount**</span></span>
</dt> <dd>

<span data-ttu-id="75425-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75425-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="75425-116">Число вбланк, когда планировщик последний раз выборке время на компьютере, вызывая QueryPerformanceCounter.</span><span class="sxs-lookup"><span data-stu-id="75425-116">The vblank count when the scheduler last sampled the machine time by calling QueryPerformanceCounter.</span></span>

</dd> <dt>

<span data-ttu-id="75425-117">**синккпктиме**</span><span class="sxs-lookup"><span data-stu-id="75425-117">**SyncQPCTime**</span></span>
</dt> <dd>

<span data-ttu-id="75425-118">Тип: **[ **большое \_ целое число**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span><span class="sxs-lookup"><span data-stu-id="75425-118">Type: **[**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span></span>

</dd> <dd>

<span data-ttu-id="75425-119">Время последней выборки на компьютере планировщика, полученное путем вызова [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span><span class="sxs-lookup"><span data-stu-id="75425-119">The scheduler's last sampled machine time, obtained by calling [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

</dd> <dt>

<span data-ttu-id="75425-120">**синкгпутиме**</span><span class="sxs-lookup"><span data-stu-id="75425-120">**SyncGPUTime**</span></span>
</dt> <dd>

<span data-ttu-id="75425-121">Тип: **[ **большое \_ целое число**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span><span class="sxs-lookup"><span data-stu-id="75425-121">Type: **[**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span></span>

</dd> <dd>

<span data-ttu-id="75425-122">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="75425-122">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="75425-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="75425-123">Remarks</span></span>

<span data-ttu-id="75425-124">Когда приложение 9Ex применяет режим перелистывания (D3DSWAPEFFECT \_ флипекс), приложения могут обнаруживать удаление кадров, вызывая жетпресентстатистикс в любой момент времени.</span><span class="sxs-lookup"><span data-stu-id="75425-124">When a 9Ex application adopts Flip Mode present (D3DSWAPEFFECT\_FLIPEX), applications can detect frame dropping by calling GetPresentStatistics at any point in time.</span></span> <span data-ttu-id="75425-125">Фактически они могут выполнять следующие действия.</span><span class="sxs-lookup"><span data-stu-id="75425-125">In effect, they can do the following.</span></span>

1.  <span data-ttu-id="75425-126">Подготовка к просмотру в обратном буфере</span><span class="sxs-lookup"><span data-stu-id="75425-126">Render to the back buffer</span></span>
2.  <span data-ttu-id="75425-127">Имеется вызов</span><span class="sxs-lookup"><span data-stu-id="75425-127">Call Present</span></span>
3.  <span data-ttu-id="75425-128">Вызовите Жетпресентстатс и сохраните полученную структуру D3DPRESENTSTATS</span><span class="sxs-lookup"><span data-stu-id="75425-128">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure</span></span>
4.  <span data-ttu-id="75425-129">Преобразовать следующий кадр в задний буфер</span><span class="sxs-lookup"><span data-stu-id="75425-129">Render the next frame to the back buffer</span></span>
5.  <span data-ttu-id="75425-130">Имеется вызов</span><span class="sxs-lookup"><span data-stu-id="75425-130">Call Present</span></span>
6.  <span data-ttu-id="75425-131">Повторите шаги 4 и 5 1 или несколько раз.</span><span class="sxs-lookup"><span data-stu-id="75425-131">Repeat steps 4 and 5 one or more times</span></span>
7.  <span data-ttu-id="75425-132">Вызовите Жетпресентстатс и сохраните полученную структуру D3DPRESENTSTATS</span><span class="sxs-lookup"><span data-stu-id="75425-132">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure</span></span>
8.  <span data-ttu-id="75425-133">Сравните значения Пресентрефрешкаунт из двух хранимых структур D3DPRESENTSTATS.</span><span class="sxs-lookup"><span data-stu-id="75425-133">Compare the values of PresentRefreshCount from the two stored D3DPRESENTSTATS structures.</span></span> <span data-ttu-id="75425-134">Приложение может вычислить соответствующий Пресентрефрешкаунт определенного параметра Пресенткаунт, основываясь на предположений Пресентрефрешкаунт Increment и Пресенткаунт присваивания кадров.</span><span class="sxs-lookup"><span data-stu-id="75425-134">The application can calculate the corresponding PresentRefreshCount of a particular PresentCount parameter based on the assumptions of PresentRefreshCount increment and PresentCount assignment of frame presents.</span></span> <span data-ttu-id="75425-135">Если Пресентрефрешкаунт последний пример не соответствует Пресенткаунт (т. е. Если Пресентрефрешкаунт был увеличен, но Пресенткаунт — нет, то это значит, что произошло удаление кадра).</span><span class="sxs-lookup"><span data-stu-id="75425-135">If the PresentRefreshCount last sampled does not match the PresentCount (i.e. if the PresentRefreshCount has incremented but PresentCount has not, then there was frame dropping.)</span></span>

<span data-ttu-id="75425-136">Приложения могут определить, была ли удалена рамка с помощью выборки двух экземпляров Пресенткаунт и Жетпресентстатс (путем вызова API Жетпресентстатс в любые две точки во времени).</span><span class="sxs-lookup"><span data-stu-id="75425-136">Applications can determine whether a frame has been dropped by sampling any two instances of PresentCount and GetPresentStats (by calling GetPresentStats API at any two points in time).</span></span> <span data-ttu-id="75425-137">Например, приложение мультимедиа, представленное в той же скорости, что и частота обновления монитора (например, частота обновления монитора 60 Гц, приложение представляет кадр каждые 1/60 секунд), должно представлять кадры A, B, C, D, E, каждый из которых соответствует идентификаторам (Пресенткаунт) 1, 2, 3, 7, 8.</span><span class="sxs-lookup"><span data-stu-id="75425-137">For example, a media application that is presenting at the same rate as the monitor refresh rate (for example, monitor refresh rate is 60Hz, the application presents a frame every 1/60 seconds) wants to present frames A, B, C, D, E, each corresponding to Present IDs (PresentCount) 1, 2, 3, 7, 8.</span></span>

<span data-ttu-id="75425-138">Код приложения выглядит так, как в следующей последовательности.</span><span class="sxs-lookup"><span data-stu-id="75425-138">The application code looks like the following sequence.</span></span>

1.  <span data-ttu-id="75425-139">Отображение кадра A в задний буфер</span><span class="sxs-lookup"><span data-stu-id="75425-139">Render frame A to the back buffer</span></span>
2.  <span data-ttu-id="75425-140">Вызов Present, Пресенткаунт = 1</span><span class="sxs-lookup"><span data-stu-id="75425-140">Call Present, PresentCount = 1</span></span>
3.  <span data-ttu-id="75425-141">Вызовите Жетпресентстатс и сохраните полученную структуру D3DPRESENTSTATS</span><span class="sxs-lookup"><span data-stu-id="75425-141">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure</span></span>
4.  <span data-ttu-id="75425-142">Отображать следующие 4 кадра, B, C, D, E соответственно</span><span class="sxs-lookup"><span data-stu-id="75425-142">Render the next 4 frames, B, C, D, E, respectively</span></span>
5.  <span data-ttu-id="75425-143">Вызов представлен 4 раза, Пресенткаунтс = 2, 3, 7, 8 соответственно</span><span class="sxs-lookup"><span data-stu-id="75425-143">Call Present 4 times, PresentCounts = 2, 3, 7, 8, respectively</span></span>
6.  <span data-ttu-id="75425-144">Вызовите Жетпресентстатс и сохраните полученную структуру D3DPRESENTSTATS</span><span class="sxs-lookup"><span data-stu-id="75425-144">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure</span></span>
7.  <span data-ttu-id="75425-145">Сравните значения Пресентрефрешкаунт из двух хранимых структур D3DPRESENTSTATS.</span><span class="sxs-lookup"><span data-stu-id="75425-145">Compare the values of PresentRefreshCount from the two stored D3DPRESENTSTATS structures.</span></span> <span data-ttu-id="75425-146">Если разница составляет 2, т. е. 2 вбланк интервалов между двумя вызовами API Жетпресентстатс, последний представленный кадр должен быть кадром C. Так как приложение представляет один вбланк интервал (частота обновления монитора), время, прошедшее между выводимым кадром а и, если представление Frame C должно быть равно 2 вбланкс.</span><span class="sxs-lookup"><span data-stu-id="75425-146">If the difference is 2, i.e. 2 vblank intervals has elapsed between the two GetPresentStats API calls, then the last presented frame should be frame C. Because the application presents once very vblank interval (the refresh rate of the monitor), the time elapsed between when frame A is presented and when frame C is presented should be 2 vblanks.</span></span>
8.  <span data-ttu-id="75425-147">Сравните значения Пресенткаунт из двух хранимых структур D3DPRESENTSTATS.</span><span class="sxs-lookup"><span data-stu-id="75425-147">Compare the values of PresentCount from the two stored D3DPRESENTSTATS structures.</span></span> <span data-ttu-id="75425-148">Если первый Пресенткаунт — 1 (соответствующий кадру A), а второй Пресенткаунт — 3 (соответствующий кадру C), то кадры не были удалены.</span><span class="sxs-lookup"><span data-stu-id="75425-148">If the first PresentCount is 1 (corresponding to frame A) and the second PresentCount is 3 (corresponding to frame C), then no frames have been dropped.</span></span> <span data-ttu-id="75425-149">Если второй Пресенткаунт имеет значение 3, что соответствует кадру D, то приложение знает, что один кадр был удален.</span><span class="sxs-lookup"><span data-stu-id="75425-149">If the second PresentCount is 3, which corresponds to frame D, then the application knows that one frame has been dropped.</span></span>

<span data-ttu-id="75425-150">Обратите внимание, что Жетпресентстатистикс будет обрабатываться после вызова, независимо от состояния ФЛИПЕКС режима Пресентекс вызовов.</span><span class="sxs-lookup"><span data-stu-id="75425-150">Note that GetPresentStatistics will be processed after it is called, regardless of the state of FLIPEX mode PresentEx calls.</span></span>

<span data-ttu-id="75425-151">**Windows Vista:** В настоящее время вызовы будут поставлены в очередь, а затем будут обработаны до обработки вызова Жетпресентстатс.</span><span class="sxs-lookup"><span data-stu-id="75425-151">**Windows Vista:** The Present calls will be queued and then processed before GetPresentStats call will be processed.</span></span>

<span data-ttu-id="75425-152">Когда приложение обнаруживает, что представление определенных кадров находится позади, оно может пропустить эти кадры и исправить презентацию для повторной синхронизации с вбланк.</span><span class="sxs-lookup"><span data-stu-id="75425-152">When an application detects that the presentation of certain frames are behind, it can skip those frames and correct the presentation to re-synchronize with the vblank.</span></span> <span data-ttu-id="75425-153">Для этого приложение может просто не визуализировать последние кадры и начать отрисовку со следующим правильным кадром в очереди.</span><span class="sxs-lookup"><span data-stu-id="75425-153">To do this, an application can simply not render the late frames and start rendering with the next correct frame in the queue.</span></span> <span data-ttu-id="75425-154">Однако если приложение уже запустило отрисовку последних кадров, оно может использовать новый параметр present в D3D9Ex с именем D3DPRESENT \_ форцеиммедиате.</span><span class="sxs-lookup"><span data-stu-id="75425-154">However, if an application has already started the rendering of late frames, it can use a new Present parameter in D3D9Ex called D3DPRESENT\_FORCEIMMEDIATE.</span></span> <span data-ttu-id="75425-155">Флаг передается в параметрах текущего вызова API и указывает среде выполнения, что кадр будет обрабатываться немедленно в течение следующего вбланк интервала, который фактически не отображается на экране.</span><span class="sxs-lookup"><span data-stu-id="75425-155">The flag will be passed in the parameters of Present API call and indicates to the runtime that the frame will be processed immediately within the next vblank interval, effectively not visible on screen at all.</span></span> <span data-ttu-id="75425-156">Ниже приведен пример использования приложения после последнего шага в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="75425-156">Here is the application usage example after the last step in the previous example.</span></span>

1.  <span data-ttu-id="75425-157">Преобразовать следующий кадр в задний буфер</span><span class="sxs-lookup"><span data-stu-id="75425-157">Render the next frame to the back buffer</span></span>
2.  <span data-ttu-id="75425-158">Обнаружение из Пресентрефрешкаунт, что следующий кадр уже поздно</span><span class="sxs-lookup"><span data-stu-id="75425-158">Discover from PresentRefreshCount that the next frame is already late</span></span>
3.  <span data-ttu-id="75425-159">Задать для текущего интервала значение D3DPRESENT \_ форцеиммедиате</span><span class="sxs-lookup"><span data-stu-id="75425-159">Set Present interval to D3DPRESENT\_FORCEIMMEDIATE</span></span>
4.  <span data-ttu-id="75425-160">Вызов, имеющийся на следующем кадре</span><span class="sxs-lookup"><span data-stu-id="75425-160">Call Present on the next frame</span></span>

<span data-ttu-id="75425-161">Приложения могут синхронизировать видео-и звуковые потоки таким же образом, так как поведение Жетпресентстатистикс не меняется в этом сценарии.</span><span class="sxs-lookup"><span data-stu-id="75425-161">Applications can synchronize video and audio streams in the same manner because the behavior of GetPresentStatistics does not change in that scenario.</span></span>

<span data-ttu-id="75425-162">Режим отражения D3D9Ex предоставляет сведения о статистике кадров для оконных приложений и полноэкранных 9Ex приложений.</span><span class="sxs-lookup"><span data-stu-id="75425-162">D3D9Ex Flip Mode provides frame statistics information to windowed applications and full screen 9Ex applications.</span></span>

<span data-ttu-id="75425-163">**Windows Vista:** Используйте API DWM для получения текущей статистики.</span><span class="sxs-lookup"><span data-stu-id="75425-163">**Windows Vista:** Use the DWM APIs for retrieving present statistics.</span></span>

<span data-ttu-id="75425-164">Когда диспетчер окон рабочего стола отключена, оконный режим 9Ex приложения, использующие режим отражения, получит данные статистики ограниченной точности.</span><span class="sxs-lookup"><span data-stu-id="75425-164">When Desktop Window Manager is turned off, windowed mode 9Ex applications using flip mode will receive present statistics information of limited accuracy.</span></span>

<span data-ttu-id="75425-165">\* \* Windows Vista: \* \*</span><span class="sxs-lookup"><span data-stu-id="75425-165">\*\*Windows Vista:  \*\*</span></span>

<span data-ttu-id="75425-166">Если приложение не обладает достаточной скоростью, чтобы не допустить частоты обновления монитора, возможно, из-за низкой производительности оборудования или нехватки системных ресурсов, то может возникнуть сбой графики.</span><span class="sxs-lookup"><span data-stu-id="75425-166">If an application is not fast enough to keep up with the monitor's refresh rate, possibly due to slow hardware or lack of system resources, then it can experience a graphics glitch.</span></span> <span data-ttu-id="75425-167">Сбой — это так называемый Visual затруднения.</span><span class="sxs-lookup"><span data-stu-id="75425-167">A glitch is a so-called visual hiccup.</span></span> <span data-ttu-id="75425-168">Если монитор настроен на обновление с частотой 60 Гц и приложение может управлять только 30 кадрами/с, то половина этих кадров будет иметь сбой.</span><span class="sxs-lookup"><span data-stu-id="75425-168">If a monitor is set to refresh at 60 Hz, and the application can only manage 30 fps, then half of the frames will have glitches.</span></span>

<span data-ttu-id="75425-169">Приложения могут обнаружить сбой, отслеживая Синчрефрешкаунт.</span><span class="sxs-lookup"><span data-stu-id="75425-169">Applications can detect a glitch by keeping track of SynchRefreshCount.</span></span> <span data-ttu-id="75425-170">Например, приложение может выполнять следующую последовательность действий.</span><span class="sxs-lookup"><span data-stu-id="75425-170">For example, an application might perform the following sequence of actions.</span></span>

1.  <span data-ttu-id="75425-171">Отрисовывается в обратном буфере.</span><span class="sxs-lookup"><span data-stu-id="75425-171">Render to the back buffer.</span></span>
2.  <span data-ttu-id="75425-172">Имеется вызов.</span><span class="sxs-lookup"><span data-stu-id="75425-172">Call Present.</span></span>
3.  <span data-ttu-id="75425-173">Вызовите Жетпресентстатс и сохраните полученную структуру D3DPRESENTSTATS.</span><span class="sxs-lookup"><span data-stu-id="75425-173">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure.</span></span>
4.  <span data-ttu-id="75425-174">Прорисовка следующего кадра в задний буфер.</span><span class="sxs-lookup"><span data-stu-id="75425-174">Render the next frame to the back buffer.</span></span>
5.  <span data-ttu-id="75425-175">Имеется вызов.</span><span class="sxs-lookup"><span data-stu-id="75425-175">Call Present.</span></span>
6.  <span data-ttu-id="75425-176">Вызовите Жетпресентстатс и сохраните полученную структуру D3DPRESENTSTATS.</span><span class="sxs-lookup"><span data-stu-id="75425-176">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure.</span></span>
7.  <span data-ttu-id="75425-177">Сравните значения Синкрефрешкаунт из двух хранимых структур D3DPRESENTSTATS.</span><span class="sxs-lookup"><span data-stu-id="75425-177">Compare the values of SyncRefreshCount from the two stored D3DPRESENTSTATS structures.</span></span> <span data-ttu-id="75425-178">Если разность больше единицы, кадр пропускается.</span><span class="sxs-lookup"><span data-stu-id="75425-178">If the difference is greater than one, then a frame was skipped.</span></span>

## <a name="requirements"></a><span data-ttu-id="75425-179">Требования</span><span class="sxs-lookup"><span data-stu-id="75425-179">Requirements</span></span>



| <span data-ttu-id="75425-180">Требование</span><span class="sxs-lookup"><span data-stu-id="75425-180">Requirement</span></span> | <span data-ttu-id="75425-181">Значение</span><span class="sxs-lookup"><span data-stu-id="75425-181">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="75425-182">Header</span><span class="sxs-lookup"><span data-stu-id="75425-182">Header</span></span><br/> | <dl> <span data-ttu-id="75425-183"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="75425-183"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75425-184">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="75425-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75425-185">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="75425-185">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
