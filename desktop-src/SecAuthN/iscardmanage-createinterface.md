---
description: Создает указанный интерфейс.
ms.assetid: f4cfc407-b006-46a2-9751-834b532309ec
title: 'Метод Искардманаже:: Креатеинтерфаце'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateInterface
api_type:
- COM
api_location: ''
ms.openlocfilehash: 99a3f7c1acd4266395917b47c81f044d5385b3d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265809"
---
# <a name="iscardmanagecreateinterface-method"></a><span data-ttu-id="7ebd7-103">Метод Искардманаже:: Креатеинтерфаце</span><span class="sxs-lookup"><span data-stu-id="7ebd7-103">ISCardManage::CreateInterface method</span></span>

<span data-ttu-id="7ebd7-104">\[Метод **креатеинтерфаце** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="7ebd7-104">\[The **CreateInterface** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7ebd7-105">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="7ebd7-105">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="7ebd7-106">Метод **креатеинтерфаце** создает указанный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="7ebd7-106">The **CreateInterface** method creates the specified interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ebd7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ebd7-107">Syntax</span></span>


```C++
HRESULT CreateInterface(
  [in]  LPGUID    pguidInterface,
  [in]  BSTR      bstrName,
  [in]  LONG      *pUserData,
  [out] LPUNKNOWN *ppInterface
);
```



## <a name="parameters"></a><span data-ttu-id="7ebd7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ebd7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ebd7-109">*пгуидинтерфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7ebd7-109">*pguidInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ebd7-110">Значение GUID создаваемого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7ebd7-110">The GUID value of the interface to create.</span></span>

</dd> <dt>

<span data-ttu-id="7ebd7-111">*bstrName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7ebd7-111">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ebd7-112">Имя создаваемого интерфейса, если GUID недоступен.</span><span class="sxs-lookup"><span data-stu-id="7ebd7-112">The name of the interface to create if the GUID is unavailable.</span></span> <span data-ttu-id="7ebd7-113">Стандартные значения: "CryptoProvider".</span><span class="sxs-lookup"><span data-stu-id="7ebd7-113">Standard values are "CryptoProvider".</span></span>

</dd> <dt>

<span data-ttu-id="7ebd7-114">*пусердата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7ebd7-114">*pUserData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ebd7-115">Указатель на данные пользователя для использования при создании интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7ebd7-115">Pointer to user-specific data to use in the creation of an interface.</span></span>

</dd> <dt>

<span data-ttu-id="7ebd7-116">*ппинтерфаце* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7ebd7-116">*ppInterface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ebd7-117">Указатель на возвращаемый интерфейс.</span><span class="sxs-lookup"><span data-stu-id="7ebd7-117">Pointer to the returned interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ebd7-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ebd7-118">Return value</span></span>

<span data-ttu-id="7ebd7-119">Возможны следующие возвращаемые значения:</span><span class="sxs-lookup"><span data-stu-id="7ebd7-119">The possible return values are the following:</span></span>



| <span data-ttu-id="7ebd7-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7ebd7-120">Return code</span></span>                                                                                   | <span data-ttu-id="7ebd7-121">Описание</span><span class="sxs-lookup"><span data-stu-id="7ebd7-121">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7ebd7-122"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7ebd7-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7ebd7-123">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="7ebd7-123">Operation completed successfully.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="7ebd7-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7ebd7-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="7ebd7-125">Один из переданных параметров недопустим.</span><span class="sxs-lookup"><span data-stu-id="7ebd7-125">One of the supplied parameters are not valid.</span></span><br/>                                         |
| <dl> <span data-ttu-id="7ebd7-126"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="7ebd7-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7ebd7-127">Недопустимый указатель был передан в параметре *пгуидинтерфаце* или *пусердата* .</span><span class="sxs-lookup"><span data-stu-id="7ebd7-127">A bad pointer was passed in either the *pguidInterface* or the *pUserData* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="7ebd7-128"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7ebd7-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7ebd7-129">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="7ebd7-129">Out of memory.</span></span><br/>                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="7ebd7-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7ebd7-130">Remarks</span></span>

<span data-ttu-id="7ebd7-131">Список всех методов, определенных интерфейсом [**искардманаже**](iscardmanage.md) , см. в разделе **искардманаже**.</span><span class="sxs-lookup"><span data-stu-id="7ebd7-131">For a list of all the methods defined by the [**ISCardManage**](iscardmanage.md) interface, see **ISCardManage**.</span></span>

<span data-ttu-id="7ebd7-132">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="7ebd7-132">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="7ebd7-133">Дополнительные сведения о кодах ошибок смарт-карт см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="7ebd7-133">For information about smart card error codes, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7ebd7-134">Требования</span><span class="sxs-lookup"><span data-stu-id="7ebd7-134">Requirements</span></span>



| <span data-ttu-id="7ebd7-135">Требование</span><span class="sxs-lookup"><span data-stu-id="7ebd7-135">Requirement</span></span> | <span data-ttu-id="7ebd7-136">Значение</span><span class="sxs-lookup"><span data-stu-id="7ebd7-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7ebd7-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7ebd7-137">Minimum supported client</span></span><br/> | <span data-ttu-id="7ebd7-138">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7ebd7-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="7ebd7-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7ebd7-139">Minimum supported server</span></span><br/> | <span data-ttu-id="7ebd7-140">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7ebd7-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7ebd7-141">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="7ebd7-141">End of client support</span></span><br/>    | <span data-ttu-id="7ebd7-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7ebd7-142">Windows XP</span></span><br/>                                |
| <span data-ttu-id="7ebd7-143">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="7ebd7-143">End of server support</span></span><br/>    | <span data-ttu-id="7ebd7-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7ebd7-144">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="7ebd7-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7ebd7-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ebd7-146">**искардманаже**</span><span class="sxs-lookup"><span data-stu-id="7ebd7-146">**ISCardManage**</span></span>](iscardmanage.md)
</dt> </dl>

 

 
