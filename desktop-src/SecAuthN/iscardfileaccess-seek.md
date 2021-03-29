---
description: Метод Seek выбирает объект, из которого будет осуществляться доступ (чтение и запись).
ms.assetid: 9e06df70-6415-46dd-b34f-59614d1cbee7
title: 'Метод Искардфилеакцесс:: Seek'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Seek
api_type:
- COM
api_location: ''
ms.openlocfilehash: c0d23925ba1c38a05e15bea5e6ee63b3a1c87125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814200"
---
# <a name="iscardfileaccessseek-method"></a><span data-ttu-id="13d5b-103">Метод Искардфилеакцесс:: Seek</span><span class="sxs-lookup"><span data-stu-id="13d5b-103">ISCardFileAccess::Seek method</span></span>

<span data-ttu-id="13d5b-104">\[Метод **Seek** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="13d5b-104">\[The **Seek** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="13d5b-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="13d5b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="13d5b-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="13d5b-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="13d5b-107">Метод **Seek** выбирает объект, из которого будет осуществляться доступ (чтение и запись).</span><span class="sxs-lookup"><span data-stu-id="13d5b-107">The **Seek** method selects the object from which (read/write) access will be done.</span></span>

## <a name="syntax"></a><span data-ttu-id="13d5b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13d5b-108">Syntax</span></span>


```C++
HRESULT Seek(
  [in] HSCARD_FILE hFile,
  [in] SEEKTYPE    *Seek,
  [in] LONG        lOffset 
);
```



## <a name="parameters"></a><span data-ttu-id="13d5b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="13d5b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13d5b-110">*hFile* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="13d5b-110">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13d5b-111">Маркер открытого файла.</span><span class="sxs-lookup"><span data-stu-id="13d5b-111">Handle of the open file.</span></span>

</dd> <dt>

<span data-ttu-id="13d5b-112">*Поиск* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="13d5b-112">*Seek* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13d5b-113">Расположение, где должен начинаться поиск.</span><span class="sxs-lookup"><span data-stu-id="13d5b-113">Location where the seek should begin.</span></span>



| <span data-ttu-id="13d5b-114">Значение</span><span class="sxs-lookup"><span data-stu-id="13d5b-114">Value</span></span>                                                                                                | <span data-ttu-id="13d5b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="13d5b-115">Meaning</span></span>                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="13d5b-116"><dt>SC \_ Поиск \_ с \_ начала</dt></span><span class="sxs-lookup"><span data-stu-id="13d5b-116"><dt>SC\_SEEK\_FROM\_BEGINNING</dt></span></span> </dl> | <span data-ttu-id="13d5b-117">Начните поиск с начала.</span><span class="sxs-lookup"><span data-stu-id="13d5b-117">Begin search at the beginning.</span></span><br/>          |
| <dl> <span data-ttu-id="13d5b-118"><dt>\_Поиск \_ с \_ конца по SC</dt></span><span class="sxs-lookup"><span data-stu-id="13d5b-118"><dt>SC\_SEEK\_FROM\_END </dt></span></span> </dl>      | <span data-ttu-id="13d5b-119">Начните поиск с конца.</span><span class="sxs-lookup"><span data-stu-id="13d5b-119">Begin search from the end.</span></span><br/>              |
| <dl> <span data-ttu-id="13d5b-120"><dt>\_относительный поиск по SC \_</dt></span><span class="sxs-lookup"><span data-stu-id="13d5b-120"><dt>SC\_SEEK\_RELATIVE</dt></span></span> </dl>        | <span data-ttu-id="13d5b-121">Начать поиск с текущей позицией.</span><span class="sxs-lookup"><span data-stu-id="13d5b-121">Begin search from the current position.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="13d5b-122">*лоффсет* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="13d5b-122">*lOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13d5b-123">Количество объектов данных из эталонного объекта.</span><span class="sxs-lookup"><span data-stu-id="13d5b-123">Number of data objects from the reference object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13d5b-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="13d5b-124">Return value</span></span>

<span data-ttu-id="13d5b-125">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="13d5b-125">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="13d5b-126">Код возврата</span><span class="sxs-lookup"><span data-stu-id="13d5b-126">Return code</span></span>                                                                                   | <span data-ttu-id="13d5b-127">Описание</span><span class="sxs-lookup"><span data-stu-id="13d5b-127">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="13d5b-128"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="13d5b-128"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="13d5b-129">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="13d5b-129">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="13d5b-130"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="13d5b-130"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="13d5b-131">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="13d5b-131">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="13d5b-132"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="13d5b-132"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="13d5b-133">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="13d5b-133">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="13d5b-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="13d5b-134">Remarks</span></span>

<span data-ttu-id="13d5b-135">Чтобы выполнить чтение или запись из файла, вызовите метод [**Read**](iscardfileaccess-read.md) или [**Write**](iscardfileaccess-write.md) соответственно.</span><span class="sxs-lookup"><span data-stu-id="13d5b-135">To read to or write from a file, call [**Read**](iscardfileaccess-read.md) or [**Write**](iscardfileaccess-write.md) respectively.</span></span>

<span data-ttu-id="13d5b-136">Список всех методов, определенных этим интерфейсом, см. в разделе [**искардфилеакцесс**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="13d5b-136">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="13d5b-137">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="13d5b-137">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="13d5b-138">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="13d5b-138">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="13d5b-139">Требования</span><span class="sxs-lookup"><span data-stu-id="13d5b-139">Requirements</span></span>



| <span data-ttu-id="13d5b-140">Требование</span><span class="sxs-lookup"><span data-stu-id="13d5b-140">Requirement</span></span> | <span data-ttu-id="13d5b-141">Значение</span><span class="sxs-lookup"><span data-stu-id="13d5b-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="13d5b-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="13d5b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="13d5b-143">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="13d5b-143">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="13d5b-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="13d5b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="13d5b-145">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="13d5b-145">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="13d5b-146">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="13d5b-146">End of client support</span></span><br/>    | <span data-ttu-id="13d5b-147">Windows XP</span><span class="sxs-lookup"><span data-stu-id="13d5b-147">Windows XP</span></span><br/>                                |
| <span data-ttu-id="13d5b-148">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="13d5b-148">End of server support</span></span><br/>    | <span data-ttu-id="13d5b-149">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="13d5b-149">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="13d5b-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13d5b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13d5b-151">**искардфилеакцесс**</span><span class="sxs-lookup"><span data-stu-id="13d5b-151">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> <dt>

[<span data-ttu-id="13d5b-152">**Просмотр**</span><span class="sxs-lookup"><span data-stu-id="13d5b-152">**Read**</span></span>](iscardfileaccess-read.md)
</dt> <dt>

[<span data-ttu-id="13d5b-153">**Будет**</span><span class="sxs-lookup"><span data-stu-id="13d5b-153">**Write**</span></span>](iscardfileaccess-write.md)
</dt> </dl>

 

 
