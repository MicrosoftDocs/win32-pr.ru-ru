---
description: Снимает эксклюзивное использование подключенной смарт-карты.
ms.assetid: a236743a-1d12-44db-853d-f757f43a7e8f
title: 'Метод Искардманаже:: Скардунлокк'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.SCardUnlock
api_type:
- COM
api_location: ''
ms.openlocfilehash: 90c6b10d407992ae8147998d2d420989cc91e970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263944"
---
# <a name="iscardmanagescardunlock-method"></a><span data-ttu-id="18db8-103">Метод Искардманаже:: Скардунлокк</span><span class="sxs-lookup"><span data-stu-id="18db8-103">ISCardManage::SCardUnlock method</span></span>

<span data-ttu-id="18db8-104">\[Метод **скардунлокк** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="18db8-104">\[The **SCardUnlock** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="18db8-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="18db8-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="18db8-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="18db8-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="18db8-107">Метод **скардунлокк** освобождает эксклюзивное использование подключенной [*смарт-карты*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="18db8-107">The **SCardUnlock** method releases exclusive use of the connected [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="18db8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18db8-108">Syntax</span></span>


```C++
HRESULT SCardUnlock(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a><span data-ttu-id="18db8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="18db8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18db8-110">*Расстановка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18db8-110">*Disposition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18db8-111">Состояние для выхода смарт-карты при снятии блокировки.</span><span class="sxs-lookup"><span data-stu-id="18db8-111">The state to leave the smart card in when the lock is released.</span></span>

<dl><span id="LEAVE"></span><span id="leave"></span><dt>

<span data-ttu-id="18db8-112">**ВЫХОДА**</span><span class="sxs-lookup"><span data-stu-id="18db8-112">**LEAVE**</span></span>
</dt><span id="RESET"></span><span id="reset"></span><dt>

<span data-ttu-id="18db8-113">**RESET**</span><span class="sxs-lookup"><span data-stu-id="18db8-113">**RESET**</span></span>
</dt><span id="UNPOWER"></span><span id="unpower"></span><dt>

<span data-ttu-id="18db8-114">**Непитание**</span><span class="sxs-lookup"><span data-stu-id="18db8-114">**UNPOWER**</span></span>
</dt><span id="EJECT"></span><span id="eject"></span><dt>

<span data-ttu-id="18db8-115">**ВЫДВИНУТ**</span><span class="sxs-lookup"><span data-stu-id="18db8-115">**EJECT**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18db8-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="18db8-116">Return value</span></span>

<span data-ttu-id="18db8-117">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="18db8-117">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="18db8-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="18db8-118">Return code</span></span>                                                                                  | <span data-ttu-id="18db8-119">Описание</span><span class="sxs-lookup"><span data-stu-id="18db8-119">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="18db8-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="18db8-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="18db8-121">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="18db8-121">Operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="18db8-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="18db8-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="18db8-123">Недопустимый параметр *метода обработки* .</span><span class="sxs-lookup"><span data-stu-id="18db8-123">The *Disposition* parameter is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="18db8-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="18db8-124">Remarks</span></span>

<span data-ttu-id="18db8-125">Чтобы заблокировать подключенную смарт-карту, вызовите [**скардлокк**](iscardmanage-scardlock.md).</span><span class="sxs-lookup"><span data-stu-id="18db8-125">To lock the connected smart card, call [**SCardLock**](iscardmanage-scardlock.md).</span></span>

<span data-ttu-id="18db8-126">Список всех методов, определенных этим интерфейсом, см. в разделе [**искардманаже**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="18db8-126">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="18db8-127">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="18db8-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="18db8-128">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="18db8-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="18db8-129">Требования</span><span class="sxs-lookup"><span data-stu-id="18db8-129">Requirements</span></span>



| <span data-ttu-id="18db8-130">Требование</span><span class="sxs-lookup"><span data-stu-id="18db8-130">Requirement</span></span> | <span data-ttu-id="18db8-131">Значение</span><span class="sxs-lookup"><span data-stu-id="18db8-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="18db8-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="18db8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="18db8-133">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="18db8-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="18db8-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="18db8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="18db8-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="18db8-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="18db8-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="18db8-136">End of client support</span></span><br/>    | <span data-ttu-id="18db8-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="18db8-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="18db8-138">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="18db8-138">End of server support</span></span><br/>    | <span data-ttu-id="18db8-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="18db8-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="18db8-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="18db8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18db8-141">**искардманаже**</span><span class="sxs-lookup"><span data-stu-id="18db8-141">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="18db8-142">**скардлокк**</span><span class="sxs-lookup"><span data-stu-id="18db8-142">**SCardLock**</span></span>](iscardmanage-scardlock.md)
</dt> </dl>

 

 
