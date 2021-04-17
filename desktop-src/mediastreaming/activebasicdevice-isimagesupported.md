---
title: Свойство Исимажесуппортед Активебасикдевице (Плайтодевице. h)
description: Возвращает значение, указывающее, поддерживает ли устройство изображения.
ms.assetid: FC53B87C-D739-4AD4-9DD3-415AC8692224
keywords:
- API потоковой передачи мультимедиа свойства Исимажесуппортед
- API потоковой передачи мультимедиа свойства Исимажесуппортед, интерфейс Активебасикдевице
- API потоковой передачи мультимедиа интерфейса Активебасикдевице, свойство Исимажесуппортед
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsImageSupported
- ActiveBasicDevice.get_IsImageSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2e90f51d2dd59ffec8221787b9ee7c247536abb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691774"
---
# <a name="activebasicdeviceisimagesupported-property"></a><span data-ttu-id="affb3-106">Свойство Активебасикдевице:: Исимажесуппортед</span><span class="sxs-lookup"><span data-stu-id="affb3-106">ActiveBasicDevice::IsImageSupported property</span></span>

<span data-ttu-id="affb3-107">Возвращает значение, указывающее, поддерживает ли устройство изображения.</span><span class="sxs-lookup"><span data-stu-id="affb3-107">Gets a value that indicates if the device supports images.</span></span>

<span data-ttu-id="affb3-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="affb3-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="affb3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="affb3-109">Syntax</span></span>


```C++
HRESULT get_IsImageSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="affb3-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="affb3-110">Property value</span></span>

<span data-ttu-id="affb3-111">Указатель на **логическое значение** , указывающее, поддерживает ли устройство изображения.</span><span class="sxs-lookup"><span data-stu-id="affb3-111">A pointer to a **boolean** that indicates if the device supports images.</span></span>

<span data-ttu-id="affb3-112">**значение true** , если устройство поддерживает образы; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="affb3-112">**true** if the device supports images; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="affb3-113">Требования</span><span class="sxs-lookup"><span data-stu-id="affb3-113">Requirements</span></span>



| <span data-ttu-id="affb3-114">Требование</span><span class="sxs-lookup"><span data-stu-id="affb3-114">Requirement</span></span> | <span data-ttu-id="affb3-115">Значение</span><span class="sxs-lookup"><span data-stu-id="affb3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="affb3-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="affb3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="affb3-117">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="affb3-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="affb3-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="affb3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="affb3-119">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="affb3-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="affb3-120">Header</span><span class="sxs-lookup"><span data-stu-id="affb3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="affb3-121"><dt>Плайтодевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="affb3-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="affb3-122">IDL</span><span class="sxs-lookup"><span data-stu-id="affb3-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="affb3-123"><dt>Плайтодевице. idl</dt></span><span class="sxs-lookup"><span data-stu-id="affb3-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="affb3-124">DLL</span><span class="sxs-lookup"><span data-stu-id="affb3-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="affb3-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="affb3-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="affb3-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="affb3-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="affb3-127">[**активебасикдевице**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="affb3-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

