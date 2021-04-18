---
description: Делает файл (EF или DF), который был ранее сделан недопустимым, с помощью метода unvalidate, доступного приложению.
ms.assetid: 1906fcc5-ae76-4950-b2eb-e5ce1882637f
title: 'Метод Искардфилеакцесс:: Рехабилитате'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Rehabilitate
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7ed02131de08104dab8aff23ee9054659fd4cd63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650812"
---
# <a name="iscardfileaccessrehabilitate-method"></a><span data-ttu-id="6e968-103">Метод Искардфилеакцесс:: Рехабилитате</span><span class="sxs-lookup"><span data-stu-id="6e968-103">ISCardFileAccess::Rehabilitate method</span></span>

<span data-ttu-id="6e968-104">\[Метод **рехабилитате** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="6e968-104">\[The **Rehabilitate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6e968-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="6e968-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6e968-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="6e968-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6e968-107">Метод **рехабилитате** делает файл (EF или DF), который был ранее сделан недопустимым, с помощью метода [**unvalidate**](iscardfileaccess-invalidate.md) , доступного приложению.</span><span class="sxs-lookup"><span data-stu-id="6e968-107">The **Rehabilitate** method makes a file (EF or DF) that was previously made not valid by using the [**Invalidate**](iscardfileaccess-invalidate.md) method, accessible by the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e968-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6e968-108">Syntax</span></span>


```C++
HRESULT Rehabilitate(
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags
);
```



## <a name="parameters"></a><span data-ttu-id="6e968-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6e968-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e968-110">*бстрпасспек* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6e968-110">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e968-111">Файл в рехабилитате.</span><span class="sxs-lookup"><span data-stu-id="6e968-111">File to rehabilitate.</span></span>

</dd> <dt>

<span data-ttu-id="6e968-112">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6e968-112">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e968-113">Указывает, следует ли использовать безопасный обмен сообщениями.</span><span class="sxs-lookup"><span data-stu-id="6e968-113">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="6e968-114">**\_ \_ Защита \_ обмена сообщениями через SC FL**</span><span class="sxs-lookup"><span data-stu-id="6e968-114">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e968-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6e968-115">Return value</span></span>

<span data-ttu-id="6e968-116">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="6e968-116">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="6e968-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="6e968-117">Return code</span></span>                                                                                   | <span data-ttu-id="6e968-118">Описание</span><span class="sxs-lookup"><span data-stu-id="6e968-118">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="6e968-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="6e968-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6e968-120">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="6e968-120">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="6e968-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6e968-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="6e968-122">Недействительный параметр.</span><span class="sxs-lookup"><span data-stu-id="6e968-122">A parameter is not valid.</span></span><br/>         |
| <dl> <span data-ttu-id="6e968-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6e968-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6e968-124">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="6e968-124">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="6e968-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6e968-125">Remarks</span></span>

<span data-ttu-id="6e968-126">Список всех методов, определенных этим интерфейсом, см. в разделе [**искардфилеакцесс**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="6e968-126">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="6e968-127">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="6e968-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="6e968-128">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="6e968-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6e968-129">Требования</span><span class="sxs-lookup"><span data-stu-id="6e968-129">Requirements</span></span>



| <span data-ttu-id="6e968-130">Требование</span><span class="sxs-lookup"><span data-stu-id="6e968-130">Requirement</span></span> | <span data-ttu-id="6e968-131">Значение</span><span class="sxs-lookup"><span data-stu-id="6e968-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6e968-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6e968-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6e968-133">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6e968-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="6e968-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6e968-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6e968-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6e968-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6e968-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="6e968-136">End of client support</span></span><br/>    | <span data-ttu-id="6e968-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6e968-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="6e968-138">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="6e968-138">End of server support</span></span><br/>    | <span data-ttu-id="6e968-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6e968-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="6e968-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6e968-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e968-141">**Недействительным**</span><span class="sxs-lookup"><span data-stu-id="6e968-141">**Invalidate**</span></span>](iscardfileaccess-invalidate.md)
</dt> <dt>

[<span data-ttu-id="6e968-142">**искардфилеакцесс**</span><span class="sxs-lookup"><span data-stu-id="6e968-142">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
