---
description: Задает новый идентификатор класса в блоке данных протокола приложения (КАТЕГОРИЯХ APDU).
ms.assetid: 7e7d42f2-2858-4b37-a7d5-a919e3e005da
title: 'Искардкмд: метод ut_ClassId:p (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_ClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ed4b1f273ebe9ea0a5e105ec3d88fc8446f7a831
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991359"
---
# <a name="iscardcmdput_classid-method"></a><span data-ttu-id="03d05-103">Искардкмд::p \_ метод UT ClassID</span><span class="sxs-lookup"><span data-stu-id="03d05-103">ISCardCmd::put\_ClassId method</span></span>

<span data-ttu-id="03d05-104">\[Метод **размещения \_ ClassID** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="03d05-104">\[The **put\_ClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="03d05-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="03d05-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="03d05-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="03d05-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="03d05-107">Метод **размещения \_ ClassID** задает новый идентификатор класса в [*блоке данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).</span><span class="sxs-lookup"><span data-stu-id="03d05-107">The **put\_ClassId** method sets a new class identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="03d05-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03d05-108">Syntax</span></span>


```C++
HRESULT put_ClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a><span data-ttu-id="03d05-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="03d05-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03d05-110">*бикласс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="03d05-110">*byClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03d05-111">Байт, представляющий идентификатор класса.</span><span class="sxs-lookup"><span data-stu-id="03d05-111">The byte that represents the class identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03d05-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="03d05-112">Return value</span></span>

<span data-ttu-id="03d05-113">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="03d05-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="03d05-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="03d05-114">Return code</span></span>                                                                                   | <span data-ttu-id="03d05-115">Описание</span><span class="sxs-lookup"><span data-stu-id="03d05-115">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="03d05-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="03d05-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="03d05-117">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="03d05-117">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="03d05-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="03d05-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="03d05-119">Недопустимый *бикласс* .</span><span class="sxs-lookup"><span data-stu-id="03d05-119">The *byClass* is not valid.</span></span><br/>       |
| <dl> <span data-ttu-id="03d05-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="03d05-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="03d05-121">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="03d05-121">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="03d05-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="03d05-122">Remarks</span></span>

<span data-ttu-id="03d05-123">Чтобы получить текущий идентификатор класса, вызовите [**Get \_ ClassID**](iscardcmd-get-classid.md).</span><span class="sxs-lookup"><span data-stu-id="03d05-123">To retrieve the current class identifier, call [**get\_ClassId**](iscardcmd-get-classid.md).</span></span>

<span data-ttu-id="03d05-124">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардкмд**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="03d05-124">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="03d05-125">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="03d05-125">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="03d05-126">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="03d05-126">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="03d05-127">Примеры</span><span class="sxs-lookup"><span data-stu-id="03d05-127">Examples</span></span>

<span data-ttu-id="03d05-128">В следующем примере показано, как задать новый идентификатор класса в [*блоке данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).</span><span class="sxs-lookup"><span data-stu-id="03d05-128">The following example shows how to set a new class identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="03d05-129">В примере предполагается, что Пискардкмд является допустимым указателем на экземпляр интерфейса [**искардкмд**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="03d05-129">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT  hr;

// Set the class ID.
hr = pISCardCmd->put_ClassId(0xC0);
if (FAILED(hr))
{
  printf("Failed put_ClassId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="03d05-130">Требования</span><span class="sxs-lookup"><span data-stu-id="03d05-130">Requirements</span></span>



| <span data-ttu-id="03d05-131">Требование</span><span class="sxs-lookup"><span data-stu-id="03d05-131">Requirement</span></span> | <span data-ttu-id="03d05-132">Значение</span><span class="sxs-lookup"><span data-stu-id="03d05-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03d05-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="03d05-133">Minimum supported client</span></span><br/> | <span data-ttu-id="03d05-134">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="03d05-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="03d05-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="03d05-135">Minimum supported server</span></span><br/> | <span data-ttu-id="03d05-136">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="03d05-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="03d05-137">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="03d05-137">End of client support</span></span><br/>    | <span data-ttu-id="03d05-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="03d05-138">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="03d05-139">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="03d05-139">End of server support</span></span><br/>    | <span data-ttu-id="03d05-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="03d05-140">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="03d05-141">Header</span><span class="sxs-lookup"><span data-stu-id="03d05-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="03d05-142"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="03d05-142"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="03d05-143">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="03d05-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="03d05-144"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="03d05-144"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="03d05-145">DLL</span><span class="sxs-lookup"><span data-stu-id="03d05-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03d05-146"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03d05-146"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="03d05-147">IID</span><span class="sxs-lookup"><span data-stu-id="03d05-147">IID</span></span><br/>                      | <span data-ttu-id="03d05-148">IID \_ искардкмд определен как D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="03d05-148">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="03d05-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="03d05-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03d05-150">**получение \_ ClassID**</span><span class="sxs-lookup"><span data-stu-id="03d05-150">**get\_ClassId**</span></span>](iscardcmd-get-classid.md)
</dt> <dt>

[<span data-ttu-id="03d05-151">**искардкмд**</span><span class="sxs-lookup"><span data-stu-id="03d05-151">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
