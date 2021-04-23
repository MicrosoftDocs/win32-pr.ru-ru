---
description: Метод Листкардинтерфацес извлекает идентификаторы (GUID) всех интерфейсов, поддерживаемых для указанной смарт-карты.
ms.assetid: c9dfd17e-f4a9-47d3-974e-66e78bc4b06a
title: 'Метод Искарддатабасе:: Листкардинтерфацес (Скардмгр. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListCardInterfaces
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d52324edd4a502388ac6064de07a6ab58a68074d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262885"
---
# <a name="iscarddatabaselistcardinterfaces-method"></a><span data-ttu-id="7d82a-103">Метод Искарддатабасе:: Листкардинтерфацес</span><span class="sxs-lookup"><span data-stu-id="7d82a-103">ISCardDatabase::ListCardInterfaces method</span></span>

<span data-ttu-id="7d82a-104">\[Метод **листкардинтерфацес** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="7d82a-104">\[The **ListCardInterfaces** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7d82a-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7d82a-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7d82a-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="7d82a-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="7d82a-107">Метод **листкардинтерфацес** извлекает идентификаторы (GUID) всех интерфейсов, поддерживаемых для указанной [*смарт-карты*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="7d82a-107">The **ListCardInterfaces** method retrieves the identifiers (GUIDs) of all the interfaces supported for the specified [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7d82a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d82a-108">Syntax</span></span>


```C++
HRESULT ListCardInterfaces(
  [in]  BSTR        bstrCardName,
  [out] LPSAFEARRAY *ppInterfaceGuids
);
```



## <a name="parameters"></a><span data-ttu-id="7d82a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d82a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d82a-110">*бстркарднаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7d82a-110">*bstrCardName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d82a-111">Имя смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="7d82a-111">Name of the smart card.</span></span>

</dd> <dt>

<span data-ttu-id="7d82a-112">*ппинтерфацегуидс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7d82a-112">*ppInterfaceGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d82a-113">Указатель на идентификаторы GUID интерфейса в случае успеха; **Null** , если операция завершилась ошибкой.</span><span class="sxs-lookup"><span data-stu-id="7d82a-113">Pointer to the interface GUIDs if successful; **NULL** if operation failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d82a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7d82a-114">Return value</span></span>

<span data-ttu-id="7d82a-115">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="7d82a-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="7d82a-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7d82a-116">Return code</span></span>                                                                                   | <span data-ttu-id="7d82a-117">Описание</span><span class="sxs-lookup"><span data-stu-id="7d82a-117">Description</span></span>                                                |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="7d82a-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7d82a-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7d82a-119">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="7d82a-119">Operation completed successfully.</span></span><br/>               |
| <dl> <span data-ttu-id="7d82a-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7d82a-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="7d82a-121">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="7d82a-121">Invalid parameter.</span></span><br/>                              |
| <dl> <span data-ttu-id="7d82a-122"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="7d82a-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7d82a-123">В *ппинтерфацегуидс* был передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="7d82a-123">A bad pointer was passed in *ppInterfaceGuids*.</span></span><br/> |
| <dl> <span data-ttu-id="7d82a-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7d82a-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7d82a-125">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="7d82a-125">Out of memory.</span></span><br/>                                  |



 

## <a name="remarks"></a><span data-ttu-id="7d82a-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7d82a-126">Remarks</span></span>

<span data-ttu-id="7d82a-127">Чтобы получить [*первичный поставщик услуг*](../secgloss/p-gly.md) смарт-карты, вызовите [**жетпровидеркардид**](iscarddatabase-getprovidercardid.md).</span><span class="sxs-lookup"><span data-stu-id="7d82a-127">To retrieve the [*primary service provider*](../secgloss/p-gly.md) of the smart card, call [**GetProviderCardId**](iscarddatabase-getprovidercardid.md).</span></span>

<span data-ttu-id="7d82a-128">Чтобы получить все известные [*смарт-карты*](../secgloss/s-gly.md), [*читатели*](../secgloss/r-gly.md)и [*группы читателей*](../secgloss/r-gly.md) , вызовите [**листкардс**](iscarddatabase-listcards.md), [**листреадерс**](iscarddatabase-listreaders.md)и [**листреадерграупс**](iscarddatabase-listreadergroups.md) соответственно.</span><span class="sxs-lookup"><span data-stu-id="7d82a-128">To retrieve all known [*smart cards*](../secgloss/s-gly.md), [*readers*](../secgloss/r-gly.md), and [*reader groups*](../secgloss/r-gly.md) call [**ListCards**](iscarddatabase-listcards.md), [**ListReaders**](iscarddatabase-listreaders.md), and [**ListReaderGroups**](iscarddatabase-listreadergroups.md) respectively.</span></span>

<span data-ttu-id="7d82a-129">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искарддатабасе**](iscarddatabase.md).</span><span class="sxs-lookup"><span data-stu-id="7d82a-129">For a list of all the methods provided by this interface, see [**ISCardDatabase**](iscarddatabase.md).</span></span>

<span data-ttu-id="7d82a-130">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="7d82a-130">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="7d82a-131">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="7d82a-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7d82a-132">Примеры</span><span class="sxs-lookup"><span data-stu-id="7d82a-132">Examples</span></span>

<span data-ttu-id="7d82a-133">В следующем примере показано получение идентификаторов интерфейсов, поддерживаемых для указанной смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="7d82a-133">The following example shows retrieving the identifiers of the interfaces supported for the specified smart card.</span></span>


```C++
BSTR         bstrCard = NULL;
LPSAFEARRAY  pGuids = NULL;
HRESULT      hr;

bstrCard = SysAllocString(L"GemSAFE");
// Call the function for the specified card.
hr = pISCDataBase->ListCardInterfaces(bstrCard,
                                      &pGuids);
if (FAILED(hr))
{
   printf("Failed ListCardInterfaces\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
   // ...
   // Free BSTR when done.
   if (bstrCard)
       SysFreeString(bstrCard);
}
```



## <a name="requirements"></a><span data-ttu-id="7d82a-134">Требования</span><span class="sxs-lookup"><span data-stu-id="7d82a-134">Requirements</span></span>



| <span data-ttu-id="7d82a-135">Требование</span><span class="sxs-lookup"><span data-stu-id="7d82a-135">Requirement</span></span> | <span data-ttu-id="7d82a-136">Значение</span><span class="sxs-lookup"><span data-stu-id="7d82a-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d82a-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7d82a-137">Minimum supported client</span></span><br/> | <span data-ttu-id="7d82a-138">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7d82a-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7d82a-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7d82a-139">Minimum supported server</span></span><br/> | <span data-ttu-id="7d82a-140">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7d82a-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7d82a-141">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="7d82a-141">End of client support</span></span><br/>    | <span data-ttu-id="7d82a-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7d82a-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="7d82a-143">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="7d82a-143">End of server support</span></span><br/>    | <span data-ttu-id="7d82a-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7d82a-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="7d82a-145">Header</span><span class="sxs-lookup"><span data-stu-id="7d82a-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d82a-146"><dt>Скардмгр. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d82a-146"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="7d82a-147">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="7d82a-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="7d82a-148"><dt>Скардмгр. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7d82a-148"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7d82a-149">DLL</span><span class="sxs-lookup"><span data-stu-id="7d82a-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d82a-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d82a-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7d82a-151">IID</span><span class="sxs-lookup"><span data-stu-id="7d82a-151">IID</span></span><br/>                      | <span data-ttu-id="7d82a-152">IID \_ искарддатабасе определен как 1461AAC8-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="7d82a-152">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="7d82a-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d82a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d82a-154">**жетпровидеркардид**</span><span class="sxs-lookup"><span data-stu-id="7d82a-154">**GetProviderCardId**</span></span>](iscarddatabase-getprovidercardid.md)
</dt> <dt>

[<span data-ttu-id="7d82a-155">**искарддатабасе**</span><span class="sxs-lookup"><span data-stu-id="7d82a-155">**ISCardDatabase**</span></span>](iscarddatabase.md)
</dt> <dt>

[<span data-ttu-id="7d82a-156">**ListCards**</span><span class="sxs-lookup"><span data-stu-id="7d82a-156">**ListCards**</span></span>](iscarddatabase-listcards.md)
</dt> <dt>

[<span data-ttu-id="7d82a-157">**листреадерграупс**</span><span class="sxs-lookup"><span data-stu-id="7d82a-157">**ListReaderGroups**</span></span>](iscarddatabase-listreadergroups.md)
</dt> <dt>

[<span data-ttu-id="7d82a-158">**листреадерс**</span><span class="sxs-lookup"><span data-stu-id="7d82a-158">**ListReaders**</span></span>](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
