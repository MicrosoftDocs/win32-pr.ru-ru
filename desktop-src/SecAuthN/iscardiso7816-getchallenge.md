---
description: Метод КАТЕГОРИЯХ APDU конструирует команду блока данных протокола приложения (например, случайное число) для использования в процедуре, связанной с безопасностью.
ms.assetid: 61f6db1c-b83a-4c1f-8ace-0222a12560ff
title: Метод ISCardISO7816::-Challenge (Скардссп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.GetChallenge
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 05fe18ad73de6c7c3ea30f986c7bb3420bc465b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081226"
---
# <a name="iscardiso7816getchallenge-method"></a><span data-ttu-id="fc4fc-103">Метод ISCardISO7816:: Challenge</span><span class="sxs-lookup"><span data-stu-id="fc4fc-103">ISCardISO7816::GetChallenge method</span></span>

<span data-ttu-id="fc4fc-104">\[Метод **метода** WebMethod доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="fc4fc-104">\[The **GetChallenge** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fc4fc-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="fc4fc-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fc4fc-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="fc4fc-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="fc4fc-107">Метод **категориях APDU** конструирует команду [*блока данных протокола приложения*](../secgloss/a-gly.md) (например, случайное число) для использования в процедуре, связанной с безопасностью.</span><span class="sxs-lookup"><span data-stu-id="fc4fc-107">The **GetChallenge** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that issue a challenge (for example, a random number) for use in a security-related procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc4fc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc4fc-108">Syntax</span></span>


```C++
HRESULT GetChallenge(
  [in]      LONG       lBytesExpected,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="fc4fc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc4fc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc4fc-110">*лбитесекспектед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fc4fc-110">*lBytesExpected* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc4fc-111">Максимальная длина ожидаемого ответа.</span><span class="sxs-lookup"><span data-stu-id="fc4fc-111">Maximum length of the expected response.</span></span>

</dd> <dt>

<span data-ttu-id="fc4fc-112">*ппкмд* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="fc4fc-112">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc4fc-113">На входе — указатель на объект интерфейса [**искардкмд**](iscardcmd.md) или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="fc4fc-113">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="fc4fc-114">При возвращении он заполняется командой КАТЕГОРИЯХ APDU, созданной этой операцией.</span><span class="sxs-lookup"><span data-stu-id="fc4fc-114">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="fc4fc-115">Если для *ппкмд* было задано **значение NULL**, то объект [*смарт-карты*](../secgloss/s-gly.md) [**искардкмд**](iscardcmd.md) создается внутренним образом и возвращается через указатель *ппкмд* .</span><span class="sxs-lookup"><span data-stu-id="fc4fc-115">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc4fc-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fc4fc-116">Return value</span></span>

<span data-ttu-id="fc4fc-117">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="fc4fc-117">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="fc4fc-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="fc4fc-118">Return code</span></span>                                                                                   | <span data-ttu-id="fc4fc-119">Описание</span><span class="sxs-lookup"><span data-stu-id="fc4fc-119">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="fc4fc-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="fc4fc-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="fc4fc-121">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="fc4fc-121">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="fc4fc-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="fc4fc-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="fc4fc-123">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="fc4fc-123">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="fc4fc-124"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="fc4fc-124"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="fc4fc-125">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="fc4fc-125">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="fc4fc-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fc4fc-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="fc4fc-127">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="fc4fc-127">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="fc4fc-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fc4fc-128">Remarks</span></span>

<span data-ttu-id="fc4fc-129">Запрос допустим по крайней мере для следующей команды.</span><span class="sxs-lookup"><span data-stu-id="fc4fc-129">The challenge is valid at least for the next command.</span></span>

<span data-ttu-id="fc4fc-130">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="fc4fc-130">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="fc4fc-131">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="fc4fc-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="fc4fc-132">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="fc4fc-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc4fc-133">Требования</span><span class="sxs-lookup"><span data-stu-id="fc4fc-133">Requirements</span></span>



| <span data-ttu-id="fc4fc-134">Требование</span><span class="sxs-lookup"><span data-stu-id="fc4fc-134">Requirement</span></span> | <span data-ttu-id="fc4fc-135">Значение</span><span class="sxs-lookup"><span data-stu-id="fc4fc-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc4fc-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fc4fc-136">Minimum supported client</span></span><br/> | <span data-ttu-id="fc4fc-137">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fc4fc-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fc4fc-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fc4fc-138">Minimum supported server</span></span><br/> | <span data-ttu-id="fc4fc-139">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fc4fc-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fc4fc-140">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="fc4fc-140">End of client support</span></span><br/>    | <span data-ttu-id="fc4fc-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fc4fc-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="fc4fc-142">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="fc4fc-142">End of server support</span></span><br/>    | <span data-ttu-id="fc4fc-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fc4fc-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="fc4fc-144">Header</span><span class="sxs-lookup"><span data-stu-id="fc4fc-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc4fc-145"><dt>Скардссп. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc4fc-145"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fc4fc-146">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="fc4fc-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="fc4fc-147"><dt>Скардсрв. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fc4fc-147"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fc4fc-148">DLL</span><span class="sxs-lookup"><span data-stu-id="fc4fc-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc4fc-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc4fc-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fc4fc-150">IID</span><span class="sxs-lookup"><span data-stu-id="fc4fc-150">IID</span></span><br/>                      | <span data-ttu-id="fc4fc-151">IID \_ ISCardISO7816 определен как 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="fc4fc-151">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="fc4fc-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc4fc-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc4fc-153">**екстерналаусентикате**</span><span class="sxs-lookup"><span data-stu-id="fc4fc-153">**ExternalAuthenticate**</span></span>](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="fc4fc-154">**интерналаусентикате**</span><span class="sxs-lookup"><span data-stu-id="fc4fc-154">**InternalAuthenticate**</span></span>](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="fc4fc-155">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="fc4fc-155">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
