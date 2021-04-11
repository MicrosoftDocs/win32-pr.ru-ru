---
description: Метод Листреадерграупс извлекает имена групп читателей, зарегистрированных в базе данных смарт-карты.
ms.assetid: 81f6356a-92eb-4d27-abfe-e4a32de14d1c
title: 'Метод Искарддатабасе:: Листреадерграупс (Скардмгр. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListReaderGroups
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 00753b0ca3964dc5a35e26db0eec2aedda4d2511
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145265"
---
# <a name="iscarddatabaselistreadergroups-method"></a><span data-ttu-id="444f9-103">Метод Искарддатабасе:: Листреадерграупс</span><span class="sxs-lookup"><span data-stu-id="444f9-103">ISCardDatabase::ListReaderGroups method</span></span>

<span data-ttu-id="444f9-104">\[Метод **листреадерграупс** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="444f9-104">\[The **ListReaderGroups** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="444f9-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="444f9-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="444f9-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="444f9-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="444f9-107">Метод **листреадерграупс** извлекает имена [*групп читателей*](../secgloss/r-gly.md) , зарегистрированных в базе данных смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="444f9-107">The **ListReaderGroups** method retrieves the names of the [*reader groups*](../secgloss/r-gly.md) registered in the smart card database.</span></span>

## <a name="syntax"></a><span data-ttu-id="444f9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="444f9-108">Syntax</span></span>


```C++
HRESULT ListReaderGroups(
  [in]  LONG        localeId,
  [out] LPSAFEARRAY *ppReaderGroups
);
```



## <a name="parameters"></a><span data-ttu-id="444f9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="444f9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="444f9-110">*LocaleID* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="444f9-110">*localeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="444f9-111">ИДЕНТИФИКАТОР локализации языка.</span><span class="sxs-lookup"><span data-stu-id="444f9-111">Language localization ID.</span></span>

</dd> <dt>

<span data-ttu-id="444f9-112">*ппреадерграупс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="444f9-112">*ppReaderGroups* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="444f9-113">Указатель на массив SAFEARRAY, содержащий имена групп считывателей смарт-карт, которые удовлетворяют параметрам поиска в случае успеха. **Значение NULL** , если операция завершилась ошибкой.</span><span class="sxs-lookup"><span data-stu-id="444f9-113">Pointer to a SAFEARRAY of BSTRs that contains the names of the smart card reader groups that satisfied the search parameters if successful; **NULL** if the operation failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="444f9-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="444f9-114">Return value</span></span>

<span data-ttu-id="444f9-115">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="444f9-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="444f9-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="444f9-116">Return code</span></span>                                                                                   | <span data-ttu-id="444f9-117">Описание</span><span class="sxs-lookup"><span data-stu-id="444f9-117">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="444f9-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="444f9-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="444f9-119">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="444f9-119">Operation completed successfully.</span></span><br/>             |
| <dl> <span data-ttu-id="444f9-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="444f9-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="444f9-121">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="444f9-121">Invalid parameter.</span></span><br/>                            |
| <dl> <span data-ttu-id="444f9-122"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="444f9-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="444f9-123">В *ппреадерграупс* был передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="444f9-123">A bad pointer was passed in *ppReaderGroups*.</span></span><br/> |
| <dl> <span data-ttu-id="444f9-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="444f9-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="444f9-125">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="444f9-125">Out of memory.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="444f9-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="444f9-126">Remarks</span></span>

<span data-ttu-id="444f9-127">Чтобы получить все известные [*смарт-карты*](../secgloss/s-gly.md) или [*модули чтения*](../secgloss/r-gly.md), вызовите [**листкардс**](iscarddatabase-listcards.md) или [**листреадерс**](iscarddatabase-listreaders.md) соответственно.</span><span class="sxs-lookup"><span data-stu-id="444f9-127">To retrieve all known [*smart cards*](../secgloss/s-gly.md) or [*readers*](../secgloss/r-gly.md), call [**ListCards**](iscarddatabase-listcards.md) or [**ListReaders**](iscarddatabase-listreaders.md) respectively.</span></span>

<span data-ttu-id="444f9-128">Получение [*первичного поставщика услуг*](../secgloss/p-gly.md) или интерфейсов конкретного адаптера [**жетпровидеркардид**](iscarddatabase-getprovidercardid.md) или [**листкардинтерфацес**](iscarddatabase-listcardinterfaces.md) соответственно.</span><span class="sxs-lookup"><span data-stu-id="444f9-128">To retrieve the [*primary service provider*](../secgloss/p-gly.md) or the interfaces of a specific card [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) or [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) respectively.</span></span>

<span data-ttu-id="444f9-129">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искарддатабасе**](iscarddatabase.md).</span><span class="sxs-lookup"><span data-stu-id="444f9-129">For a list of all the methods provided by this interface, see [**ISCardDatabase**](iscarddatabase.md).</span></span>

<span data-ttu-id="444f9-130">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="444f9-130">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="444f9-131">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="444f9-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="444f9-132">Примеры</span><span class="sxs-lookup"><span data-stu-id="444f9-132">Examples</span></span>

<span data-ttu-id="444f9-133">В следующем примере показано получение имен групп читателей, зарегистрированных в базе данных смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="444f9-133">The following example shows retrieving the names of the reader groups registered in the smart card database.</span></span>


```C++
LPSAFEARRAY pGroups = NULL;
HRESULT     hr;

// Determine the reader groups.
hr = pISCDataBase->ListReaderGroups(0x0409,  // English (US)
                                    &pGroups);
if (FAILED(hr))
{
   printf("Failed ListReaderGroups\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
   // ...
}
```



## <a name="requirements"></a><span data-ttu-id="444f9-134">Требования</span><span class="sxs-lookup"><span data-stu-id="444f9-134">Requirements</span></span>



| <span data-ttu-id="444f9-135">Требование</span><span class="sxs-lookup"><span data-stu-id="444f9-135">Requirement</span></span> | <span data-ttu-id="444f9-136">Значение</span><span class="sxs-lookup"><span data-stu-id="444f9-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="444f9-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="444f9-137">Minimum supported client</span></span><br/> | <span data-ttu-id="444f9-138">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="444f9-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="444f9-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="444f9-139">Minimum supported server</span></span><br/> | <span data-ttu-id="444f9-140">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="444f9-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="444f9-141">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="444f9-141">End of client support</span></span><br/>    | <span data-ttu-id="444f9-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="444f9-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="444f9-143">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="444f9-143">End of server support</span></span><br/>    | <span data-ttu-id="444f9-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="444f9-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="444f9-145">Header</span><span class="sxs-lookup"><span data-stu-id="444f9-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="444f9-146"><dt>Скардмгр. h</dt></span><span class="sxs-lookup"><span data-stu-id="444f9-146"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="444f9-147">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="444f9-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="444f9-148"><dt>Скардмгр. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="444f9-148"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="444f9-149">DLL</span><span class="sxs-lookup"><span data-stu-id="444f9-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="444f9-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="444f9-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="444f9-151">IID</span><span class="sxs-lookup"><span data-stu-id="444f9-151">IID</span></span><br/>                      | <span data-ttu-id="444f9-152">IID \_ искарддатабасе определен как 1461AAC8-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="444f9-152">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="444f9-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="444f9-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="444f9-154">**жетпровидеркардид**</span><span class="sxs-lookup"><span data-stu-id="444f9-154">**GetProviderCardId**</span></span>](iscarddatabase-getprovidercardid.md)
</dt> <dt>

[<span data-ttu-id="444f9-155">**искарддатабасе**</span><span class="sxs-lookup"><span data-stu-id="444f9-155">**ISCardDatabase**</span></span>](iscarddatabase.md)
</dt> <dt>

[<span data-ttu-id="444f9-156">**листкардинтерфацес**</span><span class="sxs-lookup"><span data-stu-id="444f9-156">**ListCardInterfaces**</span></span>](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[<span data-ttu-id="444f9-157">**ListCards**</span><span class="sxs-lookup"><span data-stu-id="444f9-157">**ListCards**</span></span>](iscarddatabase-listcards.md)
</dt> <dt>

[<span data-ttu-id="444f9-158">**листреадерс**</span><span class="sxs-lookup"><span data-stu-id="444f9-158">**ListReaders**</span></span>](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
