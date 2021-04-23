---
description: Извлекает слово состояния сообщения ответа КАТЕГОРИЯХ APDU.
ms.assetid: c8a4b713-4ae9-49f2-a623-6ee305123638
title: 'Метод Искардкмд:: get_ReplyStatus (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyStatus
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 021c5395dbca6275161a53cb7e8a0c2247ab9410
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145277"
---
# <a name="iscardcmdget_replystatus-method"></a><span data-ttu-id="bd2c2-103">Метод Искардкмд:: Get \_ реплистатус</span><span class="sxs-lookup"><span data-stu-id="bd2c2-103">ISCardCmd::get\_ReplyStatus method</span></span>

<span data-ttu-id="bd2c2-104">\[Метод **Get \_ реплистатус** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="bd2c2-104">\[The **get\_ReplyStatus** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bd2c2-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="bd2c2-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bd2c2-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="bd2c2-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="bd2c2-107">Метод **Get \_ реплистатус** извлекает слово Status сообщения [*Reply категориях APDU*](../secgloss/r-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="bd2c2-107">The **get\_ReplyStatus** method retrieves the [*reply APDU's*](../secgloss/r-gly.md) message status word.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd2c2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bd2c2-108">Syntax</span></span>


```C++
HRESULT get_ReplyStatus(
  [out] LPWORD pwStatus
);
```



## <a name="parameters"></a><span data-ttu-id="bd2c2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="bd2c2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd2c2-110">*пвстатус* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bd2c2-110">*pwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd2c2-111">Указатель на слово, которое является состоянием возврата.</span><span class="sxs-lookup"><span data-stu-id="bd2c2-111">Pointer to the word that is the status on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd2c2-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bd2c2-112">Return value</span></span>

<span data-ttu-id="bd2c2-113">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="bd2c2-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="bd2c2-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="bd2c2-114">Return code</span></span>                                                                                   | <span data-ttu-id="bd2c2-115">Описание</span><span class="sxs-lookup"><span data-stu-id="bd2c2-115">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="bd2c2-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="bd2c2-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="bd2c2-117">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="bd2c2-117">Operation completed successfully.</span></span><br/>       |
| <dl> <span data-ttu-id="bd2c2-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="bd2c2-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="bd2c2-119">Недопустимый параметр *пвстатус* .</span><span class="sxs-lookup"><span data-stu-id="bd2c2-119">The *pwStatus* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="bd2c2-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="bd2c2-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="bd2c2-121">В *пвстатус* был передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="bd2c2-121">A bad pointer was passed in *pwStatus*.</span></span><br/> |
| <dl> <span data-ttu-id="bd2c2-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="bd2c2-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="bd2c2-123">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="bd2c2-123">Out of memory.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="bd2c2-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bd2c2-124">Remarks</span></span>

<span data-ttu-id="bd2c2-125">Чтобы задать слово состояния сообщения ответа КАТЕГОРИЯХ APDU, вызовите метод [**Set \_ реплистатус**](iscardcmd-put-replystatus.md).</span><span class="sxs-lookup"><span data-stu-id="bd2c2-125">To set the reply APDU's message status word, call [**put\_ReplyStatus**](iscardcmd-put-replystatus.md).</span></span>

<span data-ttu-id="bd2c2-126">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардкмд**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="bd2c2-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="bd2c2-127">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="bd2c2-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="bd2c2-128">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="bd2c2-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="bd2c2-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="bd2c2-129">Examples</span></span>

<span data-ttu-id="bd2c2-130">В следующем примере показано, как получить слово состояния сообщения для [*ответа категориях APDU*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="bd2c2-130">The following example shows how to retrieve the message status word of the [*reply APDU*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="bd2c2-131">В примере предполагается, что Пискардкмд является допустимым указателем на экземпляр интерфейса [**искардкмд**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="bd2c2-131">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
WORD    wReplyStatus;
HRESULT hr;

// Get reply status.
hr = pISCardCmd->get_ReplyStatus(&wReplyStatus);
if (FAILED(hr))
{
  printf("Failed get_ReplyStatus\n");
  // Take other error handling action as needed.
}
else
{
  if (wReplyStatus != 0x9000)
  {
    printf("APDU failed - Error [0x%x]\n", wReplyStatus);
    // Take other error handling action as needed.
  }
}
```



## <a name="requirements"></a><span data-ttu-id="bd2c2-132">Требования</span><span class="sxs-lookup"><span data-stu-id="bd2c2-132">Requirements</span></span>



| <span data-ttu-id="bd2c2-133">Требование</span><span class="sxs-lookup"><span data-stu-id="bd2c2-133">Requirement</span></span> | <span data-ttu-id="bd2c2-134">Значение</span><span class="sxs-lookup"><span data-stu-id="bd2c2-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd2c2-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bd2c2-135">Minimum supported client</span></span><br/> | <span data-ttu-id="bd2c2-136">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bd2c2-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bd2c2-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bd2c2-137">Minimum supported server</span></span><br/> | <span data-ttu-id="bd2c2-138">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bd2c2-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bd2c2-139">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="bd2c2-139">End of client support</span></span><br/>    | <span data-ttu-id="bd2c2-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bd2c2-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="bd2c2-141">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="bd2c2-141">End of server support</span></span><br/>    | <span data-ttu-id="bd2c2-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bd2c2-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="bd2c2-143">Header</span><span class="sxs-lookup"><span data-stu-id="bd2c2-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd2c2-144"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd2c2-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="bd2c2-145">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="bd2c2-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="bd2c2-146"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bd2c2-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bd2c2-147">DLL</span><span class="sxs-lookup"><span data-stu-id="bd2c2-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd2c2-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd2c2-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bd2c2-149">IID</span><span class="sxs-lookup"><span data-stu-id="bd2c2-149">IID</span></span><br/>                      | <span data-ttu-id="bd2c2-150">IID \_ искардкмд определен как D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="bd2c2-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="bd2c2-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bd2c2-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd2c2-152">**искардкмд**</span><span class="sxs-lookup"><span data-stu-id="bd2c2-152">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="bd2c2-153">**разместить \_ реплистатус**</span><span class="sxs-lookup"><span data-stu-id="bd2c2-153">**put\_ReplyStatus**</span></span>](iscardcmd-put-replystatus.md)
</dt> </dl>

 

 
