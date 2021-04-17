---
description: Присоединяет объект открытк к открытому и настроенному обработчику смарт-карты.
ms.assetid: e735d33d-a337-404e-a760-4cf8f19d172a
title: Метод Аттачбихандле (Скардмгр. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.AttachByHandle
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e72ce215b373ef8bd48921f796083e9bc5e801be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647616"
---
# <a name="iscardattachbyhandle-method"></a><span data-ttu-id="49db7-103">Метод Аттачбихандле::</span><span class="sxs-lookup"><span data-stu-id="49db7-103">ISCard::AttachByHandle method</span></span>

<span data-ttu-id="49db7-104">\[Метод **аттачбихандле** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="49db7-104">\[The **AttachByHandle** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="49db7-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="49db7-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="49db7-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="49db7-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="49db7-107">Метод **аттачбихандле** Присоединяет объект [**кредитной карты**](iscard.md) к открытому и настроенному обработчику [*смарт-карты*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="49db7-107">The **AttachByHandle** method attaches the [**ISCard**](iscard.md) object to an open and configured [*smart card*](../secgloss/s-gly.md) handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="49db7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="49db7-108">Syntax</span></span>


```C++
HRESULT AttachByHandle(
  [in] HSCARD hCard
);
```



## <a name="parameters"></a><span data-ttu-id="49db7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="49db7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49db7-110">*хкард* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="49db7-110">*hCard* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49db7-111">Маркер открытого соединения со смарт-картой.</span><span class="sxs-lookup"><span data-stu-id="49db7-111">A handle to an open connection to a smart card.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49db7-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="49db7-112">Return value</span></span>

<span data-ttu-id="49db7-113">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="49db7-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="49db7-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="49db7-114">Return code</span></span>                                                                                  | <span data-ttu-id="49db7-115">Описание</span><span class="sxs-lookup"><span data-stu-id="49db7-115">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="49db7-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="49db7-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="49db7-117">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="49db7-117">Operation completed successfully.</span></span><br/>   |
| <dl> <span data-ttu-id="49db7-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="49db7-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="49db7-119">Недопустимый параметр *хкард* .</span><span class="sxs-lookup"><span data-stu-id="49db7-119">The *hCard* parameter is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="49db7-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="49db7-120">Remarks</span></span>

<span data-ttu-id="49db7-121">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="49db7-121">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="49db7-122">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="49db7-122">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

<span data-ttu-id="49db7-123">Завершив использование этого маркера, отпустите вложение, вызвав метод [**етач::D**](iscard-detach.md) .</span><span class="sxs-lookup"><span data-stu-id="49db7-123">When you have finished using the handle, release the attachment by calling the [**ISCard::Detach**](iscard-detach.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="49db7-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="49db7-124">Examples</span></span>

<span data-ttu-id="49db7-125">В следующем примере показано подключение к обработчику смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="49db7-125">The following example shows attaching to a smart card handle.</span></span>


```C++
HRESULT  hr;

// hSC is of type HSCARD and has been previously assigned.
// Attach SCard to the smart card using the value in hSC.
hr = pISCard->AttachByHandle(hSC);
if (FAILED(hr))
{
   printf("Failed AttachByHandle\n");
   // Take other error handling action as needed.
}
// Proceed using attached reader.
```



## <a name="requirements"></a><span data-ttu-id="49db7-126">Требования</span><span class="sxs-lookup"><span data-stu-id="49db7-126">Requirements</span></span>



| <span data-ttu-id="49db7-127">Требование</span><span class="sxs-lookup"><span data-stu-id="49db7-127">Requirement</span></span> | <span data-ttu-id="49db7-128">Значение</span><span class="sxs-lookup"><span data-stu-id="49db7-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49db7-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="49db7-129">Minimum supported client</span></span><br/> | <span data-ttu-id="49db7-130">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="49db7-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="49db7-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="49db7-131">Minimum supported server</span></span><br/> | <span data-ttu-id="49db7-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="49db7-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="49db7-133">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="49db7-133">End of client support</span></span><br/>    | <span data-ttu-id="49db7-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="49db7-134">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="49db7-135">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="49db7-135">End of server support</span></span><br/>    | <span data-ttu-id="49db7-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="49db7-136">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="49db7-137">Header</span><span class="sxs-lookup"><span data-stu-id="49db7-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="49db7-138"><dt>Скардмгр. h</dt></span><span class="sxs-lookup"><span data-stu-id="49db7-138"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="49db7-139">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="49db7-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="49db7-140"><dt>Скардмгр. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="49db7-140"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="49db7-141">DLL</span><span class="sxs-lookup"><span data-stu-id="49db7-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49db7-142"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49db7-142"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="49db7-143">IID</span><span class="sxs-lookup"><span data-stu-id="49db7-143">IID</span></span><br/>                      | <span data-ttu-id="49db7-144">Идентификатор IID \_ -карты определен как 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="49db7-144">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="49db7-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="49db7-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49db7-146">**аттачбиреадер**</span><span class="sxs-lookup"><span data-stu-id="49db7-146">**AttachByReader**</span></span>](iscard-attachbyreader.md)
</dt> <dt>

[<span data-ttu-id="49db7-147">**Соединил**</span><span class="sxs-lookup"><span data-stu-id="49db7-147">**Detach**</span></span>](iscard-detach.md)
</dt> <dt>

[<span data-ttu-id="49db7-148">**получить \_ кардхандле**</span><span class="sxs-lookup"><span data-stu-id="49db7-148">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="49db7-149">**Карточка**</span><span class="sxs-lookup"><span data-stu-id="49db7-149">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="49db7-150">**Повторно подключиться**</span><span class="sxs-lookup"><span data-stu-id="49db7-150">**ReAttach**</span></span>](iscard-reattach.md)
</dt> </dl>

 

 
