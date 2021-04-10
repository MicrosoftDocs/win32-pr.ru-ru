---
description: Метод Delete удаляет файл в указанном месте в файловой системе смарт-карты.
ms.assetid: f51b0329-c5dc-4f70-a92e-19dc0dbc55f8
title: Искардфилеакцесс::D удалить метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Delete
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6331225cd3baf105682e2d275ad6be53f16f5b64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343602"
---
# <a name="iscardfileaccessdelete-method"></a><span data-ttu-id="59a06-103">Искардфилеакцесс::D удалить метод</span><span class="sxs-lookup"><span data-stu-id="59a06-103">ISCardFileAccess::Delete method</span></span>

<span data-ttu-id="59a06-104">\[Метод **Delete** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="59a06-104">\[The **Delete** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="59a06-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="59a06-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="59a06-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="59a06-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="59a06-107">Метод **Delete** удаляет файл в указанном месте в файловой системе [*смарт-карты*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="59a06-107">The **Delete** method deletes a file at a given location within the [*smart card*](../secgloss/s-gly.md) file system.</span></span>

## <a name="syntax"></a><span data-ttu-id="59a06-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59a06-108">Syntax</span></span>


```C++
HRESULT Delete(
  [in] REFTYPE     refType,
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags
);
```



## <a name="parameters"></a><span data-ttu-id="59a06-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="59a06-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59a06-110">*рефтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="59a06-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59a06-111">Тип ссылки, используемый в *бстрпасспек*.</span><span class="sxs-lookup"><span data-stu-id="59a06-111">Type of reference used in *bstrPathSpec*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="59a06-112">**\_тип SC \_ по \_ имени**</span><span class="sxs-lookup"><span data-stu-id="59a06-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="59a06-113">**\_тип SC \_ по \_ идентификатору**</span><span class="sxs-lookup"><span data-stu-id="59a06-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="59a06-114">**SC \_ Type \_ по \_ короткому типу**</span><span class="sxs-lookup"><span data-stu-id="59a06-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="59a06-115">**SC \_ Type \_ по \_ любому**</span><span class="sxs-lookup"><span data-stu-id="59a06-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="59a06-116">*бстрпасспек* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="59a06-116">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59a06-117">Идентификатор удаляемого файла.</span><span class="sxs-lookup"><span data-stu-id="59a06-117">Identifier of the file to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="59a06-118">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="59a06-118">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59a06-119">Указывает, следует ли использовать безопасный обмен сообщениями и предварительно выделенные данные.</span><span class="sxs-lookup"><span data-stu-id="59a06-119">Specifies whether secure messaging has to be used and data preallocated.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="59a06-120">**\_ \_ Защита \_ обмена сообщениями через SC FL**</span><span class="sxs-lookup"><span data-stu-id="59a06-120">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

<span data-ttu-id="59a06-121">**предварительно \_ \_ выделенный SC FL**</span><span class="sxs-lookup"><span data-stu-id="59a06-121">**SC\_FL\_PREALLOCATED**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59a06-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="59a06-122">Return value</span></span>

<span data-ttu-id="59a06-123">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="59a06-123">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="59a06-124">Код возврата</span><span class="sxs-lookup"><span data-stu-id="59a06-124">Return code</span></span>                                                                                  | <span data-ttu-id="59a06-125">Описание</span><span class="sxs-lookup"><span data-stu-id="59a06-125">Description</span></span>                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="59a06-126"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="59a06-126"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="59a06-127">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="59a06-127">Operation was completed successfully.</span></span><br/>          |
| <dl> <span data-ttu-id="59a06-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="59a06-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="59a06-129">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="59a06-129">Invalid parameter.</span></span><br/>                             |
| <dl> <span data-ttu-id="59a06-130"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="59a06-130"><dt>**E\_NOTIMPL**</dt></span></span> </dl>    | <span data-ttu-id="59a06-131">Этот метод не реализован в интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="59a06-131">The interface has not implemented this method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="59a06-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="59a06-132">Remarks</span></span>

<span data-ttu-id="59a06-133">Список всех методов, определенных этим интерфейсом, см. в разделе [**искардфилеакцесс**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="59a06-133">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="59a06-134">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="59a06-134">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="59a06-135">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="59a06-135">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="59a06-136">Требования</span><span class="sxs-lookup"><span data-stu-id="59a06-136">Requirements</span></span>



| <span data-ttu-id="59a06-137">Требование</span><span class="sxs-lookup"><span data-stu-id="59a06-137">Requirement</span></span> | <span data-ttu-id="59a06-138">Значение</span><span class="sxs-lookup"><span data-stu-id="59a06-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="59a06-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="59a06-139">Minimum supported client</span></span><br/> | <span data-ttu-id="59a06-140">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="59a06-140">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="59a06-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="59a06-141">Minimum supported server</span></span><br/> | <span data-ttu-id="59a06-142">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="59a06-142">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="59a06-143">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="59a06-143">End of client support</span></span><br/>    | <span data-ttu-id="59a06-144">Windows XP</span><span class="sxs-lookup"><span data-stu-id="59a06-144">Windows XP</span></span><br/>                                |
| <span data-ttu-id="59a06-145">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="59a06-145">End of server support</span></span><br/>    | <span data-ttu-id="59a06-146">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="59a06-146">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="59a06-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="59a06-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59a06-148">**Создать**</span><span class="sxs-lookup"><span data-stu-id="59a06-148">**Create**</span></span>](iscardfileaccess-create.md)
</dt> <dt>

[<span data-ttu-id="59a06-149">**искардфилеакцесс**</span><span class="sxs-lookup"><span data-stu-id="59a06-149">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
