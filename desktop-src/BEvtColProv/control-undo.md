---
description: Восстановите активную конфигурацию сборщика из предыдущего файла резервной копии (определяется путем возврата из текущей исходной метки времени).
ms.assetid: 150fa554-9efd-483e-a177-5fc7766a6a6c
ms.tgt_platform: multiple
title: Метод Undo класса Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Undo
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 285f1ec39ea52f6c388e324f72745d72f65207e6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655651"
---
# <a name="undo-method-of-the-control-class"></a><span data-ttu-id="2a520-103">Метод Undo класса Control</span><span class="sxs-lookup"><span data-stu-id="2a520-103">Undo method of the Control class</span></span>

<span data-ttu-id="2a520-104">Восстановите активную конфигурацию сборщика из предыдущего файла резервной копии (определяется путем возврата из текущей исходной метки времени).</span><span class="sxs-lookup"><span data-stu-id="2a520-104">Restore the active configuration of the collector from the previous backup file (determined by going back from the current original timestamp).</span></span> <span data-ttu-id="2a520-105">Если конфигурация была только что установлена, это означает отмену этого изменения.</span><span class="sxs-lookup"><span data-stu-id="2a520-105">If the configuration has been just set, this means undoing that change.</span></span> <span data-ttu-id="2a520-106">Последовательные вызовы будут отменяться до более ранних и более ранних конфигураций.</span><span class="sxs-lookup"><span data-stu-id="2a520-106">The consecutive calls will undo to the earlier and earlier configurations.</span></span> <span data-ttu-id="2a520-107">Возвращает 1 при успешном выполнении, 0 при ошибке.</span><span class="sxs-lookup"><span data-stu-id="2a520-107">Returns 1 on success, 0 on error.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a520-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2a520-108">Syntax</span></span>


```mof
Uint32 Undo(
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



## <a name="parameters"></a><span data-ttu-id="2a520-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2a520-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a520-110">*Олдтиместамплов* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2a520-110">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a520-111">Метка времени, когда была задана предыдущая конфигурация.</span><span class="sxs-lookup"><span data-stu-id="2a520-111">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="2a520-112">Если значение не равно 0, включает проверку атомарности: Новая конфигурация будет применена только в том случае, если метка времени старой конфигурации совпадает (т. е. конфигурация не изменилась).</span><span class="sxs-lookup"><span data-stu-id="2a520-112">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="2a520-113">Это Младшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="2a520-113">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="2a520-114">*Олдтиместамфигх* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2a520-114">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a520-115">Метка времени, когда была задана предыдущая конфигурация.</span><span class="sxs-lookup"><span data-stu-id="2a520-115">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="2a520-116">Если значение не равно 0, включает проверку атомарности: Новая конфигурация будет применена только в том случае, если метка времени старой конфигурации совпадает (т. е. конфигурация не изменилась).</span><span class="sxs-lookup"><span data-stu-id="2a520-116">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="2a520-117">Это старшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="2a520-117">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="2a520-118">*Невтиместамплов* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2a520-118">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a520-119">Метка времени, когда была задана новая конфигурация, если вызов завершился успешно.</span><span class="sxs-lookup"><span data-stu-id="2a520-119">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="2a520-120">Это Младшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="2a520-120">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="2a520-121">*Невтиместамфигх* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2a520-121">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a520-122">Метка времени, когда была задана новая конфигурация, если вызов завершился успешно.</span><span class="sxs-lookup"><span data-stu-id="2a520-122">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="2a520-123">Это старшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="2a520-123">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="2a520-124">*Оригиналтиместамплов* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2a520-124">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a520-125">Исходная метка времени, когда Восстановленная конфигурация была задана в первый раз.</span><span class="sxs-lookup"><span data-stu-id="2a520-125">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="2a520-126">Это Младшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="2a520-126">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="2a520-127">*Оригиналтиместамфигх* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2a520-127">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a520-128">Исходная метка времени, когда Восстановленная конфигурация была задана в первый раз.</span><span class="sxs-lookup"><span data-stu-id="2a520-128">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="2a520-129">Это старшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="2a520-129">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="2a520-130">*ErrorString* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2a520-130">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a520-131">Текстовая строка с описанием ошибки.</span><span class="sxs-lookup"><span data-stu-id="2a520-131">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="2a520-132">*Варнингстринг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2a520-132">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a520-133">Текстовая строка с предупреждениями.</span><span class="sxs-lookup"><span data-stu-id="2a520-133">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="2a520-134">*Инфостринг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2a520-134">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a520-135">Текстовая строка со сведениями о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="2a520-135">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="2a520-136">*ErrorType* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2a520-136">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a520-137">Тип ошибки: Обратите внимание, что 0 или отсутствует указывает на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="2a520-137">The type of the error: note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="2a520-138">0</span><span class="sxs-lookup"><span data-stu-id="2a520-138">0</span></span>
</dt> <dd>

<span data-ttu-id="2a520-139">Успешно.</span><span class="sxs-lookup"><span data-stu-id="2a520-139">Success.</span></span>

</dd> <dt>

<span data-ttu-id="2a520-140">1</span><span class="sxs-lookup"><span data-stu-id="2a520-140">1</span></span>
</dt> <dd>

<span data-ttu-id="2a520-141">неправильный формат аргумента</span><span class="sxs-lookup"><span data-stu-id="2a520-141">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="2a520-142">2</span><span class="sxs-lookup"><span data-stu-id="2a520-142">2</span></span>
</dt> <dd>

<span data-ttu-id="2a520-143">неверное значение аргумента</span><span class="sxs-lookup"><span data-stu-id="2a520-143">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="2a520-144">3</span><span class="sxs-lookup"><span data-stu-id="2a520-144">3</span></span>
</dt> <dd>

<span data-ttu-id="2a520-145">Ошибка при открытии ресурса (сокет)</span><span class="sxs-lookup"><span data-stu-id="2a520-145">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="2a520-146">4</span><span class="sxs-lookup"><span data-stu-id="2a520-146">4</span></span>
</dt> <dd>

<span data-ttu-id="2a520-147">Ошибка сохраняемости (запись файла)</span><span class="sxs-lookup"><span data-stu-id="2a520-147">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="2a520-148">5</span><span class="sxs-lookup"><span data-stu-id="2a520-148">5</span></span>
</dt> <dd>

<span data-ttu-id="2a520-149">Ошибка атомарности (старая метка времени не совпадает)</span><span class="sxs-lookup"><span data-stu-id="2a520-149">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a520-150">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2a520-150">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="2a520-151">0</span><span class="sxs-lookup"><span data-stu-id="2a520-151">0</span></span>

<span data-ttu-id="2a520-152">Сбой</span><span class="sxs-lookup"><span data-stu-id="2a520-152">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2a520-153">1</span><span class="sxs-lookup"><span data-stu-id="2a520-153">1</span></span>

<span data-ttu-id="2a520-154">Успешно</span><span class="sxs-lookup"><span data-stu-id="2a520-154">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2a520-155">Требования</span><span class="sxs-lookup"><span data-stu-id="2a520-155">Requirements</span></span>



| <span data-ttu-id="2a520-156">Требование</span><span class="sxs-lookup"><span data-stu-id="2a520-156">Requirement</span></span> | <span data-ttu-id="2a520-157">Значение</span><span class="sxs-lookup"><span data-stu-id="2a520-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a520-158">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2a520-158">Minimum supported client</span></span><br/> | <span data-ttu-id="2a520-159">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2a520-159">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2a520-160">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2a520-160">Minimum supported server</span></span><br/> | <span data-ttu-id="2a520-161">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2a520-161">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="2a520-162">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2a520-162">Namespace</span></span><br/>                | <span data-ttu-id="2a520-163">Корневой \\ узел Microsoft \\ Windows \\ бутевентколлектор</span><span class="sxs-lookup"><span data-stu-id="2a520-163">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="2a520-164">MOF</span><span class="sxs-lookup"><span data-stu-id="2a520-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a520-165"><dt>Бутевентколлекторвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2a520-165"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="2a520-166">DLL</span><span class="sxs-lookup"><span data-stu-id="2a520-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a520-167"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2a520-167"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="2a520-168">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2a520-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a520-169">**Элемента**</span><span class="sxs-lookup"><span data-stu-id="2a520-169">**Control**</span></span>](control.md)
</dt> </dl>

 

