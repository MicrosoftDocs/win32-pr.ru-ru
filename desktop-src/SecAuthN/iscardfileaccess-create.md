---
description: Метод Create создает файл в указанном месте в файловой системе смарт-карты.
ms.assetid: 6bfe0b22-6aad-4818-bb2a-d5b0af4ee3a6
title: 'Метод Искардфилеакцесс:: Create'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Create
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2cfc7e1492505191a7912f23e5471f5fa72fdcd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145253"
---
# <a name="iscardfileaccesscreate-method"></a><span data-ttu-id="8463b-103">Метод Искардфилеакцесс:: Create</span><span class="sxs-lookup"><span data-stu-id="8463b-103">ISCardFileAccess::Create method</span></span>

<span data-ttu-id="8463b-104">\[Метод **CREATE** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="8463b-104">\[The **Create** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8463b-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="8463b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8463b-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="8463b-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="8463b-107">Метод **CREATE** создает файл в указанном месте в файловой системе [*смарт-карты*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="8463b-107">The **Create** method creates a file at a given location within the [*smart card*](../secgloss/s-gly.md) file system.</span></span>

## <a name="syntax"></a><span data-ttu-id="8463b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8463b-108">Syntax</span></span>


```C++
HRESULT Create(
  [in] REFTYPE      refType,
  [in] BSTR         bstrPathSpec,
  [in] TLV_TABLE    TLV,
  [in] SCARD_FLAGS  flags,
  [in] LPBYTEBUFFER pDataBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="8463b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8463b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8463b-110">*рефтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8463b-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8463b-111">Тип ссылки, используемый в *бстрпасспек*.</span><span class="sxs-lookup"><span data-stu-id="8463b-111">Type of reference used in *bstrPathSpec*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="8463b-112">**\_тип SC \_ по \_ имени**</span><span class="sxs-lookup"><span data-stu-id="8463b-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="8463b-113">**\_тип SC \_ по \_ идентификатору**</span><span class="sxs-lookup"><span data-stu-id="8463b-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="8463b-114">**SC \_ Type \_ по \_ короткому типу**</span><span class="sxs-lookup"><span data-stu-id="8463b-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="8463b-115">**SC \_ Type \_ по \_ любому**</span><span class="sxs-lookup"><span data-stu-id="8463b-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="8463b-116">*бстрпасспек* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8463b-116">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8463b-117">Идентификатор файла, создаваемого в текущем контексте.</span><span class="sxs-lookup"><span data-stu-id="8463b-117">File ID to be created within the current context.</span></span>

</dd> <dt>

<span data-ttu-id="8463b-118">*TLV* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8463b-118">*TLV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8463b-119">Список (тег, длина, значение) структур TLV, значения которых должны быть заданы.</span><span class="sxs-lookup"><span data-stu-id="8463b-119">List of TLV (tag,length,value) structures which values have to be set.</span></span>

</dd> <dt>

<span data-ttu-id="8463b-120">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8463b-120">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8463b-121">Указывает, следует ли использовать безопасный обмен сообщениями и предварительно выделенные данные.</span><span class="sxs-lookup"><span data-stu-id="8463b-121">Specifies whether secure messaging has to be used and data preallocated.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="8463b-122">**\_ \_ Защита \_ обмена сообщениями через SC FL**</span><span class="sxs-lookup"><span data-stu-id="8463b-122">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

<span data-ttu-id="8463b-123">**предварительно \_ \_ выделенный SC FL**</span><span class="sxs-lookup"><span data-stu-id="8463b-123">**SC\_FL\_PREALLOCATED**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="8463b-124">*пдатабуффер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8463b-124">*pDataBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8463b-125">Указатель на предварительно выделенные данные.</span><span class="sxs-lookup"><span data-stu-id="8463b-125">Pointer to preallocated data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8463b-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8463b-126">Return value</span></span>

<span data-ttu-id="8463b-127">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="8463b-127">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="8463b-128">Код возврата</span><span class="sxs-lookup"><span data-stu-id="8463b-128">Return code</span></span>                                                                                   | <span data-ttu-id="8463b-129">Описание</span><span class="sxs-lookup"><span data-stu-id="8463b-129">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="8463b-130"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="8463b-130"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8463b-131">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="8463b-131">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="8463b-132"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8463b-132"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="8463b-133">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="8463b-133">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="8463b-134"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="8463b-134"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8463b-135">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="8463b-135">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="8463b-136"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8463b-136"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8463b-137">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="8463b-137">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="8463b-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8463b-138">Remarks</span></span>

<span data-ttu-id="8463b-139">Список всех методов, определенных этим интерфейсом, см. в разделе [**искардфилеакцесс**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="8463b-139">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="8463b-140">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="8463b-140">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="8463b-141">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="8463b-141">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8463b-142">Требования</span><span class="sxs-lookup"><span data-stu-id="8463b-142">Requirements</span></span>



| <span data-ttu-id="8463b-143">Требование</span><span class="sxs-lookup"><span data-stu-id="8463b-143">Requirement</span></span> | <span data-ttu-id="8463b-144">Значение</span><span class="sxs-lookup"><span data-stu-id="8463b-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8463b-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8463b-145">Minimum supported client</span></span><br/> | <span data-ttu-id="8463b-146">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8463b-146">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="8463b-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8463b-147">Minimum supported server</span></span><br/> | <span data-ttu-id="8463b-148">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8463b-148">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8463b-149">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="8463b-149">End of client support</span></span><br/>    | <span data-ttu-id="8463b-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8463b-150">Windows XP</span></span><br/>                                |
| <span data-ttu-id="8463b-151">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="8463b-151">End of server support</span></span><br/>    | <span data-ttu-id="8463b-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8463b-152">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="8463b-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8463b-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8463b-154">**искардфилеакцесс**</span><span class="sxs-lookup"><span data-stu-id="8463b-154">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
