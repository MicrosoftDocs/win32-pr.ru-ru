---
description: Метод Open открывает указанный файл для дальнейшего использования.
ms.assetid: a970daba-ed04-45f0-9b2d-3883807050df
title: 'Метод Искардфилеакцесс:: Open'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Open
api_type:
- COM
api_location: ''
ms.openlocfilehash: d1b68c004d4de308b641a1c4cb187312150f4d2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156302"
---
# <a name="iscardfileaccessopen-method"></a><span data-ttu-id="9285d-103">Метод Искардфилеакцесс:: Open</span><span class="sxs-lookup"><span data-stu-id="9285d-103">ISCardFileAccess::Open method</span></span>

<span data-ttu-id="9285d-104">\[Метод **Open** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="9285d-104">\[The **Open** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9285d-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="9285d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9285d-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="9285d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="9285d-107">Метод **Open** открывает указанный файл для дальнейшего использования.</span><span class="sxs-lookup"><span data-stu-id="9285d-107">The **Open** method opens the specified file for further use.</span></span>

## <a name="syntax"></a><span data-ttu-id="9285d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9285d-108">Syntax</span></span>


```C++
HRESULT Open(
  [in]  REFTYPE     refType,
  [in]  BSTR        bstrPathSpec,
  [out] HSCARD_FILE *phFile
);
```



## <a name="parameters"></a><span data-ttu-id="9285d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9285d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9285d-110">*рефтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9285d-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9285d-111">Тип ссылки, используемый в *бстрпасспек*.</span><span class="sxs-lookup"><span data-stu-id="9285d-111">Type of reference used in *bstrPathSpec*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="9285d-112">**\_тип SC \_ по \_ имени**</span><span class="sxs-lookup"><span data-stu-id="9285d-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="9285d-113">**\_тип SC \_ по \_ идентификатору**</span><span class="sxs-lookup"><span data-stu-id="9285d-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="9285d-114">**SC \_ Type \_ по \_ короткому типу**</span><span class="sxs-lookup"><span data-stu-id="9285d-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="9285d-115">**SC \_ Type \_ по \_ любому**</span><span class="sxs-lookup"><span data-stu-id="9285d-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="9285d-116">*бстрпасспек* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9285d-116">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9285d-117">Открываемый файл.</span><span class="sxs-lookup"><span data-stu-id="9285d-117">File to open.</span></span>

</dd> <dt>

<span data-ttu-id="9285d-118">*ффиле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9285d-118">*phFile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9285d-119">Указатель на файл ХСКАРД \_ , в котором будет храниться этот файл.</span><span class="sxs-lookup"><span data-stu-id="9285d-119">Pointer to an HSCARD\_FILE that will hold the file handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9285d-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9285d-120">Return value</span></span>

<span data-ttu-id="9285d-121">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="9285d-121">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="9285d-122">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9285d-122">Return code</span></span>                                                                                   | <span data-ttu-id="9285d-123">Описание</span><span class="sxs-lookup"><span data-stu-id="9285d-123">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="9285d-124"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="9285d-124"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9285d-125">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="9285d-125">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="9285d-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9285d-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="9285d-127">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="9285d-127">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="9285d-128"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="9285d-128"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="9285d-129">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="9285d-129">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="9285d-130"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="9285d-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9285d-131">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="9285d-131">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="9285d-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9285d-132">Remarks</span></span>

<span data-ttu-id="9285d-133">Чтобы закрыть файл, вызовите метод [**Close**](iscardfileaccess-close.md).</span><span class="sxs-lookup"><span data-stu-id="9285d-133">To close a file, call [**Close**](iscardfileaccess-close.md).</span></span>

<span data-ttu-id="9285d-134">Список всех методов, определенных этим интерфейсом, см. в разделе [**искардфилеакцесс**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="9285d-134">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="9285d-135">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="9285d-135">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="9285d-136">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="9285d-136">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9285d-137">Требования</span><span class="sxs-lookup"><span data-stu-id="9285d-137">Requirements</span></span>



| <span data-ttu-id="9285d-138">Требование</span><span class="sxs-lookup"><span data-stu-id="9285d-138">Requirement</span></span> | <span data-ttu-id="9285d-139">Значение</span><span class="sxs-lookup"><span data-stu-id="9285d-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9285d-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9285d-140">Minimum supported client</span></span><br/> | <span data-ttu-id="9285d-141">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9285d-141">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="9285d-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9285d-142">Minimum supported server</span></span><br/> | <span data-ttu-id="9285d-143">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9285d-143">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9285d-144">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="9285d-144">End of client support</span></span><br/>    | <span data-ttu-id="9285d-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9285d-145">Windows XP</span></span><br/>                                |
| <span data-ttu-id="9285d-146">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="9285d-146">End of server support</span></span><br/>    | <span data-ttu-id="9285d-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9285d-147">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="9285d-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9285d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9285d-149">**Закрыть**</span><span class="sxs-lookup"><span data-stu-id="9285d-149">**Close**</span></span>](iscardfileaccess-close.md)
</dt> <dt>

[<span data-ttu-id="9285d-150">**искардфилеакцесс**</span><span class="sxs-lookup"><span data-stu-id="9285d-150">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
