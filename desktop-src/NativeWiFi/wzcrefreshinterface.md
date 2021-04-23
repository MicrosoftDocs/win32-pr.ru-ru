---
description: Обновляет сведения о интерфейсе для определенного интерфейса беспроводной локальной сети.
ms.assetid: 584b95b7-3218-4e3e-b5d9-9542488af16b
title: Функция Взкрефрешинтерфаце (Взксапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCRefreshInterface
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: 3f2ac1bd546403dca781b3a132b44f96d80bb5c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348112"
---
# <a name="wzcrefreshinterface-function"></a><span data-ttu-id="a433d-103">Функция Взкрефрешинтерфаце</span><span class="sxs-lookup"><span data-stu-id="a433d-103">WZCRefreshInterface function</span></span>

<span data-ttu-id="a433d-104">\[**Взкрефрешинтерфаце** не поддерживается в Windows Vista и windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="a433d-104">\[**WZCRefreshInterface** is not supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="a433d-105">Вместо этого используйте [собственный интерфейс API Wi-Fi](native-wifi-reference.md), который предоставляет аналогичные функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="a433d-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="a433d-106">Дополнительные сведения см. [в статье о встроенном API Wi-Fi](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="a433d-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="a433d-107">Функция **взкрефрешинтерфаце** обновляет сведения о интерфейсе для определенного интерфейса беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="a433d-107">The **WZCRefreshInterface** function refreshes interface information for a specific wireless LAN interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="a433d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a433d-108">Syntax</span></span>


```C++
DWORD WZCRefreshInterface(
  _In_  LPWSTR      pSrvAddr,
  _In_  DWORD       dwInFlags,
  _In_  PINTF_ENTRY pIntf,
  _Out_ LPDWORD     pdwOutFlags
);
```



## <a name="parameters"></a><span data-ttu-id="a433d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a433d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a433d-110">*псрваддр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a433d-110">*pSrvAddr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a433d-111">Указатель на строку, содержащую имя компьютера, на котором должна быть выполнена эта функция.</span><span class="sxs-lookup"><span data-stu-id="a433d-111">A pointer to a string containing the name of the computer on which to execute this function.</span></span> <span data-ttu-id="a433d-112">Если этот параметр имеет **значение NULL**, то на локальном компьютере вызывается служба настройки беспроводной связи.</span><span class="sxs-lookup"><span data-stu-id="a433d-112">If this parameter is **NULL**, then the Wireless Zero Configuration service is called on the local computer.</span></span>

<span data-ttu-id="a433d-113">Если указанный параметр *псрваддр* является удаленным компьютером, удаленный компьютер должен поддерживать удаленные вызовы RPC.</span><span class="sxs-lookup"><span data-stu-id="a433d-113">If the *pSrvAddr* parameter specified is a remote computer, then the remote computer must support remote RPC calls.</span></span>

</dd> <dt>

<span data-ttu-id="a433d-114">*двинфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a433d-114">*dwInFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a433d-115">Набор полей, которые будут обновляться вместе с конкретными действиями по обновлению.</span><span class="sxs-lookup"><span data-stu-id="a433d-115">A set of fields to be refreshed along with specific refresh actions to be taken.</span></span> <span data-ttu-id="a433d-116">Это битовая маска, которая может содержать любое сочетание следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="a433d-116">This is a bitmask that can contain any combination of the following flags.</span></span>



| <span data-ttu-id="a433d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a433d-117">Value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="a433d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="a433d-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <span data-ttu-id="a433d-119"><dt>**Intf \_ DESCR**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="a433d-119"><dt>**INTF\_DESCR**</dt> <dt>0x00010000</dt></span></span> </dl>             | <span data-ttu-id="a433d-120">Обновите описание интерфейса для интерфейса беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="a433d-120">Refresh the interface description for a wireless LAN interface.</span></span><br/> <span data-ttu-id="a433d-121">Обновленное описание интерфейса можно получить, вызвав функцию [**взккуеринтерфаце**](wzcqueryinterface.md) с установленным битом **intf \_ Descr** в параметре *двинфлагс* .</span><span class="sxs-lookup"><span data-stu-id="a433d-121">The refreshed interface description can be retrieved by calling the [**WZCQueryInterface**](wzcqueryinterface.md) function with the **INTF\_DESCR** bit set in the *dwInFlags* parameter.</span></span> <span data-ttu-id="a433d-122">Описание интерфейса возвращается в элементе **всздескр** структуры [**\_ записи intf**](intf-entry.md) , на которую указывает параметр *пинтф* , возвращаемый функцией **взккуеринтерфаце** .</span><span class="sxs-lookup"><span data-stu-id="a433d-122">The interface description is returned in the **wszDescr** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter that is returned by the **WZCQueryInterface** function.</span></span><br/>                                                           |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <span data-ttu-id="a433d-123"><dt>**Intf \_ НДИСМЕДИА**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="a433d-123"><dt>**INTF\_NDISMEDIA**</dt> <dt>0x00020000</dt></span></span> </dl> | <span data-ttu-id="a433d-124">Обновите сведения о носителе NDIS для интерфейса беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="a433d-124">Refresh the NDIS media information for a wireless LAN interface.</span></span><br/> <span data-ttu-id="a433d-125">Обновленные сведения о носителе NDIS можно получить, вызвав функцию [**взккуеринтерфаце**](wzcqueryinterface.md) с установленным битом **intf \_ Ндисмедиа** в параметре *двинфлагс* .</span><span class="sxs-lookup"><span data-stu-id="a433d-125">The refreshed NDIS media information can be retrieved by calling the [**WZCQueryInterface**](wzcqueryinterface.md) function with the **INTF\_NDISMEDIA** bit set in the *dwInFlags* parameter.</span></span> <span data-ttu-id="a433d-126">Сведения о медиа-файле NDIS возвращаются в элементах **улмедиастате**, **улмедиатипе** и **улфисикалмедиатипе** структуры [**\_ записи intf**](intf-entry.md) , на которую указывает параметр *пинтф* , возвращаемый функцией **взккуеринтерфаце** .</span><span class="sxs-lookup"><span data-stu-id="a433d-126">The NDIS media information is returned in the **ulMediaState**, **ulMediaType**, and **ulPhysicalMediaType** members of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter that is returned by the **WZCQueryInterface** function.</span></span><br/> |
| <span id="INTF_ALL_OIDS"></span><span id="intf_all_oids"></span><dl> <span data-ttu-id="a433d-127"><dt>**Intf \_ ВСЕ \_ идентификаторы OID**</dt> <dt>0xFFF00000</dt></span><span class="sxs-lookup"><span data-stu-id="a433d-127"><dt>**INTF\_ALL\_OIDS**</dt> <dt>0xFFF00000</dt></span></span> </dl>   | <span data-ttu-id="a433d-128">Обновите все идентификаторы (OID) NDIS для интерфейса беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="a433d-128">Refresh all of the NDIS OIDs for a wireless LAN interface.</span></span> <span data-ttu-id="a433d-129">Этот параметр обновляет большую часть данных для интерфейса беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="a433d-129">This option refreshes most of the data for a wireless LAN interface.</span></span><br/> <span data-ttu-id="a433d-130">Обновленные сведения можно получить, вызвав функцию [**взккуеринтерфаце**](wzcqueryinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="a433d-130">The refreshed information can be retrieved by calling the [**WZCQueryInterface**](wzcqueryinterface.md) function.</span></span><br/>                                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

<span data-ttu-id="a433d-131">*пинтф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a433d-131">*pIntf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a433d-132">Указатель на структуру [**\_ записи intf**](intf-entry.md) , содержащую ключ обновляемого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a433d-132">A pointer to an [**INTF\_ENTRY**](intf-entry.md) structure that contains the key of the interface to be refreshed.</span></span>

</dd> <dt>

<span data-ttu-id="a433d-133">*пдваутфлагс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a433d-133">*pdwOutFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a433d-134">Набор полей, которые были успешно обновлены.</span><span class="sxs-lookup"><span data-stu-id="a433d-134">A set of fields that were successfully refreshed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a433d-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a433d-135">Return value</span></span>

<span data-ttu-id="a433d-136">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="a433d-136">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="a433d-137">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="a433d-137">If the function fails, the return value may be one of the following return codes.</span></span>



| <span data-ttu-id="a433d-138">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a433d-138">Return code</span></span>                                                                                              | <span data-ttu-id="a433d-139">Описание</span><span class="sxs-lookup"><span data-stu-id="a433d-139">Description</span></span>                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a433d-140"><dt>**некоторая ошибка в \_ \_ корзине**</dt></span><span class="sxs-lookup"><span data-stu-id="a433d-140"><dt>**ERROR\_ARENA\_TRASHED**</dt></span></span> </dl>     | <span data-ttu-id="a433d-141">Блоки управления хранилищем были уничтожены.</span><span class="sxs-lookup"><span data-stu-id="a433d-141">The storage control blocks were destroyed.</span></span> <span data-ttu-id="a433d-142">Эта ошибка возвращается, если служба настройки беспроводной связи не инициализирует внутренние объекты.</span><span class="sxs-lookup"><span data-stu-id="a433d-142">This error is returned if the Wireless Zero Configuration service has not initialized internal objects.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="a433d-143"><dt>**\_файл ошибок \_ не \_ найден**</dt></span><span class="sxs-lookup"><span data-stu-id="a433d-143"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="a433d-144">Системе не удается найти указанный файл.</span><span class="sxs-lookup"><span data-stu-id="a433d-144">The system cannot find the file specified.</span></span> <span data-ttu-id="a433d-145">Эта ошибка возвращается, если идентификатор GUID в элементе **всзгуид** структуры [**\_ записи intf**](intf-entry.md) , на который указывает параметр *пинтф* , не соответствует ни одному из интерфейсов беспроводной локальной сети на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="a433d-145">This error is returned if the GUID in the **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter did not match any of the wireless LAN interfaces on the local computer.</span></span> <br/> |
| <dl> <span data-ttu-id="a433d-146"><dt>**Ошибка \_ недопустимого \_ параметра**</dt></span><span class="sxs-lookup"><span data-stu-id="a433d-146"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="a433d-147">Неверный параметр.</span><span class="sxs-lookup"><span data-stu-id="a433d-147">A parameter is incorrect.</span></span> <span data-ttu-id="a433d-148">Эта ошибка возвращается, если параметр *пинтф* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="a433d-148">This error is returned if the *pIntf* parameter is **NULL**.</span></span> <span data-ttu-id="a433d-149">Эта ошибка возвращается, если элемент **всзгуид** структуры [**\_ записи intf**](intf-entry.md) , на которую указывает параметр *пинтф* , имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="a433d-149">This error is returned if the **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter is **NULL**.</span></span> <br/>                            |
| <dl> <span data-ttu-id="a433d-150"><dt>**\_Состояние RPC**</dt></span><span class="sxs-lookup"><span data-stu-id="a433d-150"><dt>**RPC\_STATUS**</dt></span></span> </dl>               | <span data-ttu-id="a433d-151">Различные коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="a433d-151">Various error codes.</span></span><br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="a433d-152">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a433d-152">Remarks</span></span>

<span data-ttu-id="a433d-153">Элемент **всзгуид** структуры [**\_ записи intf**](intf-entry.md) , на который указывает параметр *пинтф* , должен содержать идентификатор GUID интерфейса для беспроводных локальных сетей.</span><span class="sxs-lookup"><span data-stu-id="a433d-153">The **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter must contain an interface GUID for a wireless LAN interface.</span></span> <span data-ttu-id="a433d-154">Список интерфейсов беспроводной локальной сети можно получить, вызвав функцию [**взценуминтерфацес**](wzcenuminterfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="a433d-154">A list of wireless LAN interfaces can be retrieved by calling the [**WZCEnumInterfaces**](wzcenuminterfaces.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="a433d-155">Файл заголовка *взксапи. h* и файл библиотеки импорта *взксапи. lib* недоступны в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="a433d-155">The *Wzcsapi.h* header file and *Wzcsapi.lib* import library file are not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a433d-156">Требования</span><span class="sxs-lookup"><span data-stu-id="a433d-156">Requirements</span></span>



| <span data-ttu-id="a433d-157">Требование</span><span class="sxs-lookup"><span data-stu-id="a433d-157">Requirement</span></span> | <span data-ttu-id="a433d-158">Значение</span><span class="sxs-lookup"><span data-stu-id="a433d-158">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a433d-159">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a433d-159">Minimum supported client</span></span><br/> | <span data-ttu-id="a433d-160">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a433d-160">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a433d-161">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a433d-161">Minimum supported server</span></span><br/> | <span data-ttu-id="a433d-162">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a433d-162">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a433d-163">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="a433d-163">End of client support</span></span><br/>    | <span data-ttu-id="a433d-164">Windows XP с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="a433d-164">Windows XP with SP3</span></span><br/>                                                         |
| <span data-ttu-id="a433d-165">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="a433d-165">End of server support</span></span><br/>    | <span data-ttu-id="a433d-166">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a433d-166">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="a433d-167">Header</span><span class="sxs-lookup"><span data-stu-id="a433d-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="a433d-168"><dt>Взксапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="a433d-168"><dt>Wzcsapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="a433d-169">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a433d-169">Library</span></span><br/>                  | <dl> <span data-ttu-id="a433d-170"><dt>Взксапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a433d-170"><dt>Wzcsapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="a433d-171">DLL</span><span class="sxs-lookup"><span data-stu-id="a433d-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a433d-172"><dt>Wzcsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a433d-172"><dt>Wzcsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a433d-173">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a433d-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a433d-174">**взцеаполжетинтерфацепарамс**</span><span class="sxs-lookup"><span data-stu-id="a433d-174">**WZCEapolGetInterfaceParams**</span></span>](wzceapolgetinterfaceparams.md)
</dt> <dt>

[<span data-ttu-id="a433d-175">**взценуминтерфацес**</span><span class="sxs-lookup"><span data-stu-id="a433d-175">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> <dt>

[<span data-ttu-id="a433d-176">**взккуеринтерфаце**</span><span class="sxs-lookup"><span data-stu-id="a433d-176">**WZCQueryInterface**</span></span>](wzcqueryinterface.md)
</dt> <dt>

[<span data-ttu-id="a433d-177">**\_запись intf**</span><span class="sxs-lookup"><span data-stu-id="a433d-177">**INTF\_ENTRY**</span></span>](intf-entry.md)
</dt> </dl>

 

 




