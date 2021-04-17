---
description: Получает параметры конфигурации EAPOL для указанного интерфейса беспроводной локальной сети.
ms.assetid: 3dce15be-879d-42e9-b8eb-96d52c004acb
title: Функция Взцеаполжетинтерфацепарамс (Взксапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCEapolGetInterfaceParams
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: bc89fd2defb75662fa90b5ed00c7969d483da590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674208"
---
# <a name="wzceapolgetinterfaceparams-function"></a><span data-ttu-id="69516-103">Функция Взцеаполжетинтерфацепарамс</span><span class="sxs-lookup"><span data-stu-id="69516-103">WZCEapolGetInterfaceParams function</span></span>

<span data-ttu-id="69516-104">\[**Взцеаполжетинтерфацепарамс** больше не поддерживается в Windows Vista и windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="69516-104">\[**WZCEapolGetInterfaceParams** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="69516-105">Вместо этого используйте [собственный интерфейс API Wi-Fi](native-wifi-reference.md), который предоставляет аналогичные функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="69516-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="69516-106">Дополнительные сведения см. [в статье о встроенном API Wi-Fi](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="69516-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="69516-107">Функция **взцеаполжетинтерфацепарамс** получает параметры конфигурации EAPOL для указанного интерфейса беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="69516-107">The **WZCEapolGetInterfaceParams** function gets EAPOL configuration parameters for the specified wireless LAN interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="69516-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="69516-108">Syntax</span></span>


```C++
DWORD WZCEapolGetInterfaceParams(
  _In_    LPWSTR            pSrvAddr,
  _In_    PWCHAR            pwszGuid,
  _In_    DWORD             dwSizeOfSSID,
  _In_    BYTE              *pbSSID,
  _Inout_ EAPOL_INTF_PARAMS *pIntfParams
);
```



## <a name="parameters"></a><span data-ttu-id="69516-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="69516-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69516-110">*псрваддр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="69516-110">*pSrvAddr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69516-111">Указатель на строку, содержащую имя компьютера, на котором должна быть выполнена эта функция.</span><span class="sxs-lookup"><span data-stu-id="69516-111">A pointer to a string containing the name of the computer on which to execute this function.</span></span> <span data-ttu-id="69516-112">Если этот параметр имеет **значение NULL**, то на локальном компьютере вызывается служба настройки беспроводной связи.</span><span class="sxs-lookup"><span data-stu-id="69516-112">If this parameter is **NULL**, then the Wireless Zero Configuration service is called on the local computer.</span></span>

<span data-ttu-id="69516-113">Если указанный параметр *псрваддр* является удаленным компьютером, удаленный компьютер должен поддерживать удаленные вызовы RPC.</span><span class="sxs-lookup"><span data-stu-id="69516-113">If the *pSrvAddr* parameter specified is a remote computer, then the remote computer must support remote RPC calls.</span></span>

</dd> <dt>

<span data-ttu-id="69516-114">*пвсзгуид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="69516-114">*pwszGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69516-115">Идентификатор GUID интерфейса, для которого должны быть получены данные.</span><span class="sxs-lookup"><span data-stu-id="69516-115">The GUID of the interface for which data is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="69516-116">*двсизеофссид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="69516-116">*dwSizeOfSSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69516-117">Размер сетевого идентификатора, для которого извлекаются данные.</span><span class="sxs-lookup"><span data-stu-id="69516-117">The size of the network identifier for which data is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="69516-118">*пбссид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="69516-118">*pbSSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69516-119">Указатель на идентификатор сети, для которого необходимо получить данные.</span><span class="sxs-lookup"><span data-stu-id="69516-119">A pointer to the network identifier for which data is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="69516-120">*пинтфпарамс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="69516-120">*pIntfParams* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="69516-121">Указатель на структуру [**\_ \_ params EAPOL intf**](eapol-intf-params.md) , содержащую параметры интерфейса.</span><span class="sxs-lookup"><span data-stu-id="69516-121">A pointer to a [**EAPOL\_INTF\_PARAMS**](eapol-intf-params.md) structure that contains interface parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69516-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="69516-122">Return value</span></span>

<span data-ttu-id="69516-123">Возвращает ошибку \_ при успешном завершении операции; в противном случае возвращает один из кодов системных ошибок Windows.</span><span class="sxs-lookup"><span data-stu-id="69516-123">Returns ERROR\_SUCCESS if the operation completes successfully; otherwise, returns one of the Windows system error codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="69516-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="69516-124">Remarks</span></span>

<span data-ttu-id="69516-125">Если **взцеаполжетинтерфацепарамс** возвращает ошибку \_ успешно, вызывающий объект должен вызвать [**функции LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) , чтобы освободить внутренние буферы, выделенные для данных, возвращаемых после того, как эти сведения больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="69516-125">If the **WZCEapolGetInterfaceParams** returns ERROR\_SUCCESS, the caller should call [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) to release the internal buffers allocated for the data returned once this information is no longer needed.</span></span>

> [!Note]  
> <span data-ttu-id="69516-126">Файл заголовка *взксапи. h* и файл библиотеки импорта *взксапи. lib* недоступны в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="69516-126">The *Wzcsapi.h* header file and *Wzcsapi.lib* import library file are not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="69516-127">Требования</span><span class="sxs-lookup"><span data-stu-id="69516-127">Requirements</span></span>



| <span data-ttu-id="69516-128">Требование</span><span class="sxs-lookup"><span data-stu-id="69516-128">Requirement</span></span> | <span data-ttu-id="69516-129">Значение</span><span class="sxs-lookup"><span data-stu-id="69516-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="69516-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="69516-130">Minimum supported client</span></span><br/> | <span data-ttu-id="69516-131">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="69516-131">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="69516-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="69516-132">Minimum supported server</span></span><br/> | <span data-ttu-id="69516-133">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="69516-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="69516-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="69516-134">End of client support</span></span><br/>    | <span data-ttu-id="69516-135">Windows XP с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="69516-135">Windows XP with SP3</span></span><br/>                                                         |
| <span data-ttu-id="69516-136">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="69516-136">End of server support</span></span><br/>    | <span data-ttu-id="69516-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="69516-137">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="69516-138">Header</span><span class="sxs-lookup"><span data-stu-id="69516-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="69516-139"><dt>Взксапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="69516-139"><dt>Wzcsapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="69516-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="69516-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="69516-141"><dt>Взксапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69516-141"><dt>Wzcsapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="69516-142">DLL</span><span class="sxs-lookup"><span data-stu-id="69516-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69516-143"><dt>Wzcsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69516-143"><dt>Wzcsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69516-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="69516-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69516-145">**взценуминтерфацес**</span><span class="sxs-lookup"><span data-stu-id="69516-145">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> <dt>

[<span data-ttu-id="69516-146">**взккуеринтерфаце**</span><span class="sxs-lookup"><span data-stu-id="69516-146">**WZCQueryInterface**</span></span>](wzcqueryinterface.md)
</dt> <dt>

[<span data-ttu-id="69516-147">**взкрефрешинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="69516-147">**WZCRefreshInterface**</span></span>](wzcrefreshinterface.md)
</dt> </dl>

 

 
