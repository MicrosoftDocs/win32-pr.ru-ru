---
description: Метод GetResponse конструирует команду блока данных протокола приложения (КАТЕГОРИЯХ APDU), которая передает команды КАТЕГОРИЯХ APDU (или часть команды КАТЕГОРИЯХ APDU), которые в противном случае не могут быть переданы доступными протоколами.
ms.assetid: 1aa83d38-d46d-4d3b-8f57-0256e5875e35
title: 'Метод ISCardISO7816:: GetResponse (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.GetResponse
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0b74fe9620aefc390957b88f9cf286f7871c1d18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650992"
---
# <a name="iscardiso7816getresponse-method"></a><span data-ttu-id="f98f2-103">Метод ISCardISO7816:: GetResponse</span><span class="sxs-lookup"><span data-stu-id="f98f2-103">ISCardISO7816::GetResponse method</span></span>

<span data-ttu-id="f98f2-104">\[Метод **GetResponse** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="f98f2-104">\[The **GetResponse** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f98f2-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="f98f2-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f98f2-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="f98f2-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="f98f2-107">Метод **GetResponse** конструирует команду [*блока данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU), которая передает команды категориях APDU (или часть команды категориях APDU), которые в противном случае не могут быть переданы доступными протоколами.</span><span class="sxs-lookup"><span data-stu-id="f98f2-107">The **GetResponse** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that transmits APDU commands (or part of an APDU command) which otherwise could not be transmitted by the available protocols.</span></span>

## <a name="syntax"></a><span data-ttu-id="f98f2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f98f2-108">Syntax</span></span>


```C++
HRESULT GetResponse(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lDataLength,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="f98f2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f98f2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f98f2-110">*byP1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f98f2-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f98f2-111">Для ISO 7816-4 P1 должен быть равен нулю (РФУ).</span><span class="sxs-lookup"><span data-stu-id="f98f2-111">Per the ISO 7816-4, P1 should be zero (RFU).</span></span>

</dd> <dt>

<span data-ttu-id="f98f2-112">*byP2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f98f2-112">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f98f2-113">Для ISO 7816-4 P2 должно быть равно нулю (РФУ).</span><span class="sxs-lookup"><span data-stu-id="f98f2-113">Per the ISO 7816-4, P2 should be zero (RFU).</span></span>

</dd> <dt>

<span data-ttu-id="f98f2-114">*лдаталенгс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f98f2-114">*lDataLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f98f2-115">Длина передаваемых данных.</span><span class="sxs-lookup"><span data-stu-id="f98f2-115">Length of data transmitted.</span></span>

</dd> <dt>

<span data-ttu-id="f98f2-116">*ппкмд* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="f98f2-116">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f98f2-117">На входе — указатель на объект интерфейса [**искардкмд**](iscardcmd.md) или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="f98f2-117">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="f98f2-118">При возвращении он заполняется командой КАТЕГОРИЯХ APDU, созданной этой операцией.</span><span class="sxs-lookup"><span data-stu-id="f98f2-118">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="f98f2-119">Если для *ппкмд* было задано **значение NULL**, то объект [*смарт-карты*](../secgloss/s-gly.md) [**искардкмд**](iscardcmd.md) создается внутренним образом и возвращается через указатель *ппкмд* .</span><span class="sxs-lookup"><span data-stu-id="f98f2-119">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f98f2-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f98f2-120">Return value</span></span>

<span data-ttu-id="f98f2-121">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="f98f2-121">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="f98f2-122">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f98f2-122">Return code</span></span>                                                                                   | <span data-ttu-id="f98f2-123">Описание</span><span class="sxs-lookup"><span data-stu-id="f98f2-123">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="f98f2-124"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="f98f2-124"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f98f2-125">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="f98f2-125">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="f98f2-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f98f2-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f98f2-127">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="f98f2-127">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="f98f2-128"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="f98f2-128"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f98f2-129">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="f98f2-129">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="f98f2-130"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f98f2-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f98f2-131">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="f98f2-131">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="f98f2-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f98f2-132">Remarks</span></span>

<span data-ttu-id="f98f2-133">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="f98f2-133">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="f98f2-134">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="f98f2-134">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="f98f2-135">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="f98f2-135">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f98f2-136">Требования</span><span class="sxs-lookup"><span data-stu-id="f98f2-136">Requirements</span></span>



| <span data-ttu-id="f98f2-137">Требование</span><span class="sxs-lookup"><span data-stu-id="f98f2-137">Requirement</span></span> | <span data-ttu-id="f98f2-138">Значение</span><span class="sxs-lookup"><span data-stu-id="f98f2-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f98f2-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f98f2-139">Minimum supported client</span></span><br/> | <span data-ttu-id="f98f2-140">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f98f2-140">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f98f2-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f98f2-141">Minimum supported server</span></span><br/> | <span data-ttu-id="f98f2-142">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f98f2-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f98f2-143">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="f98f2-143">End of client support</span></span><br/>    | <span data-ttu-id="f98f2-144">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f98f2-144">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="f98f2-145">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="f98f2-145">End of server support</span></span><br/>    | <span data-ttu-id="f98f2-146">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f98f2-146">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="f98f2-147">Header</span><span class="sxs-lookup"><span data-stu-id="f98f2-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="f98f2-148"><dt>Скардссп. h</dt></span><span class="sxs-lookup"><span data-stu-id="f98f2-148"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f98f2-149">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="f98f2-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="f98f2-150"><dt>Скардсрв. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f98f2-150"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f98f2-151">DLL</span><span class="sxs-lookup"><span data-stu-id="f98f2-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f98f2-152"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f98f2-152"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f98f2-153">IID</span><span class="sxs-lookup"><span data-stu-id="f98f2-153">IID</span></span><br/>                      | <span data-ttu-id="f98f2-154">IID \_ ISCardISO7816 определен как 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="f98f2-154">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="f98f2-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f98f2-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f98f2-156">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="f98f2-156">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
