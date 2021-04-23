---
description: Извлекает байт состояния ответа Апдус SW1.
ms.assetid: 5f74d0c9-cf82-4694-bca6-a2655e717a1f
title: 'Метод Искардкмд:: get_ReplyStatusSW1 (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyStatusSW1
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 92bcf490a3cb1fc533bcf9a1046642d3c3e55b59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541826"
---
# <a name="iscardcmdget_replystatussw1-method"></a><span data-ttu-id="a4343-103">Метод Искардкмд:: Get \_ ReplyStatusSW1</span><span class="sxs-lookup"><span data-stu-id="a4343-103">ISCardCmd::get\_ReplyStatusSW1 method</span></span>

<span data-ttu-id="a4343-104">\[Метод **Get \_ ReplyStatusSW1** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="a4343-104">\[The **get\_ReplyStatusSW1** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a4343-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="a4343-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a4343-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="a4343-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="a4343-107">Метод **Get \_ ReplyStatusSW1** извлекает байт состояния SW1 [*ответа апдус*](../secgloss/r-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="a4343-107">The **get\_ReplyStatusSW1** method retrieves the [*reply APDUs*](../secgloss/r-gly.md) SW1 status byte.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4343-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4343-108">Syntax</span></span>


```C++
HRESULT get_ReplyStatusSW1(
  [out] LPBYTE pbySW1
);
```



## <a name="parameters"></a><span data-ttu-id="a4343-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4343-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4343-110">*pbySW1* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a4343-110">*pbySW1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4343-111">Указатель на байт, который содержит значение SW1 байта при возврате.</span><span class="sxs-lookup"><span data-stu-id="a4343-111">Pointer to the byte that contains the value of the SW1 byte on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4343-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a4343-112">Return value</span></span>

<span data-ttu-id="a4343-113">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="a4343-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="a4343-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a4343-114">Return code</span></span>                                                                                   | <span data-ttu-id="a4343-115">Описание</span><span class="sxs-lookup"><span data-stu-id="a4343-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="a4343-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a4343-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a4343-117">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="a4343-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="a4343-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a4343-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a4343-119">Недопустимый параметр *pbySW1* .</span><span class="sxs-lookup"><span data-stu-id="a4343-119">The *pbySW1* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="a4343-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="a4343-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a4343-121">В *pbySW1* был передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="a4343-121">A bad pointer was passed in *pbySW1*.</span></span><br/> |
| <dl> <span data-ttu-id="a4343-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a4343-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a4343-123">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="a4343-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="a4343-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a4343-124">Remarks</span></span>

<span data-ttu-id="a4343-125">Байт состояния SW1 для [*ответа категориях APDU*](../secgloss/r-gly.md) доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a4343-125">The [*reply APDU's*](../secgloss/r-gly.md) SW1 status byte is read-only.</span></span>

<span data-ttu-id="a4343-126">Чтобы получить байт состояния SW2 для ответа КАТЕГОРИЯХ APDU, вызовите [**Get \_ ReplyStatusSW2**](iscardcmd-get-replystatussw2.md).</span><span class="sxs-lookup"><span data-stu-id="a4343-126">To retrieve the reply APDU's SW2 status byte, call [**get\_ReplyStatusSW2**](iscardcmd-get-replystatussw2.md).</span></span>

<span data-ttu-id="a4343-127">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардкмд**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="a4343-127">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="a4343-128">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="a4343-128">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="a4343-129">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="a4343-129">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a4343-130">Примеры</span><span class="sxs-lookup"><span data-stu-id="a4343-130">Examples</span></span>

<span data-ttu-id="a4343-131">В следующем примере показано, как получить байт состояния SW1 для [*ответа категориях APDU*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a4343-131">The following example shows how to retrieve the SW1 status byte of the [*reply APDU*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="a4343-132">В примере предполагается, что Пискардкмд является допустимым указателем на экземпляр интерфейса [**искардкмд**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="a4343-132">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE     bySW1;
HRESULT  hr;

// Retrieve the reply status SW1 byte.
hr = pISCardCmd->get_ReplyStatusSW1(&bySW1);
if (FAILED(hr))
{
  printf("Failed get_ReplyStatusSW1\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="a4343-133">Требования</span><span class="sxs-lookup"><span data-stu-id="a4343-133">Requirements</span></span>



| <span data-ttu-id="a4343-134">Требование</span><span class="sxs-lookup"><span data-stu-id="a4343-134">Requirement</span></span> | <span data-ttu-id="a4343-135">Значение</span><span class="sxs-lookup"><span data-stu-id="a4343-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4343-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a4343-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a4343-137">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a4343-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a4343-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a4343-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a4343-139">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a4343-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a4343-140">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="a4343-140">End of client support</span></span><br/>    | <span data-ttu-id="a4343-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a4343-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="a4343-142">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="a4343-142">End of server support</span></span><br/>    | <span data-ttu-id="a4343-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a4343-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="a4343-144">Header</span><span class="sxs-lookup"><span data-stu-id="a4343-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4343-145"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4343-145"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="a4343-146">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="a4343-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="a4343-147"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a4343-147"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a4343-148">DLL</span><span class="sxs-lookup"><span data-stu-id="a4343-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4343-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4343-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a4343-150">IID</span><span class="sxs-lookup"><span data-stu-id="a4343-150">IID</span></span><br/>                      | <span data-ttu-id="a4343-151">IID \_ искардкмд определен как D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="a4343-151">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="a4343-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4343-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4343-153">**получить \_ ReplyStatusSW2**</span><span class="sxs-lookup"><span data-stu-id="a4343-153">**get\_ReplyStatusSW2**</span></span>](iscardcmd-get-replystatussw2.md)
</dt> <dt>

[<span data-ttu-id="a4343-154">**получить \_ реплистатус**</span><span class="sxs-lookup"><span data-stu-id="a4343-154">**get\_ReplyStatus**</span></span>](iscardcmd-get-replystatus.md)
</dt> <dt>

[<span data-ttu-id="a4343-155">**искардкмд**</span><span class="sxs-lookup"><span data-stu-id="a4343-155">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
