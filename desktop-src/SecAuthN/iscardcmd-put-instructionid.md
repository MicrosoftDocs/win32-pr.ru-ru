---
description: Задает заданный идентификатор инструкции в блоке данных протокола приложения (КАТЕГОРИЯХ APDU).
ms.assetid: ea527ffd-b053-467d-883d-b93d5bbfb071
title: 'Искардкмд: метод ut_InstructionId:p (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_InstructionId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6194accfb834152cf07a58fbb8036b13d3fdcd5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991358"
---
# <a name="iscardcmdput_instructionid-method"></a><span data-ttu-id="d6dcb-103">Искардкмд::p UT \_ инструктионид метод</span><span class="sxs-lookup"><span data-stu-id="d6dcb-103">ISCardCmd::put\_InstructionId method</span></span>

<span data-ttu-id="d6dcb-104">\[Метод **размещения \_ инструктионид** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="d6dcb-104">\[The **put\_InstructionId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d6dcb-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d6dcb-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d6dcb-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="d6dcb-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d6dcb-107">Метод **размещения \_ инструктионид** задает заданный идентификатор инструкции в [*блоке данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).</span><span class="sxs-lookup"><span data-stu-id="d6dcb-107">The **put\_InstructionId** method sets the given instruction identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="d6dcb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d6dcb-108">Syntax</span></span>


```C++
HRESULT put_InstructionId(
  [in] BYTE byIns
);
```



## <a name="parameters"></a><span data-ttu-id="d6dcb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d6dcb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6dcb-110">*Бинс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6dcb-110">*byIns* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6dcb-111">Байт, который является идентификатором инструкции.</span><span class="sxs-lookup"><span data-stu-id="d6dcb-111">The byte that is the instruction identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6dcb-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6dcb-112">Return value</span></span>

<span data-ttu-id="d6dcb-113">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="d6dcb-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="d6dcb-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d6dcb-114">Return code</span></span>                                                                                   | <span data-ttu-id="d6dcb-115">Описание</span><span class="sxs-lookup"><span data-stu-id="d6dcb-115">Description</span></span>                                    |
|-----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="d6dcb-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="d6dcb-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d6dcb-117">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="d6dcb-117">Operation completed successfully.</span></span><br/>   |
| <dl> <span data-ttu-id="d6dcb-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d6dcb-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d6dcb-119">Недопустимый параметр *Бинс* .</span><span class="sxs-lookup"><span data-stu-id="d6dcb-119">The *byIns* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="d6dcb-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d6dcb-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d6dcb-121">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="d6dcb-121">Out of memory.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="d6dcb-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d6dcb-122">Remarks</span></span>

<span data-ttu-id="d6dcb-123">Чтобы получить существующий идентификатор инструкции, вызовите [**Get \_ инструктионид**](iscardcmd-get-instructionid.md).</span><span class="sxs-lookup"><span data-stu-id="d6dcb-123">To get the existing instructional identifier, call [**get\_InstructionId**](iscardcmd-get-instructionid.md).</span></span>

<span data-ttu-id="d6dcb-124">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардкмд**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="d6dcb-124">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="d6dcb-125">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="d6dcb-125">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="d6dcb-126">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="d6dcb-126">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d6dcb-127">Примеры</span><span class="sxs-lookup"><span data-stu-id="d6dcb-127">Examples</span></span>

<span data-ttu-id="d6dcb-128">В следующем примере показано, как задать идентификатор инструкции в [*блоке данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).</span><span class="sxs-lookup"><span data-stu-id="d6dcb-128">The following example shows how to set an instruction identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="d6dcb-129">В примере предполагается, что Пискардкмд является допустимым указателем на экземпляр интерфейса [**искардкмд**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="d6dcb-129">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT hr;

// Set the instruction ID.
hr = pISCardCmd->put_InstructionId(0xb2);
if (FAILED(hr))
{
  printf("Failed put_InstructionId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="d6dcb-130">Требования</span><span class="sxs-lookup"><span data-stu-id="d6dcb-130">Requirements</span></span>



| <span data-ttu-id="d6dcb-131">Требование</span><span class="sxs-lookup"><span data-stu-id="d6dcb-131">Requirement</span></span> | <span data-ttu-id="d6dcb-132">Значение</span><span class="sxs-lookup"><span data-stu-id="d6dcb-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6dcb-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d6dcb-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d6dcb-134">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d6dcb-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d6dcb-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d6dcb-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d6dcb-136">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d6dcb-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d6dcb-137">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d6dcb-137">End of client support</span></span><br/>    | <span data-ttu-id="d6dcb-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d6dcb-138">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="d6dcb-139">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="d6dcb-139">End of server support</span></span><br/>    | <span data-ttu-id="d6dcb-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d6dcb-140">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="d6dcb-141">Header</span><span class="sxs-lookup"><span data-stu-id="d6dcb-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6dcb-142"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6dcb-142"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="d6dcb-143">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d6dcb-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="d6dcb-144"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d6dcb-144"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d6dcb-145">DLL</span><span class="sxs-lookup"><span data-stu-id="d6dcb-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6dcb-146"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6dcb-146"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d6dcb-147">IID</span><span class="sxs-lookup"><span data-stu-id="d6dcb-147">IID</span></span><br/>                      | <span data-ttu-id="d6dcb-148">IID \_ искардкмд определен как D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="d6dcb-148">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="d6dcb-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d6dcb-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6dcb-150">**получить \_ инструктионид**</span><span class="sxs-lookup"><span data-stu-id="d6dcb-150">**get\_InstructionId**</span></span>](iscardcmd-get-instructionid.md)
</dt> <dt>

[<span data-ttu-id="d6dcb-151">**искардкмд**</span><span class="sxs-lookup"><span data-stu-id="d6dcb-151">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
