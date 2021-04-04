---
description: Сбрасывает текущий контекст безопасности смарт-карты.
ms.assetid: fcd55b65-a741-4244-8597-ec61cea3f4b7
title: 'Метод Искардверифи:: Ресетсекуритистате'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.ResetSecurityState
api_type:
- COM
api_location: ''
ms.openlocfilehash: ba96d400258fb58957c8c263438160d6710806db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896746"
---
# <a name="iscardverifyresetsecuritystate-method"></a><span data-ttu-id="09c20-103">Метод Искардверифи:: Ресетсекуритистате</span><span class="sxs-lookup"><span data-stu-id="09c20-103">ISCardVerify::ResetSecurityState method</span></span>

<span data-ttu-id="09c20-104">\[Метод **ресетсекуритистате** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="09c20-104">\[The **ResetSecurityState** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="09c20-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="09c20-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="09c20-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="09c20-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="09c20-107">Метод **ресетсекуритистате** Сбрасывает текущий [*контекст безопасности*](../secgloss/s-gly.md) [*смарт-карты*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="09c20-107">The **ResetSecurityState** method resets the current [*security context*](../secgloss/s-gly.md) of the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="09c20-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="09c20-108">Syntax</span></span>


```C++
HRESULT ResetSecurityState();
```



## <a name="parameters"></a><span data-ttu-id="09c20-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="09c20-109">Parameters</span></span>

<span data-ttu-id="09c20-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="09c20-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="09c20-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="09c20-111">Return value</span></span>

<span data-ttu-id="09c20-112">Метод возвращает одно из следующих возможных значений:</span><span class="sxs-lookup"><span data-stu-id="09c20-112">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="09c20-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="09c20-113">Return code</span></span>                                                                                   | <span data-ttu-id="09c20-114">Описание</span><span class="sxs-lookup"><span data-stu-id="09c20-114">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="09c20-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="09c20-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="09c20-116">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="09c20-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="09c20-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="09c20-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="09c20-118">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="09c20-118">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="09c20-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="09c20-119">Remarks</span></span>

<span data-ttu-id="09c20-120">Чтобы повторно включить [*контекст безопасности*](../secgloss/s-gly.md) без сброса параметров, вызовите метод [**Unblock**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="09c20-120">To re-enable the [*security context*](../secgloss/s-gly.md) without resetting, call [**Unblock**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85)).</span></span>

<span data-ttu-id="09c20-121">Список всех методов, определенных этим интерфейсом, см. в разделе [**искардверифи**](iscardverify.md).</span><span class="sxs-lookup"><span data-stu-id="09c20-121">For a list of all the methods defined by this interface, see [**ISCardVerify**](iscardverify.md).</span></span>

<span data-ttu-id="09c20-122">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="09c20-122">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="09c20-123">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="09c20-123">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="09c20-124">Требования</span><span class="sxs-lookup"><span data-stu-id="09c20-124">Requirements</span></span>



| <span data-ttu-id="09c20-125">Требование</span><span class="sxs-lookup"><span data-stu-id="09c20-125">Requirement</span></span> | <span data-ttu-id="09c20-126">Значение</span><span class="sxs-lookup"><span data-stu-id="09c20-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="09c20-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="09c20-127">Minimum supported client</span></span><br/> | <span data-ttu-id="09c20-128">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="09c20-128">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="09c20-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="09c20-129">Minimum supported server</span></span><br/> | <span data-ttu-id="09c20-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="09c20-130">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="09c20-131">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="09c20-131">End of client support</span></span><br/>    | <span data-ttu-id="09c20-132">Windows XP</span><span class="sxs-lookup"><span data-stu-id="09c20-132">Windows XP</span></span><br/>                                |
| <span data-ttu-id="09c20-133">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="09c20-133">End of server support</span></span><br/>    | <span data-ttu-id="09c20-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="09c20-134">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="09c20-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="09c20-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09c20-136">**искардверифи**</span><span class="sxs-lookup"><span data-stu-id="09c20-136">**ISCardVerify**</span></span>](iscardverify.md)
</dt> <dt>

<span data-ttu-id="09c20-137">[**Внести**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="09c20-137">[**Unblock**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))</span></span>
</dt> </dl>

 

 
