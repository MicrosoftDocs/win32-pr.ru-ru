---
title: Функция Мперрормессажеформат (Мпклиент. h)
description: Возвращает отформатированное сообщение об ошибке на основе кода ошибки.
ms.assetid: C125FCE4-3BB0-4608-BBF3-E7FEF17D0807
keywords:
- Функции Мперрормессажеформат устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MpErrorMessageFormat
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a3499b3be885b29135d22b470da4143cfb23ea6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989232"
---
# <a name="mperrormessageformat-function"></a><span data-ttu-id="bceab-104">Функция Мперрормессажеформат</span><span class="sxs-lookup"><span data-stu-id="bceab-104">MpErrorMessageFormat function</span></span>

<span data-ttu-id="bceab-105">Возвращает отформатированное сообщение об ошибке на основе кода ошибки.</span><span class="sxs-lookup"><span data-stu-id="bceab-105">Returns a formatted error message based on an error code.</span></span>

## <a name="syntax"></a><span data-ttu-id="bceab-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bceab-106">Syntax</span></span>


```C++
HRESULT WINAPI MpErrorMessageFormat(
  _In_  MPHANDLE hMpHandle,
  _In_  HRESULT  hrError,
  _Out_ LPWSTR   *pwszErrorDesc
);
```



## <a name="parameters"></a><span data-ttu-id="bceab-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="bceab-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bceab-108">*хмфандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bceab-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bceab-109">Тип: **мфандле**</span><span class="sxs-lookup"><span data-stu-id="bceab-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="bceab-110">Обработчик для интерфейса диспетчера защиты от вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="bceab-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="bceab-111">Этот маркер возвращается функцией [**мпманажеропен**](mpmanageropen.md) .</span><span class="sxs-lookup"><span data-stu-id="bceab-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="bceab-112">*хреррор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bceab-112">*hrError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bceab-113">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bceab-113">Type: **HRESULT**</span></span>

<span data-ttu-id="bceab-114">Код ошибки на основе **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="bceab-114">An **HRESULT**-based error code.</span></span>

</dd> <dt>

<span data-ttu-id="bceab-115">*пвсзеррордеск* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bceab-115">*pwszErrorDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bceab-116">Введите: \**LPWSTR \** _</span><span class="sxs-lookup"><span data-stu-id="bceab-116">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="bceab-117">Возвращает отформатированное сообщение об ошибке на основе _hrError \*.</span><span class="sxs-lookup"><span data-stu-id="bceab-117">Returns a formatted error message based on _hrError\*.</span></span> <span data-ttu-id="bceab-118">Эту строку необходимо освободить с помощью [**мпфримемори**](mpfreememory.md).</span><span class="sxs-lookup"><span data-stu-id="bceab-118">This string must be freed using [**MpFreeMemory**](mpfreememory.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bceab-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bceab-119">Return value</span></span>

<span data-ttu-id="bceab-120">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bceab-120">Type: **HRESULT**</span></span>

<span data-ttu-id="bceab-121">Если функция выполнена успешно, возвращается значение **S \_**.</span><span class="sxs-lookup"><span data-stu-id="bceab-121">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="bceab-122">Если функция завершается ошибкой, возвращаемое значение является неудачным кодом **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bceab-122">If the function fails then the return value is a failed **HRESULT** code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bceab-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bceab-123">Remarks</span></span>

<span data-ttu-id="bceab-124">Эта функция поддерживает форматирование системных кодов ошибок в дополнение к конкретным кодам ошибок, возвращаемым функциями защиты от вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="bceab-124">This function is capable of formatting system error codes in addition to specific error codes returned by malware protection functions.</span></span> <span data-ttu-id="bceab-125">Коды ошибок **HRESULT** , характерные для функций защиты от вредоносных программ, имеют значение 0x50.</span><span class="sxs-lookup"><span data-stu-id="bceab-125">The **HRESULT** error codes specific to malware protection functions have a facility of 0x50.</span></span> <span data-ttu-id="bceab-126">Ниже приведен список подмножества кодов ошибок, связанных с защитой от вредоносных программ, которые могут возвращаться различными функциями защиты от вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="bceab-126">Below is a list of a subset of the malware protection-specific error codes that can be returned by various malware protection functions.</span></span> <span data-ttu-id="bceab-127">При использовании макроса **HRESULT \_ из \_ \_ состояния MP** приведенные ниже коды ошибок можно преобразовать в **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="bceab-127">Using the macro **HRESULT\_FROM\_MP\_STATUS**, the following error codes can be converted to **HRESULT**.</span></span> <span data-ttu-id="bceab-128">Список других возможных кодов ошибок см. в статье [коды ошибок модуля защиты клиента Forefront Client Security](https://support.microsoft.com/kb/939359) .</span><span class="sxs-lookup"><span data-stu-id="bceab-128">See also [Forefront Client Security anti-malware engine error codes](https://support.microsoft.com/kb/939359) for a list of other possible error codes.</span></span>



| <span data-ttu-id="bceab-129">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="bceab-129">Error Code</span></span>                              | <span data-ttu-id="bceab-130">Описание</span><span class="sxs-lookup"><span data-stu-id="bceab-130">Description</span></span>                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bceab-131">Ошибка \_ \_ подсистемы MP</span><span class="sxs-lookup"><span data-stu-id="bceab-131">ERROR\_MP\_NOENGINE</span></span>                     | <span data-ttu-id="bceab-132">В службе защиты от вредоносных программ не загружено ни одного модуля для выполнения запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="bceab-132">No engine is loaded in antimalware service to perform the requested operation.</span></span>                                              |
| <span data-ttu-id="bceab-133">Ошибка \_ MP \_ без \_ памяти</span><span class="sxs-lookup"><span data-stu-id="bceab-133">ERROR\_MP\_NO\_MEMORY</span></span>                   | <span data-ttu-id="bceab-134">Модуль защиты от вредоносных программ обнаружил нехватки памяти.</span><span class="sxs-lookup"><span data-stu-id="bceab-134">The antimalware engine has encountered a no memory situation.</span></span>                                                               |
| <span data-ttu-id="bceab-135">\_сбой удаления пакета управления с ошибками \_ \_</span><span class="sxs-lookup"><span data-stu-id="bceab-135">ERROR\_MP\_REMOVE\_FAILED</span></span>               | <span data-ttu-id="bceab-136">Не удалось выполнить операцию удаления для определенной угрозы.</span><span class="sxs-lookup"><span data-stu-id="bceab-136">Remove operation failed for a specific threat.</span></span>                                                                              |
| <span data-ttu-id="bceab-137">\_ \_ сбой карантина пакета управления с ошибками \_</span><span class="sxs-lookup"><span data-stu-id="bceab-137">ERROR\_MP\_QUARANTINE\_FAILED</span></span>           | <span data-ttu-id="bceab-138">Сбой операции карантина для определенной угрозы.</span><span class="sxs-lookup"><span data-stu-id="bceab-138">Quarantine operation failed for a specific threat.</span></span>                                                                          |
| <span data-ttu-id="bceab-139">\_ \_ \_ не \_ найдена угроза пакета управления с ошибками</span><span class="sxs-lookup"><span data-stu-id="bceab-139">ERROR\_MP\_THREAT\_NOT\_FOUND</span></span>           | <span data-ttu-id="bceab-140">Конкретная угроза больше не существует в системе.</span><span class="sxs-lookup"><span data-stu-id="bceab-140">The specific threat no longer exists in the system.</span></span>                                                                         |
| <span data-ttu-id="bceab-141">\_Удаление пакета управления с ошибками \_ \_ не \_ поддерживается</span><span class="sxs-lookup"><span data-stu-id="bceab-141">ERROR\_MP\_REMOVE\_NOT\_SUPPORTED</span></span>       | <span data-ttu-id="bceab-142">Операция удаления для определенной угрозы в типе контейнера не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="bceab-142">Remove operation for a specific threat inside the container type is not supported.</span></span>                                          |
| <span data-ttu-id="bceab-143">пакет управления с ОШИБКАми \_ \_ Удаление \_ неизменяемого \_ контейнера</span><span class="sxs-lookup"><span data-stu-id="bceab-143">ERROR\_MP\_REMOVE\_IMMUTABLE\_CONTAINER</span></span> | <span data-ttu-id="bceab-144">Из-за политики ядра операция удаления определенной угрозы в заблокированном контейнере не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="bceab-144">Due to engine policy, a remove operation of a specific threat inside a blocked container is not supported.</span></span> <span data-ttu-id="bceab-145">(Архивы почты.)</span><span class="sxs-lookup"><span data-stu-id="bceab-145">(Mail archives.)</span></span> |
| <span data-ttu-id="bceab-146">Ошибка \_ MP \_ баддб \_ олденгине</span><span class="sxs-lookup"><span data-stu-id="bceab-146">ERROR\_MP\_BADDB\_OLDENGINE</span></span>             | <span data-ttu-id="bceab-147">В запросе на обновление сигнатуры были указаны старые файлы подсистемы или подписи.</span><span class="sxs-lookup"><span data-stu-id="bceab-147">Signature update request provided an older engine or signature files(s).</span></span>                                                    |



 

## <a name="requirements"></a><span data-ttu-id="bceab-148">Требования</span><span class="sxs-lookup"><span data-stu-id="bceab-148">Requirements</span></span>



| <span data-ttu-id="bceab-149">Требование</span><span class="sxs-lookup"><span data-stu-id="bceab-149">Requirement</span></span> | <span data-ttu-id="bceab-150">Значение</span><span class="sxs-lookup"><span data-stu-id="bceab-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bceab-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bceab-151">Minimum supported client</span></span><br/> | <span data-ttu-id="bceab-152">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="bceab-152">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="bceab-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bceab-153">Minimum supported server</span></span><br/> | <span data-ttu-id="bceab-154">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="bceab-154">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bceab-155">Header</span><span class="sxs-lookup"><span data-stu-id="bceab-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="bceab-156"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="bceab-156"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="bceab-157">DLL</span><span class="sxs-lookup"><span data-stu-id="bceab-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bceab-158"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bceab-158"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bceab-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bceab-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bceab-160">**мпфримемори**</span><span class="sxs-lookup"><span data-stu-id="bceab-160">**MpFreeMemory**</span></span>](mpfreememory.md)
</dt> <dt>

[<span data-ttu-id="bceab-161">**мпманажеропен**</span><span class="sxs-lookup"><span data-stu-id="bceab-161">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="bceab-162">Коды ошибок модуля защиты от вредоносных программ Forefront Client Security</span><span class="sxs-lookup"><span data-stu-id="bceab-162">Forefront Client Security anti-malware engine error codes</span></span>](https://support.microsoft.com/kb/939359)
</dt> </dl>

 

 





