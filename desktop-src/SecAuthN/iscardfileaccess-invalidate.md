---
description: Делает указанный файл (EF или DF) недопустимым. Недопустимый файл не может быть доступен другим методам до использования Рехабилитате.
ms.assetid: 5600fcf0-091c-437e-a45c-4de5b0a47d68
title: 'Метод Искардфилеакцесс:: unvalidate'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Invalidate
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3e1d74885f97eca64f403155f1dba52e398b9426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651027"
---
# <a name="iscardfileaccessinvalidate-method"></a><span data-ttu-id="d8b99-104">Метод Искардфилеакцесс:: unvalidate</span><span class="sxs-lookup"><span data-stu-id="d8b99-104">ISCardFileAccess::Invalidate method</span></span>

<span data-ttu-id="d8b99-105">\[Метод **Validate** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="d8b99-105">\[The **Invalidate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d8b99-106">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d8b99-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d8b99-107">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="d8b99-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d8b99-108">Метод **unvalidate** делает указанный файл (EF или DF) недопустимым.</span><span class="sxs-lookup"><span data-stu-id="d8b99-108">The **Invalidate** method makes the specified file (EF or DF) not valid.</span></span> <span data-ttu-id="d8b99-109">Недопустимый файл не может быть доступен другим методам до использования [**рехабилитате**](iscardfileaccess-rehabilitate.md).</span><span class="sxs-lookup"><span data-stu-id="d8b99-109">A file that is not valid cannot be accessed by other methods prior to using [**Rehabilitate**](iscardfileaccess-rehabilitate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d8b99-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d8b99-110">Syntax</span></span>


```C++
HRESULT Invalidate(
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags
);
```



## <a name="parameters"></a><span data-ttu-id="d8b99-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8b99-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8b99-112">*бстрпасспек* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8b99-112">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8b99-113">File.</span><span class="sxs-lookup"><span data-stu-id="d8b99-113">File.</span></span>

</dd> <dt>

<span data-ttu-id="d8b99-114">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8b99-114">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8b99-115">Указывает, следует ли использовать безопасный обмен сообщениями.</span><span class="sxs-lookup"><span data-stu-id="d8b99-115">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="d8b99-116">**\_ \_ Защита \_ обмена сообщениями через SC FL**</span><span class="sxs-lookup"><span data-stu-id="d8b99-116">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8b99-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d8b99-117">Return value</span></span>

<span data-ttu-id="d8b99-118">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="d8b99-118">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="d8b99-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d8b99-119">Return code</span></span>                                                                                   | <span data-ttu-id="d8b99-120">Описание</span><span class="sxs-lookup"><span data-stu-id="d8b99-120">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="d8b99-121"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="d8b99-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d8b99-122">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="d8b99-122">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="d8b99-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d8b99-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d8b99-124">Недействительный параметр.</span><span class="sxs-lookup"><span data-stu-id="d8b99-124">A parameter is not valid.</span></span><br/>         |
| <dl> <span data-ttu-id="d8b99-125"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="d8b99-125"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d8b99-126">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="d8b99-126">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="d8b99-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d8b99-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d8b99-128">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="d8b99-128">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="d8b99-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d8b99-129">Remarks</span></span>

<span data-ttu-id="d8b99-130">Список всех методов, определенных этим интерфейсом, см. в разделе [**искардфилеакцесс**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="d8b99-130">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="d8b99-131">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="d8b99-131">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="d8b99-132">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="d8b99-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d8b99-133">Требования</span><span class="sxs-lookup"><span data-stu-id="d8b99-133">Requirements</span></span>



| <span data-ttu-id="d8b99-134">Требование</span><span class="sxs-lookup"><span data-stu-id="d8b99-134">Requirement</span></span> | <span data-ttu-id="d8b99-135">Значение</span><span class="sxs-lookup"><span data-stu-id="d8b99-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d8b99-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d8b99-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d8b99-137">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d8b99-137">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="d8b99-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d8b99-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d8b99-139">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d8b99-139">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d8b99-140">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d8b99-140">End of client support</span></span><br/>    | <span data-ttu-id="d8b99-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d8b99-141">Windows XP</span></span><br/>                                |
| <span data-ttu-id="d8b99-142">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="d8b99-142">End of server support</span></span><br/>    | <span data-ttu-id="d8b99-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d8b99-143">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="d8b99-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d8b99-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8b99-145">**искардфилеакцесс**</span><span class="sxs-lookup"><span data-stu-id="d8b99-145">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> <dt>

[<span data-ttu-id="d8b99-146">**рехабилитате**</span><span class="sxs-lookup"><span data-stu-id="d8b99-146">**Rehabilitate**</span></span>](iscardfileaccess-rehabilitate.md)
</dt> </dl>

 

 
