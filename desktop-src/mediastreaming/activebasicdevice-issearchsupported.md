---
title: Свойство Иссеарчсуппортед Активебасикдевице (Плайтодевице. h)
description: Возвращает значение, указывающее, поддерживает ли устройство Поиск.
ms.assetid: 091D467A-1FF6-4635-BF89-4E62AC9C660A
keywords:
- API потоковой передачи мультимедиа свойства Иссеарчсуппортед
- API потоковой передачи мультимедиа свойства Иссеарчсуппортед, интерфейс Активебасикдевице
- API потоковой передачи мультимедиа интерфейса Активебасикдевице, свойство Иссеарчсуппортед
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsSearchSupported
- ActiveBasicDevice.get_IsSearchSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff97b20697388b1e3079f6993b97b948fa12091e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416081"
---
# <a name="activebasicdeviceissearchsupported-property"></a><span data-ttu-id="1183b-106">Свойство Активебасикдевице:: Иссеарчсуппортед</span><span class="sxs-lookup"><span data-stu-id="1183b-106">ActiveBasicDevice::IsSearchSupported property</span></span>

<span data-ttu-id="1183b-107">Возвращает значение, указывающее, поддерживает ли устройство Поиск.</span><span class="sxs-lookup"><span data-stu-id="1183b-107">Gets a value that indicates if the device supports search.</span></span>

<span data-ttu-id="1183b-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1183b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1183b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1183b-109">Syntax</span></span>


```C++
HRESULT get_IsSearchSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="1183b-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1183b-110">Property value</span></span>

<span data-ttu-id="1183b-111">Указатель на **логическое значение** , указывающее, поддерживает ли устройство Поиск.</span><span class="sxs-lookup"><span data-stu-id="1183b-111">A pointer to a **boolean** that indicates if the device supports search.</span></span>

<span data-ttu-id="1183b-112">**значение true** , если устройство поддерживает поиск; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="1183b-112">**true** if the device supports search; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1183b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="1183b-113">Requirements</span></span>



| <span data-ttu-id="1183b-114">Требование</span><span class="sxs-lookup"><span data-stu-id="1183b-114">Requirement</span></span> | <span data-ttu-id="1183b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="1183b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1183b-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1183b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1183b-117">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1183b-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1183b-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1183b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1183b-119">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1183b-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1183b-120">Header</span><span class="sxs-lookup"><span data-stu-id="1183b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1183b-121"><dt>Плайтодевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="1183b-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="1183b-122">IDL</span><span class="sxs-lookup"><span data-stu-id="1183b-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1183b-123"><dt>Плайтодевице. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1183b-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="1183b-124">DLL</span><span class="sxs-lookup"><span data-stu-id="1183b-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1183b-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1183b-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1183b-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1183b-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="1183b-127">[**активебасикдевице**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1183b-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

