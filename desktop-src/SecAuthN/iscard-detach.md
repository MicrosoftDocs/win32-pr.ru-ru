---
description: Закрывает открытое подключение к смарт-карте.
ms.assetid: 7d768945-8d5d-4d29-b5bc-1b2ac5b0e114
title: A-карта::D метод етач (Скардмгр. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.Detach
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f9fd2b2a6d9ea2df8e886c6ff9851706c2030a1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647614"
---
# <a name="iscarddetach-method"></a><span data-ttu-id="fe4ea-103">Етач: метод:D</span><span class="sxs-lookup"><span data-stu-id="fe4ea-103">ISCard::Detach method</span></span>

<span data-ttu-id="fe4ea-104">\[Метод **Detach** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="fe4ea-104">\[The **Detach** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fe4ea-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="fe4ea-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fe4ea-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="fe4ea-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="fe4ea-107">Метод **Detach** закрывает открытое подключение к [*смарт-карте*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="fe4ea-107">The **Detach** method closes the open connection to the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fe4ea-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe4ea-108">Syntax</span></span>


```C++
HRESULT Detach(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a><span data-ttu-id="fe4ea-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe4ea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe4ea-110">*Расстановка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fe4ea-110">*Disposition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe4ea-111">Указывает, что следует делать с картой в подключенном [*модуле чтения*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="fe4ea-111">Indicates what should be done with the card in the connected [*reader*](../secgloss/r-gly.md).</span></span>



| <span data-ttu-id="fe4ea-112">Значение</span><span class="sxs-lookup"><span data-stu-id="fe4ea-112">Value</span></span>                                                                                                                                      | <span data-ttu-id="fe4ea-113">Значение</span><span class="sxs-lookup"><span data-stu-id="fe4ea-113">Meaning</span></span>                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="LEAVE"></span><span id="leave"></span><dl> <span data-ttu-id="fe4ea-114"><dt>**ВЫХОДА**</dt></span><span class="sxs-lookup"><span data-stu-id="fe4ea-114"><dt>**LEAVE**</dt></span></span> </dl>       | <span data-ttu-id="fe4ea-115">Оставляет смарт-карту в текущем [*состоянии*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="fe4ea-115">Leaves the smart card in the current [*state*](../secgloss/s-gly.md).</span></span><br/> |
| <span id="RESET"></span><span id="reset"></span><dl> <span data-ttu-id="fe4ea-116"><dt>**ПЕРЕЗАПУСК**</dt></span><span class="sxs-lookup"><span data-stu-id="fe4ea-116"><dt>**RESET**</dt></span></span> </dl>       | <span data-ttu-id="fe4ea-117">Сбрасывает смарт-карту в известное состояние.</span><span class="sxs-lookup"><span data-stu-id="fe4ea-117">Resets the smart card to some known state.</span></span><br/>                                                              |
| <span id="UNPOWER"></span><span id="unpower"></span><dl> <span data-ttu-id="fe4ea-118"><dt>**Непитание**</dt></span><span class="sxs-lookup"><span data-stu-id="fe4ea-118"><dt>**UNPOWER**</dt></span></span> </dl> | <span data-ttu-id="fe4ea-119">Удаляет электроэнергию смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="fe4ea-119">Removes power from the smart card.</span></span><br/>                                                                      |
| <span id="EJECT"></span><span id="eject"></span><dl> <span data-ttu-id="fe4ea-120"><dt>**ВЫДВИНУТ**</dt></span><span class="sxs-lookup"><span data-stu-id="fe4ea-120"><dt>**EJECT**</dt></span></span> </dl>       | <span data-ttu-id="fe4ea-121">Извлекает смарт-карту, если у читателя есть возможности извлечения.</span><span class="sxs-lookup"><span data-stu-id="fe4ea-121">Ejects the smart card if the reader has eject capabilities.</span></span><br/>                                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe4ea-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe4ea-122">Return value</span></span>

<span data-ttu-id="fe4ea-123">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="fe4ea-123">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="fe4ea-124">Код возврата</span><span class="sxs-lookup"><span data-stu-id="fe4ea-124">Return code</span></span>                                                                                  | <span data-ttu-id="fe4ea-125">Описание</span><span class="sxs-lookup"><span data-stu-id="fe4ea-125">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="fe4ea-126"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="fe4ea-126"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="fe4ea-127">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="fe4ea-127">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="fe4ea-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="fe4ea-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="fe4ea-129">Недопустимое *Расположение* .</span><span class="sxs-lookup"><span data-stu-id="fe4ea-129">*Disposition* is not valid.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="fe4ea-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fe4ea-130">Remarks</span></span>

<span data-ttu-id="fe4ea-131">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="fe4ea-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="fe4ea-132">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="fe4ea-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="fe4ea-133">Примеры</span><span class="sxs-lookup"><span data-stu-id="fe4ea-133">Examples</span></span>

<span data-ttu-id="fe4ea-134">В следующем примере показано закрытие подключения к смарт-карте.</span><span class="sxs-lookup"><span data-stu-id="fe4ea-134">The following example shows closing the connection to the smart card.</span></span>


```C++
HRESULT    hr;

// Detach the smart card.
hr = pISCard->Detach(LEAVE);
if (FAILED(hr))
{
   printf("Failed Detach\n");
   // Take error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="fe4ea-135">Требования</span><span class="sxs-lookup"><span data-stu-id="fe4ea-135">Requirements</span></span>



| <span data-ttu-id="fe4ea-136">Требование</span><span class="sxs-lookup"><span data-stu-id="fe4ea-136">Requirement</span></span> | <span data-ttu-id="fe4ea-137">Значение</span><span class="sxs-lookup"><span data-stu-id="fe4ea-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe4ea-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fe4ea-138">Minimum supported client</span></span><br/> | <span data-ttu-id="fe4ea-139">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fe4ea-139">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fe4ea-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fe4ea-140">Minimum supported server</span></span><br/> | <span data-ttu-id="fe4ea-141">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fe4ea-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fe4ea-142">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="fe4ea-142">End of client support</span></span><br/>    | <span data-ttu-id="fe4ea-143">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fe4ea-143">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="fe4ea-144">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="fe4ea-144">End of server support</span></span><br/>    | <span data-ttu-id="fe4ea-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fe4ea-145">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="fe4ea-146">Header</span><span class="sxs-lookup"><span data-stu-id="fe4ea-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe4ea-147"><dt>Скардмгр. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe4ea-147"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="fe4ea-148">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="fe4ea-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="fe4ea-149"><dt>Скардмгр. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fe4ea-149"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fe4ea-150">DLL</span><span class="sxs-lookup"><span data-stu-id="fe4ea-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe4ea-151"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe4ea-151"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fe4ea-152">IID</span><span class="sxs-lookup"><span data-stu-id="fe4ea-152">IID</span></span><br/>                      | <span data-ttu-id="fe4ea-153">Идентификатор IID \_ -карты определен как 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="fe4ea-153">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="fe4ea-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe4ea-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe4ea-155">**аттачбихандле**</span><span class="sxs-lookup"><span data-stu-id="fe4ea-155">**AttachByHandle**</span></span>](iscard-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="fe4ea-156">**аттачбиреадер**</span><span class="sxs-lookup"><span data-stu-id="fe4ea-156">**AttachByReader**</span></span>](iscard-attachbyreader.md)
</dt> <dt>

[<span data-ttu-id="fe4ea-157">**Карточка**</span><span class="sxs-lookup"><span data-stu-id="fe4ea-157">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="fe4ea-158">**Повторно подключиться**</span><span class="sxs-lookup"><span data-stu-id="fe4ea-158">**ReAttach**</span></span>](iscard-reattach.md)
</dt> </dl>

 

 
