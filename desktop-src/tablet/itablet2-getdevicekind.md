---
description: Возвращает тип аппаратного устройства, которое представляет объект планшета, например мышь, перо или сенсорный ввод.
ms.assetid: 693cb45f-958d-42e2-a3ee-a7cfcc72e5c3
title: 'Метод ITablet2:: Жетдевицекинд'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet2.GetDeviceKind
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: f20b1fe6a5a48196f6b3adc5982f2596d93f0863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719563"
---
# <a name="itablet2getdevicekind-method"></a><span data-ttu-id="77979-103">Метод ITablet2:: Жетдевицекинд</span><span class="sxs-lookup"><span data-stu-id="77979-103">ITablet2::GetDeviceKind method</span></span>

<span data-ttu-id="77979-104">Возвращает тип аппаратного устройства, которое представляет объект планшета, например мышь, перо или сенсорный ввод.</span><span class="sxs-lookup"><span data-stu-id="77979-104">Returns the type of hardware device the tablet object represents such as mouse, pen or touch.</span></span>

## <a name="syntax"></a><span data-ttu-id="77979-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="77979-105">Syntax</span></span>


```C++
HRESULT GetDeviceKind(
  [out] TABLET_DEVICE_KIND *pKind
);
```



## <a name="parameters"></a><span data-ttu-id="77979-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="77979-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77979-107">*пкинд* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="77979-107">*pKind* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77979-108">Значение перечисления, указывающее тип планшета, например мышь, перо или сенсорный ввод.</span><span class="sxs-lookup"><span data-stu-id="77979-108">Enumeration value that indicates the type of tablet such as mouse, pen or touch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77979-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="77979-109">Return value</span></span>

<span data-ttu-id="77979-110">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="77979-110">This method can return one of these values.</span></span>



| <span data-ttu-id="77979-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="77979-111">Return code</span></span>                                                                            | <span data-ttu-id="77979-112">Описание</span><span class="sxs-lookup"><span data-stu-id="77979-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="77979-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="77979-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="77979-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="77979-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="77979-115"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="77979-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="77979-116">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="77979-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="77979-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="77979-117">Remarks</span></span>

<span data-ttu-id="77979-118">Этот интерфейс и метод появились в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="77979-118">This interface and method were introduced in Windows Vista.</span></span>

## <a name="requirements"></a><span data-ttu-id="77979-119">Требования</span><span class="sxs-lookup"><span data-stu-id="77979-119">Requirements</span></span>



| <span data-ttu-id="77979-120">Требование</span><span class="sxs-lookup"><span data-stu-id="77979-120">Requirement</span></span> | <span data-ttu-id="77979-121">Значение</span><span class="sxs-lookup"><span data-stu-id="77979-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="77979-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="77979-122">Minimum supported client</span></span><br/> | <span data-ttu-id="77979-123">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="77979-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="77979-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="77979-124">Minimum supported server</span></span><br/> | <span data-ttu-id="77979-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="77979-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="77979-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="77979-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="77979-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="77979-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77979-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="77979-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77979-129">**Интерфейс ITablet2**</span><span class="sxs-lookup"><span data-stu-id="77979-129">**ITablet2 Interface**</span></span>](itablet2.md)
</dt> <dt>

[<span data-ttu-id="77979-130">**\_Перечисление типов планшетных устройств \_**</span><span class="sxs-lookup"><span data-stu-id="77979-130">**TABLET\_DEVICE\_KIND Enumeration**</span></span>](tablet-device-kind.md)
</dt> <dt>

[<span data-ttu-id="77979-131">**Интерфейс Итаблет**</span><span class="sxs-lookup"><span data-stu-id="77979-131">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

 




