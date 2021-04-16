---
description: Запрашивает проверку пользователя.
ms.assetid: e8b7155c-3444-4aa8-8a15-3b3624a44a77
title: 'Метод Искардверифи:: Verify'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.Verify
api_type:
- COM
api_location: ''
ms.openlocfilehash: 68f3a97df672d97e635180f41405a75c4cb84661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650768"
---
# <a name="iscardverifyverify-method"></a><span data-ttu-id="1ee92-103">Метод Искардверифи:: Verify</span><span class="sxs-lookup"><span data-stu-id="1ee92-103">ISCardVerify::Verify method</span></span>

<span data-ttu-id="1ee92-104">\[Метод **Verify** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="1ee92-104">\[The **Verify** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1ee92-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="1ee92-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1ee92-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="1ee92-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="1ee92-107">Метод **Verify** запрашивает проверку пользователя.</span><span class="sxs-lookup"><span data-stu-id="1ee92-107">The **Verify** method requests a verification of the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ee92-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ee92-108">Syntax</span></span>


```C++
HRESULT Verify(
  [in] LPBYTEBUFFER pCode,
  [in] SCARD_FLAGS  Flags,
  [in] LONG         lRef
);
```



## <a name="parameters"></a><span data-ttu-id="1ee92-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ee92-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ee92-110">*коде Pcode* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1ee92-110">*pCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ee92-111">Содержит код, который будет представлен [*смарт-карте*](../secgloss/s-gly.md) в процессе ЧВ (проверка держателя карты).</span><span class="sxs-lookup"><span data-stu-id="1ee92-111">Contains the code to be presented to the [*smart card*](../secgloss/s-gly.md) in the CHV (card holder verification) process.</span></span>

</dd> <dt>

<span data-ttu-id="1ee92-112">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1ee92-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ee92-113">Указывает, является ли код глобальным или локальным.</span><span class="sxs-lookup"><span data-stu-id="1ee92-113">Indicates whether the code is global or local.</span></span>

<dl><span id="SC_FL_IHV_GLOBAL"></span><span id="sc_fl_ihv_global"></span><dt>

<span data-ttu-id="1ee92-114">**\_ \_ глобальный IHV для SC FL \_**</span><span class="sxs-lookup"><span data-stu-id="1ee92-114">**SC\_FL\_IHV\_GLOBAL**</span></span>
</dt><span id="SC_FL_IHV_LOCAL"></span><span id="sc_fl_ihv_local"></span><dt>

<span data-ttu-id="1ee92-115">**локальный поставщик IHV для SC \_ FL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1ee92-115">**SC\_FL\_IHV\_LOCAL**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="1ee92-116">*лреф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1ee92-116">*lRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ee92-117">Ссылка на смарт-карту.</span><span class="sxs-lookup"><span data-stu-id="1ee92-117">Smart card specific reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ee92-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1ee92-118">Return value</span></span>

<span data-ttu-id="1ee92-119">Метод **Verify** возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="1ee92-119">The **Verify** method returns one of the following values:</span></span>



| <span data-ttu-id="1ee92-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1ee92-120">Return code</span></span>                                                                                   | <span data-ttu-id="1ee92-121">Описание</span><span class="sxs-lookup"><span data-stu-id="1ee92-121">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="1ee92-122"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="1ee92-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1ee92-123">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="1ee92-123">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="1ee92-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1ee92-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1ee92-125">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="1ee92-125">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="1ee92-126"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="1ee92-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="1ee92-127">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="1ee92-127">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="1ee92-128"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1ee92-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1ee92-129">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="1ee92-129">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="1ee92-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1ee92-130">Remarks</span></span>

<span data-ttu-id="1ee92-131">Список всех методов, определенных этим интерфейсом, см. в разделе [**искардверифи**](iscardverify.md).</span><span class="sxs-lookup"><span data-stu-id="1ee92-131">For a list of all the methods defined by this interface, see [**ISCardVerify**](iscardverify.md).</span></span>

<span data-ttu-id="1ee92-132">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="1ee92-132">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="1ee92-133">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="1ee92-133">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1ee92-134">Требования</span><span class="sxs-lookup"><span data-stu-id="1ee92-134">Requirements</span></span>



| <span data-ttu-id="1ee92-135">Требование</span><span class="sxs-lookup"><span data-stu-id="1ee92-135">Requirement</span></span> | <span data-ttu-id="1ee92-136">Значение</span><span class="sxs-lookup"><span data-stu-id="1ee92-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1ee92-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1ee92-137">Minimum supported client</span></span><br/> | <span data-ttu-id="1ee92-138">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1ee92-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="1ee92-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1ee92-139">Minimum supported server</span></span><br/> | <span data-ttu-id="1ee92-140">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1ee92-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1ee92-141">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="1ee92-141">End of client support</span></span><br/>    | <span data-ttu-id="1ee92-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1ee92-142">Windows XP</span></span><br/>                                |
| <span data-ttu-id="1ee92-143">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="1ee92-143">End of server support</span></span><br/>    | <span data-ttu-id="1ee92-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1ee92-144">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="1ee92-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ee92-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ee92-146">**искардверифи**</span><span class="sxs-lookup"><span data-stu-id="1ee92-146">**ISCardVerify**</span></span>](iscardverify.md)
</dt> </dl>

 

 
