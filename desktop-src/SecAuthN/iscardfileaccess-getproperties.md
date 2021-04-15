---
description: Получает примитивные данные, на которые ссылается ТЛВС (тег, длина, значение) для указанного объекта.
ms.assetid: 135aeb9a-b851-4522-862f-02a7e020c36b
title: 'Метод Искардфилеакцесс:: Properties'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.GetProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: 25e6ae1ab657d92dda0ad421b650eaaa7076bd63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647469"
---
# <a name="iscardfileaccessgetproperties-method"></a><span data-ttu-id="325db-103">Метод Искардфилеакцесс:: Properties</span><span class="sxs-lookup"><span data-stu-id="325db-103">ISCardFileAccess::GetProperties method</span></span>

<span data-ttu-id="325db-104">\[Метод **Properties** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="325db-104">\[The **GetProperties** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="325db-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="325db-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="325db-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="325db-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="325db-107">Метод **GetObject** извлекает примитивные данные, на которые ссылается ТЛВС (тег, длина, значение) для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="325db-107">The **GetProperties** method retrieves the primitive data referred by TLVs (tag, length, value) for the specified object.</span></span>

## <a name="syntax"></a><span data-ttu-id="325db-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="325db-108">Syntax</span></span>


```C++
HRESULT GetProperties(
  [in]      REFTYPE     refType,
  [in]      BSTR        bstrPathSpec,
  [in]      SCARD_FLAGS flags,
  [in, out] LPTLV_TABLE *ppTLV
);
```



## <a name="parameters"></a><span data-ttu-id="325db-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="325db-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="325db-110">*рефтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="325db-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="325db-111">Тип ссылки, используемый в *бстрневдир*.</span><span class="sxs-lookup"><span data-stu-id="325db-111">Type of reference used in *bstrNewDir*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="325db-112">**\_тип SC \_ по \_ имени**</span><span class="sxs-lookup"><span data-stu-id="325db-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="325db-113">**\_тип SC \_ по \_ идентификатору**</span><span class="sxs-lookup"><span data-stu-id="325db-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="325db-114">**SC \_ Type \_ по \_ короткому типу**</span><span class="sxs-lookup"><span data-stu-id="325db-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="325db-115">**SC \_ Type \_ по \_ любому**</span><span class="sxs-lookup"><span data-stu-id="325db-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="325db-116">*бстрпасспек* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="325db-116">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="325db-117">File.</span><span class="sxs-lookup"><span data-stu-id="325db-117">File.</span></span>

</dd> <dt>

<span data-ttu-id="325db-118">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="325db-118">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="325db-119">Указывает, следует ли использовать безопасный обмен сообщениями.</span><span class="sxs-lookup"><span data-stu-id="325db-119">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="325db-120">**\_ \_ Защита \_ обмена сообщениями через SC FL**</span><span class="sxs-lookup"><span data-stu-id="325db-120">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="325db-121">*пптлв* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="325db-121">*ppTLV* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="325db-122">Указатель на TLV структуры, значение которых было получено.</span><span class="sxs-lookup"><span data-stu-id="325db-122">Pointer to TLV structures whose value has been retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="325db-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="325db-123">Return value</span></span>

<span data-ttu-id="325db-124">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="325db-124">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="325db-125">Код возврата</span><span class="sxs-lookup"><span data-stu-id="325db-125">Return code</span></span>                                                                                   | <span data-ttu-id="325db-126">Описание</span><span class="sxs-lookup"><span data-stu-id="325db-126">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="325db-127"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="325db-127"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="325db-128">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="325db-128">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="325db-129"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="325db-129"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="325db-130">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="325db-130">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="325db-131"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="325db-131"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="325db-132">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="325db-132">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="325db-133"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="325db-133"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="325db-134">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="325db-134">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="325db-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="325db-135">Remarks</span></span>

<span data-ttu-id="325db-136">Список всех методов, определенных этим интерфейсом, см. в разделе [**искардфилеакцесс**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="325db-136">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="325db-137">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="325db-137">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="325db-138">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="325db-138">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="325db-139">Требования</span><span class="sxs-lookup"><span data-stu-id="325db-139">Requirements</span></span>



| <span data-ttu-id="325db-140">Требование</span><span class="sxs-lookup"><span data-stu-id="325db-140">Requirement</span></span> | <span data-ttu-id="325db-141">Значение</span><span class="sxs-lookup"><span data-stu-id="325db-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="325db-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="325db-142">Minimum supported client</span></span><br/> | <span data-ttu-id="325db-143">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="325db-143">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="325db-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="325db-144">Minimum supported server</span></span><br/> | <span data-ttu-id="325db-145">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="325db-145">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="325db-146">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="325db-146">End of client support</span></span><br/>    | <span data-ttu-id="325db-147">Windows XP</span><span class="sxs-lookup"><span data-stu-id="325db-147">Windows XP</span></span><br/>                                |
| <span data-ttu-id="325db-148">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="325db-148">End of server support</span></span><br/>    | <span data-ttu-id="325db-149">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="325db-149">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="325db-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="325db-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="325db-151">**искардфилеакцесс**</span><span class="sxs-lookup"><span data-stu-id="325db-151">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
