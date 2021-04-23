---
description: Если текущая конфигурация является результатом операции отмены/повтора или восстановления, помечает ее как, если она задана явным образом, чтобы журнал сохранял время, когда оно было задано, и файл резервной копии будет создан для него при следующем изменении конфигурации.
ms.assetid: 1b3d398a-c7f9-4e21-9e43-1245a13fe564
ms.tgt_platform: multiple
title: Метод Checkpoint класса Control (Срресторептапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Checkpoint
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 44453f647d55f29a9a6cfc5622e29dcc88ad2446
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140882"
---
# <a name="checkpoint-method-of-the-control-class"></a><span data-ttu-id="0a657-103">Метод Checkpoint класса Control</span><span class="sxs-lookup"><span data-stu-id="0a657-103">Checkpoint method of the Control class</span></span>

<span data-ttu-id="0a657-104">Если текущая конфигурация является результатом операции отмены/повтора или восстановления, помечает ее как, если она задана явным образом, чтобы журнал сохранял время, когда оно было задано, и файл резервной копии будет создан для него при следующем изменении конфигурации.</span><span class="sxs-lookup"><span data-stu-id="0a657-104">If the current configuration is a result of the Undo/Redo/Restore, marks it as if it has been set explicitly, so that the history will preserve the time when it was set, and a backup file will be created for it on the next configuration change.</span></span> <span data-ttu-id="0a657-105">Если текущая конфигурация уже задана явно, не оказывает никакого влияния.</span><span class="sxs-lookup"><span data-stu-id="0a657-105">If the current configuration was already set explicitly, has no effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a657-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0a657-106">Syntax</span></span>


```mof
Uint32 Checkpoint(
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a><span data-ttu-id="0a657-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0a657-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a657-108">*Олдтиместамплов* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0a657-108">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a657-109">Метка времени, когда была задана текущая конфигурация.</span><span class="sxs-lookup"><span data-stu-id="0a657-109">The timestamp of when the current configuration was set.</span></span> <span data-ttu-id="0a657-110">Если значение не равно 0, включает проверку атомарности: действие будет применено только в том случае, если метка времени старой конфигурации совпадает (т. е. конфигурация не изменилась).</span><span class="sxs-lookup"><span data-stu-id="0a657-110">If not 0, enables the atomicity check: the action will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="0a657-111">Это Младшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="0a657-111">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="0a657-112">*Олдтиместамфигх* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0a657-112">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a657-113">Метка времени, когда была задана текущая конфигурация.</span><span class="sxs-lookup"><span data-stu-id="0a657-113">The timestamp of when the current configuration was set.</span></span> <span data-ttu-id="0a657-114">Если значение не равно 0, включает проверку атомарности: действие будет применено только в том случае, если метка времени старой конфигурации совпадает (т. е. конфигурация не изменилась).</span><span class="sxs-lookup"><span data-stu-id="0a657-114">If not 0, enables the atomicity check: the action will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="0a657-115">Это старшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="0a657-115">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="0a657-116">*ErrorString* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0a657-116">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a657-117">Текстовая строка с описанием ошибки.</span><span class="sxs-lookup"><span data-stu-id="0a657-117">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="0a657-118">*Варнингстринг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0a657-118">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a657-119">Текстовая строка с предупреждениями.</span><span class="sxs-lookup"><span data-stu-id="0a657-119">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="0a657-120">*Инфостринг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0a657-120">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a657-121">Текстовая строка со сведениями о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="0a657-121">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="0a657-122">*ErrorType* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0a657-122">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a657-123">Тип ошибки.</span><span class="sxs-lookup"><span data-stu-id="0a657-123">The type of the error.</span></span> <span data-ttu-id="0a657-124">Обратите внимание, что 0 или отсутствует указывает на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="0a657-124">Note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="0a657-125">0</span><span class="sxs-lookup"><span data-stu-id="0a657-125">0</span></span>
</dt> <dd>

<span data-ttu-id="0a657-126">Успешно.</span><span class="sxs-lookup"><span data-stu-id="0a657-126">Success.</span></span>

</dd> <dt>

<span data-ttu-id="0a657-127">1</span><span class="sxs-lookup"><span data-stu-id="0a657-127">1</span></span>
</dt> <dd>

<span data-ttu-id="0a657-128">неправильный формат аргумента</span><span class="sxs-lookup"><span data-stu-id="0a657-128">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="0a657-129">2</span><span class="sxs-lookup"><span data-stu-id="0a657-129">2</span></span>
</dt> <dd>

<span data-ttu-id="0a657-130">неверное значение аргумента</span><span class="sxs-lookup"><span data-stu-id="0a657-130">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="0a657-131">3</span><span class="sxs-lookup"><span data-stu-id="0a657-131">3</span></span>
</dt> <dd>

<span data-ttu-id="0a657-132">Ошибка при открытии ресурса (сокет)</span><span class="sxs-lookup"><span data-stu-id="0a657-132">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="0a657-133">4</span><span class="sxs-lookup"><span data-stu-id="0a657-133">4</span></span>
</dt> <dd>

<span data-ttu-id="0a657-134">Ошибка сохраняемости (запись файла)</span><span class="sxs-lookup"><span data-stu-id="0a657-134">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="0a657-135">5</span><span class="sxs-lookup"><span data-stu-id="0a657-135">5</span></span>
</dt> <dd>

<span data-ttu-id="0a657-136">Ошибка атомарности (старая метка времени не совпадает)</span><span class="sxs-lookup"><span data-stu-id="0a657-136">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a657-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0a657-137">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="0a657-138">0</span><span class="sxs-lookup"><span data-stu-id="0a657-138">0</span></span>

<span data-ttu-id="0a657-139">Сбой</span><span class="sxs-lookup"><span data-stu-id="0a657-139">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0a657-140">1</span><span class="sxs-lookup"><span data-stu-id="0a657-140">1</span></span>

<span data-ttu-id="0a657-141">Успешно</span><span class="sxs-lookup"><span data-stu-id="0a657-141">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0a657-142">Требования</span><span class="sxs-lookup"><span data-stu-id="0a657-142">Requirements</span></span>



| <span data-ttu-id="0a657-143">Требование</span><span class="sxs-lookup"><span data-stu-id="0a657-143">Requirement</span></span> | <span data-ttu-id="0a657-144">Значение</span><span class="sxs-lookup"><span data-stu-id="0a657-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a657-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0a657-145">Minimum supported client</span></span><br/> | <span data-ttu-id="0a657-146">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0a657-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="0a657-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0a657-147">Minimum supported server</span></span><br/> | <span data-ttu-id="0a657-148">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0a657-148">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="0a657-149">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0a657-149">Namespace</span></span><br/>                | <span data-ttu-id="0a657-150">Корневой \\ узел Microsoft \\ Windows \\ бутевентколлектор</span><span class="sxs-lookup"><span data-stu-id="0a657-150">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="0a657-151">Header</span><span class="sxs-lookup"><span data-stu-id="0a657-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a657-152"><dt>Срресторептапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a657-152"><dt>Srrestoreptapi.h</dt></span></span> </dl>          |
| <span data-ttu-id="0a657-153">MOF</span><span class="sxs-lookup"><span data-stu-id="0a657-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0a657-154"><dt>Бутевентколлекторвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0a657-154"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="0a657-155">DLL</span><span class="sxs-lookup"><span data-stu-id="0a657-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a657-156"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0a657-156"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="0a657-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0a657-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a657-158">**Элемента**</span><span class="sxs-lookup"><span data-stu-id="0a657-158">**Control**</span></span>](control.md)
</dt> </dl>

 

