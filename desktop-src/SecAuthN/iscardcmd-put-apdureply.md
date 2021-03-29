---
description: Задает новый ответ КАТЕГОРИЯХ APDU.
ms.assetid: 1d058c89-0de9-4809-b008-ae24c62acc5b
title: 'Искардкмд: метод ut_ApduReply:p (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_ApduReply
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0292f3ebd4e5f18638ad496cdf15cd9f5c4320f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897402"
---
# <a name="iscardcmdput_apdureply-method"></a><span data-ttu-id="7a4aa-103">Искардкмд::p UT \_ апдурепли метод</span><span class="sxs-lookup"><span data-stu-id="7a4aa-103">ISCardCmd::put\_ApduReply method</span></span>

<span data-ttu-id="7a4aa-104">\[Метод **размещения \_ апдурепли** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="7a4aa-104">\[The **put\_ApduReply** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7a4aa-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7a4aa-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7a4aa-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="7a4aa-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="7a4aa-107">Метод **размещения \_ апдурепли** ЗАДАЕТ новый [*ответ категориях APDU*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="7a4aa-107">The **put\_ApduReply** method sets a new [*reply APDU*](../secgloss/r-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7a4aa-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a4aa-108">Syntax</span></span>


```C++
HRESULT put_ApduReply(
  [in] LPBYTEBUFFER pReplyApdu
);
```



## <a name="parameters"></a><span data-ttu-id="7a4aa-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7a4aa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a4aa-110">*препляпду* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7a4aa-110">*pReplyApdu* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a4aa-111">Указатель на буфер байтов (сопоставляется через объект **IStream** ), который содержит сообщение категориях APDU воспроизведения для возврата.</span><span class="sxs-lookup"><span data-stu-id="7a4aa-111">Pointer to the byte buffer (mapped through an **IStream** object) that contains the replay APDU message on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a4aa-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7a4aa-112">Return value</span></span>

<span data-ttu-id="7a4aa-113">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="7a4aa-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="7a4aa-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7a4aa-114">Return code</span></span>                                                                                   | <span data-ttu-id="7a4aa-115">Описание</span><span class="sxs-lookup"><span data-stu-id="7a4aa-115">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="7a4aa-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7a4aa-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7a4aa-117">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="7a4aa-117">Operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="7a4aa-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7a4aa-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="7a4aa-119">Недопустимый параметр *препляпду* .</span><span class="sxs-lookup"><span data-stu-id="7a4aa-119">The *pReplyApdu* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="7a4aa-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="7a4aa-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7a4aa-121">В *препляпду* был передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="7a4aa-121">A bad pointer was passed in *pReplyApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="7a4aa-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7a4aa-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7a4aa-123">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="7a4aa-123">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="7a4aa-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7a4aa-124">Remarks</span></span>

<span data-ttu-id="7a4aa-125">Чтобы получить существующий ответ КАТЕГОРИЯХ APDU, вызовите [**Get \_ апдурепли**](iscardcmd-get-apdureply.md).</span><span class="sxs-lookup"><span data-stu-id="7a4aa-125">To get an existing reply APDU, call [**get\_ApduReply**](iscardcmd-get-apdureply.md).</span></span>

<span data-ttu-id="7a4aa-126">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардкмд**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="7a4aa-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="7a4aa-127">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="7a4aa-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="7a4aa-128">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="7a4aa-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7a4aa-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="7a4aa-129">Examples</span></span>

<span data-ttu-id="7a4aa-130">В следующем примере показано, как задать новый [*ответ категориях APDU*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="7a4aa-130">The following example shows how to set a new [*reply APDU*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="7a4aa-131">В примере предполагается, что Пибитерепли является допустимым указателем на экземпляр [**ибитебуффер**](ibytebuffer.md), а пискардкмд является допустимым указателем на экземпляр интерфейса [**искардкмд**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="7a4aa-131">The example assumes that pIByteReply is a valid pointer to an instance of [**IByteBuffer**](ibytebuffer.md), and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT    hr;

// Set the reply data.
hr = pISCardCmd->put_ApduReply(pIByteReply);
if (FAILED(hr)) 
{
    printf("Failed put_ApduReply.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="7a4aa-132">Требования</span><span class="sxs-lookup"><span data-stu-id="7a4aa-132">Requirements</span></span>



| <span data-ttu-id="7a4aa-133">Требование</span><span class="sxs-lookup"><span data-stu-id="7a4aa-133">Requirement</span></span> | <span data-ttu-id="7a4aa-134">Значение</span><span class="sxs-lookup"><span data-stu-id="7a4aa-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a4aa-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7a4aa-135">Minimum supported client</span></span><br/> | <span data-ttu-id="7a4aa-136">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7a4aa-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7a4aa-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7a4aa-137">Minimum supported server</span></span><br/> | <span data-ttu-id="7a4aa-138">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7a4aa-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7a4aa-139">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="7a4aa-139">End of client support</span></span><br/>    | <span data-ttu-id="7a4aa-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7a4aa-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="7a4aa-141">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="7a4aa-141">End of server support</span></span><br/>    | <span data-ttu-id="7a4aa-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7a4aa-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="7a4aa-143">Header</span><span class="sxs-lookup"><span data-stu-id="7a4aa-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a4aa-144"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a4aa-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="7a4aa-145">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="7a4aa-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="7a4aa-146"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7a4aa-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7a4aa-147">DLL</span><span class="sxs-lookup"><span data-stu-id="7a4aa-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a4aa-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a4aa-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7a4aa-149">IID</span><span class="sxs-lookup"><span data-stu-id="7a4aa-149">IID</span></span><br/>                      | <span data-ttu-id="7a4aa-150">IID \_ искардкмд определен как D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="7a4aa-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="7a4aa-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a4aa-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a4aa-152">**получить \_ апдурепли**</span><span class="sxs-lookup"><span data-stu-id="7a4aa-152">**get\_ApduReply**</span></span>](iscardcmd-get-apdureply.md)
</dt> <dt>

[<span data-ttu-id="7a4aa-153">**получить \_ апдуреплиленгс**</span><span class="sxs-lookup"><span data-stu-id="7a4aa-153">**get\_ApduReplyLength**</span></span>](iscardcmd-get-apdureplylength.md)
</dt> <dt>

[<span data-ttu-id="7a4aa-154">**искардкмд**</span><span class="sxs-lookup"><span data-stu-id="7a4aa-154">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
