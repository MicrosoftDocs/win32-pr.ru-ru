---
description: Определяет длину (в байтах) единицы данных протокола приложения (КАТЕГОРИЯХ APDU).
ms.assetid: 25011db1-a037-4764-b700-8ad2200419da
title: 'Метод Искардкмд:: get_ApduReplyLength (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ApduReplyLength
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b62e67154ab48f8378c96a78c8bd54765962c3fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272775"
---
# <a name="iscardcmdget_apdureplylength-method"></a><span data-ttu-id="0e02f-103">Метод Искардкмд:: Get \_ апдуреплиленгс</span><span class="sxs-lookup"><span data-stu-id="0e02f-103">ISCardCmd::get\_ApduReplyLength method</span></span>

<span data-ttu-id="0e02f-104">\[Метод **Get \_ апдуреплиленгс** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="0e02f-104">\[The **get\_ApduReplyLength** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0e02f-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="0e02f-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0e02f-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="0e02f-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="0e02f-107">Метод **Get \_ апдуреплиленгс** определяет длину (в байтах) [*единицы данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).</span><span class="sxs-lookup"><span data-stu-id="0e02f-107">The **get\_ApduReplyLength** method determines the length (in bytes) of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="0e02f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e02f-108">Syntax</span></span>


```C++
HRESULT get_ApduReplyLength(
  [out] LONG *plSize
);
```



## <a name="parameters"></a><span data-ttu-id="0e02f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e02f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e02f-110">*плсизе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0e02f-110">*plSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e02f-111">Указатель на размер сообщения ответа КАТЕГОРИЯХ APDU.</span><span class="sxs-lookup"><span data-stu-id="0e02f-111">Pointer to the size of the reply APDU message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e02f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0e02f-112">Return value</span></span>

<span data-ttu-id="0e02f-113">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="0e02f-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="0e02f-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="0e02f-114">Return code</span></span>                                                                                   | <span data-ttu-id="0e02f-115">Описание</span><span class="sxs-lookup"><span data-stu-id="0e02f-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="0e02f-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="0e02f-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0e02f-117">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="0e02f-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="0e02f-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0e02f-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="0e02f-119">Недопустимый параметр *плсизе* .</span><span class="sxs-lookup"><span data-stu-id="0e02f-119">The *plSize* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="0e02f-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="0e02f-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="0e02f-121">В *плсизе* был передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="0e02f-121">A bad pointer was passed in *plSize*.</span></span><br/> |
| <dl> <span data-ttu-id="0e02f-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0e02f-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0e02f-123">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="0e02f-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="0e02f-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0e02f-124">Remarks</span></span>

<span data-ttu-id="0e02f-125">Чтобы получить существующий ответ КАТЕГОРИЯХ APDU, вызовите [**Get \_ апдурепли**](iscardcmd-get-apdureply.md).</span><span class="sxs-lookup"><span data-stu-id="0e02f-125">To get an existing reply APDU, call [**get\_ApduReply**](iscardcmd-get-apdureply.md).</span></span>

<span data-ttu-id="0e02f-126">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардкмд**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="0e02f-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="0e02f-127">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="0e02f-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="0e02f-128">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="0e02f-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0e02f-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="0e02f-129">Examples</span></span>

<span data-ttu-id="0e02f-130">В следующем примере показано, как получить длину [*ответа категориях APDU*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0e02f-130">The following example shows how to retrieve the length of the [*reply APDU*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="0e02f-131">В примере предполагается, что Пискардкмд является допустимым указателем на экземпляр интерфейса [**искардкмд**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="0e02f-131">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
LONG    lLen;
HRESULT hr;

// Retrieve the APDU reply length.
hr = pISCardCmd->get_ApduReplyLength(&lLen);
if (FAILED(hr))
{
    printf("Failed get_ApduReplyLength\n");
    // Take other error handling action.
}
else
    printf("Length returned is %d\n", lLen);
```



## <a name="requirements"></a><span data-ttu-id="0e02f-132">Требования</span><span class="sxs-lookup"><span data-stu-id="0e02f-132">Requirements</span></span>



| <span data-ttu-id="0e02f-133">Требование</span><span class="sxs-lookup"><span data-stu-id="0e02f-133">Requirement</span></span> | <span data-ttu-id="0e02f-134">Значение</span><span class="sxs-lookup"><span data-stu-id="0e02f-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e02f-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0e02f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="0e02f-136">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0e02f-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0e02f-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0e02f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="0e02f-138">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0e02f-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0e02f-139">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="0e02f-139">End of client support</span></span><br/>    | <span data-ttu-id="0e02f-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0e02f-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="0e02f-141">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="0e02f-141">End of server support</span></span><br/>    | <span data-ttu-id="0e02f-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0e02f-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="0e02f-143">Header</span><span class="sxs-lookup"><span data-stu-id="0e02f-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e02f-144"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e02f-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="0e02f-145">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="0e02f-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="0e02f-146"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0e02f-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0e02f-147">DLL</span><span class="sxs-lookup"><span data-stu-id="0e02f-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e02f-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e02f-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0e02f-149">IID</span><span class="sxs-lookup"><span data-stu-id="0e02f-149">IID</span></span><br/>                      | <span data-ttu-id="0e02f-150">IID \_ искардкмд определен как D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="0e02f-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="0e02f-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e02f-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e02f-152">**получить \_ апдурепли**</span><span class="sxs-lookup"><span data-stu-id="0e02f-152">**get\_ApduReply**</span></span>](iscardcmd-get-apdureply.md)
</dt> <dt>

[<span data-ttu-id="0e02f-153">**искардкмд**</span><span class="sxs-lookup"><span data-stu-id="0e02f-153">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="0e02f-154">**разместить \_ апдурепли**</span><span class="sxs-lookup"><span data-stu-id="0e02f-154">**put\_ApduReply**</span></span>](iscardcmd-put-apdureply.md)
</dt> </dl>

 

 
