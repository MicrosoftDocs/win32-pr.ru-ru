---
description: Позволяет приложению повторно подключаться к смарт-карте или модулю чтения без необходимости выдавать вызов отсоединения, за которым следует вызов Аттачбихандле или Аттачбифд соответственно.
ms.assetid: 450e817d-2cb2-4752-a86e-50cc8e434723
title: 'Метод Искардманаже:: Reconnect'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.Reconnect
api_type:
- COM
api_location: ''
ms.openlocfilehash: b8b05e6292a92267569eb1f53e10f6143554aba1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898814"
---
# <a name="iscardmanagereconnect-method"></a><span data-ttu-id="47657-103">Метод Искардманаже:: Reconnect</span><span class="sxs-lookup"><span data-stu-id="47657-103">ISCardManage::Reconnect method</span></span>

<span data-ttu-id="47657-104">\[Метод **Reconnect** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="47657-104">\[The **Reconnect** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="47657-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="47657-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="47657-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="47657-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="47657-107">Метод **Reconnect** позволяет приложению повторно подключаться к [*смарт-карте*](../secgloss/s-gly.md) или [*модулю чтения*](../secgloss/r-gly.md) без необходимости выдавать вызов [**отсоединения**](iscardmanage-detach.md) , за которым следует вызов [**аттачбихандле**](iscardmanage-attachbyhandle.md) или [**аттачбифд**](iscardmanage-attachbyifd.md) соответственно.</span><span class="sxs-lookup"><span data-stu-id="47657-107">The **Reconnect** method allows an application to reconnect to a [*smart card*](../secgloss/s-gly.md) or [*reader*](../secgloss/r-gly.md) without having to issue a [**Detach**](iscardmanage-detach.md) call followed by an [**AttachByHandle**](iscardmanage-attachbyhandle.md) or [**AttachByIFD**](iscardmanage-attachbyifd.md) call respectively.</span></span>

## <a name="syntax"></a><span data-ttu-id="47657-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47657-108">Syntax</span></span>


```C++
HRESULT Reconnect();
```



## <a name="parameters"></a><span data-ttu-id="47657-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="47657-109">Parameters</span></span>

<span data-ttu-id="47657-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="47657-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="47657-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="47657-111">Return value</span></span>

<span data-ttu-id="47657-112">Метод возвращает одно из следующих возможных значений:</span><span class="sxs-lookup"><span data-stu-id="47657-112">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="47657-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="47657-113">Return code</span></span>                                                                                   | <span data-ttu-id="47657-114">Описание</span><span class="sxs-lookup"><span data-stu-id="47657-114">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="47657-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="47657-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="47657-116">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="47657-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="47657-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="47657-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="47657-118">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="47657-118">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="47657-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="47657-119">Remarks</span></span>

<span data-ttu-id="47657-120">Чтобы подключить смарт-карту, вызовите [**аттачбихандле**](iscardmanage-attachbyhandle.md) или [**аттачбифд**](iscardmanage-attachbyifd.md).</span><span class="sxs-lookup"><span data-stu-id="47657-120">To attach a smart card call [**AttachByHandle**](iscardmanage-attachbyhandle.md) or [**AttachByIFD**](iscardmanage-attachbyifd.md).</span></span>

<span data-ttu-id="47657-121">Чтобы отключить смарт-карту, вызовите [**отсоединение**](iscardmanage-detach.md).</span><span class="sxs-lookup"><span data-stu-id="47657-121">To detach a smart card, call [**Detach**](iscardmanage-detach.md).</span></span>

<span data-ttu-id="47657-122">Список всех методов, определенных этим интерфейсом, см. в разделе [**искардманаже**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="47657-122">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="47657-123">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="47657-123">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="47657-124">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="47657-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="47657-125">Требования</span><span class="sxs-lookup"><span data-stu-id="47657-125">Requirements</span></span>



| <span data-ttu-id="47657-126">Требование</span><span class="sxs-lookup"><span data-stu-id="47657-126">Requirement</span></span> | <span data-ttu-id="47657-127">Значение</span><span class="sxs-lookup"><span data-stu-id="47657-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="47657-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="47657-128">Minimum supported client</span></span><br/> | <span data-ttu-id="47657-129">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="47657-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="47657-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="47657-130">Minimum supported server</span></span><br/> | <span data-ttu-id="47657-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="47657-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="47657-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="47657-132">End of client support</span></span><br/>    | <span data-ttu-id="47657-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="47657-133">Windows XP</span></span><br/>                                |
| <span data-ttu-id="47657-134">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="47657-134">End of server support</span></span><br/>    | <span data-ttu-id="47657-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="47657-135">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="47657-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47657-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47657-137">**аттачбихандле**</span><span class="sxs-lookup"><span data-stu-id="47657-137">**AttachByHandle**</span></span>](iscardmanage-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="47657-138">**аттачбифд**</span><span class="sxs-lookup"><span data-stu-id="47657-138">**AttachByIFD**</span></span>](iscardmanage-attachbyifd.md)
</dt> <dt>

[<span data-ttu-id="47657-139">**Соединил**</span><span class="sxs-lookup"><span data-stu-id="47657-139">**Detach**</span></span>](iscardmanage-detach.md)
</dt> <dt>

[<span data-ttu-id="47657-140">**искардманаже**</span><span class="sxs-lookup"><span data-stu-id="47657-140">**ISCardManage**</span></span>](iscardmanage.md)
</dt> </dl>

 

 
