---
description: Метод Write записывает данные в текущий открытый файл.
ms.assetid: 0c92af34-a9db-4242-8b6e-d1010a0d7afa
title: 'Метод Искардфилеакцесс:: Write'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Write
api_type:
- COM
api_location: ''
ms.openlocfilehash: 48091d39fff49e54d57f5a26fb7d033bfd8e5952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156299"
---
# <a name="iscardfileaccesswrite-method"></a><span data-ttu-id="e1275-103">Метод Искардфилеакцесс:: Write</span><span class="sxs-lookup"><span data-stu-id="e1275-103">ISCardFileAccess::Write method</span></span>

<span data-ttu-id="e1275-104">\[Метод **Write** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="e1275-104">\[The **Write** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e1275-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e1275-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e1275-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="e1275-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="e1275-107">Метод **Write** записывает данные в текущий открытый файл.</span><span class="sxs-lookup"><span data-stu-id="e1275-107">The **Write** method writes data to a current opened file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1275-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1275-108">Syntax</span></span>


```C++
HRESULT Write(
  [in] HSCARD_FILE  hFile,
  [in] LPBYTEBUFFER pData,
  [in] SCARD_FLAGS  flags
);
```



## <a name="parameters"></a><span data-ttu-id="e1275-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1275-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1275-110">*hFile* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e1275-110">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1275-111">Маркер открытого файла.</span><span class="sxs-lookup"><span data-stu-id="e1275-111">A handle to an open file.</span></span>

</dd> <dt>

<span data-ttu-id="e1275-112">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e1275-112">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1275-113">Записываемый объект или данные.</span><span class="sxs-lookup"><span data-stu-id="e1275-113">Object/data to be written.</span></span>

</dd> <dt>

<span data-ttu-id="e1275-114">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e1275-114">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1275-115">Указывает, следует ли использовать безопасный обмен сообщениями.</span><span class="sxs-lookup"><span data-stu-id="e1275-115">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="e1275-116">**\_ \_ Защита \_ обмена сообщениями через SC FL**</span><span class="sxs-lookup"><span data-stu-id="e1275-116">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1275-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e1275-117">Return value</span></span>

<span data-ttu-id="e1275-118">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="e1275-118">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="e1275-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e1275-119">Return code</span></span>                                                                                   | <span data-ttu-id="e1275-120">Описание</span><span class="sxs-lookup"><span data-stu-id="e1275-120">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="e1275-121"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="e1275-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e1275-122">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="e1275-122">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="e1275-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e1275-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="e1275-124">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="e1275-124">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="e1275-125"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="e1275-125"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e1275-126">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="e1275-126">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="e1275-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e1275-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e1275-128">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="e1275-128">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="e1275-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e1275-129">Remarks</span></span>

<span data-ttu-id="e1275-130">Чтобы открыть или закрыть файл, вызовите метод [**Open**](iscardfileaccess-open.md) или [**Close**](iscardfileaccess-close.md)соответственно.</span><span class="sxs-lookup"><span data-stu-id="e1275-130">To open or close a file, call [**Open**](iscardfileaccess-open.md) or [**Close**](iscardfileaccess-close.md), respectively.</span></span>

<span data-ttu-id="e1275-131">Список всех методов, определенных этим интерфейсом, см. в разделе [**искардфилеакцесс**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="e1275-131">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="e1275-132">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="e1275-132">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="e1275-133">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="e1275-133">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e1275-134">Требования</span><span class="sxs-lookup"><span data-stu-id="e1275-134">Requirements</span></span>



| <span data-ttu-id="e1275-135">Требование</span><span class="sxs-lookup"><span data-stu-id="e1275-135">Requirement</span></span> | <span data-ttu-id="e1275-136">Значение</span><span class="sxs-lookup"><span data-stu-id="e1275-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e1275-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e1275-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e1275-138">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e1275-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="e1275-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e1275-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e1275-140">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e1275-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e1275-141">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="e1275-141">End of client support</span></span><br/>    | <span data-ttu-id="e1275-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e1275-142">Windows XP</span></span><br/>                                |
| <span data-ttu-id="e1275-143">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="e1275-143">End of server support</span></span><br/>    | <span data-ttu-id="e1275-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e1275-144">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="e1275-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e1275-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1275-146">**Закрыть**</span><span class="sxs-lookup"><span data-stu-id="e1275-146">**Close**</span></span>](iscardfileaccess-close.md)
</dt> <dt>

[<span data-ttu-id="e1275-147">**искардфилеакцесс**</span><span class="sxs-lookup"><span data-stu-id="e1275-147">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> <dt>

[<span data-ttu-id="e1275-148">**Открыт**</span><span class="sxs-lookup"><span data-stu-id="e1275-148">**Open**</span></span>](iscardfileaccess-open.md)
</dt> </dl>

 

 
