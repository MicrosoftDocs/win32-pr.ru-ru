---
description: Создает канал связи со смарт-картой (ICC) с помощью маркера, возвращенного диспетчером ресурсов смарт-карты.
ms.assetid: dfd05dce-4416-4881-92ca-c85baccf3b86
title: 'Метод Искардманаже:: Аттачбихандле'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.AttachByHandle
api_type:
- COM
api_location: ''
ms.openlocfilehash: 266b6a0d2a4027fe85f1f5539b970a44fc21bbee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910631"
---
# <a name="iscardmanageattachbyhandle-method"></a><span data-ttu-id="9cf9b-103">Метод Искардманаже:: Аттачбихандле</span><span class="sxs-lookup"><span data-stu-id="9cf9b-103">ISCardManage::AttachByHandle method</span></span>

<span data-ttu-id="9cf9b-104">\[Метод **аттачбихандле** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="9cf9b-104">\[The **AttachByHandle** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9cf9b-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="9cf9b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9cf9b-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="9cf9b-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="9cf9b-107">Метод **аттачбихандле** создает канал связи со [*смарт-картой*](../secgloss/s-gly.md) (ICC) с помощью маркера, возвращенного [*диспетчером ресурсов*](../secgloss/r-gly.md)смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="9cf9b-107">The **AttachByHandle** method creates a communication link to a [*smart card*](../secgloss/s-gly.md) (ICC) using a handle returned by the smart card [*resource manager*](../secgloss/r-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9cf9b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9cf9b-108">Syntax</span></span>


```C++
HRESULT AttachByHandle(
  [in] HSCARD hICC
);
```



## <a name="parameters"></a><span data-ttu-id="9cf9b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9cf9b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cf9b-110">*хикк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9cf9b-110">*hICC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cf9b-111">Маркер смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="9cf9b-111">A handle to a smart card.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cf9b-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9cf9b-112">Return value</span></span>

<span data-ttu-id="9cf9b-113">Метод возвращает одно из следующих возможных значений:</span><span class="sxs-lookup"><span data-stu-id="9cf9b-113">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="9cf9b-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9cf9b-114">Return code</span></span>                                                                                   | <span data-ttu-id="9cf9b-115">Описание</span><span class="sxs-lookup"><span data-stu-id="9cf9b-115">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="9cf9b-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="9cf9b-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9cf9b-117">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="9cf9b-117">Operation completed successfully.</span></span><br/>  |
| <dl> <span data-ttu-id="9cf9b-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9cf9b-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="9cf9b-119">Недопустимый параметр *хикк* .</span><span class="sxs-lookup"><span data-stu-id="9cf9b-119">The *hICC* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="9cf9b-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="9cf9b-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9cf9b-121">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="9cf9b-121">Out of memory.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="9cf9b-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9cf9b-122">Remarks</span></span>

<span data-ttu-id="9cf9b-123">Чтобы присоединить [*средство чтения*](../secgloss/r-gly.md) Call [**аттачбифд**](iscardmanage-attachbyifd.md).</span><span class="sxs-lookup"><span data-stu-id="9cf9b-123">To attach a [*reader*](../secgloss/r-gly.md) call [**AttachByIFD**](iscardmanage-attachbyifd.md).</span></span>

<span data-ttu-id="9cf9b-124">Освобождение вызова [**отсоединения**](iscardmanage-detach.md)вложений.</span><span class="sxs-lookup"><span data-stu-id="9cf9b-124">To release an attachment call [**Detach**](iscardmanage-detach.md).</span></span>

<span data-ttu-id="9cf9b-125">Чтобы повторно подключиться к смарт-карте, не вызывая [**Detach**](iscardmanage-detach.md) и **аттачбихандле**, вызовите [**Reconnect**](iscardmanage-reconnect.md).</span><span class="sxs-lookup"><span data-stu-id="9cf9b-125">To reconnect with the smart card without calling [**Detach**](iscardmanage-detach.md) and **AttachByHandle**, call [**Reconnect**](iscardmanage-reconnect.md).</span></span>

<span data-ttu-id="9cf9b-126">Список всех методов, определенных интерфейсом [**искардманаже**](iscardmanage.md) , см. в разделе [**искардманаже**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="9cf9b-126">For a list of all the methods defined by the [**ISCardManage**](iscardmanage.md) interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="9cf9b-127">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="9cf9b-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="9cf9b-128">Дополнительные сведения о кодах ошибок смарт-карт см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="9cf9b-128">For information about smart card error codes, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9cf9b-129">Требования</span><span class="sxs-lookup"><span data-stu-id="9cf9b-129">Requirements</span></span>



| <span data-ttu-id="9cf9b-130">Требование</span><span class="sxs-lookup"><span data-stu-id="9cf9b-130">Requirement</span></span> | <span data-ttu-id="9cf9b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="9cf9b-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9cf9b-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9cf9b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9cf9b-133">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9cf9b-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="9cf9b-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9cf9b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9cf9b-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9cf9b-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9cf9b-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="9cf9b-136">End of client support</span></span><br/>    | <span data-ttu-id="9cf9b-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9cf9b-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="9cf9b-138">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="9cf9b-138">End of server support</span></span><br/>    | <span data-ttu-id="9cf9b-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9cf9b-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="9cf9b-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9cf9b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cf9b-141">**аттачбифд**</span><span class="sxs-lookup"><span data-stu-id="9cf9b-141">**AttachByIFD**</span></span>](iscardmanage-attachbyifd.md)
</dt> <dt>

[<span data-ttu-id="9cf9b-142">**Соединил**</span><span class="sxs-lookup"><span data-stu-id="9cf9b-142">**Detach**</span></span>](iscardmanage-detach.md)
</dt> <dt>

[<span data-ttu-id="9cf9b-143">**искардманаже**</span><span class="sxs-lookup"><span data-stu-id="9cf9b-143">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="9cf9b-144">**Повтор соединения**</span><span class="sxs-lookup"><span data-stu-id="9cf9b-144">**Reconnect**</span></span>](iscardmanage-reconnect.md)
</dt> </dl>

 

 
