---
description: Возвращает идентификатор протокола, используемого в данный момент на смарт-карте.
ms.assetid: 68c75e98-da5c-4e3e-9836-369941751fb0
title: Метод get_Protocol. h.
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Protocol
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: fb58f890da85e3348ede6af70a006f98daac38a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348052"
---
# <a name="iscardget_protocol-method"></a><span data-ttu-id="a7857-103">Метод "карточки:: получение \_ протокола"</span><span class="sxs-lookup"><span data-stu-id="a7857-103">ISCard::get\_Protocol method</span></span>

<span data-ttu-id="a7857-104">\[Метод **Get \_ Protocol** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="a7857-104">\[The **get\_Protocol** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a7857-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="a7857-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a7857-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="a7857-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="a7857-107">Метод **получения \_ протокола** получает идентификатор протокола, используемого на [*смарт-карте*](../secgloss/s-gly.md)в настоящий момент.</span><span class="sxs-lookup"><span data-stu-id="a7857-107">The **get\_Protocol** method retrieves the identifier of the protocol currently in use on the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a7857-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7857-108">Syntax</span></span>


```C++
HRESULT get_Protocol(
  [out] SCARD_PROTOCOLS *pProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="a7857-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7857-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7857-110">*ппротокол* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a7857-110">*pProtocol* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7857-111">Указатель на идентификатор протокола.</span><span class="sxs-lookup"><span data-stu-id="a7857-111">Pointer to the protocol identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7857-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a7857-112">Return value</span></span>

<span data-ttu-id="a7857-113">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="a7857-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="a7857-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a7857-114">Return code</span></span>                                                                                  | <span data-ttu-id="a7857-115">Описание</span><span class="sxs-lookup"><span data-stu-id="a7857-115">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="a7857-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a7857-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="a7857-117">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="a7857-117">Operation completed successfully.</span></span><br/>        |
| <dl> <span data-ttu-id="a7857-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a7857-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="a7857-119">Недопустимый параметр *ппротокол* .</span><span class="sxs-lookup"><span data-stu-id="a7857-119">The *pProtocol* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="a7857-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="a7857-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="a7857-121">В *ппротокол* был передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="a7857-121">A bad pointer was passed in *pProtocol*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a7857-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a7857-122">Remarks</span></span>

<span data-ttu-id="a7857-123">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="a7857-123">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="a7857-124">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="a7857-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a7857-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="a7857-125">Examples</span></span>

<span data-ttu-id="a7857-126">В следующем примере показано, как получить идентификатор протокола, используемого на смарт-карте в данный момент.</span><span class="sxs-lookup"><span data-stu-id="a7857-126">The following example shows retrieving the identifier of the protocol currently in use on the smart card.</span></span>


```C++
SCARD_PROTOCOLS   scProtocol;
HRESULT           hr;

// Retrieve the protocol.
hr = pISCard->get_Protocol(&scProtocol);
if (FAILED(hr))
{
   printf("Failed get_Protocol\n");
   // Take other error handling action as needed.
}
// Use the retrieved protocol. (This example merely displays it.)
switch (scProtocol)
{
    case T0:
        printf("T0 protocol\n");
        break;
    case T1:
        printf("T1 protocol\n");
        break;
    default:
        printf("Other protocol\n");
        break;
}
```



## <a name="requirements"></a><span data-ttu-id="a7857-127">Требования</span><span class="sxs-lookup"><span data-stu-id="a7857-127">Requirements</span></span>



| <span data-ttu-id="a7857-128">Требование</span><span class="sxs-lookup"><span data-stu-id="a7857-128">Requirement</span></span> | <span data-ttu-id="a7857-129">Значение</span><span class="sxs-lookup"><span data-stu-id="a7857-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7857-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a7857-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a7857-131">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a7857-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a7857-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a7857-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a7857-133">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a7857-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a7857-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="a7857-134">End of client support</span></span><br/>    | <span data-ttu-id="a7857-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a7857-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="a7857-136">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="a7857-136">End of server support</span></span><br/>    | <span data-ttu-id="a7857-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a7857-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="a7857-138">Header</span><span class="sxs-lookup"><span data-stu-id="a7857-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7857-139"><dt>Скардмгр. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7857-139"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="a7857-140">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="a7857-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="a7857-141"><dt>Скардмгр. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a7857-141"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a7857-142">DLL</span><span class="sxs-lookup"><span data-stu-id="a7857-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7857-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7857-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a7857-144">IID</span><span class="sxs-lookup"><span data-stu-id="a7857-144">IID</span></span><br/>                      | <span data-ttu-id="a7857-145">Идентификатор IID \_ -карты определен как 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="a7857-145">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="a7857-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a7857-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7857-147">**получение \_ ATR**</span><span class="sxs-lookup"><span data-stu-id="a7857-147">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="a7857-148">**получить \_ кардхандле**</span><span class="sxs-lookup"><span data-stu-id="a7857-148">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="a7857-149">**получить \_ контекст**</span><span class="sxs-lookup"><span data-stu-id="a7857-149">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="a7857-150">**получение \_ состояния**</span><span class="sxs-lookup"><span data-stu-id="a7857-150">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="a7857-151">**Карточка**</span><span class="sxs-lookup"><span data-stu-id="a7857-151">**ISCard**</span></span>](iscard.md)
</dt> </dl>

 

 
