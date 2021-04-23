---
description: Метод Жетпровидеркардид извлекает идентификатор (GUID) основного поставщика услуг для указанной смарт-карты.
ms.assetid: 0008bb5a-872f-4e5d-9029-a863cd3eea00
title: 'Метод Искарддатабасе:: Жетпровидеркардид (Скардмгр. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.GetProviderCardId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 9f361e83431fa7c6e0a0c2c0ea363bef7e487738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816792"
---
# <a name="iscarddatabasegetprovidercardid-method"></a><span data-ttu-id="822b8-103">Метод Искарддатабасе:: Жетпровидеркардид</span><span class="sxs-lookup"><span data-stu-id="822b8-103">ISCardDatabase::GetProviderCardId method</span></span>

<span data-ttu-id="822b8-104">\[Метод **жетпровидеркардид** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="822b8-104">\[The **GetProviderCardId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="822b8-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="822b8-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="822b8-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="822b8-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="822b8-107">Метод **жетпровидеркардид** извлекает идентификатор (GUID) [*основного поставщика услуг*](../secgloss/p-gly.md) для указанной [*смарт-карты*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="822b8-107">The **GetProviderCardId** method retrieves the identifier (GUID) of the [*primary service provider*](../secgloss/p-gly.md) for the specified [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="822b8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="822b8-108">Syntax</span></span>


```C++
HRESULT GetProviderCardId(
  [in]  BSTR   bstrCardName,
  [out] LPGUID *ppguidProviderId
);
```



## <a name="parameters"></a><span data-ttu-id="822b8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="822b8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="822b8-110">*бстркарднаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="822b8-110">*bstrCardName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="822b8-111">Имя смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="822b8-111">Name of the smart card.</span></span>

</dd> <dt>

<span data-ttu-id="822b8-112">*ппгуидпровидерид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="822b8-112">*ppguidProviderId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="822b8-113">Указатель на идентификатор первичного поставщика служб (GUID) в случае успешного выполнения; **Null** , если операция завершилась ошибкой.</span><span class="sxs-lookup"><span data-stu-id="822b8-113">Pointer to the primary service provider's identifier (GUID) if successful; **NULL** if operation failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="822b8-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="822b8-114">Return value</span></span>

<span data-ttu-id="822b8-115">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="822b8-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="822b8-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="822b8-116">Return code</span></span>                                                                                   | <span data-ttu-id="822b8-117">Описание</span><span class="sxs-lookup"><span data-stu-id="822b8-117">Description</span></span>                                                |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="822b8-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="822b8-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="822b8-119">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="822b8-119">Operation completed successfully.</span></span><br/>               |
| <dl> <span data-ttu-id="822b8-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="822b8-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="822b8-121">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="822b8-121">Invalid parameter.</span></span><br/>                              |
| <dl> <span data-ttu-id="822b8-122"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="822b8-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="822b8-123">В *ппгуидпровидерид* был передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="822b8-123">A bad pointer was passed in *ppguidProviderId*.</span></span><br/> |
| <dl> <span data-ttu-id="822b8-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="822b8-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="822b8-125">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="822b8-125">Out of memory.</span></span><br/>                                  |



 

## <a name="remarks"></a><span data-ttu-id="822b8-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="822b8-126">Remarks</span></span>

<span data-ttu-id="822b8-127">Чтобы получить список интерфейсов смарт-карты, вызовите [**листкардинтерфацес**](iscarddatabase-listcardinterfaces.md).</span><span class="sxs-lookup"><span data-stu-id="822b8-127">To list the interfaces of the smart card, call [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md).</span></span>

<span data-ttu-id="822b8-128">Чтобы получить все известные [*смарт-карты*](../secgloss/s-gly.md), [*читатели*](../secgloss/r-gly.md) и [*группы читателей*](../secgloss/r-gly.md) вызывают [**листкардс**](iscarddatabase-listcards.md), [**листреадерс**](iscarddatabase-listreaders.md)и [**листреадерграупс**](iscarddatabase-listreadergroups.md) соответственно.</span><span class="sxs-lookup"><span data-stu-id="822b8-128">To retrieve all known [*smart cards*](../secgloss/s-gly.md), [*readers*](../secgloss/r-gly.md) and [*reader groups*](../secgloss/r-gly.md) call [**ListCards**](iscarddatabase-listcards.md), [**ListReaders**](iscarddatabase-listreaders.md), and [**ListReaderGroups**](iscarddatabase-listreadergroups.md) respectively.</span></span>

<span data-ttu-id="822b8-129">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искарддатабасе**](iscarddatabase.md).</span><span class="sxs-lookup"><span data-stu-id="822b8-129">For a list of all the methods provided by this interface, see [**ISCardDatabase**](iscarddatabase.md).</span></span>

<span data-ttu-id="822b8-130">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="822b8-130">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="822b8-131">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="822b8-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="822b8-132">Примеры</span><span class="sxs-lookup"><span data-stu-id="822b8-132">Examples</span></span>

<span data-ttu-id="822b8-133">В следующем примере показано получение идентификатора первичного поставщика услуг для указанной смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="822b8-133">The following example shows retrieving the identifier of the primary service provider for the specified smart card.</span></span>


```C++
BSTR     bstrCard = NULL;
LPGUID   pguidProvId = NULL;
HRESULT  hr;

bstrCard = SysAllocString(L"My Card");
hr = pISCDataBase->GetProviderCardId(bstrCard,&pguidProvId);
if (FAILED(hr))
{
   printf("Failed GetProviderCardId\n");
}
else
{
    // Use pguidProvId as needed.
}

// Free BSTR when done.
if ( NULL != bstrCard )
{
    SysFreeString(bstrCard);
    bstrCard=NULL;
}
```



## <a name="requirements"></a><span data-ttu-id="822b8-134">Требования</span><span class="sxs-lookup"><span data-stu-id="822b8-134">Requirements</span></span>



| <span data-ttu-id="822b8-135">Требование</span><span class="sxs-lookup"><span data-stu-id="822b8-135">Requirement</span></span> | <span data-ttu-id="822b8-136">Значение</span><span class="sxs-lookup"><span data-stu-id="822b8-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="822b8-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="822b8-137">Minimum supported client</span></span><br/> | <span data-ttu-id="822b8-138">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="822b8-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="822b8-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="822b8-139">Minimum supported server</span></span><br/> | <span data-ttu-id="822b8-140">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="822b8-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="822b8-141">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="822b8-141">End of client support</span></span><br/>    | <span data-ttu-id="822b8-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="822b8-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="822b8-143">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="822b8-143">End of server support</span></span><br/>    | <span data-ttu-id="822b8-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="822b8-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="822b8-145">Header</span><span class="sxs-lookup"><span data-stu-id="822b8-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="822b8-146"><dt>Скардмгр. h</dt></span><span class="sxs-lookup"><span data-stu-id="822b8-146"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="822b8-147">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="822b8-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="822b8-148"><dt>Скардмгр. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="822b8-148"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="822b8-149">DLL</span><span class="sxs-lookup"><span data-stu-id="822b8-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="822b8-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="822b8-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="822b8-151">IID</span><span class="sxs-lookup"><span data-stu-id="822b8-151">IID</span></span><br/>                      | <span data-ttu-id="822b8-152">IID \_ искарддатабасе определен как 1461AAC8-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="822b8-152">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="822b8-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="822b8-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="822b8-154">**искарддатабасе**</span><span class="sxs-lookup"><span data-stu-id="822b8-154">**ISCardDatabase**</span></span>](iscarddatabase.md)
</dt> <dt>

[<span data-ttu-id="822b8-155">**листкардинтерфацес**</span><span class="sxs-lookup"><span data-stu-id="822b8-155">**ListCardInterfaces**</span></span>](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[<span data-ttu-id="822b8-156">**ListCards**</span><span class="sxs-lookup"><span data-stu-id="822b8-156">**ListCards**</span></span>](iscarddatabase-listcards.md)
</dt> <dt>

[<span data-ttu-id="822b8-157">**листреадерграупс**</span><span class="sxs-lookup"><span data-stu-id="822b8-157">**ListReaderGroups**</span></span>](iscarddatabase-listreadergroups.md)
</dt> <dt>

[<span data-ttu-id="822b8-158">**листреадерс**</span><span class="sxs-lookup"><span data-stu-id="822b8-158">**ListReaders**</span></span>](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
