---
description: Метод Чанжедир изменяет текущий каталог смарт-карты на новый указанный каталог.
ms.assetid: 1eb53236-c88f-4b43-ac91-de67d4029433
title: 'Метод Искардфилеакцесс:: Чанжедир'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.ChangeDir
api_type:
- COM
api_location: ''
ms.openlocfilehash: 147456bd705eea3073f2e65cb375494187ca2473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897397"
---
# <a name="iscardfileaccesschangedir-method"></a><span data-ttu-id="a3b8a-103">Метод Искардфилеакцесс:: Чанжедир</span><span class="sxs-lookup"><span data-stu-id="a3b8a-103">ISCardFileAccess::ChangeDir method</span></span>

<span data-ttu-id="a3b8a-104">\[Метод **чанжедир** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="a3b8a-104">\[The **ChangeDir** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a3b8a-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="a3b8a-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a3b8a-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="a3b8a-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="a3b8a-107">Метод **чанжедир** изменяет текущий каталог [*смарт-карты*](../secgloss/s-gly.md) на новый указанный каталог.</span><span class="sxs-lookup"><span data-stu-id="a3b8a-107">The **ChangeDir** method changes the current [*smart card*](../secgloss/s-gly.md) directory to the new specified directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3b8a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3b8a-108">Syntax</span></span>


```C++
HRESULT ChangeDir(
  [in] REFTYPE refType,
  [in] BSTR    bstrNewDir
);
```



## <a name="parameters"></a><span data-ttu-id="a3b8a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3b8a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3b8a-110">*рефтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a3b8a-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3b8a-111">Тип ссылки, используемый в *бстрневдир*.</span><span class="sxs-lookup"><span data-stu-id="a3b8a-111">Type of reference used in *bstrNewDir*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="a3b8a-112">**\_тип SC \_ по \_ имени**</span><span class="sxs-lookup"><span data-stu-id="a3b8a-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="a3b8a-113">**\_тип SC \_ по \_ идентификатору**</span><span class="sxs-lookup"><span data-stu-id="a3b8a-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="a3b8a-114">**SC \_ Type \_ по \_ короткому типу**</span><span class="sxs-lookup"><span data-stu-id="a3b8a-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="a3b8a-115">**SC \_ Type \_ по \_ любому**</span><span class="sxs-lookup"><span data-stu-id="a3b8a-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="a3b8a-116">*бстрневдир* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a3b8a-116">*bstrNewDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3b8a-117">Имя файла или каталога ( *рефтипе*) для выбора.</span><span class="sxs-lookup"><span data-stu-id="a3b8a-117">File/directory name (by *refType*) to select.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3b8a-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a3b8a-118">Return value</span></span>

<span data-ttu-id="a3b8a-119">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="a3b8a-119">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="a3b8a-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a3b8a-120">Return code</span></span>                                                                                   | <span data-ttu-id="a3b8a-121">Описание</span><span class="sxs-lookup"><span data-stu-id="a3b8a-121">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a3b8a-122"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a3b8a-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a3b8a-123">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="a3b8a-123">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="a3b8a-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a3b8a-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a3b8a-125">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="a3b8a-125">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="a3b8a-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a3b8a-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a3b8a-127">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="a3b8a-127">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="a3b8a-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a3b8a-128">Remarks</span></span>

<span data-ttu-id="a3b8a-129">Чтобы получить абсолютный путь к текущему выбранному каталогу, вызовите [**жеткуррентдир**](iscardfileaccess-getcurrentdir.md).</span><span class="sxs-lookup"><span data-stu-id="a3b8a-129">To get an absolute path to the currently selected directory, call [**GetCurrentDir**](iscardfileaccess-getcurrentdir.md).</span></span>

<span data-ttu-id="a3b8a-130">Список всех методов, определенных этим интерфейсом, см. в разделе [**искардфилеакцесс**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="a3b8a-130">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="a3b8a-131">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="a3b8a-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="a3b8a-132">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="a3b8a-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a3b8a-133">Требования</span><span class="sxs-lookup"><span data-stu-id="a3b8a-133">Requirements</span></span>



| <span data-ttu-id="a3b8a-134">Требование</span><span class="sxs-lookup"><span data-stu-id="a3b8a-134">Requirement</span></span> | <span data-ttu-id="a3b8a-135">Значение</span><span class="sxs-lookup"><span data-stu-id="a3b8a-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a3b8a-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a3b8a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a3b8a-137">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a3b8a-137">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="a3b8a-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a3b8a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a3b8a-139">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a3b8a-139">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a3b8a-140">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="a3b8a-140">End of client support</span></span><br/>    | <span data-ttu-id="a3b8a-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a3b8a-141">Windows XP</span></span><br/>                                |
| <span data-ttu-id="a3b8a-142">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="a3b8a-142">End of server support</span></span><br/>    | <span data-ttu-id="a3b8a-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a3b8a-143">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="a3b8a-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3b8a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3b8a-145">**жеткуррентдир**</span><span class="sxs-lookup"><span data-stu-id="a3b8a-145">**GetCurrentDir**</span></span>](iscardfileaccess-getcurrentdir.md)
</dt> <dt>

[<span data-ttu-id="a3b8a-146">**искардфилеакцесс**</span><span class="sxs-lookup"><span data-stu-id="a3b8a-146">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
