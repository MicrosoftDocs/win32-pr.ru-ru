---
title: Свойство Исмутесуппортед Активебасикдевице (Плайтодевице. h)
description: Возвращает значение, указывающее, поддерживает ли устройство отключение звука.
ms.assetid: FF4B533F-B416-4DBE-BF86-FA34E785FFA2
keywords:
- API потоковой передачи мультимедиа свойства Исмутесуппортед
- API потоковой передачи мультимедиа свойства Исмутесуппортед, интерфейс Активебасикдевице
- API потоковой передачи мультимедиа интерфейса Активебасикдевице, свойство Исмутесуппортед
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsMuteSupported
- ActiveBasicDevice.get_IsMuteSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcec2e4520bd3b15b715c01e4369da87887355e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491262"
---
# <a name="activebasicdeviceismutesupported-property"></a><span data-ttu-id="adb94-106">Свойство Активебасикдевице:: Исмутесуппортед</span><span class="sxs-lookup"><span data-stu-id="adb94-106">ActiveBasicDevice::IsMuteSupported property</span></span>

<span data-ttu-id="adb94-107">Возвращает значение, указывающее, поддерживает ли устройство отключение звука.</span><span class="sxs-lookup"><span data-stu-id="adb94-107">Gets a value that indicates if the device supports muting the audio.</span></span>

<span data-ttu-id="adb94-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="adb94-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="adb94-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="adb94-109">Syntax</span></span>


```C++
HRESULT get_IsMuteSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="adb94-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="adb94-110">Property value</span></span>

<span data-ttu-id="adb94-111">Указатель на **логическое значение** , указывающее, поддерживает ли устройство озвучивание звука.</span><span class="sxs-lookup"><span data-stu-id="adb94-111">A pointer to a **boolean** that indicates if the device supports muting the audio.</span></span>

<span data-ttu-id="adb94-112">**значение true** , если устройство поддерживает выключение звука; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="adb94-112">**true** if the device supports muting the audio; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="adb94-113">Требования</span><span class="sxs-lookup"><span data-stu-id="adb94-113">Requirements</span></span>



| <span data-ttu-id="adb94-114">Требование</span><span class="sxs-lookup"><span data-stu-id="adb94-114">Requirement</span></span> | <span data-ttu-id="adb94-115">Значение</span><span class="sxs-lookup"><span data-stu-id="adb94-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="adb94-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="adb94-116">Minimum supported client</span></span><br/> | <span data-ttu-id="adb94-117">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="adb94-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="adb94-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="adb94-118">Minimum supported server</span></span><br/> | <span data-ttu-id="adb94-119">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="adb94-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="adb94-120">Header</span><span class="sxs-lookup"><span data-stu-id="adb94-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="adb94-121"><dt>Плайтодевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="adb94-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="adb94-122">IDL</span><span class="sxs-lookup"><span data-stu-id="adb94-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="adb94-123"><dt>Плайтодевице. idl</dt></span><span class="sxs-lookup"><span data-stu-id="adb94-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="adb94-124">DLL</span><span class="sxs-lookup"><span data-stu-id="adb94-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adb94-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adb94-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adb94-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="adb94-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="adb94-127">[**активебасикдевице**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="adb94-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

