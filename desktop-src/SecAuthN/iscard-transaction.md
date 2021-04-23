---
description: Выполняет операцию записи и чтения для объекта команды смарт-карты (блок данных протокола приложения).
ms.assetid: 4dc8ed56-97e0-4c05-a70a-ea2ffd976d47
title: Метод "Скардмгр. h"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.Transaction
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2abe9d4acd4d59019fe0c8ce122baa12fde06f2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650630"
---
# <a name="iscardtransaction-method"></a><span data-ttu-id="ec675-103">Метод "a Card:: Transaction"</span><span class="sxs-lookup"><span data-stu-id="ec675-103">ISCard::Transaction method</span></span>

<span data-ttu-id="ec675-104">\[Метод **Transaction** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="ec675-104">\[The **Transaction** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ec675-105">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="ec675-105">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="ec675-106">Метод **Transaction** выполняет операцию записи и чтения для команды [*смарт-карты*](../secgloss/s-gly.md) ([*блок данных протокола приложения*](../secgloss/a-gly.md)).</span><span class="sxs-lookup"><span data-stu-id="ec675-106">The **Transaction** method executes a write and read operation on the [*smart card*](../secgloss/s-gly.md) command ([*application protocol data unit*](../secgloss/a-gly.md)) object.</span></span> <span data-ttu-id="ec675-107">Строка ответа смарт-карты для строки команды, определенной в карточке, отправленной на смарт-карту, будет доступна после возврата этой функции.</span><span class="sxs-lookup"><span data-stu-id="ec675-107">The reply string from the smart card for the command string defined in the card that was sent to the smart card will be accessible after this function returns.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec675-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ec675-108">Syntax</span></span>


```C++
HRESULT Transaction(
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="ec675-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ec675-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec675-110">*ппкмд* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="ec675-110">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec675-111">Указатель на объект команды смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="ec675-111">A pointer to the smart card command object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec675-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ec675-112">Return value</span></span>

<span data-ttu-id="ec675-113">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="ec675-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="ec675-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ec675-114">Return code</span></span>                                                                                   | <span data-ttu-id="ec675-115">Описание</span><span class="sxs-lookup"><span data-stu-id="ec675-115">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="ec675-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="ec675-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ec675-117">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="ec675-117">The operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="ec675-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ec675-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ec675-119">Недопустимый параметр *ппкмд* .</span><span class="sxs-lookup"><span data-stu-id="ec675-119">The *ppCmd* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="ec675-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="ec675-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ec675-121">В *ппкмд* был передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="ec675-121">A bad pointer was passed in *ppCmd*.</span></span><br/>          |
| <dl> <span data-ttu-id="ec675-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ec675-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ec675-123">Память для удовлетворения запроса недоступна.</span><span class="sxs-lookup"><span data-stu-id="ec675-123">Memory to satisfy the request is unavailable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ec675-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ec675-124">Remarks</span></span>

<span data-ttu-id="ec675-125">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="ec675-125">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="ec675-126">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="ec675-126">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ec675-127">Примеры</span><span class="sxs-lookup"><span data-stu-id="ec675-127">Examples</span></span>

<span data-ttu-id="ec675-128">В следующем примере показано выполнение операции записи и чтения для объекта команды смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="ec675-128">The following example shows executing a write and read operation on the smart card command object.</span></span>


```C++
HRESULT    hr;

// pISCard is a pointer to an instance of ISCard.
// pISCardCmd is a pointer to an instance of ISCardCmd,
// and ISCardCmd::BuildCmd has already been called.
hr = pISCard->Transaction(&pISCardCmd);
if (FAILED(hr))
{
    printf("Failed ISCard::Transaction\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="ec675-129">Требования</span><span class="sxs-lookup"><span data-stu-id="ec675-129">Requirements</span></span>



| <span data-ttu-id="ec675-130">Требование</span><span class="sxs-lookup"><span data-stu-id="ec675-130">Requirement</span></span> | <span data-ttu-id="ec675-131">Значение</span><span class="sxs-lookup"><span data-stu-id="ec675-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec675-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ec675-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ec675-133">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ec675-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ec675-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ec675-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ec675-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ec675-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ec675-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="ec675-136">End of client support</span></span><br/>    | <span data-ttu-id="ec675-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ec675-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="ec675-138">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="ec675-138">End of server support</span></span><br/>    | <span data-ttu-id="ec675-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ec675-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="ec675-140">Header</span><span class="sxs-lookup"><span data-stu-id="ec675-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec675-141"><dt>Скардмгр. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec675-141"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="ec675-142">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="ec675-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="ec675-143"><dt>Скардмгр. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ec675-143"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ec675-144">DLL</span><span class="sxs-lookup"><span data-stu-id="ec675-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec675-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec675-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ec675-146">IID</span><span class="sxs-lookup"><span data-stu-id="ec675-146">IID</span></span><br/>                      | <span data-ttu-id="ec675-147">Идентификатор IID \_ -карты определен как 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="ec675-147">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="ec675-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec675-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec675-149">**аттачбихандле**</span><span class="sxs-lookup"><span data-stu-id="ec675-149">**AttachByHandle**</span></span>](iscard-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="ec675-150">**аттачбиреадер**</span><span class="sxs-lookup"><span data-stu-id="ec675-150">**AttachByReader**</span></span>](iscard-attachbyreader.md)
</dt> <dt>

[<span data-ttu-id="ec675-151">**Соединил**</span><span class="sxs-lookup"><span data-stu-id="ec675-151">**Detach**</span></span>](iscard-detach.md)
</dt> <dt>

[<span data-ttu-id="ec675-152">**получение \_ ATR**</span><span class="sxs-lookup"><span data-stu-id="ec675-152">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="ec675-153">**получить \_ кардхандле**</span><span class="sxs-lookup"><span data-stu-id="ec675-153">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="ec675-154">**получить \_ контекст**</span><span class="sxs-lookup"><span data-stu-id="ec675-154">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="ec675-155">**получить \_ протокол**</span><span class="sxs-lookup"><span data-stu-id="ec675-155">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="ec675-156">**получение \_ состояния**</span><span class="sxs-lookup"><span data-stu-id="ec675-156">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="ec675-157">**Карточка**</span><span class="sxs-lookup"><span data-stu-id="ec675-157">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="ec675-158">**локкскард**</span><span class="sxs-lookup"><span data-stu-id="ec675-158">**LockSCard**</span></span>](iscard-lockscard.md)
</dt> <dt>

[<span data-ttu-id="ec675-159">**Повторно подключиться**</span><span class="sxs-lookup"><span data-stu-id="ec675-159">**ReAttach**</span></span>](iscard-reattach.md)
</dt> <dt>

[<span data-ttu-id="ec675-160">**унлоккскард**</span><span class="sxs-lookup"><span data-stu-id="ec675-160">**UnlockSCard**</span></span>](iscard-unlockscard.md)
</dt> </dl>

 

 
