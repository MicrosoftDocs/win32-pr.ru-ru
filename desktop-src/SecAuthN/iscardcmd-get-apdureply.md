---
description: Извлекает ответ КАТЕГОРИЯХ APDU, помещая его в конкретный буфер байтов.
ms.assetid: ab349e7a-350f-4e72-98b4-4c6431b6e380
title: 'Метод Искардкмд:: get_ApduReply (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ApduReply
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2ce11ec2d3d8202574ab23074531c393c9fecb98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081572"
---
# <a name="iscardcmdget_apdureply-method"></a><span data-ttu-id="4d3a4-103">Метод Искардкмд:: Get \_ апдурепли</span><span class="sxs-lookup"><span data-stu-id="4d3a4-103">ISCardCmd::get\_ApduReply method</span></span>

<span data-ttu-id="4d3a4-104">\[Метод **Get \_ апдурепли** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="4d3a4-104">\[The **get\_ApduReply** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4d3a4-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="4d3a4-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4d3a4-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="4d3a4-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="4d3a4-107">Метод **Get \_ апдурепли** извлекает [*ответ категориях APDU*](../secgloss/r-gly.md), помещая его в конкретный буфер байтов.</span><span class="sxs-lookup"><span data-stu-id="4d3a4-107">The **get\_ApduReply** method retrieves the [*reply APDU*](../secgloss/r-gly.md), placing it in a specific byte buffer.</span></span> <span data-ttu-id="4d3a4-108">Ответ может быть **равен null** , если в команде категориях APDU не выполнялась [*транзакция*](../secgloss/t-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="4d3a4-108">The reply may be **NULL** if no [*transaction*](../secgloss/t-gly.md) has been performed on the command APDU.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d3a4-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4d3a4-109">Syntax</span></span>


```C++
HRESULT get_ApduReply(
  [out] LPBYTEBUFFER *ppReplyApdu
);
```



## <a name="parameters"></a><span data-ttu-id="4d3a4-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="4d3a4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d3a4-111">*ппрепляпду* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4d3a4-111">*ppReplyApdu* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d3a4-112">Указатель на байтовый буфер (сопоставляется через объект **IStream** ), содержащий ответное сообщение категориях APDU при возврате.</span><span class="sxs-lookup"><span data-stu-id="4d3a4-112">Pointer to the byte buffer (mapped through an **IStream** object) that contains the APDU reply message on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d3a4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4d3a4-113">Return value</span></span>

<span data-ttu-id="4d3a4-114">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="4d3a4-114">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="4d3a4-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4d3a4-115">Return code</span></span>                                                                                   | <span data-ttu-id="4d3a4-116">Описание</span><span class="sxs-lookup"><span data-stu-id="4d3a4-116">Description</span></span>                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="4d3a4-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="4d3a4-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4d3a4-118">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="4d3a4-118">Operation completed successfully.</span></span><br/>          |
| <dl> <span data-ttu-id="4d3a4-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4d3a4-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="4d3a4-120">Недопустимый параметр *ппрепляпду* .</span><span class="sxs-lookup"><span data-stu-id="4d3a4-120">The *ppReplyApdu* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="4d3a4-121"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="4d3a4-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="4d3a4-122">В *ппрепляпду* был передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="4d3a4-122">A bad pointer was passed in *ppReplyApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="4d3a4-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4d3a4-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4d3a4-124">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="4d3a4-124">Out of memory.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="4d3a4-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4d3a4-125">Remarks</span></span>

<span data-ttu-id="4d3a4-126">Чтобы определить длину ответа КАТЕГОРИЯХ APDU, вызовите [**Get \_ апдуреплиленгс**](iscardcmd-get-apdureplylength.md).</span><span class="sxs-lookup"><span data-stu-id="4d3a4-126">To determine the length of the APDU reply, call [**get\_ApduReplyLength**](iscardcmd-get-apdureplylength.md).</span></span>

<span data-ttu-id="4d3a4-127">Чтобы задать новый ответ КАТЕГОРИЯХ APDU, вызовите метод Set [**\_ апдурепли**](iscardcmd-put-apdureply.md).</span><span class="sxs-lookup"><span data-stu-id="4d3a4-127">To set a new reply APDU, call [**put\_ApduReply**](iscardcmd-put-apdureply.md).</span></span>

<span data-ttu-id="4d3a4-128">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардкмд**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="4d3a4-128">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="4d3a4-129">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="4d3a4-129">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="4d3a4-130">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="4d3a4-130">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4d3a4-131">Примеры</span><span class="sxs-lookup"><span data-stu-id="4d3a4-131">Examples</span></span>

<span data-ttu-id="4d3a4-132">В следующем примере показано, как получить данные ответа.</span><span class="sxs-lookup"><span data-stu-id="4d3a4-132">The following example shows how to retrieve reply data.</span></span> <span data-ttu-id="4d3a4-133">В примере предполагается, что лле является переменной типа **Long** , значение которой было задано предыдущим вызовом [**метода искардкмд:: Get \_ апдуреплиленгс**](iscardcmd-get-apdureplylength.md) , пибитерепли является допустимым указателем на экземпляр интерфейса [**ибитебуффер**](ibytebuffer.md) , а пискардкмд является допустимым указателем на экземпляр интерфейса [**искардкмд**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="4d3a4-133">The example assumes that lLe is a variable of type **LONG** whose value was set by a previous call to the [**ISCardCmd::get\_ApduReplyLength**](iscardcmd-get-apdureplylength.md) method, that pIByteReply is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface, and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT      hr;

if (lLe > 0)
{
    // Get reply data if available.
    hr = pISCardCmd->get_ApduReply(&pIByteReply);
    if (FAILED(hr)) 
    {
        printf("Failed ISCardCmd::get_ApduReply.\n");
        // Take other error handling action as needed.
    }
    else
    {
        BYTE byReplyBytes[256];
        LONG lBytesRead;

        hr = pIByteReply->Read(byReplyBytes, lLe, &lBytesRead);
        if (FAILED(hr))
        {
            printf("Failed IByteBuffer::Read.\n");
            // Take other error handling action as needed.
        }
        // Use the bytes in byReplyBytes as needed.
    }
}
```



## <a name="requirements"></a><span data-ttu-id="4d3a4-134">Требования</span><span class="sxs-lookup"><span data-stu-id="4d3a4-134">Requirements</span></span>



| <span data-ttu-id="4d3a4-135">Требование</span><span class="sxs-lookup"><span data-stu-id="4d3a4-135">Requirement</span></span> | <span data-ttu-id="4d3a4-136">Значение</span><span class="sxs-lookup"><span data-stu-id="4d3a4-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d3a4-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4d3a4-137">Minimum supported client</span></span><br/> | <span data-ttu-id="4d3a4-138">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4d3a4-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4d3a4-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4d3a4-139">Minimum supported server</span></span><br/> | <span data-ttu-id="4d3a4-140">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4d3a4-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4d3a4-141">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="4d3a4-141">End of client support</span></span><br/>    | <span data-ttu-id="4d3a4-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4d3a4-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="4d3a4-143">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="4d3a4-143">End of server support</span></span><br/>    | <span data-ttu-id="4d3a4-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4d3a4-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="4d3a4-145">Header</span><span class="sxs-lookup"><span data-stu-id="4d3a4-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d3a4-146"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d3a4-146"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="4d3a4-147">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="4d3a4-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="4d3a4-148"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4d3a4-148"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4d3a4-149">DLL</span><span class="sxs-lookup"><span data-stu-id="4d3a4-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d3a4-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d3a4-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4d3a4-151">IID</span><span class="sxs-lookup"><span data-stu-id="4d3a4-151">IID</span></span><br/>                      | <span data-ttu-id="4d3a4-152">IID \_ искардкмд определен как D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="4d3a4-152">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="4d3a4-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4d3a4-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d3a4-154">**получить \_ апдуреплиленгс**</span><span class="sxs-lookup"><span data-stu-id="4d3a4-154">**get\_ApduReplyLength**</span></span>](iscardcmd-get-apdureplylength.md)
</dt> <dt>

[<span data-ttu-id="4d3a4-155">**искардкмд**</span><span class="sxs-lookup"><span data-stu-id="4d3a4-155">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="4d3a4-156">**разместить \_ апдурепли**</span><span class="sxs-lookup"><span data-stu-id="4d3a4-156">**put\_ApduReply**</span></span>](iscardcmd-put-apdureply.md)
</dt> </dl>

 

 
