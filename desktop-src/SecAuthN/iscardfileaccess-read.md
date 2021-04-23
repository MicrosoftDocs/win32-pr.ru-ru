---
description: Метод Read считывает и возвращает указанные данные из заданного файла.
ms.assetid: 697b8dfa-754b-46cf-ab5c-1ac1d8ae47f2
title: 'Метод Искардфилеакцесс:: Read'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Read
api_type:
- COM
api_location: ''
ms.openlocfilehash: b3d66b5c6e314a4ef7a00a76fabc8660f3bf65eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264692"
---
# <a name="iscardfileaccessread-method"></a><span data-ttu-id="13c64-103">Метод Искардфилеакцесс:: Read</span><span class="sxs-lookup"><span data-stu-id="13c64-103">ISCardFileAccess::Read method</span></span>

<span data-ttu-id="13c64-104">\[Метод **Read** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="13c64-104">\[The **Read** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="13c64-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="13c64-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="13c64-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="13c64-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="13c64-107">Метод **Read** считывает и возвращает указанные данные из заданного файла.</span><span class="sxs-lookup"><span data-stu-id="13c64-107">The **Read** method reads and returns the specified data from a given file.</span></span>

## <a name="syntax"></a><span data-ttu-id="13c64-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13c64-108">Syntax</span></span>


```C++
HRESULT Read(
  [in]  HSCARD_FILE  hFile,
  [in]  LONG         *lBytesToRead,
  [in]  SCARD_FLAGS  flags,
  [out] LPBYTEBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="13c64-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="13c64-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13c64-110">*hFile* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="13c64-110">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13c64-111">Маркер открытого файла для доступа.</span><span class="sxs-lookup"><span data-stu-id="13c64-111">Handle of the open file to access.</span></span>

</dd> <dt>

<span data-ttu-id="13c64-112">*лбитестореад* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="13c64-112">*lBytesToRead* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13c64-113">Длина данных для чтения (в) или числа считанных байтов.</span><span class="sxs-lookup"><span data-stu-id="13c64-113">Length of data to be read (in) or number of bytes read (out).</span></span> <span data-ttu-id="13c64-114">Возвращает список файлов в виде массива BSTRs.</span><span class="sxs-lookup"><span data-stu-id="13c64-114">Returns list of files as an array of BSTRs.</span></span>

</dd> <dt>

<span data-ttu-id="13c64-115">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="13c64-115">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13c64-116">Указывает, следует ли использовать безопасный обмен сообщениями.</span><span class="sxs-lookup"><span data-stu-id="13c64-116">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="13c64-117">**\_ \_ Защита \_ обмена сообщениями через SC FL**</span><span class="sxs-lookup"><span data-stu-id="13c64-117">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="13c64-118">*ппбуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="13c64-118">*ppBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13c64-119">Объект [**ибитебуффер**](ibytebuffer.md) , содержащий данные для чтения.</span><span class="sxs-lookup"><span data-stu-id="13c64-119">An [**IByteBuffer**](ibytebuffer.md) object containing the read data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13c64-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="13c64-120">Return value</span></span>

<span data-ttu-id="13c64-121">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="13c64-121">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="13c64-122">Код возврата</span><span class="sxs-lookup"><span data-stu-id="13c64-122">Return code</span></span>                                                                                   | <span data-ttu-id="13c64-123">Описание</span><span class="sxs-lookup"><span data-stu-id="13c64-123">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="13c64-124"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="13c64-124"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="13c64-125">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="13c64-125">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="13c64-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="13c64-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="13c64-127">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="13c64-127">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="13c64-128"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="13c64-128"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="13c64-129">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="13c64-129">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="13c64-130"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="13c64-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="13c64-131">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="13c64-131">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="13c64-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="13c64-132">Remarks</span></span>

<span data-ttu-id="13c64-133">Список всех методов, определенных этим интерфейсом, см. в разделе [**искардфилеакцесс**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="13c64-133">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="13c64-134">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="13c64-134">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="13c64-135">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="13c64-135">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="13c64-136">Требования</span><span class="sxs-lookup"><span data-stu-id="13c64-136">Requirements</span></span>



| <span data-ttu-id="13c64-137">Требование</span><span class="sxs-lookup"><span data-stu-id="13c64-137">Requirement</span></span> | <span data-ttu-id="13c64-138">Значение</span><span class="sxs-lookup"><span data-stu-id="13c64-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="13c64-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="13c64-139">Minimum supported client</span></span><br/> | <span data-ttu-id="13c64-140">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="13c64-140">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="13c64-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="13c64-141">Minimum supported server</span></span><br/> | <span data-ttu-id="13c64-142">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="13c64-142">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="13c64-143">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="13c64-143">End of client support</span></span><br/>    | <span data-ttu-id="13c64-144">Windows XP</span><span class="sxs-lookup"><span data-stu-id="13c64-144">Windows XP</span></span><br/>                                |
| <span data-ttu-id="13c64-145">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="13c64-145">End of server support</span></span><br/>    | <span data-ttu-id="13c64-146">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="13c64-146">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="13c64-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13c64-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13c64-148">**искардфилеакцесс**</span><span class="sxs-lookup"><span data-stu-id="13c64-148">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
