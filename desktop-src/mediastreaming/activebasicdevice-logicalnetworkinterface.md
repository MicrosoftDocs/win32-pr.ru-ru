---
title: Свойство Логикалнетворкинтерфаце Активебасикдевице (Плайтодевице. h)
description: Возвращает идентификатор логического сетевого интерфейса.
ms.assetid: 47C2E0BE-D3E3-4A9F-9FC6-873882811506
keywords:
- API потоковой передачи мультимедиа свойства Логикалнетворкинтерфаце
- API потоковой передачи мультимедиа свойства Логикалнетворкинтерфаце, интерфейс Активебасикдевице
- API потоковой передачи мультимедиа интерфейса Активебасикдевице, свойство Логикалнетворкинтерфаце
topic_type:
- apiref
api_name:
- ActiveBasicDevice.LogicalNetworkInterface
- ActiveBasicDevice.get_LogicalNetworkInterface
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95a87f2951ea09a0bba3d56da50b8f77a9d4a980
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415384"
---
# <a name="activebasicdevicelogicalnetworkinterface-property"></a><span data-ttu-id="472d1-106">Свойство Активебасикдевице:: Логикалнетворкинтерфаце</span><span class="sxs-lookup"><span data-stu-id="472d1-106">ActiveBasicDevice::LogicalNetworkInterface property</span></span>

<span data-ttu-id="472d1-107">Возвращает идентификатор логического сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="472d1-107">Gets the id of the logical network interface.</span></span>

<span data-ttu-id="472d1-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="472d1-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="472d1-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="472d1-109">Syntax</span></span>


```C++
HRESULT get_LogicalNetworkInterface(
  [out] GUID *value
);
```



## <a name="property-value"></a><span data-ttu-id="472d1-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="472d1-110">Property value</span></span>

<span data-ttu-id="472d1-111">Указатель на **идентификатор GUID** , указывающий идентификатор логического сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="472d1-111">A pointer to a **GUID** that specifies the id of the logical network interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="472d1-112">Требования</span><span class="sxs-lookup"><span data-stu-id="472d1-112">Requirements</span></span>



| <span data-ttu-id="472d1-113">Требование</span><span class="sxs-lookup"><span data-stu-id="472d1-113">Requirement</span></span> | <span data-ttu-id="472d1-114">Значение</span><span class="sxs-lookup"><span data-stu-id="472d1-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="472d1-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="472d1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="472d1-116">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="472d1-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="472d1-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="472d1-117">Minimum supported server</span></span><br/> | <span data-ttu-id="472d1-118">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="472d1-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="472d1-119">Header</span><span class="sxs-lookup"><span data-stu-id="472d1-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="472d1-120"><dt>Плайтодевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="472d1-120"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="472d1-121">IDL</span><span class="sxs-lookup"><span data-stu-id="472d1-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="472d1-122"><dt>Плайтодевице. idl</dt></span><span class="sxs-lookup"><span data-stu-id="472d1-122"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="472d1-123">DLL</span><span class="sxs-lookup"><span data-stu-id="472d1-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="472d1-124"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="472d1-124"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="472d1-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="472d1-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="472d1-126">[**активебасикдевице**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="472d1-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

