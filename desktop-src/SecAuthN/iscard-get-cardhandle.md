---
description: Извлекает маркер подключенной смарт-карты. Этот метод возвращает ( \* фандле) = = null, если соединение отсутствует.
ms.assetid: f03f8f25-b2e4-4fae-b7d2-bb0f1a7cd987
title: Метод get_CardHandle. h.
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_CardHandle
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d7e945f0f4a300dfed444c7e8f5921b806d96b1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990890"
---
# <a name="iscardget_cardhandle-method"></a><span data-ttu-id="02501-104">Метод кардхандле:: Get \_</span><span class="sxs-lookup"><span data-stu-id="02501-104">ISCard::get\_CardHandle method</span></span>

<span data-ttu-id="02501-105">\[Метод **Get \_ кардхандле** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="02501-105">\[The **get\_CardHandle** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="02501-106">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="02501-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="02501-107">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="02501-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="02501-108">Метод **Get \_ кардхандле** Извлекает маркер подключенной [*смарт-карты*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="02501-108">The **get\_CardHandle** method retrieves the handle for a connected [*smart card*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="02501-109">Этот метод возвращает ( \* фандле) = = **null** , если соединение отсутствует.</span><span class="sxs-lookup"><span data-stu-id="02501-109">This method returns (\*pHandle) == **NULL** if not connected.</span></span>

## <a name="syntax"></a><span data-ttu-id="02501-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02501-110">Syntax</span></span>


```C++
HRESULT get_CardHandle(
  [out] HSCARD *pHandle
);
```



## <a name="parameters"></a><span data-ttu-id="02501-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="02501-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02501-112">*фандле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="02501-112">*pHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02501-113">Указатель на маркер карты при возврате.</span><span class="sxs-lookup"><span data-stu-id="02501-113">Pointer to the card handle on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02501-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="02501-114">Return value</span></span>

<span data-ttu-id="02501-115">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="02501-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="02501-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="02501-116">Return code</span></span>                                                                                  | <span data-ttu-id="02501-117">Описание</span><span class="sxs-lookup"><span data-stu-id="02501-117">Description</span></span>                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="02501-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="02501-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="02501-119">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="02501-119">Operation completed successfully.</span></span><br/>      |
| <dl> <span data-ttu-id="02501-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="02501-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="02501-121">Недопустимый параметр *фандле* .</span><span class="sxs-lookup"><span data-stu-id="02501-121">The *pHandle* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="02501-122"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="02501-122"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="02501-123">В *фандле* был передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="02501-123">A bad pointer was passed in *pHandle*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="02501-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="02501-124">Remarks</span></span>

<span data-ttu-id="02501-125">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="02501-125">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="02501-126">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="02501-126">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="02501-127">Примеры</span><span class="sxs-lookup"><span data-stu-id="02501-127">Examples</span></span>

<span data-ttu-id="02501-128">В следующем примере показано получение маркера смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="02501-128">The following example shows retrieving the smart card handle.</span></span>


```C++
HSCARD   hSC;
HRESULT  hr;

// Retrieve the card handle.
hr = pISCard->get_CardHandle(&hSC);
if (FAILED(hr))
{
   printf("Failed get_CardHandle\n");
   // Take other error handling action as needed.
}
// Use card handle as needed.
```



## <a name="requirements"></a><span data-ttu-id="02501-129">Требования</span><span class="sxs-lookup"><span data-stu-id="02501-129">Requirements</span></span>



| <span data-ttu-id="02501-130">Требование</span><span class="sxs-lookup"><span data-stu-id="02501-130">Requirement</span></span> | <span data-ttu-id="02501-131">Значение</span><span class="sxs-lookup"><span data-stu-id="02501-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02501-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="02501-132">Minimum supported client</span></span><br/> | <span data-ttu-id="02501-133">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="02501-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="02501-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="02501-134">Minimum supported server</span></span><br/> | <span data-ttu-id="02501-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="02501-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="02501-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="02501-136">End of client support</span></span><br/>    | <span data-ttu-id="02501-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="02501-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="02501-138">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="02501-138">End of server support</span></span><br/>    | <span data-ttu-id="02501-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="02501-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="02501-140">Header</span><span class="sxs-lookup"><span data-stu-id="02501-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="02501-141"><dt>Скардмгр. h</dt></span><span class="sxs-lookup"><span data-stu-id="02501-141"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="02501-142">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="02501-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="02501-143"><dt>Скардмгр. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="02501-143"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="02501-144">DLL</span><span class="sxs-lookup"><span data-stu-id="02501-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02501-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02501-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="02501-146">IID</span><span class="sxs-lookup"><span data-stu-id="02501-146">IID</span></span><br/>                      | <span data-ttu-id="02501-147">Идентификатор IID \_ -карты определен как 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="02501-147">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="02501-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02501-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02501-149">**получение \_ ATR**</span><span class="sxs-lookup"><span data-stu-id="02501-149">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="02501-150">**получить \_ контекст**</span><span class="sxs-lookup"><span data-stu-id="02501-150">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="02501-151">**получить \_ протокол**</span><span class="sxs-lookup"><span data-stu-id="02501-151">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="02501-152">**получение \_ состояния**</span><span class="sxs-lookup"><span data-stu-id="02501-152">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="02501-153">**Карточка**</span><span class="sxs-lookup"><span data-stu-id="02501-153">**ISCard**</span></span>](iscard.md)
</dt> </dl>

 

 
