---
description: Задает байт второго параметра (P2) в блоке данных протокола приложения (КАТЕГОРИЯХ APDU).
ms.assetid: 8d11b967-33cd-4bfa-b294-cc0c422cf6cf
title: 'Искардкмд: метод ut_P2:p (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_P2
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 362da530dece37a0a0ca600b1edb414d29e1bd48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262886"
---
# <a name="iscardcmdput_p2-method"></a><span data-ttu-id="5386d-103">Искардкмд::p \_ метод UT P2</span><span class="sxs-lookup"><span data-stu-id="5386d-103">ISCardCmd::put\_P2 method</span></span>

<span data-ttu-id="5386d-104">\[Метод **размещения \_ P2** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="5386d-104">\[The **put\_P2** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5386d-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="5386d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5386d-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="5386d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="5386d-107">Метод **размещения \_ P2** задает байт второго параметра (P2) в [*блоке данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).</span><span class="sxs-lookup"><span data-stu-id="5386d-107">The **put\_P2** method sets the second parameter (P2) byte in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="5386d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5386d-108">Syntax</span></span>


```C++
HRESULT put_P2(
  [in] BYTE byP2
);
```



## <a name="parameters"></a><span data-ttu-id="5386d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5386d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5386d-110">*byP2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5386d-110">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5386d-111">Байт, который является полем P2.</span><span class="sxs-lookup"><span data-stu-id="5386d-111">The byte that is the P2 field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5386d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5386d-112">Return value</span></span>

<span data-ttu-id="5386d-113">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="5386d-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="5386d-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5386d-114">Return code</span></span>                                                                                   | <span data-ttu-id="5386d-115">Описание</span><span class="sxs-lookup"><span data-stu-id="5386d-115">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="5386d-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5386d-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5386d-117">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="5386d-117">Operation completed successfully.</span></span><br/>  |
| <dl> <span data-ttu-id="5386d-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5386d-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="5386d-119">Недопустимый параметр *byP2* .</span><span class="sxs-lookup"><span data-stu-id="5386d-119">The *byP2* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="5386d-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5386d-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="5386d-121">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="5386d-121">Out of memory.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="5386d-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5386d-122">Remarks</span></span>

<span data-ttu-id="5386d-123">Чтобы задать значение P1 объекта КАТЕГОРИЯХ APDU, вызовите метод [**Set \_ P1**](iscardcmd-put-p1.md).</span><span class="sxs-lookup"><span data-stu-id="5386d-123">To set the P1 value of the APDU, call [**put\_P1**](iscardcmd-put-p1.md).</span></span>

<span data-ttu-id="5386d-124">Чтобы получить существующие значения P1, P2 и P3, вызовите [**Get \_ P1**](iscardcmd-get-p1.md), [**Get \_ P2**](iscardcmd-get-p2.md) или [**Get \_ P3**](iscardcmd-get-p3.md) соответственно.</span><span class="sxs-lookup"><span data-stu-id="5386d-124">To retrieve the existing P1, P2, and P3 values, call [**get\_P1**](iscardcmd-get-p1.md), [**get\_P2**](iscardcmd-get-p2.md) or [**get\_P3**](iscardcmd-get-p3.md) respectively.</span></span>

<span data-ttu-id="5386d-125">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардкмд**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="5386d-125">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="5386d-126">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="5386d-126">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="5386d-127">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="5386d-127">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5386d-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="5386d-128">Examples</span></span>

<span data-ttu-id="5386d-129">В следующем примере показано, как задать байт второго параметра (P2) для [*единицы данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).</span><span class="sxs-lookup"><span data-stu-id="5386d-129">The following example shows how to set the second parameter (P2) byte of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="5386d-130">В примере предполагается, что Пискардкмд является допустимым указателем на экземпляр интерфейса [**искардкмд**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="5386d-130">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT  hr;

// Set the P2 byte.
hr = pISCardCmd->put_P2(0x06);
if (FAILED(hr))
{
  printf("Failed put_P2\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="5386d-131">Требования</span><span class="sxs-lookup"><span data-stu-id="5386d-131">Requirements</span></span>



| <span data-ttu-id="5386d-132">Требование</span><span class="sxs-lookup"><span data-stu-id="5386d-132">Requirement</span></span> | <span data-ttu-id="5386d-133">Значение</span><span class="sxs-lookup"><span data-stu-id="5386d-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5386d-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5386d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5386d-135">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5386d-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5386d-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5386d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5386d-137">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5386d-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5386d-138">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="5386d-138">End of client support</span></span><br/>    | <span data-ttu-id="5386d-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5386d-139">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="5386d-140">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="5386d-140">End of server support</span></span><br/>    | <span data-ttu-id="5386d-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5386d-141">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="5386d-142">Header</span><span class="sxs-lookup"><span data-stu-id="5386d-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="5386d-143"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="5386d-143"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="5386d-144">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="5386d-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="5386d-145"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5386d-145"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5386d-146">DLL</span><span class="sxs-lookup"><span data-stu-id="5386d-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5386d-147"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5386d-147"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5386d-148">IID</span><span class="sxs-lookup"><span data-stu-id="5386d-148">IID</span></span><br/>                      | <span data-ttu-id="5386d-149">IID \_ искардкмд определен как D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="5386d-149">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="5386d-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5386d-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5386d-151">**получить \_ P1**</span><span class="sxs-lookup"><span data-stu-id="5386d-151">**get\_P1**</span></span>](iscardcmd-get-p1.md)
</dt> <dt>

[<span data-ttu-id="5386d-152">**получить \_ P2**</span><span class="sxs-lookup"><span data-stu-id="5386d-152">**get\_P2**</span></span>](iscardcmd-get-p2.md)
</dt> <dt>

[<span data-ttu-id="5386d-153">**получение \_ P3**</span><span class="sxs-lookup"><span data-stu-id="5386d-153">**get\_P3**</span></span>](iscardcmd-get-p3.md)
</dt> <dt>

[<span data-ttu-id="5386d-154">**искардкмд**</span><span class="sxs-lookup"><span data-stu-id="5386d-154">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="5386d-155">**разместить \_ P1**</span><span class="sxs-lookup"><span data-stu-id="5386d-155">**put\_P1**</span></span>](iscardcmd-put-p1.md)
</dt> </dl>

 

 
