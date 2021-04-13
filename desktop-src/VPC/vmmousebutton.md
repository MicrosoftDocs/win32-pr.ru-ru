---
title: Перечисление Вммаусебуттон (Впккоминтерфацес. h)
description: Задает кнопку мыши.
ms.assetid: d09e63cb-9dc5-424f-b130-c0b0dd07fe11
keywords:
- Перечисление Вммаусебуттон Virtual PC
topic_type:
- apiref
api_name:
- VMMouseButton
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18744af5a4f8068b9bb371cb15e06c365561f2cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492201"
---
# <a name="vmmousebutton-enumeration"></a><span data-ttu-id="530a3-104">Перечисление Вммаусебуттон</span><span class="sxs-lookup"><span data-stu-id="530a3-104">VMMouseButton enumeration</span></span>

<span data-ttu-id="530a3-105">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="530a3-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="530a3-106">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="530a3-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="530a3-107">Задает кнопку мыши.</span><span class="sxs-lookup"><span data-stu-id="530a3-107">Specifies the mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="530a3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="530a3-108">Syntax</span></span>


```C++
typedef enum  { 
  vmMouseButton_Left    = 1,
  vmMouseButton_Right   = 2,
  vmMouseButton_Center  = 3
} VMMouseButton;
```



## <a name="constants"></a><span data-ttu-id="530a3-109">Константы</span><span class="sxs-lookup"><span data-stu-id="530a3-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="530a3-110"><span id="vmMouseButton_Left"></span><span id="vmmousebutton_left"></span><span id="VMMOUSEBUTTON_LEFT"></span>**Вммаусебуттон \_ слева**</span><span class="sxs-lookup"><span data-stu-id="530a3-110"><span id="vmMouseButton_Left"></span><span id="vmmousebutton_left"></span><span id="VMMOUSEBUTTON_LEFT"></span>**vmMouseButton\_Left**</span></span>
</dt> <dd>

<span data-ttu-id="530a3-111">Левая кнопка мыши.</span><span class="sxs-lookup"><span data-stu-id="530a3-111">The left mouse button.</span></span>

</dd> <dt>

<span data-ttu-id="530a3-112"><span id="vmMouseButton_Right"></span><span id="vmmousebutton_right"></span><span id="VMMOUSEBUTTON_RIGHT"></span>**Вммаусебуттон \_ вправо**</span><span class="sxs-lookup"><span data-stu-id="530a3-112"><span id="vmMouseButton_Right"></span><span id="vmmousebutton_right"></span><span id="VMMOUSEBUTTON_RIGHT"></span>**vmMouseButton\_Right**</span></span>
</dt> <dd>

<span data-ttu-id="530a3-113">Правая кнопка мыши.</span><span class="sxs-lookup"><span data-stu-id="530a3-113">The right mouse button.</span></span>

</dd> <dt>

<span data-ttu-id="530a3-114"><span id="vmMouseButton_Center"></span><span id="vmmousebutton_center"></span><span id="VMMOUSEBUTTON_CENTER"></span>**Вммаусебуттон \_ Center**</span><span class="sxs-lookup"><span data-stu-id="530a3-114"><span id="vmMouseButton_Center"></span><span id="vmmousebutton_center"></span><span id="VMMOUSEBUTTON_CENTER"></span>**vmMouseButton\_Center**</span></span>
</dt> <dd>

<span data-ttu-id="530a3-115">Центральная кнопка мыши.</span><span class="sxs-lookup"><span data-stu-id="530a3-115">The center mouse button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="530a3-116">Требования</span><span class="sxs-lookup"><span data-stu-id="530a3-116">Requirements</span></span>



| <span data-ttu-id="530a3-117">Требование</span><span class="sxs-lookup"><span data-stu-id="530a3-117">Requirement</span></span> | <span data-ttu-id="530a3-118">Значение</span><span class="sxs-lookup"><span data-stu-id="530a3-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="530a3-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="530a3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="530a3-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="530a3-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="530a3-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="530a3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="530a3-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="530a3-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="530a3-123">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="530a3-123">End of client support</span></span><br/>    | <span data-ttu-id="530a3-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="530a3-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="530a3-125">Продукт</span><span class="sxs-lookup"><span data-stu-id="530a3-125">Product</span></span><br/>                  | <span data-ttu-id="530a3-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="530a3-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="530a3-127">Header</span><span class="sxs-lookup"><span data-stu-id="530a3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="530a3-128"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="530a3-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="530a3-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="530a3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="530a3-130">**ивммаусе**</span><span class="sxs-lookup"><span data-stu-id="530a3-130">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

