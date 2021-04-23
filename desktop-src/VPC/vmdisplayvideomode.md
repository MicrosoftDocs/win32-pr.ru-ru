---
title: Перечисление Вмдисплайвидеомоде (Впккоминтерфацес. h)
description: Задает режим видеоизображения.
ms.assetid: 9ffd1bb5-115d-4554-92c6-5dcf86f904a5
keywords:
- Перечисление Вмдисплайвидеомоде Virtual PC
topic_type:
- apiref
api_name:
- VMDisplayVideoMode
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b159a8c251c83643ae9897842b313ea9be567e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490437"
---
# <a name="vmdisplayvideomode-enumeration"></a><span data-ttu-id="0bedf-104">Перечисление Вмдисплайвидеомоде</span><span class="sxs-lookup"><span data-stu-id="0bedf-104">VMDisplayVideoMode enumeration</span></span>

<span data-ttu-id="0bedf-105">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0bedf-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0bedf-106">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0bedf-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0bedf-107">Задает режим видеоизображения.</span><span class="sxs-lookup"><span data-stu-id="0bedf-107">Specifies the display video mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bedf-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0bedf-108">Syntax</span></span>


```C++
typedef enum  { 
  vmVideoMode_TextMode  = 0,
  vmVideoMode_CGAMode   = 1,
  vmVideoMode_VGAMode   = 2,
  vmVideoMode_SVGAMode  = 3
} VMDisplayVideoMode;
```



## <a name="constants"></a><span data-ttu-id="0bedf-109">Константы</span><span class="sxs-lookup"><span data-stu-id="0bedf-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0bedf-110"><span id="vmVideoMode_TextMode"></span><span id="vmvideomode_textmode"></span><span id="VMVIDEOMODE_TEXTMODE"></span>**Вмвидеомоденый \_ TextMode**</span><span class="sxs-lookup"><span data-stu-id="0bedf-110"><span id="vmVideoMode_TextMode"></span><span id="vmvideomode_textmode"></span><span id="VMVIDEOMODE_TEXTMODE"></span>**vmVideoMode\_TextMode**</span></span>
</dt> <dd>

<span data-ttu-id="0bedf-111">Текстовый режим.</span><span class="sxs-lookup"><span data-stu-id="0bedf-111">Text mode.</span></span>

</dd> <dt>

<span data-ttu-id="0bedf-112"><span id="vmVideoMode_CGAMode"></span><span id="vmvideomode_cgamode"></span><span id="VMVIDEOMODE_CGAMODE"></span>**Вмвидеомоде \_ кгамоде**</span><span class="sxs-lookup"><span data-stu-id="0bedf-112"><span id="vmVideoMode_CGAMode"></span><span id="vmvideomode_cgamode"></span><span id="VMVIDEOMODE_CGAMODE"></span>**vmVideoMode\_CGAMode**</span></span>
</dt> <dd>

<span data-ttu-id="0bedf-113">Режим КГА.</span><span class="sxs-lookup"><span data-stu-id="0bedf-113">CGA mode.</span></span>

</dd> <dt>

<span data-ttu-id="0bedf-114"><span id="vmVideoMode_VGAMode"></span><span id="vmvideomode_vgamode"></span><span id="VMVIDEOMODE_VGAMODE"></span>**Вмвидеомоде \_ вгамоде**</span><span class="sxs-lookup"><span data-stu-id="0bedf-114"><span id="vmVideoMode_VGAMode"></span><span id="vmvideomode_vgamode"></span><span id="VMVIDEOMODE_VGAMODE"></span>**vmVideoMode\_VGAMode**</span></span>
</dt> <dd>

<span data-ttu-id="0bedf-115">Режим VGA.</span><span class="sxs-lookup"><span data-stu-id="0bedf-115">VGA mode.</span></span>

</dd> <dt>

<span data-ttu-id="0bedf-116"><span id="vmVideoMode_SVGAMode"></span><span id="vmvideomode_svgamode"></span><span id="VMVIDEOMODE_SVGAMODE"></span>**Вмвидеомоде \_ свгамоде**</span><span class="sxs-lookup"><span data-stu-id="0bedf-116"><span id="vmVideoMode_SVGAMode"></span><span id="vmvideomode_svgamode"></span><span id="VMVIDEOMODE_SVGAMODE"></span>**vmVideoMode\_SVGAMode**</span></span>
</dt> <dd>

<span data-ttu-id="0bedf-117">Режим SVGA.</span><span class="sxs-lookup"><span data-stu-id="0bedf-117">SVGA mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0bedf-118">Требования</span><span class="sxs-lookup"><span data-stu-id="0bedf-118">Requirements</span></span>



| <span data-ttu-id="0bedf-119">Требование</span><span class="sxs-lookup"><span data-stu-id="0bedf-119">Requirement</span></span> | <span data-ttu-id="0bedf-120">Значение</span><span class="sxs-lookup"><span data-stu-id="0bedf-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bedf-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0bedf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0bedf-122">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0bedf-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0bedf-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0bedf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0bedf-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0bedf-124">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0bedf-125">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="0bedf-125">End of client support</span></span><br/>    | <span data-ttu-id="0bedf-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0bedf-126">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0bedf-127">Продукт</span><span class="sxs-lookup"><span data-stu-id="0bedf-127">Product</span></span><br/>                  | <span data-ttu-id="0bedf-128">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0bedf-128">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0bedf-129">Header</span><span class="sxs-lookup"><span data-stu-id="0bedf-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bedf-130"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bedf-130"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bedf-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0bedf-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bedf-132">**Ивмдисплай:: Видеомоде**</span><span class="sxs-lookup"><span data-stu-id="0bedf-132">**IVMDisplay::VideoMode**</span></span>](ivmdisplay-videomode.md)
</dt> </dl>

 

