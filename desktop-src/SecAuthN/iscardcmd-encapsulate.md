---
description: Метод инкапсуляции инкапсулирует заданную единицу данных протокола приложения командной строки (КАТЕГОРИЯХ APDU) в другую команду КАТЕГОРИЯХ APDU для передачи на смарт-карту.
ms.assetid: dfffad09-046b-46cb-b6fd-286a4bbf1066
title: 'Метод Искардкмд:: инкапсулировать (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.Encapsulate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: cd671a11edd9977695eeaf858e38f962b3dd0962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651030"
---
# <a name="iscardcmdencapsulate-method"></a><span data-ttu-id="d52bb-103">Метод Искардкмд:: инкапсулировать</span><span class="sxs-lookup"><span data-stu-id="d52bb-103">ISCardCmd::Encapsulate method</span></span>

<span data-ttu-id="d52bb-104">\[Метод **инкапсуляции** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="d52bb-104">\[The **Encapsulate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d52bb-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d52bb-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d52bb-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="d52bb-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d52bb-107">Метод **инкапсуляции** инкапсулирует заданную [*единицу данных протокола приложения*](../secgloss/a-gly.md) командной строки (категориях APDU) в другую команду категориях APDU для передачи на [*смарт-карту*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d52bb-107">The **Encapsulate** method encapsulates the given command [*application protocol data unit*](../secgloss/a-gly.md) (APDU) into another command APDU for transmission to a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d52bb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d52bb-108">Syntax</span></span>


```C++
HRESULT Encapsulate(
  [in] LPBYTEBUFFER  pApdu,
  [in] ISO_APDU_TYPE ApduType
);
```



## <a name="parameters"></a><span data-ttu-id="d52bb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d52bb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d52bb-110">*папду* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d52bb-110">*pApdu* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d52bb-111">Указатель на КАТЕГОРИЯХ APDU, который необходимо инкапсулировать.</span><span class="sxs-lookup"><span data-stu-id="d52bb-111">Pointer to the APDU to be encapsulated.</span></span>

</dd> <dt>

<span data-ttu-id="d52bb-112">*Апдутипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d52bb-112">*ApduType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d52bb-113">ISO 7816-4. вариант [*T = 0*](../secgloss/t-gly.md) передач.</span><span class="sxs-lookup"><span data-stu-id="d52bb-113">ISO 7816-4 case for [*T=0*](../secgloss/t-gly.md) transmissions.</span></span>

<dl><span id="ISO_CASE_1"></span><span id="iso_case_1"></span><dt>

<span data-ttu-id="d52bb-114">**ISO- \_ регистр \_ 1**</span><span class="sxs-lookup"><span data-stu-id="d52bb-114">**ISO\_CASE\_1**</span></span>
</dt><span id="ISO_CASE_2"></span><span id="iso_case_2"></span><dt>

<span data-ttu-id="d52bb-115">**ISO- \_ регистр \_ 2**</span><span class="sxs-lookup"><span data-stu-id="d52bb-115">**ISO\_CASE\_2**</span></span>
</dt><span id="ISO_CASE_3"></span><span id="iso_case_3"></span><dt>

<span data-ttu-id="d52bb-116">**\_Сценарий ISO \_ 3**</span><span class="sxs-lookup"><span data-stu-id="d52bb-116">**ISO\_CASE\_3**</span></span>
</dt><span id="ISO_CASE_4"></span><span id="iso_case_4"></span><dt>

<span data-ttu-id="d52bb-117">**ISO- \_ регистр \_ 4**</span><span class="sxs-lookup"><span data-stu-id="d52bb-117">**ISO\_CASE\_4**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d52bb-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d52bb-118">Return value</span></span>

<span data-ttu-id="d52bb-119">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="d52bb-119">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="d52bb-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d52bb-120">Return code</span></span>                                                                                   | <span data-ttu-id="d52bb-121">Описание</span><span class="sxs-lookup"><span data-stu-id="d52bb-121">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="d52bb-122"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="d52bb-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d52bb-123">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="d52bb-123">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="d52bb-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d52bb-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d52bb-125">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="d52bb-125">Invalid parameter.</span></span><br/>                   |
| <dl> <span data-ttu-id="d52bb-126"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="d52bb-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d52bb-127">В *папду* был передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="d52bb-127">A bad pointer was passed in *pApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="d52bb-128"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d52bb-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d52bb-129">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="d52bb-129">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="d52bb-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d52bb-130">Remarks</span></span>

<span data-ttu-id="d52bb-131">Чтобы создать команду КАТЕГОРИЯХ APDU, вызовите [**буилдкмд**](iscardcmd-buildcmd.md).</span><span class="sxs-lookup"><span data-stu-id="d52bb-131">To build a command APDU, call [**BuildCmd**](iscardcmd-buildcmd.md).</span></span>

<span data-ttu-id="d52bb-132">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардкмд**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="d52bb-132">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="d52bb-133">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="d52bb-133">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="d52bb-134">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="d52bb-134">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d52bb-135">Примеры</span><span class="sxs-lookup"><span data-stu-id="d52bb-135">Examples</span></span>

<span data-ttu-id="d52bb-136">В следующем примере показано, как инкапсулировать команду КАТЕГОРИЯХ APDU.</span><span class="sxs-lookup"><span data-stu-id="d52bb-136">The following example shows how to encapsulate a command APDU.</span></span> <span data-ttu-id="d52bb-137">В примере предполагается, что Пибитеапду является допустимым указателем на экземпляр интерфейса [**ибитебуффер**](ibytebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="d52bb-137">The example assumes that pIByteApdu is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface.</span></span>


```C++
HRESULT    hr;

// pIByteApdu is a pointer to an instance of IByteBuffer.
// Encapsulate the APDU.
hr = pISCardCmd->Encapsulate(pIByteApdu, ISO_CASE_1);
if (FAILED(hr)) 
{
    printf("Failed Encapsulate.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="d52bb-138">Требования</span><span class="sxs-lookup"><span data-stu-id="d52bb-138">Requirements</span></span>



| <span data-ttu-id="d52bb-139">Требование</span><span class="sxs-lookup"><span data-stu-id="d52bb-139">Requirement</span></span> | <span data-ttu-id="d52bb-140">Значение</span><span class="sxs-lookup"><span data-stu-id="d52bb-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d52bb-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d52bb-141">Minimum supported client</span></span><br/> | <span data-ttu-id="d52bb-142">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d52bb-142">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d52bb-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d52bb-143">Minimum supported server</span></span><br/> | <span data-ttu-id="d52bb-144">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d52bb-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d52bb-145">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d52bb-145">End of client support</span></span><br/>    | <span data-ttu-id="d52bb-146">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d52bb-146">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="d52bb-147">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="d52bb-147">End of server support</span></span><br/>    | <span data-ttu-id="d52bb-148">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d52bb-148">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="d52bb-149">Header</span><span class="sxs-lookup"><span data-stu-id="d52bb-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="d52bb-150"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="d52bb-150"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="d52bb-151">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d52bb-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="d52bb-152"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d52bb-152"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d52bb-153">DLL</span><span class="sxs-lookup"><span data-stu-id="d52bb-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d52bb-154"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d52bb-154"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d52bb-155">IID</span><span class="sxs-lookup"><span data-stu-id="d52bb-155">IID</span></span><br/>                      | <span data-ttu-id="d52bb-156">IID \_ искардкмд определен как D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="d52bb-156">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="d52bb-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d52bb-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d52bb-158">**буилдкмд**</span><span class="sxs-lookup"><span data-stu-id="d52bb-158">**BuildCmd**</span></span>](iscardcmd-buildcmd.md)
</dt> <dt>

[<span data-ttu-id="d52bb-159">**искардкмд**</span><span class="sxs-lookup"><span data-stu-id="d52bb-159">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
