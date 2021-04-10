---
description: Извлекает байт идентификатора инструкции из блока данных протокола приложения (КАТЕГОРИЯХ APDU).
ms.assetid: 294f51cd-0a13-4dfb-bf02-9edd11a7085e
title: 'Метод Искардкмд:: get_InstructionId (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_InstructionId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4b0125237ef94a5d6173f517483b9ae8781d5607
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999581"
---
# <a name="iscardcmdget_instructionid-method"></a><span data-ttu-id="9d56f-103">Метод Искардкмд:: Get \_ инструктионид</span><span class="sxs-lookup"><span data-stu-id="9d56f-103">ISCardCmd::get\_InstructionId method</span></span>

<span data-ttu-id="9d56f-104">\[Метод **Get \_ инструктионид** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="9d56f-104">\[The **get\_InstructionId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9d56f-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="9d56f-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9d56f-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="9d56f-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="9d56f-107">Метод **Get \_ инструктионид** извлекает байт идентификатора инструкции из [*блока данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).</span><span class="sxs-lookup"><span data-stu-id="9d56f-107">The **get\_InstructionId** method retrieves the instruction identifier byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="9d56f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d56f-108">Syntax</span></span>


```C++
HRESULT get_InstructionId(
  [out] BYTE *pbyIns
);
```



## <a name="parameters"></a><span data-ttu-id="9d56f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9d56f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d56f-110">*пбинс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9d56f-110">*pbyIns* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d56f-111">Указатель на байт, который является ИДЕНТИФИКАТОРом инструкции из КАТЕГОРИЯХ APDU при возврате.</span><span class="sxs-lookup"><span data-stu-id="9d56f-111">Pointer to the byte that is the instruction ID from the APDU on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d56f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9d56f-112">Return value</span></span>

<span data-ttu-id="9d56f-113">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="9d56f-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="9d56f-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9d56f-114">Return code</span></span>                                                                                   | <span data-ttu-id="9d56f-115">Описание</span><span class="sxs-lookup"><span data-stu-id="9d56f-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="9d56f-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="9d56f-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9d56f-117">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="9d56f-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="9d56f-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9d56f-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="9d56f-119">Недопустимый параметр *пбинс* .</span><span class="sxs-lookup"><span data-stu-id="9d56f-119">The *pbyIns* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="9d56f-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="9d56f-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="9d56f-121">В *пбинс* был передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="9d56f-121">A bad pointer was passed in *pbyIns*.</span></span><br/> |
| <dl> <span data-ttu-id="9d56f-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="9d56f-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9d56f-123">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="9d56f-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="9d56f-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9d56f-124">Remarks</span></span>

<span data-ttu-id="9d56f-125">Чтобы задать новое значение для идентификатора инструкции, вызовите метод [**\_ инструктионид**](iscardcmd-put-instructionid.md).</span><span class="sxs-lookup"><span data-stu-id="9d56f-125">To set the instructional identifier to a new value, call [**put\_InstructionId**](iscardcmd-put-instructionid.md).</span></span>

<span data-ttu-id="9d56f-126">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардкмд**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="9d56f-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="9d56f-127">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="9d56f-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="9d56f-128">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="9d56f-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9d56f-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="9d56f-129">Examples</span></span>

<span data-ttu-id="9d56f-130">В следующем примере показано, как получить байт идентификатора инструкции из [*блока данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).</span><span class="sxs-lookup"><span data-stu-id="9d56f-130">The following example shows how to retrieve the instruction identifier byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="9d56f-131">В примере предполагается, что Пискардкмд является допустимым указателем на экземпляр интерфейса [**искардкмд**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="9d56f-131">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE  byInstructID;
HRESULT hr;

// Retrieve the instruction ID.
hr = pISCardCmd->get_InstructionId(&byInstructID);
if (FAILED(hr))
{
  printf("Failed get_InstructionId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="9d56f-132">Требования</span><span class="sxs-lookup"><span data-stu-id="9d56f-132">Requirements</span></span>



| <span data-ttu-id="9d56f-133">Требование</span><span class="sxs-lookup"><span data-stu-id="9d56f-133">Requirement</span></span> | <span data-ttu-id="9d56f-134">Значение</span><span class="sxs-lookup"><span data-stu-id="9d56f-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d56f-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9d56f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9d56f-136">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9d56f-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9d56f-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9d56f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9d56f-138">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9d56f-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9d56f-139">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="9d56f-139">End of client support</span></span><br/>    | <span data-ttu-id="9d56f-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9d56f-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="9d56f-141">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="9d56f-141">End of server support</span></span><br/>    | <span data-ttu-id="9d56f-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9d56f-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="9d56f-143">Header</span><span class="sxs-lookup"><span data-stu-id="9d56f-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d56f-144"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d56f-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="9d56f-145">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="9d56f-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="9d56f-146"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9d56f-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9d56f-147">DLL</span><span class="sxs-lookup"><span data-stu-id="9d56f-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d56f-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d56f-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9d56f-149">IID</span><span class="sxs-lookup"><span data-stu-id="9d56f-149">IID</span></span><br/>                      | <span data-ttu-id="9d56f-150">IID \_ искардкмд определен как D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="9d56f-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="9d56f-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9d56f-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d56f-152">**искардкмд**</span><span class="sxs-lookup"><span data-stu-id="9d56f-152">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="9d56f-153">**разместить \_ инструктионид**</span><span class="sxs-lookup"><span data-stu-id="9d56f-153">**put\_InstructionId**</span></span>](iscardcmd-put-instructionid.md)
</dt> </dl>

 

 
