---
description: Восстановите активную конфигурацию сборщика из файла резервной копии.
ms.assetid: b59b04a5-d2b3-4299-8347-5026b982dc02
ms.tgt_platform: multiple
title: Метод RestoreFile класса Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.RestoreFile
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 330486da86c9cac5c5f700d2aea91e0844fdca09
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990346"
---
# <a name="restorefile-method-of-the-control-class"></a><span data-ttu-id="b4015-103">Метод RestoreFile класса Control</span><span class="sxs-lookup"><span data-stu-id="b4015-103">RestoreFile method of the Control class</span></span>

<span data-ttu-id="b4015-104">Восстановите активную конфигурацию сборщика из файла резервной копии.</span><span class="sxs-lookup"><span data-stu-id="b4015-104">Restore the active configuration of the collector from a backup file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4015-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4015-105">Syntax</span></span>


```mof
Uint32 RestoreFile(
  [in]  string File,
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



## <a name="parameters"></a><span data-ttu-id="b4015-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4015-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4015-107">*Файл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b4015-107">*File* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4015-108">Имя восстанавливаемого файла резервной копии из списка, возвращенного Листбаккупс ().</span><span class="sxs-lookup"><span data-stu-id="b4015-108">Name of the backup file to restore, from the list returned by ListBackups().</span></span>

</dd> <dt>

<span data-ttu-id="b4015-109">*Олдтиместамплов* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b4015-109">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4015-110">Метка времени, когда была задана предыдущая конфигурация.</span><span class="sxs-lookup"><span data-stu-id="b4015-110">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="b4015-111">Если значение не равно 0, включает проверку атомарности: Новая конфигурация будет применена только в том случае, если метка времени старой конфигурации совпадает (т. е. конфигурация не изменилась).</span><span class="sxs-lookup"><span data-stu-id="b4015-111">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="b4015-112">Это Младшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="b4015-112">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="b4015-113">*Олдтиместамфигх* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b4015-113">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4015-114">Метка времени, когда была задана предыдущая конфигурация.</span><span class="sxs-lookup"><span data-stu-id="b4015-114">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="b4015-115">Если значение не равно 0, включает проверку атомарности: Новая конфигурация будет применена только в том случае, если метка времени старой конфигурации совпадает (т. е. конфигурация не изменилась).</span><span class="sxs-lookup"><span data-stu-id="b4015-115">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="b4015-116">Это старшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="b4015-116">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="b4015-117">*Невтиместамплов* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b4015-117">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4015-118">Метка времени, когда была задана новая конфигурация, если вызов завершился успешно.</span><span class="sxs-lookup"><span data-stu-id="b4015-118">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="b4015-119">Это Младшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="b4015-119">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="b4015-120">*Невтиместамфигх* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b4015-120">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4015-121">Метка времени, когда была задана новая конфигурация, если вызов завершился успешно.</span><span class="sxs-lookup"><span data-stu-id="b4015-121">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="b4015-122">Это старшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="b4015-122">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="b4015-123">*Оригиналтиместамплов* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b4015-123">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4015-124">Исходная метка времени, когда Восстановленная конфигурация была задана в первый раз.</span><span class="sxs-lookup"><span data-stu-id="b4015-124">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="b4015-125">Это Младшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="b4015-125">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="b4015-126">*Оригиналтиместамфигх* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b4015-126">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4015-127">Исходная метка времени, когда Восстановленная конфигурация была задана в первый раз.</span><span class="sxs-lookup"><span data-stu-id="b4015-127">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="b4015-128">Это старшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="b4015-128">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="b4015-129">*ErrorString* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b4015-129">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4015-130">Текстовая строка с описанием ошибки.</span><span class="sxs-lookup"><span data-stu-id="b4015-130">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="b4015-131">*Варнингстринг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b4015-131">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4015-132">Текстовая строка с предупреждениями.</span><span class="sxs-lookup"><span data-stu-id="b4015-132">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="b4015-133">*Инфостринг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b4015-133">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4015-134">Текстовая строка со сведениями о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="b4015-134">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="b4015-135">*ErrorType* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b4015-135">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4015-136">Тип ошибки: Обратите внимание, что 0 или отсутствует указывает на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="b4015-136">The type of the error: note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="b4015-137">0</span><span class="sxs-lookup"><span data-stu-id="b4015-137">0</span></span>
</dt> <dd>

<span data-ttu-id="b4015-138">Успешно.</span><span class="sxs-lookup"><span data-stu-id="b4015-138">Success.</span></span>

</dd> <dt>

<span data-ttu-id="b4015-139">1</span><span class="sxs-lookup"><span data-stu-id="b4015-139">1</span></span>
</dt> <dd>

<span data-ttu-id="b4015-140">неправильный формат аргумента</span><span class="sxs-lookup"><span data-stu-id="b4015-140">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="b4015-141">2</span><span class="sxs-lookup"><span data-stu-id="b4015-141">2</span></span>
</dt> <dd>

<span data-ttu-id="b4015-142">неверное значение аргумента</span><span class="sxs-lookup"><span data-stu-id="b4015-142">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="b4015-143">3</span><span class="sxs-lookup"><span data-stu-id="b4015-143">3</span></span>
</dt> <dd>

<span data-ttu-id="b4015-144">Ошибка при открытии ресурса (сокет)</span><span class="sxs-lookup"><span data-stu-id="b4015-144">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="b4015-145">4</span><span class="sxs-lookup"><span data-stu-id="b4015-145">4</span></span>
</dt> <dd>

<span data-ttu-id="b4015-146">Ошибка сохраняемости (запись файла)</span><span class="sxs-lookup"><span data-stu-id="b4015-146">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="b4015-147">5</span><span class="sxs-lookup"><span data-stu-id="b4015-147">5</span></span>
</dt> <dd>

<span data-ttu-id="b4015-148">Ошибка атомарности (старая метка времени не совпадает)</span><span class="sxs-lookup"><span data-stu-id="b4015-148">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4015-149">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b4015-149">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="b4015-150">0</span><span class="sxs-lookup"><span data-stu-id="b4015-150">0</span></span>

<span data-ttu-id="b4015-151">Сбой</span><span class="sxs-lookup"><span data-stu-id="b4015-151">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b4015-152">1</span><span class="sxs-lookup"><span data-stu-id="b4015-152">1</span></span>

<span data-ttu-id="b4015-153">Успешно</span><span class="sxs-lookup"><span data-stu-id="b4015-153">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b4015-154">Требования</span><span class="sxs-lookup"><span data-stu-id="b4015-154">Requirements</span></span>



| <span data-ttu-id="b4015-155">Требование</span><span class="sxs-lookup"><span data-stu-id="b4015-155">Requirement</span></span> | <span data-ttu-id="b4015-156">Значение</span><span class="sxs-lookup"><span data-stu-id="b4015-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4015-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b4015-157">Minimum supported client</span></span><br/> | <span data-ttu-id="b4015-158">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b4015-158">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b4015-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b4015-159">Minimum supported server</span></span><br/> | <span data-ttu-id="b4015-160">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b4015-160">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="b4015-161">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b4015-161">Namespace</span></span><br/>                | <span data-ttu-id="b4015-162">Корневой \\ узел Microsoft \\ Windows \\ бутевентколлектор</span><span class="sxs-lookup"><span data-stu-id="b4015-162">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="b4015-163">MOF</span><span class="sxs-lookup"><span data-stu-id="b4015-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b4015-164"><dt>Бутевентколлекторвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b4015-164"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="b4015-165">DLL</span><span class="sxs-lookup"><span data-stu-id="b4015-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4015-166"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b4015-166"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="b4015-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4015-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4015-168">**Элемента**</span><span class="sxs-lookup"><span data-stu-id="b4015-168">**Control**</span></span>](control.md)
</dt> </dl>

 

