---
description: Блокирует подключенную смарт-карту для монопольного использования.
ms.assetid: c39a7cfe-04b6-4298-927a-4280664cf769
title: 'Метод Искардманаже:: Скардлокк'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.SCardLock
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2198f512fde90d1c79173f5151fc4f759944500a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263946"
---
# <a name="iscardmanagescardlock-method"></a><span data-ttu-id="b86e9-103">Метод Искардманаже:: Скардлокк</span><span class="sxs-lookup"><span data-stu-id="b86e9-103">ISCardManage::SCardLock method</span></span>

<span data-ttu-id="b86e9-104">\[Метод **скардлокк** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="b86e9-104">\[The **SCardLock** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b86e9-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="b86e9-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b86e9-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="b86e9-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="b86e9-107">Метод **скардлокк** блокирует подключенную [*смарт-карту*](../secgloss/s-gly.md) для монопольного использования.</span><span class="sxs-lookup"><span data-stu-id="b86e9-107">The **SCardLock** method locks a connected [*smart card*](../secgloss/s-gly.md) for exclusive use.</span></span>

## <a name="syntax"></a><span data-ttu-id="b86e9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b86e9-108">Syntax</span></span>


```C++
HRESULT SCardLock();
```



## <a name="parameters"></a><span data-ttu-id="b86e9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b86e9-109">Parameters</span></span>

<span data-ttu-id="b86e9-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="b86e9-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b86e9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b86e9-111">Return value</span></span>

<span data-ttu-id="b86e9-112">Метод возвращает одно из следующих возможных значений:</span><span class="sxs-lookup"><span data-stu-id="b86e9-112">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="b86e9-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b86e9-113">Return code</span></span>                                                                            | <span data-ttu-id="b86e9-114">Описание</span><span class="sxs-lookup"><span data-stu-id="b86e9-114">Description</span></span>                                  |
|----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="b86e9-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="b86e9-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="b86e9-116">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="b86e9-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="b86e9-117"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="b86e9-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="b86e9-118">Не удалось завершить операцию.</span><span class="sxs-lookup"><span data-stu-id="b86e9-118">Operation failed to complete.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="b86e9-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b86e9-119">Remarks</span></span>

<span data-ttu-id="b86e9-120">Чтобы освободить эксклюзивное использование подключенной смарт-карты, вызовите [**скардунлокк**](iscardmanage-scardunlock.md).</span><span class="sxs-lookup"><span data-stu-id="b86e9-120">To releases exclusive use of the connected smart card, call [**SCardUnlock**](iscardmanage-scardunlock.md).</span></span>

<span data-ttu-id="b86e9-121">Список всех методов, определенных этим интерфейсом, см. в разделе [**искардманаже**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="b86e9-121">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="b86e9-122">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="b86e9-122">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="b86e9-123">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="b86e9-123">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b86e9-124">Требования</span><span class="sxs-lookup"><span data-stu-id="b86e9-124">Requirements</span></span>



| <span data-ttu-id="b86e9-125">Требование</span><span class="sxs-lookup"><span data-stu-id="b86e9-125">Requirement</span></span> | <span data-ttu-id="b86e9-126">Значение</span><span class="sxs-lookup"><span data-stu-id="b86e9-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b86e9-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b86e9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b86e9-128">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b86e9-128">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="b86e9-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b86e9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b86e9-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b86e9-130">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b86e9-131">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="b86e9-131">End of client support</span></span><br/>    | <span data-ttu-id="b86e9-132">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b86e9-132">Windows XP</span></span><br/>                                |
| <span data-ttu-id="b86e9-133">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="b86e9-133">End of server support</span></span><br/>    | <span data-ttu-id="b86e9-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b86e9-134">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="b86e9-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b86e9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b86e9-136">**искардманаже**</span><span class="sxs-lookup"><span data-stu-id="b86e9-136">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="b86e9-137">**скардунлокк**</span><span class="sxs-lookup"><span data-stu-id="b86e9-137">**SCardUnlock**</span></span>](iscardmanage-scardunlock.md)
</dt> </dl>

 

 
