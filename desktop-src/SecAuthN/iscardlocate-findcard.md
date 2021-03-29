---
description: Метод Финдкард выполняет поиск смарт-карты и открывает для нее допустимое соединение.
ms.assetid: ab97eff2-0f41-4a6f-98b3-d5ad5883fa07
title: 'Метод Искардлокате:: Финдкард (Скардмгр. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate.FindCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bf3cf05ff6e6040d5cac2bde161fa2eea07d5297
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647349"
---
# <a name="iscardlocatefindcard-method"></a><span data-ttu-id="34aca-103">Метод Искардлокате:: Финдкард</span><span class="sxs-lookup"><span data-stu-id="34aca-103">ISCardLocate::FindCard method</span></span>

<span data-ttu-id="34aca-104">\[Метод **финдкард** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="34aca-104">\[The **FindCard** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="34aca-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="34aca-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="34aca-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="34aca-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="34aca-107">Метод **финдкард** выполняет поиск [*смарт-карты*](../secgloss/s-gly.md) и открывает для нее допустимое соединение.</span><span class="sxs-lookup"><span data-stu-id="34aca-107">The **FindCard** method searches for the [*smart card*](../secgloss/s-gly.md) and opens a valid connection to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="34aca-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34aca-108">Syntax</span></span>


```C++
HRESULT FindCard(
  [in]  SCARD_SHARE_MODES ShareMode,
  [in]  SCARD_PROTOCOLS   Protocols,
  [in]  LONG              lFlags,
  [out] LPSCARDINFO       *ppCardInfo
);
```



## <a name="parameters"></a><span data-ttu-id="34aca-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="34aca-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34aca-110">*Шаремоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34aca-110">*ShareMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34aca-111">Режим, в котором смарт-карта должна совместно использоваться или не предоставляться при открытии подключения к ней.</span><span class="sxs-lookup"><span data-stu-id="34aca-111">Mode in which to share or not share the smart card when a connection is opened to it.</span></span>



| <span data-ttu-id="34aca-112">Значение</span><span class="sxs-lookup"><span data-stu-id="34aca-112">Value</span></span>                                                                                                                                            | <span data-ttu-id="34aca-113">Значение</span><span class="sxs-lookup"><span data-stu-id="34aca-113">Meaning</span></span>                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <span data-ttu-id="34aca-114"><dt>**ВЗАИМОИСКЛЮЧАЮЩИМ**</dt></span><span class="sxs-lookup"><span data-stu-id="34aca-114"><dt>**EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="34aca-115">Никто больше не использует это подключение к смарт-карте.</span><span class="sxs-lookup"><span data-stu-id="34aca-115">No one else use this connection to the smart card.</span></span><br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <span data-ttu-id="34aca-116"><dt>**ИСПОЛЬЗУЕМЫЙ**</dt></span><span class="sxs-lookup"><span data-stu-id="34aca-116"><dt>**SHARED**</dt></span></span> </dl>          | <span data-ttu-id="34aca-117">Это подключение могут использовать другие приложения.</span><span class="sxs-lookup"><span data-stu-id="34aca-117">Other applications can use this connection.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="34aca-118">*Протоколы* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34aca-118">*Protocols* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34aca-119">Протокол, используемый для подключения к карте.</span><span class="sxs-lookup"><span data-stu-id="34aca-119">Protocol to use when connecting to the card.</span></span>

<span data-ttu-id="34aca-120">T0</span><span class="sxs-lookup"><span data-stu-id="34aca-120">T0</span></span>

<span data-ttu-id="34aca-121">T1</span><span class="sxs-lookup"><span data-stu-id="34aca-121">T1</span></span>

<span data-ttu-id="34aca-122">RAW</span><span class="sxs-lookup"><span data-stu-id="34aca-122">RAW</span></span>

<span data-ttu-id="34aca-123">T0 \| T1</span><span class="sxs-lookup"><span data-stu-id="34aca-123">T0\|T1</span></span>

</dd> <dt>

<span data-ttu-id="34aca-124">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34aca-124">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34aca-125">Указывает, когда отображается [*Пользовательский интерфейс*](../secgloss/u-gly.md) :</span><span class="sxs-lookup"><span data-stu-id="34aca-125">Specifies when [*user interface*](../secgloss/u-gly.md) is displayed:</span></span>



| <span data-ttu-id="34aca-126">Значение</span><span class="sxs-lookup"><span data-stu-id="34aca-126">Value</span></span>                                                                                                                                                                       | <span data-ttu-id="34aca-127">Значение</span><span class="sxs-lookup"><span data-stu-id="34aca-127">Meaning</span></span>                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_DLG_MINIMAL_UI"></span><span id="sc_dlg_minimal_ui"></span><dl> <span data-ttu-id="34aca-128"><dt>**\_ \_ Минимальный \_ Пользовательский интерфейс SC DLG**</dt></span><span class="sxs-lookup"><span data-stu-id="34aca-128"><dt>**SC\_DLG\_MINIMAL\_UI**</dt></span></span> </dl> | <span data-ttu-id="34aca-129">Отображает диалоговое окно, только если карта, поиск которой выполняется в вызывающем приложении, не найдена и недоступна для использования в модуле чтения.</span><span class="sxs-lookup"><span data-stu-id="34aca-129">Displays the dialog box only if the card being searched for by the calling application is not located and available for use in a reader.</span></span> <span data-ttu-id="34aca-130">Это позволяет найти карту, подключить ее (через внутренний механизм диалогового окна или с помощью функций обратного вызова пользователя) и вернуть вызывающему приложению.</span><span class="sxs-lookup"><span data-stu-id="34aca-130">This allows the card to be found, connected (either through an internal dialog box mechanism or by using the user callback functions), and returned to the calling application.</span></span><br/> |
| <span id="SC_DLG_NO_UI"></span><span id="sc_dlg_no_ui"></span><dl> <span data-ttu-id="34aca-131"><dt>**SC \_ DLG \_ нет \_ пользовательского интерфейса**</dt></span><span class="sxs-lookup"><span data-stu-id="34aca-131"><dt>**SC\_DLG\_NO\_UI**</dt></span></span> </dl>                | <span data-ttu-id="34aca-132">Не приводит к отображению пользовательского интерфейса, независимо от результата поиска.</span><span class="sxs-lookup"><span data-stu-id="34aca-132">Causes no UI display, regardless of the search outcome.</span></span><br/>                                                                                                                                                                                                                                                                  |
| <span id="SC_DLG_FORCE_UI"></span><span id="sc_dlg_force_ui"></span><dl> <span data-ttu-id="34aca-133"><dt>**\_ \_ Пользовательский интерфейс SC DLG Force \_ UI**</dt></span><span class="sxs-lookup"><span data-stu-id="34aca-133"><dt>**SC\_DLG\_FORCE\_UI**</dt></span></span> </dl>       | <span data-ttu-id="34aca-134">Вызывает отображение пользовательского интерфейса независимо от результата поиска.</span><span class="sxs-lookup"><span data-stu-id="34aca-134">Causes UI display regardless of the search outcome.</span></span><br/>                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="34aca-135">*ппкардинфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="34aca-135">*ppCardInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34aca-136">Указатель на указатель на структуру данных, которая содержит или возвращает сведения об открытой [*смарт-карте*](../secgloss/s-gly.md), если она выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="34aca-136">Pointer to a pointer to a data structure that contains or returns information about the opened [*smart card*](../secgloss/s-gly.md), if successful.</span></span> <span data-ttu-id="34aca-137">Если операция завершилась неудачно, будет иметь **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="34aca-137">Will be **NULL** if operation has failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34aca-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="34aca-138">Return value</span></span>

<span data-ttu-id="34aca-139">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="34aca-139">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="34aca-140">Код возврата</span><span class="sxs-lookup"><span data-stu-id="34aca-140">Return code</span></span>                                                                                   | <span data-ttu-id="34aca-141">Описание</span><span class="sxs-lookup"><span data-stu-id="34aca-141">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="34aca-142"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="34aca-142"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="34aca-143">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="34aca-143">Operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="34aca-144"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="34aca-144"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="34aca-145">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="34aca-145">Invalid parameter.</span></span><br/>                        |
| <dl> <span data-ttu-id="34aca-146"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="34aca-146"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="34aca-147">В *ппкардинфо* был передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="34aca-147">A bad pointer was passed in *ppCardInfo*.</span></span><br/> |
| <dl> <span data-ttu-id="34aca-148"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="34aca-148"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="34aca-149">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="34aca-149">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="34aca-150">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34aca-150">Remarks</span></span>

<span data-ttu-id="34aca-151">Чтобы задать условия поиска, вызовите [**конфигурекарднамесеарч**](iscardlocate-configurecardnamesearch.md) , чтобы указать названия карт смарт-карт.</span><span class="sxs-lookup"><span data-stu-id="34aca-151">To set the search criteria of the search, call [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) to specify a smart card's card names.</span></span>

<span data-ttu-id="34aca-152">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардлокате**](iscardlocate.md).</span><span class="sxs-lookup"><span data-stu-id="34aca-152">For a list of all the methods provided by this interface, see [**ISCardLocate**](iscardlocate.md).</span></span>

<span data-ttu-id="34aca-153">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="34aca-153">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="34aca-154">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="34aca-154">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="34aca-155">Требования</span><span class="sxs-lookup"><span data-stu-id="34aca-155">Requirements</span></span>



| <span data-ttu-id="34aca-156">Требование</span><span class="sxs-lookup"><span data-stu-id="34aca-156">Requirement</span></span> | <span data-ttu-id="34aca-157">Значение</span><span class="sxs-lookup"><span data-stu-id="34aca-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34aca-158">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="34aca-158">Minimum supported client</span></span><br/> | <span data-ttu-id="34aca-159">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="34aca-159">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="34aca-160">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="34aca-160">Minimum supported server</span></span><br/> | <span data-ttu-id="34aca-161">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="34aca-161">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="34aca-162">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="34aca-162">End of client support</span></span><br/>    | <span data-ttu-id="34aca-163">Windows XP</span><span class="sxs-lookup"><span data-stu-id="34aca-163">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="34aca-164">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="34aca-164">End of server support</span></span><br/>    | <span data-ttu-id="34aca-165">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="34aca-165">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="34aca-166">Header</span><span class="sxs-lookup"><span data-stu-id="34aca-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="34aca-167"><dt>Скардмгр. h</dt></span><span class="sxs-lookup"><span data-stu-id="34aca-167"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="34aca-168">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="34aca-168">Type library</span></span><br/>             | <dl> <span data-ttu-id="34aca-169"><dt>Скардмгр. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="34aca-169"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="34aca-170">DLL</span><span class="sxs-lookup"><span data-stu-id="34aca-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34aca-171"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34aca-171"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="34aca-172">IID</span><span class="sxs-lookup"><span data-stu-id="34aca-172">IID</span></span><br/>                      | <span data-ttu-id="34aca-173">IID \_ искардлокате определен как 1461AACD-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="34aca-173">IID\_ISCardLocate is defined as 1461AACD-6810-11D0-918F-00AA00C18068</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="34aca-174">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34aca-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34aca-175">**конфигурекарднамесеарч**</span><span class="sxs-lookup"><span data-stu-id="34aca-175">**ConfigureCardNameSearch**</span></span>](iscardlocate-configurecardnamesearch.md)
</dt> <dt>

[<span data-ttu-id="34aca-176">**искардлокате**</span><span class="sxs-lookup"><span data-stu-id="34aca-176">**ISCardLocate**</span></span>](iscardlocate.md)
</dt> </dl>

 

 
