---
title: Свойство Максволуме Активебасикдевице (Плайтодевице. h)
description: Возвращает максимальный объем, поддерживаемый устройством.
ms.assetid: EA0EC323-4A18-4CC1-8FA4-7BD302318863
keywords:
- API потоковой передачи мультимедиа свойства Максволуме
- API потоковой передачи мультимедиа свойства Максволуме, интерфейс Активебасикдевице
- API потоковой передачи мультимедиа интерфейса Активебасикдевице, свойство Максволуме
topic_type:
- apiref
api_name:
- ActiveBasicDevice.MaxVolume
- ActiveBasicDevice.get_MaxVolume
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b48c25ef6c0e25c35ba07914c00fb063b4e8dc79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492981"
---
# <a name="activebasicdevicemaxvolume-property"></a><span data-ttu-id="f2944-106">Свойство Активебасикдевице:: Максволуме</span><span class="sxs-lookup"><span data-stu-id="f2944-106">ActiveBasicDevice::MaxVolume property</span></span>

<span data-ttu-id="f2944-107">Возвращает максимальный объем, поддерживаемый устройством.</span><span class="sxs-lookup"><span data-stu-id="f2944-107">Gets the maximum volume supported by the device.</span></span>

<span data-ttu-id="f2944-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f2944-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2944-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2944-109">Syntax</span></span>


```C++
HRESULT get_MaxVolume(
  [out] boolean *UINT32
);
```



## <a name="property-value"></a><span data-ttu-id="f2944-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f2944-110">Property value</span></span>

<span data-ttu-id="f2944-111">Указатель на **UINT32** , указывающий максимальный объем, поддерживаемый устройством.</span><span class="sxs-lookup"><span data-stu-id="f2944-111">A pointer to a **UINT32** that specifies the maximum volume supported by the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2944-112">Требования</span><span class="sxs-lookup"><span data-stu-id="f2944-112">Requirements</span></span>



| <span data-ttu-id="f2944-113">Требование</span><span class="sxs-lookup"><span data-stu-id="f2944-113">Requirement</span></span> | <span data-ttu-id="f2944-114">Значение</span><span class="sxs-lookup"><span data-stu-id="f2944-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2944-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2944-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f2944-116">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f2944-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f2944-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2944-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f2944-118">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f2944-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f2944-119">Header</span><span class="sxs-lookup"><span data-stu-id="f2944-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2944-120"><dt>Плайтодевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2944-120"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="f2944-121">IDL</span><span class="sxs-lookup"><span data-stu-id="f2944-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f2944-122"><dt>Плайтодевице. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f2944-122"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="f2944-123">DLL</span><span class="sxs-lookup"><span data-stu-id="f2944-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2944-124"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2944-124"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2944-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2944-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="f2944-126">[**активебасикдевице**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f2944-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

