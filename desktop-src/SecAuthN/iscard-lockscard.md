---
description: Метод Локкскард заявляет эксклюзивный доступ к смарт-карте.
ms.assetid: 70af7c5a-ebe7-48ee-8a76-dfea7f73f45e
title: Метод Локкскард (Скардмгр. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.LockSCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d5b834afec339aa4c3a4eee42f9817409fabb917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266242"
---
# <a name="iscardlockscard-method"></a><span data-ttu-id="fbf30-103">Метод Локкскард::</span><span class="sxs-lookup"><span data-stu-id="fbf30-103">ISCard::LockSCard method</span></span>

<span data-ttu-id="fbf30-104">\[Метод **локкскард** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="fbf30-104">\[The **LockSCard** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fbf30-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="fbf30-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fbf30-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="fbf30-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="fbf30-107">Метод **локкскард** заявляет эксклюзивный доступ к [*смарт-карте*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="fbf30-107">The **LockSCard** method claims exclusive access to the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fbf30-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fbf30-108">Syntax</span></span>


```C++
HRESULT LockSCard();
```



## <a name="parameters"></a><span data-ttu-id="fbf30-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fbf30-109">Parameters</span></span>

<span data-ttu-id="fbf30-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="fbf30-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fbf30-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fbf30-111">Return value</span></span>

<span data-ttu-id="fbf30-112">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="fbf30-112">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="fbf30-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="fbf30-113">Return code</span></span>                                                                          | <span data-ttu-id="fbf30-114">Описание</span><span class="sxs-lookup"><span data-stu-id="fbf30-114">Description</span></span>                                  |
|--------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="fbf30-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="fbf30-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="fbf30-116">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="fbf30-116">Operation completed successfully.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fbf30-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fbf30-117">Remarks</span></span>

<span data-ttu-id="fbf30-118">В дополнение к коду ошибки COM, указанному выше, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="fbf30-118">In addition to the COM error code listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="fbf30-119">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="fbf30-119">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

<span data-ttu-id="fbf30-120">Чтобы разблокировать смарт-карту, вызовите метод [**унлоккскард::**](iscard-unlockscard.md) .</span><span class="sxs-lookup"><span data-stu-id="fbf30-120">To unlock the smart card, call the [**ISCard::UnlockSCard**](iscard-unlockscard.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="fbf30-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="fbf30-121">Examples</span></span>

<span data-ttu-id="fbf30-122">В следующем примере показано получение монопольного доступа к смарт-карте.</span><span class="sxs-lookup"><span data-stu-id="fbf30-122">The following example shows acquiring exclusive access to the smart card.</span></span>


```C++
HRESULT    hr;

// Lock the smart card.
hr = pISCard->LockSCard();
if (FAILED(hr))
{
    printf("Failed LockSCard\n");
    // Take error handling action as needed.
}
// Use smart card; unlock the smart card when done.
```



## <a name="requirements"></a><span data-ttu-id="fbf30-123">Требования</span><span class="sxs-lookup"><span data-stu-id="fbf30-123">Requirements</span></span>



| <span data-ttu-id="fbf30-124">Требование</span><span class="sxs-lookup"><span data-stu-id="fbf30-124">Requirement</span></span> | <span data-ttu-id="fbf30-125">Значение</span><span class="sxs-lookup"><span data-stu-id="fbf30-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbf30-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fbf30-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fbf30-127">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fbf30-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fbf30-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fbf30-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fbf30-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fbf30-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fbf30-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="fbf30-130">End of client support</span></span><br/>    | <span data-ttu-id="fbf30-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fbf30-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="fbf30-132">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="fbf30-132">End of server support</span></span><br/>    | <span data-ttu-id="fbf30-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fbf30-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="fbf30-134">Header</span><span class="sxs-lookup"><span data-stu-id="fbf30-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbf30-135"><dt>Скардмгр. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbf30-135"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="fbf30-136">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="fbf30-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="fbf30-137"><dt>Скардмгр. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fbf30-137"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fbf30-138">DLL</span><span class="sxs-lookup"><span data-stu-id="fbf30-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbf30-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbf30-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fbf30-140">IID</span><span class="sxs-lookup"><span data-stu-id="fbf30-140">IID</span></span><br/>                      | <span data-ttu-id="fbf30-141">Идентификатор IID \_ -карты определен как 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="fbf30-141">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="fbf30-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fbf30-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbf30-143">**Карточка**</span><span class="sxs-lookup"><span data-stu-id="fbf30-143">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="fbf30-144">**унлоккскард**</span><span class="sxs-lookup"><span data-stu-id="fbf30-144">**UnlockSCard**</span></span>](iscard-unlockscard.md)
</dt> </dl>

 

 
