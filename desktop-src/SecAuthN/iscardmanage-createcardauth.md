---
description: Создает интерфейс Искардаус.
ms.assetid: a091e361-416e-45c9-8077-617b16db654c
title: 'Метод Искардманаже:: Креатекардаус'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateCardAuth
api_type:
- COM
api_location: ''
ms.openlocfilehash: d0b81fd8211491527f39999c6873f7b047bcb32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650875"
---
# <a name="iscardmanagecreatecardauth-method"></a><span data-ttu-id="f11cc-103">Метод Искардманаже:: Креатекардаус</span><span class="sxs-lookup"><span data-stu-id="f11cc-103">ISCardManage::CreateCardAuth method</span></span>

<span data-ttu-id="f11cc-104">\[Метод **креатекардаус** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="f11cc-104">\[The **CreateCardAuth** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f11cc-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="f11cc-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f11cc-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="f11cc-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="f11cc-107">Метод **креатекардаус** создает интерфейс [**искардаус**](iscardauth.md) .</span><span class="sxs-lookup"><span data-stu-id="f11cc-107">The **CreateCardAuth** method creates an [**ISCardAuth**](iscardauth.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="f11cc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f11cc-108">Syntax</span></span>


```C++
HRESULT CreateCardAuth(
  [out] ISCardAuth **ppISCardAuth
);
```



## <a name="parameters"></a><span data-ttu-id="f11cc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f11cc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f11cc-110">*ппискардаус* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f11cc-110">*ppISCardAuth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f11cc-111">Возвращен указатель на созданный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="f11cc-111">Returned pointer to the created interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f11cc-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f11cc-112">Return value</span></span>

<span data-ttu-id="f11cc-113">Метод возвращает одно из следующих возможных значений:</span><span class="sxs-lookup"><span data-stu-id="f11cc-113">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="f11cc-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f11cc-114">Return code</span></span>                                                                                   | <span data-ttu-id="f11cc-115">Описание</span><span class="sxs-lookup"><span data-stu-id="f11cc-115">Description</span></span>                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="f11cc-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="f11cc-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f11cc-117">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="f11cc-117">Operation completed successfully.</span></span><br/>           |
| <dl> <span data-ttu-id="f11cc-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f11cc-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f11cc-119">Недопустимый параметр *ппискардаус* .</span><span class="sxs-lookup"><span data-stu-id="f11cc-119">The *ppISCardAuth* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="f11cc-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="f11cc-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f11cc-121">В *ппискардаус* был передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="f11cc-121">A bad pointer was passed in *ppISCardAuth*.</span></span><br/> |
| <dl> <span data-ttu-id="f11cc-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f11cc-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f11cc-123">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="f11cc-123">Out of memory.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="f11cc-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f11cc-124">Remarks</span></span>

<span data-ttu-id="f11cc-125">Список всех методов, определенных этим интерфейсом, см. в разделе [**искардманаже**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="f11cc-125">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="f11cc-126">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="f11cc-126">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="f11cc-127">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="f11cc-127">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f11cc-128">Требования</span><span class="sxs-lookup"><span data-stu-id="f11cc-128">Requirements</span></span>



| <span data-ttu-id="f11cc-129">Требование</span><span class="sxs-lookup"><span data-stu-id="f11cc-129">Requirement</span></span> | <span data-ttu-id="f11cc-130">Значение</span><span class="sxs-lookup"><span data-stu-id="f11cc-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f11cc-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f11cc-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f11cc-132">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f11cc-132">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="f11cc-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f11cc-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f11cc-134">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f11cc-134">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f11cc-135">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="f11cc-135">End of client support</span></span><br/>    | <span data-ttu-id="f11cc-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f11cc-136">Windows XP</span></span><br/>                                |
| <span data-ttu-id="f11cc-137">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="f11cc-137">End of server support</span></span><br/>    | <span data-ttu-id="f11cc-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f11cc-138">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="f11cc-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f11cc-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f11cc-140">**искардманаже**</span><span class="sxs-lookup"><span data-stu-id="f11cc-140">**ISCardManage**</span></span>](iscardmanage.md)
</dt> </dl>

 

 
