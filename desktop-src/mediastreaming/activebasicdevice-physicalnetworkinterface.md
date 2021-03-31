---
title: Свойство Фисикалнетворкинтерфаце Активебасикдевице (Плайтодевице. h)
description: Возвращает идентификатор физического сетевого интерфейса.
ms.assetid: F426462F-CE26-4EE1-B679-A4C80B2919A5
keywords:
- API потоковой передачи мультимедиа свойства Фисикалнетворкинтерфаце
- API потоковой передачи мультимедиа свойства Фисикалнетворкинтерфаце, интерфейс Активебасикдевице
- API потоковой передачи мультимедиа интерфейса Активебасикдевице, свойство Фисикалнетворкинтерфаце
topic_type:
- apiref
api_name:
- ActiveBasicDevice.PhysicalNetworkInterface
- ActiveBasicDevice.get_PhysicalNetworkInterface
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479618ed4d22a3d78a351fb88fcb1108a27c618f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491259"
---
# <a name="activebasicdevicephysicalnetworkinterface-property"></a><span data-ttu-id="10462-106">Активебасикдевице: свойство Хисикалнетворкинтерфаце:P</span><span class="sxs-lookup"><span data-stu-id="10462-106">ActiveBasicDevice::PhysicalNetworkInterface property</span></span>

<span data-ttu-id="10462-107">Возвращает идентификатор физического сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="10462-107">Gets the id of the physical network interface.</span></span>

<span data-ttu-id="10462-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="10462-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="10462-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="10462-109">Syntax</span></span>


```C++
HRESULT get_PhysicalNetworkInterface(
  [out] GUID *value
);
```



## <a name="property-value"></a><span data-ttu-id="10462-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="10462-110">Property value</span></span>

<span data-ttu-id="10462-111">Указатель на **идентификатор GUID** , указывающий идентификатор физического сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="10462-111">A pointer to a **GUID** that specifies the id of the physical network interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="10462-112">Требования</span><span class="sxs-lookup"><span data-stu-id="10462-112">Requirements</span></span>



| <span data-ttu-id="10462-113">Требование</span><span class="sxs-lookup"><span data-stu-id="10462-113">Requirement</span></span> | <span data-ttu-id="10462-114">Значение</span><span class="sxs-lookup"><span data-stu-id="10462-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="10462-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="10462-115">Minimum supported client</span></span><br/> | <span data-ttu-id="10462-116">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="10462-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="10462-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="10462-117">Minimum supported server</span></span><br/> | <span data-ttu-id="10462-118">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="10462-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="10462-119">Header</span><span class="sxs-lookup"><span data-stu-id="10462-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="10462-120"><dt>Плайтодевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="10462-120"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="10462-121">IDL</span><span class="sxs-lookup"><span data-stu-id="10462-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="10462-122"><dt>Плайтодевице. idl</dt></span><span class="sxs-lookup"><span data-stu-id="10462-122"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="10462-123">DLL</span><span class="sxs-lookup"><span data-stu-id="10462-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10462-124"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10462-124"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10462-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="10462-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="10462-126">[**активебасикдевице**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="10462-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

