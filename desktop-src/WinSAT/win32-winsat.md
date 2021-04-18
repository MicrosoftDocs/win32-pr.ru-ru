---
title: Класс Win32_WinSAT
description: Определяет сведения о сводных оценках для последней формальной оценки.
ms.assetid: adf4de42-9dfd-46a7-ae75-3bbcfd15dd68
keywords:
- Win32_WinSAT класс WinSAT
- Win32_WinSAT класс WinSAT, описание
topic_type:
- apiref
api_name:
- Win32_WinSAT
- Win32_WinSAT.TimeTaken
- Win32_WinSAT.WinSPRLevel
- Win32_WinSAT.WinSATAssessmentState
- Win32_WinSAT.MemoryScore
- Win32_WinSAT.CPUScore
- Win32_WinSAT.DiskScore
- Win32_WinSAT.D3DScore
- Win32_WinSAT.GraphicsScore
api_location:
- WinSATAPI.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829e5e1b3658771728aab9ef30634d90a8bc6450
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701093"
---
# <a name="win32_winsat-class"></a><span data-ttu-id="2b8d7-105">\_Класс Win32 WinSAT</span><span class="sxs-lookup"><span data-stu-id="2b8d7-105">Win32\_WinSAT class</span></span>

<span data-ttu-id="2b8d7-106">\[**Win32 \_ Служба WinSAT** может быть изменена или недоступна для выпусков после Windows 8.1.\]</span><span class="sxs-lookup"><span data-stu-id="2b8d7-106">\[**Win32\_WinSAT** may be altered or unavailable for releases after Windows 8.1.\]</span></span>

<span data-ttu-id="2b8d7-107">Определяет сведения о сводных оценках для последней формальной оценки.</span><span class="sxs-lookup"><span data-stu-id="2b8d7-107">Defines summary assessment information for the most recent formal assessment.</span></span>

<span data-ttu-id="2b8d7-108">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="2b8d7-108">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b8d7-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b8d7-109">Syntax</span></span>

``` syntax
class Win32_WinSAT
{
  string TimeTaken = "MostRecentAssessment";
  real32 WinSPRLevel;
  uint32 WinSATAssessmentState;
  real32 MemoryScore;
  real32 CPUScore;
  real32 DiskScore;
  real32 D3DScore;
  real32 GraphicsScore;
};
```

## <a name="members"></a><span data-ttu-id="2b8d7-110">Члены</span><span class="sxs-lookup"><span data-stu-id="2b8d7-110">Members</span></span>

<span data-ttu-id="2b8d7-111">Класс **Win32 \_ WinSAT** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2b8d7-111">The **Win32\_WinSAT** class has these types of members:</span></span>

-   [<span data-ttu-id="2b8d7-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="2b8d7-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2b8d7-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="2b8d7-113">Properties</span></span>

<span data-ttu-id="2b8d7-114">Класс **Win32 \_ WinSAT** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2b8d7-114">The **Win32\_WinSAT** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2b8d7-115">**кпускоре**</span><span class="sxs-lookup"><span data-stu-id="2b8d7-115">**CPUScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b8d7-116">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="2b8d7-116">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="2b8d7-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b8d7-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b8d7-118">Оценка процессоров на компьютере.</span><span class="sxs-lookup"><span data-stu-id="2b8d7-118">A score for the processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="2b8d7-119">**D3DScore**</span><span class="sxs-lookup"><span data-stu-id="2b8d7-119">**D3DScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b8d7-120">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="2b8d7-120">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="2b8d7-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b8d7-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b8d7-122">После Windows 8.1 WinSAT больше не оценивает трехмерные графические (игровые) возможности компьютера, а также возможность графического драйвера для отрисовки объектов и выполнения шейдеров с помощью этой оценки.</span><span class="sxs-lookup"><span data-stu-id="2b8d7-122">After Windows 8.1, WinSAT no longer assess the three-dimensional graphics (gaming) capabilities of the computer and the graphics driver's ability to render objects and execute shaders using this assessment.</span></span> <span data-ttu-id="2b8d7-123">Для обеспечения совместимости значения Sentinel отчета WinSAT для метрик и оценок не рассчитываются в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="2b8d7-123">For compatibility, WinSAT report sentinel values for the metrics and scores, however these are not calculated in real time.</span></span>

</dd> <dt>

<span data-ttu-id="2b8d7-124">**дискскоре**</span><span class="sxs-lookup"><span data-stu-id="2b8d7-124">**DiskScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b8d7-125">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="2b8d7-125">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="2b8d7-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b8d7-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b8d7-127">Оценка пропускной способности последовательного чтения на основном жестком диске компьютера.</span><span class="sxs-lookup"><span data-stu-id="2b8d7-127">A score for the sequential read throughput on the primary hard disk on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="2b8d7-128">**графиксскоре**</span><span class="sxs-lookup"><span data-stu-id="2b8d7-128">**GraphicsScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b8d7-129">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="2b8d7-129">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="2b8d7-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b8d7-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b8d7-131">Оценка графических возможностей компьютера.</span><span class="sxs-lookup"><span data-stu-id="2b8d7-131">A score for the graphics capabilities of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="2b8d7-132">**меморискоре**</span><span class="sxs-lookup"><span data-stu-id="2b8d7-132">**MemoryScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b8d7-133">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="2b8d7-133">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="2b8d7-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b8d7-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b8d7-135">Оценка пропускной способности и емкости компьютера в памяти.</span><span class="sxs-lookup"><span data-stu-id="2b8d7-135">A score for the memory throughput and capacity of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="2b8d7-136">**TimeTaken**</span><span class="sxs-lookup"><span data-stu-id="2b8d7-136">**TimeTaken**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b8d7-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2b8d7-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b8d7-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b8d7-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b8d7-139">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="2b8d7-139">Qualifiers: **key**</span></span>
</dt> </dl>

<span data-ttu-id="2b8d7-140">Это свойство должно иметь значение "Мострецентассессмент" в предложении WHERE WQL-запроса.</span><span class="sxs-lookup"><span data-stu-id="2b8d7-140">This property must be set to "MostRecentAssessment" in the WHERE clause of your WQL query.</span></span>

</dd> <dt>

<span data-ttu-id="2b8d7-141">**винсатассессментстате**</span><span class="sxs-lookup"><span data-stu-id="2b8d7-141">**WinSATAssessmentState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b8d7-142">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2b8d7-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2b8d7-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b8d7-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b8d7-144">Состояние оценки.</span><span class="sxs-lookup"><span data-stu-id="2b8d7-144">State of the assessment.</span></span> <span data-ttu-id="2b8d7-145">Описание возможных значений см. в разделе Перечисление [**\_ \_ состояния оценки WinSAT**](/windows/win32/api/winsatcominterfacei/ne-winsatcominterfacei-winsat_assessment_state) .</span><span class="sxs-lookup"><span data-stu-id="2b8d7-145">For a description of the possible values, see the [**WINSAT\_ASSESSMENT\_STATE**](/windows/win32/api/winsatcominterfacei/ne-winsatcominterfacei-winsat_assessment_state) enumeration.</span></span>

<dl> <dt>

<span data-ttu-id="2b8d7-146"><span id="StateUnknown"></span><span id="stateunknown"></span><span id="STATEUNKNOWN"></span>**Статеункновн** (0)</span><span class="sxs-lookup"><span data-stu-id="2b8d7-146"><span id="StateUnknown"></span><span id="stateunknown"></span><span id="STATEUNKNOWN"></span>**StateUnknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2b8d7-147"><span id="Valid"></span><span id="valid"></span><span id="VALID"></span>**Допустимый** (1)</span><span class="sxs-lookup"><span data-stu-id="2b8d7-147"><span id="Valid"></span><span id="valid"></span><span id="VALID"></span>**Valid** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2b8d7-148"><span id="IncoherentWithHardware"></span><span id="incoherentwithhardware"></span><span id="INCOHERENTWITHHARDWARE"></span>**Инкохерентвисхардваре** (2)</span><span class="sxs-lookup"><span data-stu-id="2b8d7-148"><span id="IncoherentWithHardware"></span><span id="incoherentwithhardware"></span><span id="INCOHERENTWITHHARDWARE"></span>**IncoherentWithHardware** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2b8d7-149"><span id="NoAssessmentAvailable"></span><span id="noassessmentavailable"></span><span id="NOASSESSMENTAVAILABLE"></span>**Ноассессментаваилабле** (3)</span><span class="sxs-lookup"><span data-stu-id="2b8d7-149"><span id="NoAssessmentAvailable"></span><span id="noassessmentavailable"></span><span id="NOASSESSMENTAVAILABLE"></span>**NoAssessmentAvailable** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2b8d7-150"><span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**Недопустимое** (4)</span><span class="sxs-lookup"><span data-stu-id="2b8d7-150"><span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**Invalid** (4)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2b8d7-151">**винспрлевел**</span><span class="sxs-lookup"><span data-stu-id="2b8d7-151">**WinSPRLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b8d7-152">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="2b8d7-152">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="2b8d7-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b8d7-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b8d7-154">Базовый показатель для компьютера.</span><span class="sxs-lookup"><span data-stu-id="2b8d7-154">Base score for the computer.</span></span> <span data-ttu-id="2b8d7-155">Дополнительные сведения о значении оценки см. в описании свойства [**ипровидевинсатресултсинфо:: системратинг**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating) .</span><span class="sxs-lookup"><span data-stu-id="2b8d7-155">For details on the score value, see the [**IProvideWinSATResultsInfo::SystemRating**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating) property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2b8d7-156">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2b8d7-156">Remarks</span></span>

<span data-ttu-id="2b8d7-157">Сведения о оценках подкомпонентов, например **меморискоре**, см. в описании свойства [**Ипровидевинсатассессментинфо:: Score**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score) .</span><span class="sxs-lookup"><span data-stu-id="2b8d7-157">For information on the subcomponent scores, such as **MemoryScore**, see the [**IProvideWinSATAssessmentInfo::Score**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score) property.</span></span>

## <a name="examples"></a><span data-ttu-id="2b8d7-158">Примеры</span><span class="sxs-lookup"><span data-stu-id="2b8d7-158">Examples</span></span>

<span data-ttu-id="2b8d7-159">Пример, демонстрирующий использование инструментария WMI для получения данных из этого класса, см. в описании метода [**ипровидевинсатвисуалс:: Get \_ Bitmap**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatvisuals-get_bitmap) .</span><span class="sxs-lookup"><span data-stu-id="2b8d7-159">For an example that shows how to use WMI to retrieve data from this class, see the [**IProvideWinSATVisuals::get\_Bitmap**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatvisuals-get_bitmap) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b8d7-160">Требования</span><span class="sxs-lookup"><span data-stu-id="2b8d7-160">Requirements</span></span>



| <span data-ttu-id="2b8d7-161">Требование</span><span class="sxs-lookup"><span data-stu-id="2b8d7-161">Requirement</span></span> | <span data-ttu-id="2b8d7-162">Значение</span><span class="sxs-lookup"><span data-stu-id="2b8d7-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b8d7-163">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2b8d7-163">Minimum supported client</span></span><br/> | <span data-ttu-id="2b8d7-164">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2b8d7-164">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2b8d7-165">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2b8d7-165">Minimum supported server</span></span><br/> | <span data-ttu-id="2b8d7-166">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2b8d7-166">None supported</span></span><br/>                                                                |
| <span data-ttu-id="2b8d7-167">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2b8d7-167">Namespace</span></span><br/>                | <span data-ttu-id="2b8d7-168">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="2b8d7-168">Root\\CIMv2</span></span><br/>                                                                   |
| <span data-ttu-id="2b8d7-169">MOF</span><span class="sxs-lookup"><span data-stu-id="2b8d7-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b8d7-170"><dt>WinSAT. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2b8d7-170"><dt>WinSAT.mof</dt></span></span> </dl>    |
| <span data-ttu-id="2b8d7-171">DLL</span><span class="sxs-lookup"><span data-stu-id="2b8d7-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b8d7-172"><dt>WinSATAPI.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b8d7-172"><dt>WinSATAPI.dll</dt></span></span> </dl> |



 

 





