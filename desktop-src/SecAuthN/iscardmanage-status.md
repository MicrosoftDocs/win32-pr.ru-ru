---
description: Возвращает текущее состояние смарт-карты или модуля чтения.
ms.assetid: ae285e2e-6591-43ab-b92f-1ec755872379
title: 'Метод Искардманаже:: Status'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.Status
api_type:
- COM
api_location: ''
ms.openlocfilehash: 26683823b5b709d86b36f4345b47f306f2000ef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647276"
---
# <a name="iscardmanagestatus-method"></a><span data-ttu-id="0c4e1-103">Метод Искардманаже:: Status</span><span class="sxs-lookup"><span data-stu-id="0c4e1-103">ISCardManage::Status method</span></span>

<span data-ttu-id="0c4e1-104">\[Метод **Status** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="0c4e1-104">\[The **Status** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0c4e1-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="0c4e1-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0c4e1-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="0c4e1-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="0c4e1-107">Метод **Status** получает текущее состояние [*смарт-карты*](../secgloss/s-gly.md) или [*модуля чтения*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0c4e1-107">The **Status** method gets the current status of the [*smart card*](../secgloss/s-gly.md) or [*reader*](../secgloss/r-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0c4e1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c4e1-108">Syntax</span></span>


```C++
HRESULT Status(
  [out] SCARD_STATES    *pStatus,
  [out] SCARD_PROTOCOLS *pProtocols
);
```



## <a name="parameters"></a><span data-ttu-id="0c4e1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0c4e1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c4e1-110">*пстатус* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0c4e1-110">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c4e1-111">Указатель на \_ значение ПЕРЕЧИСЛЕНИЯ бросить States.</span><span class="sxs-lookup"><span data-stu-id="0c4e1-111">Pointer to an SCARD\_STATES enumeration value.</span></span> <span data-ttu-id="0c4e1-112">При возврате содержит текущее состояние или состояние.</span><span class="sxs-lookup"><span data-stu-id="0c4e1-112">On return, contains the current status/state.</span></span>

</dd> <dt>

<span data-ttu-id="0c4e1-113">*ппротоколс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0c4e1-113">*pProtocols* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c4e1-114">Указатель на \_ значение перечисления протоколов бросить.</span><span class="sxs-lookup"><span data-stu-id="0c4e1-114">Pointer to an SCARD\_PROTOCOLS enumeration value.</span></span> <span data-ttu-id="0c4e1-115">При возврате содержит текущий протокол.</span><span class="sxs-lookup"><span data-stu-id="0c4e1-115">On return, contains the current protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c4e1-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0c4e1-116">Return value</span></span>

<span data-ttu-id="0c4e1-117">Метод возвращает одно из следующих возможных значений:</span><span class="sxs-lookup"><span data-stu-id="0c4e1-117">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="0c4e1-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="0c4e1-118">Return code</span></span>                                                                                   | <span data-ttu-id="0c4e1-119">Описание</span><span class="sxs-lookup"><span data-stu-id="0c4e1-119">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="0c4e1-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="0c4e1-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0c4e1-121">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="0c4e1-121">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="0c4e1-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0c4e1-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="0c4e1-123">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="0c4e1-123">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="0c4e1-124"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="0c4e1-124"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="0c4e1-125">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="0c4e1-125">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="0c4e1-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0c4e1-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0c4e1-127">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="0c4e1-127">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="0c4e1-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0c4e1-128">Remarks</span></span>

<span data-ttu-id="0c4e1-129">Список всех методов, определенных этим интерфейсом, см. в разделе [**искардманаже**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="0c4e1-129">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="0c4e1-130">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="0c4e1-130">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="0c4e1-131">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="0c4e1-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0c4e1-132">Требования</span><span class="sxs-lookup"><span data-stu-id="0c4e1-132">Requirements</span></span>



| <span data-ttu-id="0c4e1-133">Требование</span><span class="sxs-lookup"><span data-stu-id="0c4e1-133">Requirement</span></span> | <span data-ttu-id="0c4e1-134">Значение</span><span class="sxs-lookup"><span data-stu-id="0c4e1-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0c4e1-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0c4e1-135">Minimum supported client</span></span><br/> | <span data-ttu-id="0c4e1-136">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0c4e1-136">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="0c4e1-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0c4e1-137">Minimum supported server</span></span><br/> | <span data-ttu-id="0c4e1-138">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0c4e1-138">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0c4e1-139">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="0c4e1-139">End of client support</span></span><br/>    | <span data-ttu-id="0c4e1-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0c4e1-140">Windows XP</span></span><br/>                                |
| <span data-ttu-id="0c4e1-141">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="0c4e1-141">End of server support</span></span><br/>    | <span data-ttu-id="0c4e1-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0c4e1-142">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="0c4e1-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0c4e1-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c4e1-144">**искардманаже**</span><span class="sxs-lookup"><span data-stu-id="0c4e1-144">**ISCardManage**</span></span>](iscardmanage.md)
</dt> </dl>

 

 
