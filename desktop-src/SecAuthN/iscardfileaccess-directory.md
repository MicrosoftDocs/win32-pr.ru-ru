---
description: Метод Directory извлекает из текущего каталога список файлов указанного типа.
ms.assetid: 0ae89811-7534-497b-af9f-ae37a48bc3e5
title: 'Искардфилеакцесс: метод:D каталога'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Directory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 74293d4fa97a61133739cac75f17eaffed6e52b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898817"
---
# <a name="iscardfileaccessdirectory-method"></a><span data-ttu-id="2e1bd-103">Искардфилеакцесс: метод:D каталога</span><span class="sxs-lookup"><span data-stu-id="2e1bd-103">ISCardFileAccess::Directory method</span></span>

<span data-ttu-id="2e1bd-104">\[Метод **Directory** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="2e1bd-104">\[The **Directory** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2e1bd-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2e1bd-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2e1bd-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="2e1bd-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="2e1bd-107">Метод **Directory** извлекает из текущего каталога список файлов указанного типа.</span><span class="sxs-lookup"><span data-stu-id="2e1bd-107">The **Directory** method retrieves a list of files of the specified type from the current directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e1bd-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e1bd-108">Syntax</span></span>


```C++
HRESULT Directory(
  [in]  FILETYPE    fileType,
  [out] LPSAFEARRAY *ppFileList
);
```



## <a name="parameters"></a><span data-ttu-id="2e1bd-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2e1bd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e1bd-110">*тип* \[ файла окне\]</span><span class="sxs-lookup"><span data-stu-id="2e1bd-110">*fileType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e1bd-111">Тип файлов [*смарт-карты*](../secgloss/s-gly.md) для перечисления.</span><span class="sxs-lookup"><span data-stu-id="2e1bd-111">Type of [*smart card*](../secgloss/s-gly.md) files to list.</span></span>



| <span data-ttu-id="2e1bd-112">Значение</span><span class="sxs-lookup"><span data-stu-id="2e1bd-112">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="2e1bd-113">Значение</span><span class="sxs-lookup"><span data-stu-id="2e1bd-113">Meaning</span></span>                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="SC_TYPE_DIRECTORIES"></span><span id="sc_type_directories"></span><dl> <span data-ttu-id="2e1bd-114"><dt>**\_каталоги типов \_ SC**</dt></span><span class="sxs-lookup"><span data-stu-id="2e1bd-114"><dt>**SC\_TYPE\_DIRECTORIES**</dt></span></span> </dl>           | <span data-ttu-id="2e1bd-115">Вывод списка только файлов каталога.</span><span class="sxs-lookup"><span data-stu-id="2e1bd-115">List directory files only.</span></span><br/>                |
| <span id="SC_TYPE_FILES"></span><span id="sc_type_files"></span><dl> <span data-ttu-id="2e1bd-116"><dt>**\_файлы типов \_ SC**</dt></span><span class="sxs-lookup"><span data-stu-id="2e1bd-116"><dt>**SC\_TYPE\_FILES**</dt></span></span> </dl>                             | <span data-ttu-id="2e1bd-117">Перечисление только простейших файлов.</span><span class="sxs-lookup"><span data-stu-id="2e1bd-117">List elementary files only.</span></span><br/>               |
| <span id="SC_TYPE_ALL_FILES"></span><span id="sc_type_all_files"></span><dl> <span data-ttu-id="2e1bd-118"><dt>**SC \_ Type \_ All \_ Files**</dt></span><span class="sxs-lookup"><span data-stu-id="2e1bd-118"><dt>**SC\_TYPE\_ALL\_FILES**</dt></span></span> </dl>                | <span data-ttu-id="2e1bd-119">Перечислите каталог и простейшие файлы.</span><span class="sxs-lookup"><span data-stu-id="2e1bd-119">List both directory and elementary files.</span></span><br/> |
| <span id="SC_TYPE_DIRECTORY_FILE"></span><span id="sc_type_directory_file"></span><dl> <span data-ttu-id="2e1bd-120"><dt>**SC \_ тип \_ \_ файл каталога**</dt></span><span class="sxs-lookup"><span data-stu-id="2e1bd-120"><dt>**SC\_TYPE\_DIRECTORY\_FILE**</dt></span></span> </dl> | <span data-ttu-id="2e1bd-121">Файл каталога.</span><span class="sxs-lookup"><span data-stu-id="2e1bd-121">Directory file.</span></span><br/>                           |
| <span id="SC_TYPE_TRANSPARENT_EF"></span><span id="sc_type_transparent_ef"></span><dl> <span data-ttu-id="2e1bd-122"><dt>**SC \_ \_ прозрачный тип \_ EF**</dt></span><span class="sxs-lookup"><span data-stu-id="2e1bd-122"><dt>**SC\_TYPE\_TRANSPARENT\_EF**</dt></span></span> </dl> | <span data-ttu-id="2e1bd-123">Прозрачный простой файл.</span><span class="sxs-lookup"><span data-stu-id="2e1bd-123">Transparent elementary file.</span></span><br/>              |
| <span id="SC_TYPE_FIXED_EF"></span><span id="sc_type_fixed_ef"></span><dl> <span data-ttu-id="2e1bd-124"><dt>**\_тип SC \_ фиксированный \_ EF**</dt></span><span class="sxs-lookup"><span data-stu-id="2e1bd-124"><dt>**SC\_TYPE\_FIXED\_EF**</dt></span></span> </dl>                   | <span data-ttu-id="2e1bd-125">Линейный фиксированный файл простой.</span><span class="sxs-lookup"><span data-stu-id="2e1bd-125">Linear fixed elementary file.</span></span><br/>             |
| <span id="SC_TYPE_CYCLIC_EF"></span><span id="sc_type_cyclic_ef"></span><dl> <span data-ttu-id="2e1bd-126"><dt>**\_ \_ циклическая ссылка на тип SC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2e1bd-126"><dt>**SC\_TYPE\_CYCLIC\_EF**</dt></span></span> </dl>                | <span data-ttu-id="2e1bd-127">Циклический простой файл.</span><span class="sxs-lookup"><span data-stu-id="2e1bd-127">Cyclic elementary file.</span></span><br/>                   |
| <span id="SC_TYPE_VARIABLE_EF"></span><span id="sc_type_variable_ef"></span><dl> <span data-ttu-id="2e1bd-128"><dt>**\_переменная типа \_ SC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2e1bd-128"><dt>**SC\_TYPE\_VARIABLE\_EF**</dt></span></span> </dl>          | <span data-ttu-id="2e1bd-129">Простой файл с линейной переменной.</span><span class="sxs-lookup"><span data-stu-id="2e1bd-129">Linear variable elementary file.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="2e1bd-130">*ппфилелист* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2e1bd-130">*ppFileList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e1bd-131">Массив BSTR, представляющий список файлов, соответствующих спецификатору в *filetype*.</span><span class="sxs-lookup"><span data-stu-id="2e1bd-131">Array of BSTRs representing the list of files matching the specifier in *fileType*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e1bd-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2e1bd-132">Return value</span></span>

<span data-ttu-id="2e1bd-133">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="2e1bd-133">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="2e1bd-134">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2e1bd-134">Return code</span></span>                                                                                   | <span data-ttu-id="2e1bd-135">Описание</span><span class="sxs-lookup"><span data-stu-id="2e1bd-135">Description</span></span>                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="2e1bd-136"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="2e1bd-136"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2e1bd-137">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="2e1bd-137">Operation was completed successfully.</span></span><br/>          |
| <dl> <span data-ttu-id="2e1bd-138"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2e1bd-138"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="2e1bd-139">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="2e1bd-139">Invalid parameter.</span></span><br/>                             |
| <dl> <span data-ttu-id="2e1bd-140"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="2e1bd-140"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="2e1bd-141">Этот метод не реализован в интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="2e1bd-141">The interface has not implemented this method.</span></span><br/> |
| <dl> <span data-ttu-id="2e1bd-142"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2e1bd-142"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2e1bd-143">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="2e1bd-143">Out of memory.</span></span><br/>                                 |
| <dl> <span data-ttu-id="2e1bd-144"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="2e1bd-144"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="2e1bd-145">Для *ппфилелист* был передан недопустимый указатель.</span><span class="sxs-lookup"><span data-stu-id="2e1bd-145">A bad pointer was passed in for *ppFileList*.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="2e1bd-146">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2e1bd-146">Remarks</span></span>

<span data-ttu-id="2e1bd-147">Список всех методов, определенных этим интерфейсом, см. в разделе [**искардфилеакцесс**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="2e1bd-147">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="2e1bd-148">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="2e1bd-148">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="2e1bd-149">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="2e1bd-149">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e1bd-150">Требования</span><span class="sxs-lookup"><span data-stu-id="2e1bd-150">Requirements</span></span>



| <span data-ttu-id="2e1bd-151">Требование</span><span class="sxs-lookup"><span data-stu-id="2e1bd-151">Requirement</span></span> | <span data-ttu-id="2e1bd-152">Значение</span><span class="sxs-lookup"><span data-stu-id="2e1bd-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2e1bd-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2e1bd-153">Minimum supported client</span></span><br/> | <span data-ttu-id="2e1bd-154">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2e1bd-154">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="2e1bd-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2e1bd-155">Minimum supported server</span></span><br/> | <span data-ttu-id="2e1bd-156">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2e1bd-156">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2e1bd-157">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="2e1bd-157">End of client support</span></span><br/>    | <span data-ttu-id="2e1bd-158">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2e1bd-158">Windows XP</span></span><br/>                                |
| <span data-ttu-id="2e1bd-159">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="2e1bd-159">End of server support</span></span><br/>    | <span data-ttu-id="2e1bd-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2e1bd-160">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="2e1bd-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e1bd-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e1bd-162">**искардфилеакцесс**</span><span class="sxs-lookup"><span data-stu-id="2e1bd-162">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
