---
description: Содержит код проверки подлинности сообщения (MAC).
ms.assetid: be5515fd-1936-46b8-9fc8-8d1f87048c38
title: Структура D3D_OMAC (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3D_OMAC
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 21c710b21c31147f7208ddd1637426aeafb60234
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719276"
---
# <a name="d3d_omac-structure"></a><span data-ttu-id="bc91a-103">\_Структура D3D ОМАК</span><span class="sxs-lookup"><span data-stu-id="bc91a-103">D3D\_OMAC structure</span></span>

<span data-ttu-id="bc91a-104">Содержит код проверки подлинности сообщения (MAC).</span><span class="sxs-lookup"><span data-stu-id="bc91a-104">Contains a Message Authentication Code (MAC).</span></span>

## <a name="syntax"></a><span data-ttu-id="bc91a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc91a-105">Syntax</span></span>


```C++
typedef struct _D3D_OMAC {
  BYTE Omac[D3D_OMAC_SIZE];
} D3D_OMAC;
```



## <a name="members"></a><span data-ttu-id="bc91a-106">Члены</span><span class="sxs-lookup"><span data-stu-id="bc91a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bc91a-107">**омак**</span><span class="sxs-lookup"><span data-stu-id="bc91a-107">**Omac**</span></span>
</dt> <dd>

<span data-ttu-id="bc91a-108">Массив байтов, содержащий криптографическое значение MAC сообщения.</span><span class="sxs-lookup"><span data-stu-id="bc91a-108">A byte array that contains the cryptographic MAC value of the message.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bc91a-109">Требования</span><span class="sxs-lookup"><span data-stu-id="bc91a-109">Requirements</span></span>



| <span data-ttu-id="bc91a-110">Требование</span><span class="sxs-lookup"><span data-stu-id="bc91a-110">Requirement</span></span> | <span data-ttu-id="bc91a-111">Значение</span><span class="sxs-lookup"><span data-stu-id="bc91a-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc91a-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bc91a-112">Minimum supported client</span></span><br/> | <span data-ttu-id="bc91a-113">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="bc91a-113">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bc91a-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bc91a-114">Minimum supported server</span></span><br/> | <span data-ttu-id="bc91a-115">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="bc91a-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bc91a-116">Header</span><span class="sxs-lookup"><span data-stu-id="bc91a-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc91a-117"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc91a-117"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc91a-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc91a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc91a-119">Видеоструктуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="bc91a-119">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> </dl>

 

 




