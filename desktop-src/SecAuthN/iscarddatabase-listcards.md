---
description: Метод Листкардс извлекает все имена смарт-карт, соответствующие указанным идентификаторам интерфейса (GUID), указанную строку ATR или и то, и другое.
ms.assetid: a1cf8186-0746-4c4d-917d-40d6c3542036
title: 'Метод Искарддатабасе:: Листкардс (Скардмгр. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListCards
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e8a5bf56aa27a044d29e2e0153698bfefe69e1d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809911"
---
# <a name="iscarddatabaselistcards-method"></a><span data-ttu-id="4ed1b-103">Метод Искарддатабасе:: Листкардс</span><span class="sxs-lookup"><span data-stu-id="4ed1b-103">ISCardDatabase::ListCards method</span></span>

<span data-ttu-id="4ed1b-104">\[Метод **листкардс** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-104">\[The **ListCards** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4ed1b-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4ed1b-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="4ed1b-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="4ed1b-107">Метод **листкардс** извлекает все имена смарт-карт, соответствующие указанным идентификаторам интерфейса (GUID), указанную [*строку ATR*](../secgloss/a-gly.md)или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-107">The **ListCards** method retrieves all of the smart card names that match the specified interface identifiers (GUIDs), the specified [*ATR string*](../secgloss/a-gly.md), or both.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ed1b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4ed1b-108">Syntax</span></span>


```C++
HRESULT ListCards(
  [in]  LPBYTEBUFFER pAtr,
  [in]  LPSAFEARRAY  pInterfaceGuids,
  [in]  LONG         localeId,
  [out] LPSAFEARRAY  *ppCardNames
);
```



## <a name="parameters"></a><span data-ttu-id="4ed1b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4ed1b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ed1b-110">*Патр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4ed1b-110">*pAtr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ed1b-111">Указатель на строку ATR [*смарт-карты*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="4ed1b-111">Pointer to a [*smart card*](../secgloss/s-gly.md) ATR string.</span></span> <span data-ttu-id="4ed1b-112">Строка ATR должна быть упакована в [**ибитебуффер**](ibytebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="4ed1b-112">The ATR string must be packaged into an [**IByteBuffer**](ibytebuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ed1b-113">*пинтерфацегуидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4ed1b-113">*pInterfaceGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ed1b-114">Указатель на массив SAFEARRAY идентификаторов COM-интерфейса (GUID) в формате BSTR.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-114">Pointer to a SAFEARRAY of COM interface identifiers (GUIDs) in BSTR format.</span></span>

</dd> <dt>

<span data-ttu-id="4ed1b-115">*LocaleID* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4ed1b-115">*localeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ed1b-116">Идентификатор локализации языка.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-116">Language localization identifier.</span></span>

</dd> <dt>

<span data-ttu-id="4ed1b-117">*ппкарднамес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4ed1b-117">*ppCardNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ed1b-118">Указатель на SAFEARRAY массива типа BSTR, который содержит имена смарт-карт, удовлетворяющих параметрам поиска, если они выполнены успешно. **Значение NULL** , если операция завершилась ошибкой.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-118">Pointer to a SAFEARRAY of BSTRs that contains the names of the smart cards that satisfied the search parameters if successful; **NULL** if the operation failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ed1b-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4ed1b-119">Return value</span></span>

<span data-ttu-id="4ed1b-120">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-120">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="4ed1b-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4ed1b-121">Return code</span></span>                                                                                   | <span data-ttu-id="4ed1b-122">Описание</span><span class="sxs-lookup"><span data-stu-id="4ed1b-122">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="4ed1b-123"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="4ed1b-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4ed1b-124">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="4ed1b-124">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="4ed1b-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4ed1b-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="4ed1b-126">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-126">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="4ed1b-127"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="4ed1b-127"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="4ed1b-128">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-128">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="4ed1b-129"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4ed1b-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4ed1b-130">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-130">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="4ed1b-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4ed1b-131">Remarks</span></span>

<span data-ttu-id="4ed1b-132">Чтобы получить все известные [*средства чтения*](../secgloss/r-gly.md) или [*чтения*](../secgloss/r-gly.md), вызовите [**листреадерс**](iscarddatabase-listreaders.md) или [**листреадерграупс**](iscarddatabase-listreadergroups.md) соответственно.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-132">To retrieve all known [*readers*](../secgloss/r-gly.md) or [*reader*](../secgloss/r-gly.md), call [**ListReaders**](iscarddatabase-listreaders.md) or [**ListReaderGroups**](iscarddatabase-listreadergroups.md) respectively.</span></span>

<span data-ttu-id="4ed1b-133">Для получения [*основной службы*](../secgloss/p-gly.md) или интерфейсов определенной карты [**жетпровидеркардид**](iscarddatabase-getprovidercardid.md) или [**листкардинтерфацес**](iscarddatabase-listcardinterfaces.md) соответственно.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-133">To retrieve the [*primary service*](../secgloss/p-gly.md) or the interfaces of a specific card [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) or [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) respectively.</span></span>

<span data-ttu-id="4ed1b-134">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искарддатабасе**](iscarddatabase.md).</span><span class="sxs-lookup"><span data-stu-id="4ed1b-134">For a list of all the methods provided by this interface, see [**ISCardDatabase**](iscarddatabase.md).</span></span>

<span data-ttu-id="4ed1b-135">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-135">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="4ed1b-136">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="4ed1b-136">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4ed1b-137">Примеры</span><span class="sxs-lookup"><span data-stu-id="4ed1b-137">Examples</span></span>

<span data-ttu-id="4ed1b-138">В следующем примере показано получение имен смарт-карт, соответствующих указанной строке ATR.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-138">The following example shows retrieving the smart card names that match the specified ATR string.</span></span>


```C++
// Define or determine byAtr as needed for your ATR use.
BYTE byAtr[] = {0x3b,0x27,0x00,0x80,0x65,0xa2,0x0c,0x01,0x01,0x37};
LPSAFEARRAY pSafeArray = NULL;
HRESULT          hr;

// pIByteBuff is a pointer to an instance of IByteBuffer.
hr = pIByteBuff->Initialize(sizeof(byAtr), byAtr);

// Call the function for the specified ATR.
hr = pISCDataBase->ListCards(pIByteBuff,
                             NULL,
                             0,
                             &pSafeArray);
if (FAILED(hr))
{
   printf("Failed ListCards\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="4ed1b-139">Требования</span><span class="sxs-lookup"><span data-stu-id="4ed1b-139">Requirements</span></span>



| <span data-ttu-id="4ed1b-140">Требование</span><span class="sxs-lookup"><span data-stu-id="4ed1b-140">Requirement</span></span> | <span data-ttu-id="4ed1b-141">Значение</span><span class="sxs-lookup"><span data-stu-id="4ed1b-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ed1b-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4ed1b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="4ed1b-143">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4ed1b-143">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4ed1b-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4ed1b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="4ed1b-145">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4ed1b-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4ed1b-146">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="4ed1b-146">End of client support</span></span><br/>    | <span data-ttu-id="4ed1b-147">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4ed1b-147">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="4ed1b-148">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="4ed1b-148">End of server support</span></span><br/>    | <span data-ttu-id="4ed1b-149">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4ed1b-149">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="4ed1b-150">Header</span><span class="sxs-lookup"><span data-stu-id="4ed1b-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ed1b-151"><dt>Скардмгр. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ed1b-151"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="4ed1b-152">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="4ed1b-152">Type library</span></span><br/>             | <dl> <span data-ttu-id="4ed1b-153"><dt>Скардмгр. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4ed1b-153"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4ed1b-154">DLL</span><span class="sxs-lookup"><span data-stu-id="4ed1b-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ed1b-155"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ed1b-155"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4ed1b-156">IID</span><span class="sxs-lookup"><span data-stu-id="4ed1b-156">IID</span></span><br/>                      | <span data-ttu-id="4ed1b-157">IID \_ искарддатабасе определен как 1461AAC8-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="4ed1b-157">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="4ed1b-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4ed1b-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ed1b-159">**жетпровидеркардид**</span><span class="sxs-lookup"><span data-stu-id="4ed1b-159">**GetProviderCardId**</span></span>](iscarddatabase-getprovidercardid.md)
</dt> <dt>

[<span data-ttu-id="4ed1b-160">**искарддатабасе**</span><span class="sxs-lookup"><span data-stu-id="4ed1b-160">**ISCardDatabase**</span></span>](iscarddatabase.md)
</dt> <dt>

[<span data-ttu-id="4ed1b-161">**листкардинтерфацес**</span><span class="sxs-lookup"><span data-stu-id="4ed1b-161">**ListCardInterfaces**</span></span>](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[<span data-ttu-id="4ed1b-162">**листреадерграупс**</span><span class="sxs-lookup"><span data-stu-id="4ed1b-162">**ListReaderGroups**</span></span>](iscarddatabase-listreadergroups.md)
</dt> <dt>

[<span data-ttu-id="4ed1b-163">**листреадерс**</span><span class="sxs-lookup"><span data-stu-id="4ed1b-163">**ListReaders**</span></span>](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
