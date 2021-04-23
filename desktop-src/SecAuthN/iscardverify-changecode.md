---
description: Заменяет текущий код ЧВ (проверки держателя карты) новым кодом ЧВ.
ms.assetid: 8d47d842-67e8-4948-a63b-49bcfc8a69a1
title: 'Метод Искардверифи:: Чанжекоде'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.ChangeCode
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6fcb6d79e6135293ad91e3ea18fa535ef4edbd1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814384"
---
# <a name="iscardverifychangecode-method"></a><span data-ttu-id="3ce06-103">Метод Искардверифи:: Чанжекоде</span><span class="sxs-lookup"><span data-stu-id="3ce06-103">ISCardVerify::ChangeCode method</span></span>

<span data-ttu-id="3ce06-104">\[Метод **чанжекоде** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="3ce06-104">\[The **ChangeCode** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3ce06-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="3ce06-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3ce06-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="3ce06-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="3ce06-107">Метод **чанжекоде** заменяет текущий код ЧВ (проверка держателя карты) новым кодом ЧВ.</span><span class="sxs-lookup"><span data-stu-id="3ce06-107">The **ChangeCode** method replaces the current CHV (card holder verification) code with new CHV code.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ce06-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3ce06-108">Syntax</span></span>


```C++
HRESULT ChangeCode(
  [in] LPBYTEBUFFER pOldCode,
  [in] LPBYTEBUFFER pNewCode,
  [in] SCARD_FLAGS  Flags,
  [in] LONG         lRef
);
```



## <a name="parameters"></a><span data-ttu-id="3ce06-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ce06-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ce06-110">*полдкоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3ce06-110">*pOldCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ce06-111">Указатель на [**ибитебуффер**](ibytebuffer.md) , содержащий текущий код пользователя.</span><span class="sxs-lookup"><span data-stu-id="3ce06-111">Pointer to an [**IByteBuffer**](ibytebuffer.md) containing the user's current code.</span></span>

</dd> <dt>

<span data-ttu-id="3ce06-112">*пневкоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3ce06-112">*pNewCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ce06-113">Указатель на [**ибитебуффер**](ibytebuffer.md) , содержащий новый код, который будет представлен [*смарт-карте*](../secgloss/s-gly.md) во время процесса изменения для проверки подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="3ce06-113">Pointer to an [**IByteBuffer**](ibytebuffer.md) containing the new code that will be presented to the [*smart card*](../secgloss/s-gly.md) during the change process to authenticate the user.</span></span>

</dd> <dt>

<span data-ttu-id="3ce06-114">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3ce06-114">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ce06-115">Указывает, является ли код глобальным или локальным, а также следует ли включать или отключать код.</span><span class="sxs-lookup"><span data-stu-id="3ce06-115">Indicates whether the code is global or local, and whether the code should be enabled or disabled.</span></span>

<dl><span id="SC_FL_IHV_GLOBAL"></span><span id="sc_fl_ihv_global"></span><dt>

<span data-ttu-id="3ce06-116">**\_ \_ глобальный IHV для SC FL \_**</span><span class="sxs-lookup"><span data-stu-id="3ce06-116">**SC\_FL\_IHV\_GLOBAL**</span></span>
</dt><span id="SC_FL_IHV_LOCAL"></span><span id="sc_fl_ihv_local"></span><dt>

<span data-ttu-id="3ce06-117">**локальный поставщик IHV для SC \_ FL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ce06-117">**SC\_FL\_IHV\_LOCAL**</span></span>
</dt><span id="SC_FL_IHV_ENABLE"></span><span id="sc_fl_ihv_enable"></span><dt>

<span data-ttu-id="3ce06-118">**\_включить SC FL \_ IHV \_**</span><span class="sxs-lookup"><span data-stu-id="3ce06-118">**SC\_FL\_IHV\_ENABLE**</span></span>
</dt><span id="SC_FL_IHV_DISABLE"></span><span id="sc_fl_ihv_disable"></span><dt>

<span data-ttu-id="3ce06-119">**\_ \_ Отключение поставщика оборудования SC FL \_**</span><span class="sxs-lookup"><span data-stu-id="3ce06-119">**SC\_FL\_IHV\_DISABLE**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="3ce06-120">*лреф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3ce06-120">*lRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ce06-121">Ссылка на смарт-карту.</span><span class="sxs-lookup"><span data-stu-id="3ce06-121">Smart card specific reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ce06-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ce06-122">Return value</span></span>

<span data-ttu-id="3ce06-123">Метод возвращает одно из следующих возможных значений:</span><span class="sxs-lookup"><span data-stu-id="3ce06-123">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="3ce06-124">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3ce06-124">Return code</span></span>                                                                                   | <span data-ttu-id="3ce06-125">Описание</span><span class="sxs-lookup"><span data-stu-id="3ce06-125">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="3ce06-126"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="3ce06-126"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3ce06-127">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="3ce06-127">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="3ce06-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3ce06-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="3ce06-129">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="3ce06-129">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="3ce06-130"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="3ce06-130"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3ce06-131">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="3ce06-131">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="3ce06-132"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3ce06-132"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3ce06-133">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="3ce06-133">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="3ce06-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3ce06-134">Remarks</span></span>

<span data-ttu-id="3ce06-135">Список всех методов, определенных этим интерфейсом, см. в разделе [**искардверифи**](iscardverify.md).</span><span class="sxs-lookup"><span data-stu-id="3ce06-135">For a list of all the methods defined by this interface, see [**ISCardVerify**](iscardverify.md).</span></span>

<span data-ttu-id="3ce06-136">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="3ce06-136">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="3ce06-137">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="3ce06-137">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ce06-138">Требования</span><span class="sxs-lookup"><span data-stu-id="3ce06-138">Requirements</span></span>



| <span data-ttu-id="3ce06-139">Требование</span><span class="sxs-lookup"><span data-stu-id="3ce06-139">Requirement</span></span> | <span data-ttu-id="3ce06-140">Значение</span><span class="sxs-lookup"><span data-stu-id="3ce06-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3ce06-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3ce06-141">Minimum supported client</span></span><br/> | <span data-ttu-id="3ce06-142">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3ce06-142">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="3ce06-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3ce06-143">Minimum supported server</span></span><br/> | <span data-ttu-id="3ce06-144">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3ce06-144">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3ce06-145">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="3ce06-145">End of client support</span></span><br/>    | <span data-ttu-id="3ce06-146">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3ce06-146">Windows XP</span></span><br/>                                |
| <span data-ttu-id="3ce06-147">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="3ce06-147">End of server support</span></span><br/>    | <span data-ttu-id="3ce06-148">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3ce06-148">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="3ce06-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ce06-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ce06-150">**ибитебуффер**</span><span class="sxs-lookup"><span data-stu-id="3ce06-150">**IByteBuffer**</span></span>](ibytebuffer.md)
</dt> <dt>

[<span data-ttu-id="3ce06-151">**искардверифи**</span><span class="sxs-lookup"><span data-stu-id="3ce06-151">**ISCardVerify**</span></span>](iscardverify.md)
</dt> <dt>

[<span data-ttu-id="3ce06-152">Возвращаемые значения смарт-карты</span><span class="sxs-lookup"><span data-stu-id="3ce06-152">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
