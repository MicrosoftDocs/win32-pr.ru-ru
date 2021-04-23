---
description: Задайте новую активную конфигурацию сборщика.
ms.assetid: 1979e657-a8f3-4eab-991c-a884bde10724
ms.tgt_platform: multiple
title: Метод Сетконфигуратион класса Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.SetConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 4f482de9c4cd8f410371da51e605762a1f92e104
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103806988"
---
# <a name="setconfiguration-method-of-the-control-class"></a><span data-ttu-id="88076-103">Метод Сетконфигуратион класса Control</span><span class="sxs-lookup"><span data-stu-id="88076-103">SetConfiguration method of the Control class</span></span>

<span data-ttu-id="88076-104">Задайте новую активную конфигурацию сборщика.</span><span class="sxs-lookup"><span data-stu-id="88076-104">Set the new active configuration of the collector.</span></span>

## <a name="syntax"></a><span data-ttu-id="88076-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88076-105">Syntax</span></span>


```mof
Uint32 SetConfiguration(
  [in]  string Config,
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] Uint32 NewTimestampLow,
  [out] Uint32 NewTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a><span data-ttu-id="88076-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="88076-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88076-107">*Конфигурация* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="88076-107">*Config* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88076-108">Конфигурация для активации.</span><span class="sxs-lookup"><span data-stu-id="88076-108">The configuration to activate.</span></span>

</dd> <dt>

<span data-ttu-id="88076-109">*Олдтиместамплов* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="88076-109">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88076-110">Младшие биты метки времени, указывающие, когда была задана текущая активная конфигурация.</span><span class="sxs-lookup"><span data-stu-id="88076-110">The low-order bits of a timestamp that indicates when the current active configuration was set.</span></span> <span data-ttu-id="88076-111">Проверка атомарности включена, если для этого свойства не задано значение 0.</span><span class="sxs-lookup"><span data-stu-id="88076-111">Atomicity checking is enabled if this property is not set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="88076-112">*Олдтиместамфигх* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="88076-112">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88076-113">Старшие биты метки времени, указывающие, когда была задана текущая активная конфигурация.</span><span class="sxs-lookup"><span data-stu-id="88076-113">The high-order bits of a timestamp that indicates when the current active configuration was set.</span></span> <span data-ttu-id="88076-114">Проверка атомарности включена, если для этого свойства не задано значение 0.</span><span class="sxs-lookup"><span data-stu-id="88076-114">Atomicity checking is enabled if this property is not set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="88076-115">*Невтиместамплов* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="88076-115">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88076-116">При возврате из этого метода этот параметр содержит младшие биты метки времени, указывающие, когда была задана новая конфигурация.</span><span class="sxs-lookup"><span data-stu-id="88076-116">When this method returns, this parameter contains the low-order bits of a timestamp that indicates when the new configuration was set.</span></span> <span data-ttu-id="88076-117">Проверка атомарности включена, если для этого свойства не задано значение 0.</span><span class="sxs-lookup"><span data-stu-id="88076-117">Atomicity checking is enabled if this property is not set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="88076-118">*Невтиместамфигх* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="88076-118">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88076-119">При возврате из этого метода этот параметр содержит старшие биты метки времени, указывающие, когда была задана новая конфигурация.</span><span class="sxs-lookup"><span data-stu-id="88076-119">When this method returns, this parameter contains the high-order bits of the timestamp that indicates when the new configuration was set.</span></span> <span data-ttu-id="88076-120">Проверка атомарности включена, если для этого свойства не задано значение 0.</span><span class="sxs-lookup"><span data-stu-id="88076-120">Atomicity checking is enabled if this property is not set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="88076-121">*ErrorString* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="88076-121">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88076-122">Когда этот метод возвращает значение, если произошла ошибка, этот параметр содержит описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="88076-122">When this method returns, if there was an error, this parameter contains the error description.</span></span>

</dd> <dt>

<span data-ttu-id="88076-123">*Варнингстринг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="88076-123">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88076-124">При возврате из этого метода этот параметр содержит все сообщения о предупреждениях для операции.</span><span class="sxs-lookup"><span data-stu-id="88076-124">When this method returns, this parameter contains any warnings messages for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="88076-125">*Инфостринг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="88076-125">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88076-126">При возврате из этого метода этот параметр содержит сведения о новой активной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="88076-126">When this method returns, this parameter contains information for the new active configuration.</span></span>

</dd> <dt>

<span data-ttu-id="88076-127">*ErrorType* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="88076-127">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88076-128">Когда этот метод возвращает значение, если произошла ошибка, этот параметр указывает тип ошибки.</span><span class="sxs-lookup"><span data-stu-id="88076-128">When this method returns, if there was an error, this parameter indicates the error type.</span></span>

<dt>

<span data-ttu-id="88076-129">0</span><span class="sxs-lookup"><span data-stu-id="88076-129">0</span></span>
</dt> <dd>

<span data-ttu-id="88076-130">Отсутствует новая конфигурация.</span><span class="sxs-lookup"><span data-stu-id="88076-130">The new configuration is missing.</span></span>

</dd> <dt>

<span data-ttu-id="88076-131">1</span><span class="sxs-lookup"><span data-stu-id="88076-131">1</span></span>
</dt> <dd>

<span data-ttu-id="88076-132">Недопустимый формат новой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="88076-132">The format of the new configuration is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="88076-133">2</span><span class="sxs-lookup"><span data-stu-id="88076-133">2</span></span>
</dt> <dd>

<span data-ttu-id="88076-134">Недопустимая новая конфигурация.</span><span class="sxs-lookup"><span data-stu-id="88076-134">The new configuration is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="88076-135">3</span><span class="sxs-lookup"><span data-stu-id="88076-135">3</span></span>
</dt> <dd>

<span data-ttu-id="88076-136">Произошла ошибка, вызванная открытием сокета.</span><span class="sxs-lookup"><span data-stu-id="88076-136">There was an error caused by an open socket.</span></span>

</dd> <dt>

<span data-ttu-id="88076-137">4</span><span class="sxs-lookup"><span data-stu-id="88076-137">4</span></span>
</dt> <dd>

<span data-ttu-id="88076-138">Произошла ошибка записи в файл.</span><span class="sxs-lookup"><span data-stu-id="88076-138">There was a file write error.</span></span>

</dd> <dt>

<span data-ttu-id="88076-139">5</span><span class="sxs-lookup"><span data-stu-id="88076-139">5</span></span>
</dt> <dd>

<span data-ttu-id="88076-140">Произошла ошибка атомарности.</span><span class="sxs-lookup"><span data-stu-id="88076-140">There was an atomicity error.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88076-141">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="88076-141">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="88076-142">0</span><span class="sxs-lookup"><span data-stu-id="88076-142">0</span></span>

<span data-ttu-id="88076-143">Сбой</span><span class="sxs-lookup"><span data-stu-id="88076-143">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="88076-144">1</span><span class="sxs-lookup"><span data-stu-id="88076-144">1</span></span>

<span data-ttu-id="88076-145">Успешно</span><span class="sxs-lookup"><span data-stu-id="88076-145">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88076-146">Требования</span><span class="sxs-lookup"><span data-stu-id="88076-146">Requirements</span></span>



| <span data-ttu-id="88076-147">Требование</span><span class="sxs-lookup"><span data-stu-id="88076-147">Requirement</span></span> | <span data-ttu-id="88076-148">Значение</span><span class="sxs-lookup"><span data-stu-id="88076-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88076-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="88076-149">Minimum supported client</span></span><br/> | <span data-ttu-id="88076-150">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="88076-150">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="88076-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="88076-151">Minimum supported server</span></span><br/> | <span data-ttu-id="88076-152">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="88076-152">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="88076-153">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="88076-153">Namespace</span></span><br/>                | <span data-ttu-id="88076-154">Корневой \\ узел Microsoft \\ Windows \\ бутевентколлектор</span><span class="sxs-lookup"><span data-stu-id="88076-154">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="88076-155">MOF</span><span class="sxs-lookup"><span data-stu-id="88076-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88076-156"><dt>Бутевентколлекторвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="88076-156"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="88076-157">DLL</span><span class="sxs-lookup"><span data-stu-id="88076-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88076-158"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="88076-158"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="88076-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="88076-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88076-160">**Элемента**</span><span class="sxs-lookup"><span data-stu-id="88076-160">**Control**</span></span>](control.md)
</dt> </dl>

 

 




