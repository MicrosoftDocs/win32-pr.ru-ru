---
title: Свойство Исвидеосуппортед Активебасикдевице (Плайтодевице. h)
description: Возвращает значение, указывающее, поддерживает ли устройство видео.
ms.assetid: E8D33A04-748D-42F8-878F-35D973A6B559
keywords:
- API потоковой передачи мультимедиа свойства Исвидеосуппортед
- API потоковой передачи мультимедиа свойства Исвидеосуппортед, интерфейс Активебасикдевице
- API потоковой передачи мультимедиа интерфейса Активебасикдевице, свойство Исвидеосуппортед
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsVideoSupported
- ActiveBasicDevice.get_IsVideoSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2be369b34355b199cd47518065724242b9a422e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710545"
---
# <a name="activebasicdeviceisvideosupported-property"></a><span data-ttu-id="8e163-106">Свойство Активебасикдевице:: Исвидеосуппортед</span><span class="sxs-lookup"><span data-stu-id="8e163-106">ActiveBasicDevice::IsVideoSupported property</span></span>

<span data-ttu-id="8e163-107">Возвращает значение, указывающее, поддерживает ли устройство видео.</span><span class="sxs-lookup"><span data-stu-id="8e163-107">Gets a value that indicates if the device supports video.</span></span>

<span data-ttu-id="8e163-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="8e163-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e163-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e163-109">Syntax</span></span>


```C++
HRESULT get_IsVideoSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="8e163-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="8e163-110">Property value</span></span>

<span data-ttu-id="8e163-111">Указатель на **логическое значение** , указывающее, поддерживает ли устройство видео.</span><span class="sxs-lookup"><span data-stu-id="8e163-111">A pointer to a **boolean** that indicates if the device supports video.</span></span>

<span data-ttu-id="8e163-112">**значение true** , если устройство поддерживает видео; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="8e163-112">**true** if the device supports video; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e163-113">Требования</span><span class="sxs-lookup"><span data-stu-id="8e163-113">Requirements</span></span>



| <span data-ttu-id="8e163-114">Требование</span><span class="sxs-lookup"><span data-stu-id="8e163-114">Requirement</span></span> | <span data-ttu-id="8e163-115">Значение</span><span class="sxs-lookup"><span data-stu-id="8e163-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e163-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8e163-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8e163-117">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8e163-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8e163-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8e163-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8e163-119">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8e163-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8e163-120">Header</span><span class="sxs-lookup"><span data-stu-id="8e163-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e163-121"><dt>Плайтодевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e163-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="8e163-122">IDL</span><span class="sxs-lookup"><span data-stu-id="8e163-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8e163-123"><dt>Плайтодевице. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8e163-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="8e163-124">DLL</span><span class="sxs-lookup"><span data-stu-id="8e163-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e163-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e163-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e163-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e163-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="8e163-127">[**активебасикдевице**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8e163-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

