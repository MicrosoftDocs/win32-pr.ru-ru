---
description: Создает интерфейс Искардфилеакцесс.
ms.assetid: 06a5948f-c7bd-49bf-9032-f40f3d0d330c
title: 'Метод Искардманаже:: Креатефилеакцесс'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateFileAccess
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3eb1f544e05959cc33119091268e1c7fe6266547
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651094"
---
# <a name="iscardmanagecreatefileaccess-method"></a><span data-ttu-id="d0226-103">Метод Искардманаже:: Креатефилеакцесс</span><span class="sxs-lookup"><span data-stu-id="d0226-103">ISCardManage::CreateFileAccess method</span></span>

<span data-ttu-id="d0226-104">\[Метод **креатефилеакцесс** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="d0226-104">\[The **CreateFileAccess** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d0226-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d0226-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d0226-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="d0226-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d0226-107">Метод **креатефилеакцесс** создает интерфейс [**искардфилеакцесс**](iscardfileaccess.md) .</span><span class="sxs-lookup"><span data-stu-id="d0226-107">The **CreateFileAccess** method creates an [**ISCardFileAccess**](iscardfileaccess.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0226-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d0226-108">Syntax</span></span>


```C++
HRESULT CreateFileAccess(
  [out] ISCardFileAccess **ppISCardFileAccess
);
```



## <a name="parameters"></a><span data-ttu-id="d0226-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d0226-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0226-110">*ппискардфилеакцесс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d0226-110">*ppISCardFileAccess* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0226-111">Возвращен указатель на созданный интерфейс [**искардфилеакцесс**](iscardfileaccess.md) .</span><span class="sxs-lookup"><span data-stu-id="d0226-111">Returned pointer to the created [**ISCardFileAccess**](iscardfileaccess.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0226-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d0226-112">Return value</span></span>

<span data-ttu-id="d0226-113">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="d0226-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="d0226-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d0226-114">Return code</span></span>                                                                                   | <span data-ttu-id="d0226-115">Описание</span><span class="sxs-lookup"><span data-stu-id="d0226-115">Description</span></span>                                                  |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="d0226-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="d0226-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d0226-117">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="d0226-117">Operation completed successfully.</span></span><br/>                 |
| <dl> <span data-ttu-id="d0226-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d0226-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d0226-119">Недопустимый параметр *ппискардфилеакцесс* .</span><span class="sxs-lookup"><span data-stu-id="d0226-119">The *ppISCardFileAccess* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="d0226-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="d0226-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d0226-121">В *ппискардфилеакцесс* был передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="d0226-121">A bad pointer was passed in *ppISCardFileAccess*.</span></span><br/> |
| <dl> <span data-ttu-id="d0226-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d0226-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d0226-123">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="d0226-123">Out of memory.</span></span><br/>                                    |



 

## <a name="remarks"></a><span data-ttu-id="d0226-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d0226-124">Remarks</span></span>

<span data-ttu-id="d0226-125">Список всех методов, определенных этим интерфейсом, см. в разделе [**искардманаже**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="d0226-125">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="d0226-126">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="d0226-126">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="d0226-127">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="d0226-127">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0226-128">Требования</span><span class="sxs-lookup"><span data-stu-id="d0226-128">Requirements</span></span>



| <span data-ttu-id="d0226-129">Требование</span><span class="sxs-lookup"><span data-stu-id="d0226-129">Requirement</span></span> | <span data-ttu-id="d0226-130">Значение</span><span class="sxs-lookup"><span data-stu-id="d0226-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d0226-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d0226-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d0226-132">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d0226-132">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="d0226-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d0226-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d0226-134">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d0226-134">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d0226-135">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d0226-135">End of client support</span></span><br/>    | <span data-ttu-id="d0226-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d0226-136">Windows XP</span></span><br/>                                |
| <span data-ttu-id="d0226-137">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="d0226-137">End of server support</span></span><br/>    | <span data-ttu-id="d0226-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d0226-138">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="d0226-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d0226-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0226-140">**искардфилеакцесс**</span><span class="sxs-lookup"><span data-stu-id="d0226-140">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> <dt>

[<span data-ttu-id="d0226-141">**искардманаже**</span><span class="sxs-lookup"><span data-stu-id="d0226-141">**ISCardManage**</span></span>](iscardmanage.md)
</dt> </dl>

 

 
