---
description: Создает интерфейс Искардверифи.
ms.assetid: 6338e672-83cd-46fe-8f94-f4ba6e2581ea
title: 'Метод Искардманаже:: Креатечверификатион'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateCHVerification
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3a5909a8782571f9bd01a1c31e5ccd04c3d029df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266240"
---
# <a name="iscardmanagecreatechverification-method"></a><span data-ttu-id="c1548-103">Метод Искардманаже:: Креатечверификатион</span><span class="sxs-lookup"><span data-stu-id="c1548-103">ISCardManage::CreateCHVerification method</span></span>

<span data-ttu-id="c1548-104">\[Метод **креатечверификатион** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="c1548-104">\[The **CreateCHVerification** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c1548-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="c1548-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c1548-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="c1548-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="c1548-107">Метод **креатечверификатион** создает интерфейс [**искардверифи**](iscardverify.md) .</span><span class="sxs-lookup"><span data-stu-id="c1548-107">The **CreateCHVerification** method creates an [**ISCardVerify**](iscardverify.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1548-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1548-108">Syntax</span></span>


```C++
HRESULT CreateCHVerification(
  [out] ISCardVerify **ppISCardVerify
);
```



## <a name="parameters"></a><span data-ttu-id="c1548-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1548-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1548-110">*ппискардверифи* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c1548-110">*ppISCardVerify* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1548-111">Возвращен указатель на созданный интерфейс [**искардверифи**](iscardverify.md) .</span><span class="sxs-lookup"><span data-stu-id="c1548-111">Returned pointer to the created [**ISCardVerify**](iscardverify.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1548-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c1548-112">Return value</span></span>

<span data-ttu-id="c1548-113">Метод возвращает одно из следующих возможных значений:</span><span class="sxs-lookup"><span data-stu-id="c1548-113">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="c1548-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c1548-114">Return code</span></span>                                                                                   | <span data-ttu-id="c1548-115">Описание</span><span class="sxs-lookup"><span data-stu-id="c1548-115">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="c1548-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c1548-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c1548-117">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="c1548-117">Operation completed successfully.</span></span><br/>             |
| <dl> <span data-ttu-id="c1548-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c1548-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c1548-119">Недопустимый параметр *ппискардверифи* .</span><span class="sxs-lookup"><span data-stu-id="c1548-119">The *ppISCardVerify* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="c1548-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="c1548-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c1548-121">В *ппискардверифи* был передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="c1548-121">A bad pointer was passed in *ppISCardVerify*.</span></span><br/> |
| <dl> <span data-ttu-id="c1548-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c1548-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c1548-123">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="c1548-123">Out of memory.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="c1548-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c1548-124">Remarks</span></span>

<span data-ttu-id="c1548-125">Список всех методов, определенных этим интерфейсом, см. в разделе [**искардманаже**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="c1548-125">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="c1548-126">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="c1548-126">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="c1548-127">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="c1548-127">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1548-128">Требования</span><span class="sxs-lookup"><span data-stu-id="c1548-128">Requirements</span></span>



| <span data-ttu-id="c1548-129">Требование</span><span class="sxs-lookup"><span data-stu-id="c1548-129">Requirement</span></span> | <span data-ttu-id="c1548-130">Значение</span><span class="sxs-lookup"><span data-stu-id="c1548-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c1548-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c1548-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c1548-132">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c1548-132">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="c1548-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c1548-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c1548-134">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c1548-134">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c1548-135">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="c1548-135">End of client support</span></span><br/>    | <span data-ttu-id="c1548-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c1548-136">Windows XP</span></span><br/>                                |
| <span data-ttu-id="c1548-137">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="c1548-137">End of server support</span></span><br/>    | <span data-ttu-id="c1548-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c1548-138">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="c1548-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1548-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1548-140">**искардманаже**</span><span class="sxs-lookup"><span data-stu-id="c1548-140">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="c1548-141">**искардверифи**</span><span class="sxs-lookup"><span data-stu-id="c1548-141">**ISCardVerify**</span></span>](iscardverify.md)
</dt> </dl>

 

 
