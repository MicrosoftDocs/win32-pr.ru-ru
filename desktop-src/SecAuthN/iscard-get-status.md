---
description: Извлекает текущее состояние смарт-карты.
ms.assetid: 0e6e4a8f-ecad-4a82-8804-aaf58f13f7ca
title: Метод get_Status. h.
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Status
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f0daa47653779b3aa4b5e7cb65c0c56410b19ab9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272776"
---
# <a name="iscardget_status-method"></a><span data-ttu-id="cbd87-103">Метод карточки:: Get \_ status</span><span class="sxs-lookup"><span data-stu-id="cbd87-103">ISCard::get\_Status method</span></span>

<span data-ttu-id="cbd87-104">\[Метод **Get \_ Status** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="cbd87-104">\[The **get\_Status** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cbd87-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="cbd87-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cbd87-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="cbd87-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="cbd87-107">Метод **Get \_ Status** извлекает текущее [*состояние*](../secgloss/s-gly.md) [*смарт-карты*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="cbd87-107">The **get\_Status** method retrieves the current [*state*](../secgloss/s-gly.md) of the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cbd87-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cbd87-108">Syntax</span></span>


```C++
HRESULT get_Status(
  [out] SCARD_STATES *pStatus
);
```



## <a name="parameters"></a><span data-ttu-id="cbd87-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cbd87-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbd87-110">*пстатус* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cbd87-110">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cbd87-111">Указатель на переменную состояния.</span><span class="sxs-lookup"><span data-stu-id="cbd87-111">Pointer to the state variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbd87-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cbd87-112">Return value</span></span>

<span data-ttu-id="cbd87-113">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="cbd87-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="cbd87-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="cbd87-114">Return code</span></span>                                                                                  | <span data-ttu-id="cbd87-115">Описание</span><span class="sxs-lookup"><span data-stu-id="cbd87-115">Description</span></span>                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="cbd87-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd87-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="cbd87-117">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="cbd87-117">Operation completed successfully.</span></span><br/>      |
| <dl> <span data-ttu-id="cbd87-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd87-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="cbd87-119">Недопустимый параметр *пстатус* .</span><span class="sxs-lookup"><span data-stu-id="cbd87-119">The *pStatus* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="cbd87-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd87-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="cbd87-121">В *пстатус* был передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="cbd87-121">A bad pointer was passed in *pStatus*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cbd87-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cbd87-122">Remarks</span></span>

<span data-ttu-id="cbd87-123">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="cbd87-123">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="cbd87-124">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="cbd87-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="cbd87-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="cbd87-125">Examples</span></span>

<span data-ttu-id="cbd87-126">В следующем примере показано получение текущего состояния смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="cbd87-126">The following example shows retrieving the current state of the smart card.</span></span>


```C++
SCARD_STATES    scState;
HRESULT         hr;

// Determine the current state of the smart card.
hr = pISCard->get_Status(&scState);
if (FAILED(hr))
{
   printf("Failed get_Status\n");
   exit(1);  // Or other error handling action.
}
// Use the retrieved value. (This example merely displays it.)
switch (scState)
{
    case ABSENT:
        printf("Absent state\n");
        break;
    case PRESENT:
        printf("Present state\n");
        break;
    case SWALLOWED:
        printf("Swallowed state\n");
        break;
    case POWERED:
        printf("Powered state\n");
        break;
    case NEGOTIABLEMODE:
        printf("Negotiable mode state\n");
        break;
    case SPECIFICMODE:
        printf("Specific mode state\n");
        break;
    default:
        printf("Unexpected state\n");
        break;
}
```



## <a name="requirements"></a><span data-ttu-id="cbd87-127">Требования</span><span class="sxs-lookup"><span data-stu-id="cbd87-127">Requirements</span></span>



| <span data-ttu-id="cbd87-128">Требование</span><span class="sxs-lookup"><span data-stu-id="cbd87-128">Requirement</span></span> | <span data-ttu-id="cbd87-129">Значение</span><span class="sxs-lookup"><span data-stu-id="cbd87-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cbd87-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cbd87-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cbd87-131">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cbd87-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="cbd87-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cbd87-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cbd87-133">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cbd87-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cbd87-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="cbd87-134">End of client support</span></span><br/>    | <span data-ttu-id="cbd87-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="cbd87-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="cbd87-136">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="cbd87-136">End of server support</span></span><br/>    | <span data-ttu-id="cbd87-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cbd87-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="cbd87-138">Header</span><span class="sxs-lookup"><span data-stu-id="cbd87-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbd87-139"><dt>Скардмгр. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbd87-139"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="cbd87-140">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="cbd87-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="cbd87-141"><dt>Скардмгр. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cbd87-141"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cbd87-142">DLL</span><span class="sxs-lookup"><span data-stu-id="cbd87-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbd87-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbd87-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="cbd87-144">IID</span><span class="sxs-lookup"><span data-stu-id="cbd87-144">IID</span></span><br/>                      | <span data-ttu-id="cbd87-145">Идентификатор IID \_ -карты определен как 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="cbd87-145">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="cbd87-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cbd87-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbd87-147">**получение \_ ATR**</span><span class="sxs-lookup"><span data-stu-id="cbd87-147">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="cbd87-148">**получить \_ кардхандле**</span><span class="sxs-lookup"><span data-stu-id="cbd87-148">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="cbd87-149">**получить \_ контекст**</span><span class="sxs-lookup"><span data-stu-id="cbd87-149">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="cbd87-150">**получить \_ протокол**</span><span class="sxs-lookup"><span data-stu-id="cbd87-150">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="cbd87-151">**Карточка**</span><span class="sxs-lookup"><span data-stu-id="cbd87-151">**ISCard**</span></span>](iscard.md)
</dt> </dl>

 

 
