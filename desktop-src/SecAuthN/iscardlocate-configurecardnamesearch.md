---
description: Метод Конфигурекарднамесеарч указывает имена карточек, которые будут использоваться в поиске смарт-карты.
ms.assetid: fb406696-0cf0-4d67-8125-8888ee1b8213
title: 'Метод Искардлокате:: Конфигурекарднамесеарч (Скардмгр. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate.ConfigureCardNameSearch
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4af451bea1f08df2af0a673b26e84c9df2a0954b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265013"
---
# <a name="iscardlocateconfigurecardnamesearch-method"></a><span data-ttu-id="3445a-103">Метод Искардлокате:: Конфигурекарднамесеарч</span><span class="sxs-lookup"><span data-stu-id="3445a-103">ISCardLocate::ConfigureCardNameSearch method</span></span>

<span data-ttu-id="3445a-104">\[Метод **конфигурекарднамесеарч** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="3445a-104">\[The **ConfigureCardNameSearch** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3445a-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="3445a-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3445a-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="3445a-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="3445a-107">Метод **конфигурекарднамесеарч** указывает имена карточек, которые будут использоваться в поиске [*смарт-карты*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="3445a-107">The **ConfigureCardNameSearch** method specifies the card names to be used in the search for the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3445a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3445a-108">Syntax</span></span>


```C++
HRESULT ConfigureCardNameSearch(
  [in] LPSAFEARRAY pCardNames,
  [in] LPSAFEARRAY pGroupNames,
  [in] BSTR        bstrTitle,
  [in] LONG        lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="3445a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3445a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3445a-110">*пкарднамес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3445a-110">*pCardNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3445a-111">Указатель на защищенный массив службы автоматизации имен карточек в форме BSTR.</span><span class="sxs-lookup"><span data-stu-id="3445a-111">A pointer to an Automation safe array of card names in BSTR form.</span></span>

</dd> <dt>

<span data-ttu-id="3445a-112">*пграупнамес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3445a-112">*pGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3445a-113">Указатель на защищенный массив имен групп карточек или читателей в форме BSTR для добавления в поиск.</span><span class="sxs-lookup"><span data-stu-id="3445a-113">A pointer to an Automation safe array of names of card/reader groups in BSTR form to add to the search.</span></span>

</dd> <dt>

<span data-ttu-id="3445a-114">*бстртитле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3445a-114">*bstrTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3445a-115">Заголовок диалогового окна для общего элемента управления поиском.</span><span class="sxs-lookup"><span data-stu-id="3445a-115">Dialog box title for the search common control.</span></span>

</dd> <dt>

<span data-ttu-id="3445a-116">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3445a-116">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3445a-117">Указывает, когда отображается [*Пользовательский интерфейс*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="3445a-117">Specifies when [*user interface*](../secgloss/u-gly.md) is displayed.</span></span>



| <span data-ttu-id="3445a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3445a-118">Value</span></span>                                                                                                                                                                       | <span data-ttu-id="3445a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="3445a-119">Meaning</span></span>                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_DLG_MINIMAL_UI"></span><span id="sc_dlg_minimal_ui"></span><dl> <span data-ttu-id="3445a-120"><dt>**\_ \_ Минимальный \_ Пользовательский интерфейс SC DLG**</dt></span><span class="sxs-lookup"><span data-stu-id="3445a-120"><dt>**SC\_DLG\_MINIMAL\_UI**</dt></span></span> </dl> | <span data-ttu-id="3445a-121">Отображает диалоговое окно, только если карта, поиск которой выполняется в вызывающем приложении, не найдена и недоступна для использования в модуле чтения.</span><span class="sxs-lookup"><span data-stu-id="3445a-121">Displays the dialog box only if the card being searched for by the calling application is not located and available for use in a reader.</span></span> <span data-ttu-id="3445a-122">Это позволяет найти карту, подключить ее (через внутренний механизм диалогового окна или с помощью функций обратного вызова пользователя) и вернуть вызывающему приложению.</span><span class="sxs-lookup"><span data-stu-id="3445a-122">This allows the card to be found, connected (either through an internal dialog box mechanism or by using the user callback functions), and returned to the calling application.</span></span><br/> |
| <span id="SC_DLG_NO_UI"></span><span id="sc_dlg_no_ui"></span><dl> <span data-ttu-id="3445a-123"><dt>**SC \_ DLG \_ нет \_ пользовательского интерфейса**</dt></span><span class="sxs-lookup"><span data-stu-id="3445a-123"><dt>**SC\_DLG\_NO\_UI**</dt></span></span> </dl>                | <span data-ttu-id="3445a-124">Не приводит к отображению пользовательского интерфейса, независимо от результата поиска.</span><span class="sxs-lookup"><span data-stu-id="3445a-124">Causes no UI display, regardless of the search outcome.</span></span><br/>                                                                                                                                                                                                                                                                  |
| <span id="SC_DLG_FORCE_UI"></span><span id="sc_dlg_force_ui"></span><dl> <span data-ttu-id="3445a-125"><dt>**\_ \_ Пользовательский интерфейс SC DLG Force \_ UI**</dt></span><span class="sxs-lookup"><span data-stu-id="3445a-125"><dt>**SC\_DLG\_FORCE\_UI**</dt></span></span> </dl>       | <span data-ttu-id="3445a-126">Вызывает отображение пользовательского интерфейса независимо от результата поиска.</span><span class="sxs-lookup"><span data-stu-id="3445a-126">Causes UI display regardless of the search outcome.</span></span><br/>                                                                                                                                                                                                                                                                      |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3445a-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3445a-127">Return value</span></span>

<span data-ttu-id="3445a-128">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="3445a-128">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="3445a-129">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3445a-129">Return code</span></span>                                                                                   | <span data-ttu-id="3445a-130">Описание</span><span class="sxs-lookup"><span data-stu-id="3445a-130">Description</span></span>                                                           |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="3445a-131"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="3445a-131"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3445a-132">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="3445a-132">Operation completed successfully.</span></span><br/>                          |
| <dl> <span data-ttu-id="3445a-133"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3445a-133"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="3445a-134">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="3445a-134">Invalid parameter.</span></span><br/>                                         |
| <dl> <span data-ttu-id="3445a-135"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="3445a-135"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3445a-136">Недопустимый указатель был передан в *пкарднамес* или *пграупнамес*.</span><span class="sxs-lookup"><span data-stu-id="3445a-136">A bad pointer was passed in *pCardNames* or *pGroupNames*.</span></span><br/> |
| <dl> <span data-ttu-id="3445a-137"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3445a-137"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3445a-138">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="3445a-138">Out of memory.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="3445a-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3445a-139">Remarks</span></span>

<span data-ttu-id="3445a-140">Чтобы открыть [*смарт-карту*](../secgloss/s-gly.md), вызовите [**финдкард**](iscardlocate-findcard.md).</span><span class="sxs-lookup"><span data-stu-id="3445a-140">To locate the [*smart card*](../secgloss/s-gly.md), call [**FindCard**](iscardlocate-findcard.md).</span></span>

<span data-ttu-id="3445a-141">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардлокате**](iscardlocate.md).</span><span class="sxs-lookup"><span data-stu-id="3445a-141">For a list of all the methods provided by this interface, see [**ISCardLocate**](iscardlocate.md).</span></span>

<span data-ttu-id="3445a-142">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="3445a-142">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="3445a-143">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="3445a-143">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3445a-144">Требования</span><span class="sxs-lookup"><span data-stu-id="3445a-144">Requirements</span></span>



| <span data-ttu-id="3445a-145">Требование</span><span class="sxs-lookup"><span data-stu-id="3445a-145">Requirement</span></span> | <span data-ttu-id="3445a-146">Значение</span><span class="sxs-lookup"><span data-stu-id="3445a-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3445a-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3445a-147">Minimum supported client</span></span><br/> | <span data-ttu-id="3445a-148">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3445a-148">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3445a-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3445a-149">Minimum supported server</span></span><br/> | <span data-ttu-id="3445a-150">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3445a-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3445a-151">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="3445a-151">End of client support</span></span><br/>    | <span data-ttu-id="3445a-152">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3445a-152">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="3445a-153">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="3445a-153">End of server support</span></span><br/>    | <span data-ttu-id="3445a-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3445a-154">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="3445a-155">Header</span><span class="sxs-lookup"><span data-stu-id="3445a-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="3445a-156"><dt>Скардмгр. h</dt></span><span class="sxs-lookup"><span data-stu-id="3445a-156"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="3445a-157">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="3445a-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="3445a-158"><dt>Скардмгр. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3445a-158"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3445a-159">DLL</span><span class="sxs-lookup"><span data-stu-id="3445a-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3445a-160"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3445a-160"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3445a-161">IID</span><span class="sxs-lookup"><span data-stu-id="3445a-161">IID</span></span><br/>                      | <span data-ttu-id="3445a-162">IID \_ искардлокате определен как 1461AACD-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="3445a-162">IID\_ISCardLocate is defined as 1461AACD-6810-11D0-918F-00AA00C18068</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="3445a-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3445a-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3445a-164">**финдкард**</span><span class="sxs-lookup"><span data-stu-id="3445a-164">**FindCard**</span></span>](iscardlocate-findcard.md)
</dt> <dt>

[<span data-ttu-id="3445a-165">**искардлокате**</span><span class="sxs-lookup"><span data-stu-id="3445a-165">**ISCardLocate**</span></span>](iscardlocate.md)
</dt> </dl>

 

 
