---
description: Извлекает адрес узла (NAD), используемый смарт-картой в ответном сообщении.
ms.assetid: bf4f281c-d378-4abd-8f2e-e23c2f4e87a4
title: 'Метод Искардкмд:: get_ReplyNad (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyNad
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2088aa208a97511fd53eecec5a8cdc473b612bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145280"
---
# <a name="iscardcmdget_replynad-method"></a><span data-ttu-id="d49f4-103">Метод Искардкмд:: Get \_ реплинад</span><span class="sxs-lookup"><span data-stu-id="d49f4-103">ISCardCmd::get\_ReplyNad method</span></span>

<span data-ttu-id="d49f4-104">\[Метод **Get \_ реплинад** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="d49f4-104">\[The **get\_ReplyNad** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d49f4-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d49f4-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d49f4-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="d49f4-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d49f4-107">Метод **Get \_ реплинад** извлекает адрес узла (NAD), используемый [*смарт-картой*](../secgloss/s-gly.md) в ответном сообщении.</span><span class="sxs-lookup"><span data-stu-id="d49f4-107">The **get\_ReplyNad** method retrieves the node address (Nad) used by the [*smart card*](../secgloss/s-gly.md) in the reply message.</span></span>

## <a name="syntax"></a><span data-ttu-id="d49f4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d49f4-108">Syntax</span></span>


```C++
HRESULT get_ReplyNad(
  [out] BYTE *pbNad
);
```



## <a name="parameters"></a><span data-ttu-id="d49f4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d49f4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d49f4-110">*пбнад* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d49f4-110">*pbNad* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d49f4-111">Указатель на байт, содержащий NAD, используемый ответным сообщением, при возврате.</span><span class="sxs-lookup"><span data-stu-id="d49f4-111">Pointer to the byte that contains the Nad used by the reply message, on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d49f4-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d49f4-112">Return value</span></span>

<span data-ttu-id="d49f4-113">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="d49f4-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="d49f4-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d49f4-114">Return code</span></span>                                                                                    | <span data-ttu-id="d49f4-115">Описание</span><span class="sxs-lookup"><span data-stu-id="d49f4-115">Description</span></span>                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="d49f4-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="d49f4-116"><dt>**S\_OK**</dt></span></span> </dl>           | <span data-ttu-id="d49f4-117">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="d49f4-117">Operation was completed successfully.</span></span><br/>                   |
| <dl> <span data-ttu-id="d49f4-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d49f4-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="d49f4-119">Недопустимый параметр *пбнад* .</span><span class="sxs-lookup"><span data-stu-id="d49f4-119">The *pbNad* parameter is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="d49f4-120"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="d49f4-120"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl> | <span data-ttu-id="d49f4-121">Внутренним вызовам не удалось получить сведения об NAD.</span><span class="sxs-lookup"><span data-stu-id="d49f4-121">Internal calls were unable to retrieve Nad information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d49f4-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d49f4-122">Remarks</span></span>

<span data-ttu-id="d49f4-123">Кроме приведенных выше кодов ошибок COM, этот метод может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="d49f4-123">In addition to the COM error codes listed above, this method may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="d49f4-124">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="d49f4-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d49f4-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="d49f4-125">Examples</span></span>

<span data-ttu-id="d49f4-126">В следующем примере показано, как получить адрес узла (NAD), используемый [*смарт-картой*](../secgloss/s-gly.md) в ответном сообщении.</span><span class="sxs-lookup"><span data-stu-id="d49f4-126">The following example shows how to retrieve the node address (Nad) used by the [*smart card*](../secgloss/s-gly.md) in the reply message.</span></span> <span data-ttu-id="d49f4-127">В примере предполагается, что Пискардкмд является допустимым указателем на экземпляр интерфейса [**искардкмд**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="d49f4-127">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE    byNad;
HRESULT hr;

// Get reply Nad.
hr = pISCardCmd->get_ReplyNad(&byNad);
if (FAILED(hr))
{
  printf("Failed get_ReplyNad\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="d49f4-128">Требования</span><span class="sxs-lookup"><span data-stu-id="d49f4-128">Requirements</span></span>



| <span data-ttu-id="d49f4-129">Требование</span><span class="sxs-lookup"><span data-stu-id="d49f4-129">Requirement</span></span> | <span data-ttu-id="d49f4-130">Значение</span><span class="sxs-lookup"><span data-stu-id="d49f4-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d49f4-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d49f4-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d49f4-132">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d49f4-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d49f4-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d49f4-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d49f4-134">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d49f4-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d49f4-135">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d49f4-135">End of client support</span></span><br/>    | <span data-ttu-id="d49f4-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d49f4-136">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="d49f4-137">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="d49f4-137">End of server support</span></span><br/>    | <span data-ttu-id="d49f4-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d49f4-138">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="d49f4-139">Header</span><span class="sxs-lookup"><span data-stu-id="d49f4-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="d49f4-140"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="d49f4-140"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="d49f4-141">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d49f4-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="d49f4-142"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d49f4-142"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d49f4-143">DLL</span><span class="sxs-lookup"><span data-stu-id="d49f4-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d49f4-144"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d49f4-144"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d49f4-145">IID</span><span class="sxs-lookup"><span data-stu-id="d49f4-145">IID</span></span><br/>                      | <span data-ttu-id="d49f4-146">IID \_ искардкмд определен как D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="d49f4-146">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="d49f4-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d49f4-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d49f4-148">**искардкмд**</span><span class="sxs-lookup"><span data-stu-id="d49f4-148">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
