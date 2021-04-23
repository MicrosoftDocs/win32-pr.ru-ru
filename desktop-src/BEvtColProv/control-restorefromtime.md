---
description: Восстановление активной конфигурации сборщика из файла резервной копии, выбранного по метке времени.
ms.assetid: 3ee4156b-c68f-4c44-b9be-dd86e8f4b340
ms.tgt_platform: multiple
title: Метод Ресторефромтиме класса Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.RestoreFromTime
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 79b89c0c89e4954d8a641d037e08757f83cad618
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650464"
---
# <a name="restorefromtime-method-of-the-control-class"></a><span data-ttu-id="cb77b-103">Метод Ресторефромтиме класса Control</span><span class="sxs-lookup"><span data-stu-id="cb77b-103">RestoreFromTime method of the Control class</span></span>

<span data-ttu-id="cb77b-104">Восстановление активной конфигурации сборщика из файла резервной копии, выбранного по метке времени.</span><span class="sxs-lookup"><span data-stu-id="cb77b-104">Restore the active configuration of the collector from a backup file, selected by a timestamp.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb77b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb77b-105">Syntax</span></span>


```mof
Uint32 RestoreFromTime(
  [in]  Uint32 TargetTimestampLow,
  [in]  Uint32 TargetTimestampHigh,
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] Uint32 NewTimestampLow,
  [out] Uint32 NewTimestampHigh,
  [out] Uint32 OriginalTimestampLow,
  [out] Uint32 OriginalTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a><span data-ttu-id="cb77b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb77b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb77b-107">*Таржеттиместамплов* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cb77b-107">*TargetTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb77b-108">Восстановите файл резервной копии по этой метке времени.</span><span class="sxs-lookup"><span data-stu-id="cb77b-108">Restore to the backup file at this timestamp.</span></span> <span data-ttu-id="cb77b-109">Это Младшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="cb77b-109">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="cb77b-110">*Таржеттиместамфигх* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cb77b-110">*TargetTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb77b-111">Восстановите файл резервной копии по этой метке времени.</span><span class="sxs-lookup"><span data-stu-id="cb77b-111">Restore to the backup file at this timestamp.</span></span> <span data-ttu-id="cb77b-112">Это старшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="cb77b-112">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="cb77b-113">*Олдтиместамплов* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cb77b-113">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb77b-114">Метка времени, когда была задана предыдущая конфигурация.</span><span class="sxs-lookup"><span data-stu-id="cb77b-114">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="cb77b-115">Если значение не равно 0, включает проверку атомарности: Новая конфигурация будет применена только в том случае, если метка времени старой конфигурации совпадает (т. е. конфигурация не изменилась).</span><span class="sxs-lookup"><span data-stu-id="cb77b-115">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="cb77b-116">Это Младшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="cb77b-116">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="cb77b-117">*Олдтиместамфигх* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cb77b-117">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb77b-118">Метка времени, когда была задана предыдущая конфигурация.</span><span class="sxs-lookup"><span data-stu-id="cb77b-118">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="cb77b-119">Если значение не равно 0, включает проверку атомарности: Новая конфигурация будет применена только в том случае, если метка времени старой конфигурации совпадает (т. е. конфигурация не изменилась).</span><span class="sxs-lookup"><span data-stu-id="cb77b-119">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="cb77b-120">Это старшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="cb77b-120">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="cb77b-121">*Невтиместамплов* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cb77b-121">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb77b-122">Метка времени, когда была задана новая конфигурация, если вызов завершился успешно.</span><span class="sxs-lookup"><span data-stu-id="cb77b-122">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="cb77b-123">Это Младшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="cb77b-123">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="cb77b-124">*Невтиместамфигх* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cb77b-124">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb77b-125">Метка времени, когда была задана новая конфигурация, если вызов завершился успешно.</span><span class="sxs-lookup"><span data-stu-id="cb77b-125">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="cb77b-126">Это старшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="cb77b-126">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="cb77b-127">*Оригиналтиместамплов* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cb77b-127">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb77b-128">Исходная метка времени, когда Восстановленная конфигурация была задана в первый раз.</span><span class="sxs-lookup"><span data-stu-id="cb77b-128">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="cb77b-129">Это Младшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="cb77b-129">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="cb77b-130">*Оригиналтиместамфигх* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cb77b-130">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb77b-131">Исходная метка времени, когда Восстановленная конфигурация была задана в первый раз.</span><span class="sxs-lookup"><span data-stu-id="cb77b-131">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="cb77b-132">Это старшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="cb77b-132">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="cb77b-133">*ErrorString* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cb77b-133">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb77b-134">Текстовая строка с описанием ошибки.</span><span class="sxs-lookup"><span data-stu-id="cb77b-134">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="cb77b-135">*Варнингстринг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cb77b-135">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb77b-136">Текстовая строка с предупреждениями.</span><span class="sxs-lookup"><span data-stu-id="cb77b-136">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="cb77b-137">*Инфостринг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cb77b-137">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb77b-138">Текстовая строка со сведениями о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="cb77b-138">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="cb77b-139">*ErrorType* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cb77b-139">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb77b-140">Тип ошибки: Обратите внимание, что 0 или отсутствует указывает на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="cb77b-140">The type of the error: note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="cb77b-141">0</span><span class="sxs-lookup"><span data-stu-id="cb77b-141">0</span></span>
</dt> <dd>

<span data-ttu-id="cb77b-142">Успешно.</span><span class="sxs-lookup"><span data-stu-id="cb77b-142">Success.</span></span>

</dd> <dt>

<span data-ttu-id="cb77b-143">1</span><span class="sxs-lookup"><span data-stu-id="cb77b-143">1</span></span>
</dt> <dd>

<span data-ttu-id="cb77b-144">неправильный формат аргумента</span><span class="sxs-lookup"><span data-stu-id="cb77b-144">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="cb77b-145">2</span><span class="sxs-lookup"><span data-stu-id="cb77b-145">2</span></span>
</dt> <dd>

<span data-ttu-id="cb77b-146">неверное значение аргумента</span><span class="sxs-lookup"><span data-stu-id="cb77b-146">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="cb77b-147">3</span><span class="sxs-lookup"><span data-stu-id="cb77b-147">3</span></span>
</dt> <dd>

<span data-ttu-id="cb77b-148">Ошибка при открытии ресурса (сокет)</span><span class="sxs-lookup"><span data-stu-id="cb77b-148">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="cb77b-149">4</span><span class="sxs-lookup"><span data-stu-id="cb77b-149">4</span></span>
</dt> <dd>

<span data-ttu-id="cb77b-150">Ошибка сохраняемости (запись файла)</span><span class="sxs-lookup"><span data-stu-id="cb77b-150">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="cb77b-151">5</span><span class="sxs-lookup"><span data-stu-id="cb77b-151">5</span></span>
</dt> <dd>

<span data-ttu-id="cb77b-152">Ошибка атомарности (старая метка времени не совпадает)</span><span class="sxs-lookup"><span data-stu-id="cb77b-152">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb77b-153">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb77b-153">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="cb77b-154">0</span><span class="sxs-lookup"><span data-stu-id="cb77b-154">0</span></span>

<span data-ttu-id="cb77b-155">Сбой</span><span class="sxs-lookup"><span data-stu-id="cb77b-155">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="cb77b-156">1</span><span class="sxs-lookup"><span data-stu-id="cb77b-156">1</span></span>

<span data-ttu-id="cb77b-157">Успешно</span><span class="sxs-lookup"><span data-stu-id="cb77b-157">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cb77b-158">Требования</span><span class="sxs-lookup"><span data-stu-id="cb77b-158">Requirements</span></span>



| <span data-ttu-id="cb77b-159">Требование</span><span class="sxs-lookup"><span data-stu-id="cb77b-159">Requirement</span></span> | <span data-ttu-id="cb77b-160">Значение</span><span class="sxs-lookup"><span data-stu-id="cb77b-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb77b-161">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cb77b-161">Minimum supported client</span></span><br/> | <span data-ttu-id="cb77b-162">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="cb77b-162">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="cb77b-163">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cb77b-163">Minimum supported server</span></span><br/> | <span data-ttu-id="cb77b-164">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="cb77b-164">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="cb77b-165">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cb77b-165">Namespace</span></span><br/>                | <span data-ttu-id="cb77b-166">Корневой \\ узел Microsoft \\ Windows \\ бутевентколлектор</span><span class="sxs-lookup"><span data-stu-id="cb77b-166">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="cb77b-167">MOF</span><span class="sxs-lookup"><span data-stu-id="cb77b-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb77b-168"><dt>Бутевентколлекторвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cb77b-168"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="cb77b-169">DLL</span><span class="sxs-lookup"><span data-stu-id="cb77b-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb77b-170"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cb77b-170"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="cb77b-171">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb77b-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb77b-172">**Элемента**</span><span class="sxs-lookup"><span data-stu-id="cb77b-172">**Control**</span></span>](control.md)
</dt> </dl>

 

