---
description: Возвращает значение, представляющее возможности устройства планшета.
ms.assetid: 68936dab-3df4-42c4-9945-bcd525c996f3
title: 'Метод Итаблет:: Жесардварекапс'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetHardwareCaps
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5ada3ad58699952bac5458ddd079abaf84f63bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912340"
---
# <a name="itabletgethardwarecaps-method"></a><span data-ttu-id="3ae5b-103">Метод Итаблет:: Жесардварекапс</span><span class="sxs-lookup"><span data-stu-id="3ae5b-103">ITablet::GetHardwareCaps method</span></span>

<span data-ttu-id="3ae5b-104">Возвращает значение, представляющее возможности устройства планшета.</span><span class="sxs-lookup"><span data-stu-id="3ae5b-104">Returns a value that represents the capabilities of the tablet hardware.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ae5b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3ae5b-105">Syntax</span></span>


```C++
HRESULT GetHardwareCaps(
  [out] DWORD *pdwCaps
);
```



## <a name="parameters"></a><span data-ttu-id="3ae5b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ae5b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ae5b-107">*пдвкапс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3ae5b-107">*pdwCaps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ae5b-108">Битовые флаги, представляющие возможности планшетного оборудования.</span><span class="sxs-lookup"><span data-stu-id="3ae5b-108">Bit flags that represent the capabilities of the tablet hardware.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ae5b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ae5b-109">Return value</span></span>

<span data-ttu-id="3ae5b-110">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="3ae5b-110">This method can return one of these values.</span></span>



| <span data-ttu-id="3ae5b-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3ae5b-111">Return code</span></span>                                                                            | <span data-ttu-id="3ae5b-112">Описание</span><span class="sxs-lookup"><span data-stu-id="3ae5b-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="3ae5b-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="3ae5b-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="3ae5b-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="3ae5b-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="3ae5b-115"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="3ae5b-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="3ae5b-116">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="3ae5b-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3ae5b-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3ae5b-117">Remarks</span></span>

<span data-ttu-id="3ae5b-118">Параметр *пдвкапс* представляет собой набор битовых флагов, описывающих возможности планшетного оборудования.</span><span class="sxs-lookup"><span data-stu-id="3ae5b-118">The *pdwCaps* parameter is a set of bit flags that describe tablet hardware capabilities.</span></span> <span data-ttu-id="3ae5b-119">Эти флаги описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3ae5b-119">The following table describes these flags.</span></span>



| <span data-ttu-id="3ae5b-120">Имя флага</span><span class="sxs-lookup"><span data-stu-id="3ae5b-120">Flag Name</span></span>                         | <span data-ttu-id="3ae5b-121">Значение</span><span class="sxs-lookup"><span data-stu-id="3ae5b-121">Value</span></span>                 | <span data-ttu-id="3ae5b-122">Описание</span><span class="sxs-lookup"><span data-stu-id="3ae5b-122">Description</span></span>                                                                                                                    |
|-----------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ae5b-123">\_Встроенная СВК</span><span class="sxs-lookup"><span data-stu-id="3ae5b-123">THWC\_INTEGRATED</span></span><br/>       | <span data-ttu-id="3ae5b-124">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3ae5b-124">0x00000001</span></span><br/> | <span data-ttu-id="3ae5b-125">Указывает, что экран и дигитайзер имеют одну и ту же поверхность.</span><span class="sxs-lookup"><span data-stu-id="3ae5b-125">Indicates that the display and digitizer share the same surface.</span></span><br/>                                                    |
| <span data-ttu-id="3ae5b-126">СВК \_ CSR \_ должен \_ касаться</span><span class="sxs-lookup"><span data-stu-id="3ae5b-126">THWC\_CSR\_MUST\_TOUCH</span></span><br/> | <span data-ttu-id="3ae5b-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="3ae5b-127">0x00000002</span></span><br/> | <span data-ttu-id="3ae5b-128">Указывает, что курсор должен находиться в физическом контакте с устройством для отчета о положении.</span><span class="sxs-lookup"><span data-stu-id="3ae5b-128">Indicates that the cursor must be in physical contact with the device to report position.</span></span><br/>                           |
| <span data-ttu-id="3ae5b-129">СВК \_ жесткое \_ сходство</span><span class="sxs-lookup"><span data-stu-id="3ae5b-129">THWC\_HARD\_PROXIMITY</span></span><br/>  | <span data-ttu-id="3ae5b-130">0x00000004</span><span class="sxs-lookup"><span data-stu-id="3ae5b-130">0x00000004</span></span><br/> | <span data-ttu-id="3ae5b-131">Указывает, что устройство может создавать события при вводе курсора и открывая диапазон физического обнаружения.</span><span class="sxs-lookup"><span data-stu-id="3ae5b-131">Indicates that the device can generate events when the cursor is entering and leaving the physical detection range.</span></span><br/> |
| <span data-ttu-id="3ae5b-132">\_представители СВК фисид \_</span><span class="sxs-lookup"><span data-stu-id="3ae5b-132">THWC\_PHYSID\_CSRS</span></span><br/>     | <span data-ttu-id="3ae5b-133">0x00000008</span><span class="sxs-lookup"><span data-stu-id="3ae5b-133">0x00000008</span></span><br/> | <span data-ttu-id="3ae5b-134">Указывает, что устройство может однозначно идентифицировать активный курсор в оборудовании.</span><span class="sxs-lookup"><span data-stu-id="3ae5b-134">Indicates that the device can uniquely identify the active cursor in hardware.</span></span><br/>                                      |



 

## <a name="requirements"></a><span data-ttu-id="3ae5b-135">Требования</span><span class="sxs-lookup"><span data-stu-id="3ae5b-135">Requirements</span></span>



| <span data-ttu-id="3ae5b-136">Требование</span><span class="sxs-lookup"><span data-stu-id="3ae5b-136">Requirement</span></span> | <span data-ttu-id="3ae5b-137">Значение</span><span class="sxs-lookup"><span data-stu-id="3ae5b-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ae5b-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3ae5b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="3ae5b-139">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3ae5b-139">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3ae5b-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3ae5b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="3ae5b-141">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3ae5b-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3ae5b-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3ae5b-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="3ae5b-143"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3ae5b-143"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ae5b-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ae5b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ae5b-145">**Интерфейс Итаблет**</span><span class="sxs-lookup"><span data-stu-id="3ae5b-145">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

 




