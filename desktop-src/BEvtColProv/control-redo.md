---
description: Сброс активной конфигурации сборщика из более позднего файла резервной копии (определяется путем перехода от текущей исходной метки времени). Если конфигурация отменена, это означает, что изменение отменено.
ms.assetid: bd153ea3-9148-4e65-a44e-3f9fa1855f2f
ms.tgt_platform: multiple
title: Метод Redo класса Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Redo
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 5ed77aac62dca0bf81ed13474e8acebb0235ea71
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140875"
---
# <a name="redo-method-of-the-control-class"></a><span data-ttu-id="db256-104">Метод Redo класса Control</span><span class="sxs-lookup"><span data-stu-id="db256-104">Redo method of the Control class</span></span>

<span data-ttu-id="db256-105">Сброс активной конфигурации сборщика из более позднего файла резервной копии (определяется путем перехода от текущей исходной метки времени).</span><span class="sxs-lookup"><span data-stu-id="db256-105">Reset the active configuration of the collector from the later backup file (determined by going forward from the current original timestamp).</span></span> <span data-ttu-id="db256-106">Если конфигурация отменена, это означает, что изменение отменено.</span><span class="sxs-lookup"><span data-stu-id="db256-106">If the configuration has been undone, this means redoing the undone change.</span></span>

## <a name="syntax"></a><span data-ttu-id="db256-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db256-107">Syntax</span></span>


```mof
Uint32 Redo(
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



## <a name="parameters"></a><span data-ttu-id="db256-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="db256-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db256-109">*Олдтиместамплов* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="db256-109">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db256-110">Метка времени, когда была задана предыдущая конфигурация.</span><span class="sxs-lookup"><span data-stu-id="db256-110">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="db256-111">Если значение не равно 0, включает проверку атомарности: Новая конфигурация будет применена только в том случае, если метка времени старой конфигурации совпадает (т. е. конфигурация не изменилась).</span><span class="sxs-lookup"><span data-stu-id="db256-111">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="db256-112">Это Младшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="db256-112">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="db256-113">*Олдтиместамфигх* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="db256-113">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db256-114">Метка времени, когда была задана предыдущая конфигурация.</span><span class="sxs-lookup"><span data-stu-id="db256-114">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="db256-115">Если значение не равно 0, включает проверку атомарности: Новая конфигурация будет применена только в том случае, если метка времени старой конфигурации совпадает (т. е. конфигурация не изменилась).</span><span class="sxs-lookup"><span data-stu-id="db256-115">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="db256-116">Это старшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="db256-116">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="db256-117">*Невтиместамплов* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="db256-117">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db256-118">Метка времени, когда была задана новая конфигурация, если вызов завершился успешно.</span><span class="sxs-lookup"><span data-stu-id="db256-118">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="db256-119">Это Младшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="db256-119">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="db256-120">*Невтиместамфигх* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="db256-120">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db256-121">Метка времени, когда была задана новая конфигурация, если вызов завершился успешно.</span><span class="sxs-lookup"><span data-stu-id="db256-121">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="db256-122">Это старшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="db256-122">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="db256-123">*Оригиналтиместамплов* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="db256-123">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db256-124">Исходная метка времени, когда Восстановленная конфигурация была задана в первый раз.</span><span class="sxs-lookup"><span data-stu-id="db256-124">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="db256-125">Это Младшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="db256-125">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="db256-126">*Оригиналтиместамфигх* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="db256-126">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db256-127">Исходная метка времени, когда Восстановленная конфигурация была задана в первый раз.</span><span class="sxs-lookup"><span data-stu-id="db256-127">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="db256-128">Это старшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="db256-128">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="db256-129">*ErrorString* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="db256-129">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db256-130">Текстовая строка с описанием ошибки.</span><span class="sxs-lookup"><span data-stu-id="db256-130">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="db256-131">*Варнингстринг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="db256-131">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db256-132">Текстовая строка с предупреждениями.</span><span class="sxs-lookup"><span data-stu-id="db256-132">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="db256-133">*Инфостринг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="db256-133">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db256-134">Текстовая строка со сведениями о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="db256-134">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="db256-135">*ErrorType* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="db256-135">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db256-136">Тип ошибки.</span><span class="sxs-lookup"><span data-stu-id="db256-136">The type of the error.</span></span> <span data-ttu-id="db256-137">Обратите внимание, что 0 или отсутствует указывает на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="db256-137">Note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="db256-138">0</span><span class="sxs-lookup"><span data-stu-id="db256-138">0</span></span>
</dt> <dd>

<span data-ttu-id="db256-139">Успешно.</span><span class="sxs-lookup"><span data-stu-id="db256-139">Success.</span></span>

</dd> <dt>

<span data-ttu-id="db256-140">1</span><span class="sxs-lookup"><span data-stu-id="db256-140">1</span></span>
</dt> <dd>

<span data-ttu-id="db256-141">неправильный формат аргумента</span><span class="sxs-lookup"><span data-stu-id="db256-141">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="db256-142">2</span><span class="sxs-lookup"><span data-stu-id="db256-142">2</span></span>
</dt> <dd>

<span data-ttu-id="db256-143">неверное значение аргумента</span><span class="sxs-lookup"><span data-stu-id="db256-143">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="db256-144">3</span><span class="sxs-lookup"><span data-stu-id="db256-144">3</span></span>
</dt> <dd>

<span data-ttu-id="db256-145">Ошибка при открытии ресурса (сокет)</span><span class="sxs-lookup"><span data-stu-id="db256-145">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="db256-146">4</span><span class="sxs-lookup"><span data-stu-id="db256-146">4</span></span>
</dt> <dd>

<span data-ttu-id="db256-147">Ошибка сохраняемости (запись файла)</span><span class="sxs-lookup"><span data-stu-id="db256-147">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="db256-148">5</span><span class="sxs-lookup"><span data-stu-id="db256-148">5</span></span>
</dt> <dd>

<span data-ttu-id="db256-149">Ошибка атомарности (старая метка времени не совпадает)</span><span class="sxs-lookup"><span data-stu-id="db256-149">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db256-150">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="db256-150">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="db256-151">0</span><span class="sxs-lookup"><span data-stu-id="db256-151">0</span></span>

<span data-ttu-id="db256-152">Сбой</span><span class="sxs-lookup"><span data-stu-id="db256-152">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="db256-153">1</span><span class="sxs-lookup"><span data-stu-id="db256-153">1</span></span>

<span data-ttu-id="db256-154">Успешно</span><span class="sxs-lookup"><span data-stu-id="db256-154">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="db256-155">Требования</span><span class="sxs-lookup"><span data-stu-id="db256-155">Requirements</span></span>



| <span data-ttu-id="db256-156">Требование</span><span class="sxs-lookup"><span data-stu-id="db256-156">Requirement</span></span> | <span data-ttu-id="db256-157">Значение</span><span class="sxs-lookup"><span data-stu-id="db256-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db256-158">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="db256-158">Minimum supported client</span></span><br/> | <span data-ttu-id="db256-159">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="db256-159">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="db256-160">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="db256-160">Minimum supported server</span></span><br/> | <span data-ttu-id="db256-161">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="db256-161">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="db256-162">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="db256-162">Namespace</span></span><br/>                | <span data-ttu-id="db256-163">Корневой \\ узел Microsoft \\ Windows \\ бутевентколлектор</span><span class="sxs-lookup"><span data-stu-id="db256-163">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="db256-164">MOF</span><span class="sxs-lookup"><span data-stu-id="db256-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="db256-165"><dt>Бутевентколлекторвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="db256-165"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="db256-166">DLL</span><span class="sxs-lookup"><span data-stu-id="db256-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db256-167"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="db256-167"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="db256-168">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="db256-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db256-169">**Элемента**</span><span class="sxs-lookup"><span data-stu-id="db256-169">**Control**</span></span>](control.md)
</dt> </dl>

 

