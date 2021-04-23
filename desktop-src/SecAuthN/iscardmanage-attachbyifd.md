---
description: Создает канал связи с модулем чтения, используя предоставляемое отображаемое имя для модуля чтения.
ms.assetid: 7916896b-c460-47b2-a1db-17d8fc9bdd2e
title: 'Метод Искардманаже:: Аттачбифд'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.AttachByIFD
api_type:
- COM
api_location: ''
ms.openlocfilehash: ae0aaae2157331d5d1bae2814c563c89dc73c757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647435"
---
# <a name="iscardmanageattachbyifd-method"></a><span data-ttu-id="4c14c-103">Метод Искардманаже:: Аттачбифд</span><span class="sxs-lookup"><span data-stu-id="4c14c-103">ISCardManage::AttachByIFD method</span></span>

<span data-ttu-id="4c14c-104">\[Метод **аттачбифд** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="4c14c-104">\[The **AttachByIFD** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4c14c-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="4c14c-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4c14c-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="4c14c-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="4c14c-107">Метод **аттачбифд** создает канал связи с [*модулем чтения*](../secgloss/r-gly.md), используя предоставляемое отображаемое имя для модуля чтения.</span><span class="sxs-lookup"><span data-stu-id="4c14c-107">The **AttachByIFD** method creates a communication link to a [*reader*](../secgloss/r-gly.md), using a supplied display name for the reader.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c14c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c14c-108">Syntax</span></span>


```C++
HRESULT AttachByIFD(
  [in] BSTR bstrIFDName
);
```



## <a name="parameters"></a><span data-ttu-id="4c14c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c14c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c14c-110">*бстрифднаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c14c-110">*bstrIFDName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c14c-111">Отображаемое имя модуля чтения.</span><span class="sxs-lookup"><span data-stu-id="4c14c-111">The display name of the reader.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c14c-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4c14c-112">Return value</span></span>

<span data-ttu-id="4c14c-113">Метод возвращает одно из следующих возможных значений:</span><span class="sxs-lookup"><span data-stu-id="4c14c-113">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="4c14c-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4c14c-114">Return code</span></span>                                                                                   | <span data-ttu-id="4c14c-115">Описание</span><span class="sxs-lookup"><span data-stu-id="4c14c-115">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="4c14c-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="4c14c-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4c14c-117">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="4c14c-117">Operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="4c14c-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4c14c-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="4c14c-119">Недопустимый параметр *бстрифднаме* .</span><span class="sxs-lookup"><span data-stu-id="4c14c-119">The *bstrIFDName* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="4c14c-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4c14c-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4c14c-121">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="4c14c-121">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="4c14c-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4c14c-122">Remarks</span></span>

<span data-ttu-id="4c14c-123">Для подключения [**аттачбихандле**](iscardmanage-attachbyhandle.md)вызова [*смарт-карты*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="4c14c-123">To attach a [*smart card*](../secgloss/s-gly.md) call [**AttachByHandle**](iscardmanage-attachbyhandle.md).</span></span>

<span data-ttu-id="4c14c-124">Освобождение вызова [**отсоединения**](iscardmanage-detach.md)вложений.</span><span class="sxs-lookup"><span data-stu-id="4c14c-124">To release an attachment call [**Detach**](iscardmanage-detach.md).</span></span>

<span data-ttu-id="4c14c-125">Чтобы повторно подключиться к смарт-карте, не вызывая [**Detach**](iscardmanage-detach.md) и **аттачбифд**, вызовите [**Reconnect**](iscardmanage-reconnect.md).</span><span class="sxs-lookup"><span data-stu-id="4c14c-125">To reconnect with the smart card without calling [**Detach**](iscardmanage-detach.md) and **AttachByIFD**, call [**Reconnect**](iscardmanage-reconnect.md).</span></span>

<span data-ttu-id="4c14c-126">Список всех методов, определенных этим интерфейсом, см. в разделе [**искардманаже**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="4c14c-126">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="4c14c-127">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="4c14c-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="4c14c-128">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="4c14c-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c14c-129">Требования</span><span class="sxs-lookup"><span data-stu-id="4c14c-129">Requirements</span></span>



| <span data-ttu-id="4c14c-130">Требование</span><span class="sxs-lookup"><span data-stu-id="4c14c-130">Requirement</span></span> | <span data-ttu-id="4c14c-131">Значение</span><span class="sxs-lookup"><span data-stu-id="4c14c-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4c14c-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4c14c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4c14c-133">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4c14c-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="4c14c-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4c14c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4c14c-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4c14c-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4c14c-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="4c14c-136">End of client support</span></span><br/>    | <span data-ttu-id="4c14c-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4c14c-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="4c14c-138">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="4c14c-138">End of server support</span></span><br/>    | <span data-ttu-id="4c14c-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4c14c-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="4c14c-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c14c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c14c-141">**аттачбихандле**</span><span class="sxs-lookup"><span data-stu-id="4c14c-141">**AttachByHandle**</span></span>](iscardmanage-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="4c14c-142">**Соединил**</span><span class="sxs-lookup"><span data-stu-id="4c14c-142">**Detach**</span></span>](iscardmanage-detach.md)
</dt> <dt>

[<span data-ttu-id="4c14c-143">**искардманаже**</span><span class="sxs-lookup"><span data-stu-id="4c14c-143">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="4c14c-144">**Повтор соединения**</span><span class="sxs-lookup"><span data-stu-id="4c14c-144">**Reconnect**</span></span>](iscardmanage-reconnect.md)
</dt> </dl>

 

 
