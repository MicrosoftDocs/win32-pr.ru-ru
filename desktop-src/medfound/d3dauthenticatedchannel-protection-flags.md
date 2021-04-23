---
description: Задает уровень защиты содержимого видео.
ms.assetid: 681c6ad9-cf55-47e4-bbb9-e7fdc499a709
title: Структура D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2d3111d01f178be3128dcb79f65d2155195c2e4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692062"
---
# <a name="d3dauthenticatedchannel_protection_flags-structure"></a><span data-ttu-id="3dab4-103">\_ \_ Структура флагов защиты D3DAUTHENTICATEDCHANNEL</span><span class="sxs-lookup"><span data-stu-id="3dab4-103">D3DAUTHENTICATEDCHANNEL\_PROTECTION\_FLAGS structure</span></span>

<span data-ttu-id="3dab4-104">Задает уровень защиты содержимого видео.</span><span class="sxs-lookup"><span data-stu-id="3dab4-104">Specifies the protection level for video content.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dab4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3dab4-105">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS {
  union {
    struct {
      UINT ProtectionEnabled  :1;
      UINT OverlayOrFullscreenRequired  :1;
      UINT Reserved  :30;
    };
    UINT   Value;
  };
} D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS;
```



## <a name="members"></a><span data-ttu-id="3dab4-106">Члены</span><span class="sxs-lookup"><span data-stu-id="3dab4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3dab4-107">**протектионенаблед**</span><span class="sxs-lookup"><span data-stu-id="3dab4-107">**ProtectionEnabled**</span></span>
</dt> <dd>

<span data-ttu-id="3dab4-108">Если значение равно 1, защита содержимого видео включена.</span><span class="sxs-lookup"><span data-stu-id="3dab4-108">If 1, video content protection is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="3dab4-109">**оверлайорфуллскринрекуиред**</span><span class="sxs-lookup"><span data-stu-id="3dab4-109">**OverlayOrFullscreenRequired**</span></span>
</dt> <dd>

<span data-ttu-id="3dab4-110">Если задано значение 1, приложение должно отображать видео с помощью наложения оборудования или полноэкранного режима монопольного доступа.</span><span class="sxs-lookup"><span data-stu-id="3dab4-110">If 1, the application requires video to be displayed using either a hardware overlay or full-screen exclusive mode.</span></span>

</dd> <dt>

<span data-ttu-id="3dab4-111">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="3dab4-111">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="3dab4-112">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="3dab4-112">Reserved.</span></span> <span data-ttu-id="3dab4-113">Задайте для всех битов значение 0.</span><span class="sxs-lookup"><span data-stu-id="3dab4-113">Set all bits to zero.</span></span>

</dd> <dt>

<span data-ttu-id="3dab4-114">**Значение**</span><span class="sxs-lookup"><span data-stu-id="3dab4-114">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="3dab4-115">Используйте этот элемент для доступа ко всем битам в объединении.</span><span class="sxs-lookup"><span data-stu-id="3dab4-115">Use this member to access all of the bits in the union.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3dab4-116">Требования</span><span class="sxs-lookup"><span data-stu-id="3dab4-116">Requirements</span></span>



| <span data-ttu-id="3dab4-117">Требование</span><span class="sxs-lookup"><span data-stu-id="3dab4-117">Requirement</span></span> | <span data-ttu-id="3dab4-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3dab4-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3dab4-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3dab4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3dab4-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3dab4-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3dab4-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3dab4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3dab4-122">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3dab4-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3dab4-123">Header</span><span class="sxs-lookup"><span data-stu-id="3dab4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3dab4-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="3dab4-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dab4-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3dab4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dab4-126">Видеоструктуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="3dab4-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> </dl>

 

 




