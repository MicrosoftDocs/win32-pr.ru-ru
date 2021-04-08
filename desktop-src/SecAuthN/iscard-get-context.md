---
description: Извлекает текущий маркер контекста диспетчера ресурсов. Этот метод возвращает ( \* пконтекст) = = null, если контекст не был установлен.
ms.assetid: c031f53d-4670-4d48-934c-a1550f21c23a
title: Метод get_Context. h.
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Context
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8b5aba075d755b644a78cca23a827a70966f4ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912468"
---
# <a name="iscardget_context-method"></a><span data-ttu-id="91d7d-104">Метод "карточки:: получение \_ контекста"</span><span class="sxs-lookup"><span data-stu-id="91d7d-104">ISCard::get\_Context method</span></span>

<span data-ttu-id="91d7d-105">\[Метод **Get \_ context** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="91d7d-105">\[The **get\_Context** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="91d7d-106">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="91d7d-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="91d7d-107">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="91d7d-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="91d7d-108">Метод **получения \_ контекста** получает текущий маркер [*контекста диспетчера ресурсов*](../secgloss/r-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="91d7d-108">The **get\_Context** method retrieves the current [*resource manager context*](../secgloss/r-gly.md) handle.</span></span> <span data-ttu-id="91d7d-109">Этот метод возвращает ( \* *пконтекст*) = = **null** , если контекст не был установлен.</span><span class="sxs-lookup"><span data-stu-id="91d7d-109">This method returns (\**pContext*) == **NULL** if no context has been established.</span></span>

## <a name="syntax"></a><span data-ttu-id="91d7d-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91d7d-110">Syntax</span></span>


```C++
HRESULT get_Context(
  [out] HSCARDCONTEXT *pContext
);
```



## <a name="parameters"></a><span data-ttu-id="91d7d-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="91d7d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91d7d-112">*пконтекст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="91d7d-112">*pContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91d7d-113">Указатель на маркер контекста при возврате.</span><span class="sxs-lookup"><span data-stu-id="91d7d-113">Pointer to the context handle on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91d7d-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="91d7d-114">Return value</span></span>

<span data-ttu-id="91d7d-115">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="91d7d-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="91d7d-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="91d7d-116">Return code</span></span>                                                                                  | <span data-ttu-id="91d7d-117">Описание</span><span class="sxs-lookup"><span data-stu-id="91d7d-117">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="91d7d-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="91d7d-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="91d7d-119">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="91d7d-119">Operation completed successfully.</span></span><br/>       |
| <dl> <span data-ttu-id="91d7d-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="91d7d-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="91d7d-121">Недопустимый параметр *пконтекст* .</span><span class="sxs-lookup"><span data-stu-id="91d7d-121">The *pContext* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="91d7d-122"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="91d7d-122"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="91d7d-123">В *пконтекст* был передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="91d7d-123">A bad pointer was passed in *pContext*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="91d7d-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="91d7d-124">Remarks</span></span>

<span data-ttu-id="91d7d-125">Контекст Resource Manager задается путем вызова функции [*смарт-карты*](../secgloss/s-gly.md) [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext).</span><span class="sxs-lookup"><span data-stu-id="91d7d-125">The resource manager context is set by calling the [*smart card*](../secgloss/s-gly.md) function [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext).</span></span>

<span data-ttu-id="91d7d-126">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="91d7d-126">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="91d7d-127">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="91d7d-127">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="91d7d-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="91d7d-128">Examples</span></span>

<span data-ttu-id="91d7d-129">В следующем примере показано извлечение текущего маркера [*контекста диспетчера ресурсов*](../secgloss/r-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="91d7d-129">The following example shows retrieving the current [*resource manager context*](../secgloss/r-gly.md) handle.</span></span>


```C++
HSCARDCONTEXT  hCtx;
HRESULT        hr;

// Retrieve the smart card context.
hr = pISCard->get_Context(&hCtx);
if (FAILED(hr))
{
   printf("Failed get_Context\n");
   // Take other error handling action as needed.
}
// Use smart card context as needed.
```



## <a name="requirements"></a><span data-ttu-id="91d7d-130">Требования</span><span class="sxs-lookup"><span data-stu-id="91d7d-130">Requirements</span></span>



| <span data-ttu-id="91d7d-131">Требование</span><span class="sxs-lookup"><span data-stu-id="91d7d-131">Requirement</span></span> | <span data-ttu-id="91d7d-132">Значение</span><span class="sxs-lookup"><span data-stu-id="91d7d-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91d7d-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="91d7d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="91d7d-134">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="91d7d-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="91d7d-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="91d7d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="91d7d-136">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="91d7d-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="91d7d-137">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="91d7d-137">End of client support</span></span><br/>    | <span data-ttu-id="91d7d-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="91d7d-138">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="91d7d-139">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="91d7d-139">End of server support</span></span><br/>    | <span data-ttu-id="91d7d-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="91d7d-140">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="91d7d-141">Header</span><span class="sxs-lookup"><span data-stu-id="91d7d-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="91d7d-142"><dt>Скардмгр. h</dt></span><span class="sxs-lookup"><span data-stu-id="91d7d-142"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="91d7d-143">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="91d7d-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="91d7d-144"><dt>Скардмгр. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="91d7d-144"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="91d7d-145">DLL</span><span class="sxs-lookup"><span data-stu-id="91d7d-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91d7d-146"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91d7d-146"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="91d7d-147">IID</span><span class="sxs-lookup"><span data-stu-id="91d7d-147">IID</span></span><br/>                      | <span data-ttu-id="91d7d-148">Идентификатор IID \_ -карты определен как 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="91d7d-148">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="91d7d-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="91d7d-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91d7d-150">**получение \_ ATR**</span><span class="sxs-lookup"><span data-stu-id="91d7d-150">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="91d7d-151">**получить \_ кардхандле**</span><span class="sxs-lookup"><span data-stu-id="91d7d-151">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="91d7d-152">**получить \_ протокол**</span><span class="sxs-lookup"><span data-stu-id="91d7d-152">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="91d7d-153">**получение \_ состояния**</span><span class="sxs-lookup"><span data-stu-id="91d7d-153">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="91d7d-154">**Карточка**</span><span class="sxs-lookup"><span data-stu-id="91d7d-154">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="91d7d-155">**SCardEstablishContext**</span><span class="sxs-lookup"><span data-stu-id="91d7d-155">**SCardEstablishContext**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext)
</dt> </dl>

 

 
