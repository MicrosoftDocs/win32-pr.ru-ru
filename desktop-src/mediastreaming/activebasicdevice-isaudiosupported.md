---
title: Свойство Исаудиосуппортед Активебасикдевице (Плайтодевице. h)
description: Возвращает значение, указывающее, поддерживает ли устройство аудио.
ms.assetid: 22ABB97B-58E7-4C21-B359-C10DFC9C7194
keywords:
- API потоковой передачи мультимедиа свойства Исаудиосуппортед
- API потоковой передачи мультимедиа свойства Исаудиосуппортед, интерфейс Активебасикдевице
- API потоковой передачи мультимедиа интерфейса Активебасикдевице, свойство Исаудиосуппортед
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsAudioSupported
- ActiveBasicDevice.get_IsAudioSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66058da9dcdbac0ed1100b0ef21a4ed530d45a68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071999"
---
# <a name="activebasicdeviceisaudiosupported-property"></a><span data-ttu-id="5dbe4-106">Свойство Активебасикдевице:: Исаудиосуппортед</span><span class="sxs-lookup"><span data-stu-id="5dbe4-106">ActiveBasicDevice::IsAudioSupported property</span></span>

<span data-ttu-id="5dbe4-107">Возвращает значение, указывающее, поддерживает ли устройство аудио.</span><span class="sxs-lookup"><span data-stu-id="5dbe4-107">Gets a value that indicates if the device supports audio.</span></span>

<span data-ttu-id="5dbe4-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5dbe4-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dbe4-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5dbe4-109">Syntax</span></span>


```C++
HRESULT get_IsAudioSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="5dbe4-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5dbe4-110">Property value</span></span>

<span data-ttu-id="5dbe4-111">Указатель на **логическое значение** , указывающее, поддерживает ли устройство аудио.</span><span class="sxs-lookup"><span data-stu-id="5dbe4-111">A pointer to a **boolean** that indicates if the device supports audio.</span></span>

<span data-ttu-id="5dbe4-112">**значение true** , если устройство поддерживает аудио; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="5dbe4-112">**true** if the device supports audio; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dbe4-113">Требования</span><span class="sxs-lookup"><span data-stu-id="5dbe4-113">Requirements</span></span>



| <span data-ttu-id="5dbe4-114">Требование</span><span class="sxs-lookup"><span data-stu-id="5dbe4-114">Requirement</span></span> | <span data-ttu-id="5dbe4-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5dbe4-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5dbe4-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5dbe4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5dbe4-117">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5dbe4-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5dbe4-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5dbe4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5dbe4-119">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5dbe4-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5dbe4-120">Header</span><span class="sxs-lookup"><span data-stu-id="5dbe4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5dbe4-121"><dt>Плайтодевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="5dbe4-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="5dbe4-122">IDL</span><span class="sxs-lookup"><span data-stu-id="5dbe4-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5dbe4-123"><dt>Плайтодевице. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5dbe4-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="5dbe4-124">DLL</span><span class="sxs-lookup"><span data-stu-id="5dbe4-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5dbe4-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5dbe4-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5dbe4-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5dbe4-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="5dbe4-127">[**активебасикдевице**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5dbe4-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

