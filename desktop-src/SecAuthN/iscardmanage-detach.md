---
description: Освобождает вложение на конкретную смарт-карту или модуль чтения, выделенный Аттачбихандле и Аттачбифд соответственно.
ms.assetid: 601b35a6-9094-4786-b94c-5cd1283feef5
title: 'Искардманаже: метод:D етач'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.Detach
api_type:
- COM
api_location: ''
ms.openlocfilehash: bc5a48f76a643447b3e3d836d61ad7a769c56ff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155499"
---
# <a name="iscardmanagedetach-method"></a><span data-ttu-id="7a6b8-103">Искардманаже: метод:D етач</span><span class="sxs-lookup"><span data-stu-id="7a6b8-103">ISCardManage::Detach method</span></span>

<span data-ttu-id="7a6b8-104">\[Метод **Detach** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="7a6b8-104">\[The **Detach** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7a6b8-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7a6b8-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7a6b8-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="7a6b8-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="7a6b8-107">Метод **Detach** освобождает вложение на конкретную [*смарт-карту*](../secgloss/s-gly.md) или [*модуль чтения*](../secgloss/r-gly.md) , выделенный [**аттачбихандле**](iscardmanage-attachbyhandle.md) и [**аттачбифд**](iscardmanage-attachbyifd.md) соответственно.</span><span class="sxs-lookup"><span data-stu-id="7a6b8-107">The **Detach** method releases the attachment to a particular [*smart card*](../secgloss/s-gly.md) or [*reader*](../secgloss/r-gly.md) allocated by [**AttachByHandle**](iscardmanage-attachbyhandle.md) and [**AttachByIFD**](iscardmanage-attachbyifd.md) respectively.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a6b8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a6b8-108">Syntax</span></span>


```C++
HRESULT Detach();
```



## <a name="parameters"></a><span data-ttu-id="7a6b8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7a6b8-109">Parameters</span></span>

<span data-ttu-id="7a6b8-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7a6b8-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7a6b8-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7a6b8-111">Return value</span></span>

<span data-ttu-id="7a6b8-112">Метод возвращает одно из следующих возможных значений:</span><span class="sxs-lookup"><span data-stu-id="7a6b8-112">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="7a6b8-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7a6b8-113">Return code</span></span>                                                                                   | <span data-ttu-id="7a6b8-114">Описание</span><span class="sxs-lookup"><span data-stu-id="7a6b8-114">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="7a6b8-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7a6b8-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7a6b8-116">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="7a6b8-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="7a6b8-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7a6b8-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7a6b8-118">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="7a6b8-118">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="7a6b8-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7a6b8-119">Remarks</span></span>

<span data-ttu-id="7a6b8-120">Чтобы подключить смарт-карту, вызовите [**аттачбихандле**](iscardmanage-attachbyhandle.md) или [**аттачбифд**](iscardmanage-attachbyifd.md).</span><span class="sxs-lookup"><span data-stu-id="7a6b8-120">To attach a smart card call [**AttachByHandle**](iscardmanage-attachbyhandle.md) or [**AttachByIFD**](iscardmanage-attachbyifd.md).</span></span>

<span data-ttu-id="7a6b8-121">Чтобы повторно подключиться к смарт-карте, не вызывая **Detach** и [**аттачбихандле**](iscardmanage-attachbyhandle.md), вызовите [**Reconnect**](iscardmanage-reconnect.md).</span><span class="sxs-lookup"><span data-stu-id="7a6b8-121">To reconnect with the smart card without calling **Detach** and [**AttachByHandle**](iscardmanage-attachbyhandle.md), call [**Reconnect**](iscardmanage-reconnect.md).</span></span>

<span data-ttu-id="7a6b8-122">Список всех методов, определенных этим интерфейсом, см. в разделе [**искардманаже**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="7a6b8-122">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="7a6b8-123">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="7a6b8-123">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="7a6b8-124">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="7a6b8-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a6b8-125">Требования</span><span class="sxs-lookup"><span data-stu-id="7a6b8-125">Requirements</span></span>



| <span data-ttu-id="7a6b8-126">Требование</span><span class="sxs-lookup"><span data-stu-id="7a6b8-126">Requirement</span></span> | <span data-ttu-id="7a6b8-127">Значение</span><span class="sxs-lookup"><span data-stu-id="7a6b8-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7a6b8-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7a6b8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7a6b8-129">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7a6b8-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="7a6b8-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7a6b8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7a6b8-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7a6b8-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7a6b8-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="7a6b8-132">End of client support</span></span><br/>    | <span data-ttu-id="7a6b8-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7a6b8-133">Windows XP</span></span><br/>                                |
| <span data-ttu-id="7a6b8-134">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="7a6b8-134">End of server support</span></span><br/>    | <span data-ttu-id="7a6b8-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7a6b8-135">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="7a6b8-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a6b8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a6b8-137">**аттачбихандле**</span><span class="sxs-lookup"><span data-stu-id="7a6b8-137">**AttachByHandle**</span></span>](iscardmanage-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="7a6b8-138">**аттачбифд**</span><span class="sxs-lookup"><span data-stu-id="7a6b8-138">**AttachByIFD**</span></span>](iscardmanage-attachbyifd.md)
</dt> <dt>

[<span data-ttu-id="7a6b8-139">**искардманаже**</span><span class="sxs-lookup"><span data-stu-id="7a6b8-139">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="7a6b8-140">**Повтор соединения**</span><span class="sxs-lookup"><span data-stu-id="7a6b8-140">**Reconnect**</span></span>](iscardmanage-reconnect.md)
</dt> </dl>

 

 
