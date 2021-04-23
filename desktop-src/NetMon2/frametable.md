---
description: Структура ФРАМЕТАБЛЕ, круглый буфер указателей кадров, передается обратно в приложения, подключенные к интерфейсу ИТРК НПП.
ms.assetid: 6e2d4f8d-46f2-4d53-bc28-7b0706663490
title: Структура ФРАМЕТАБЛЕ (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAMETABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 95d7930d7943b26ebba1bb194d083ca8beb9dcf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143804"
---
# <a name="frametable-structure"></a><span data-ttu-id="42218-103">Структура ФРАМЕТАБЛЕ</span><span class="sxs-lookup"><span data-stu-id="42218-103">FRAMETABLE structure</span></span>

<span data-ttu-id="42218-104">Структура **фраметабле** , круглый буфер указателей кадров, передается обратно в приложения, подключенные к интерфейсу **итрк** НПП.</span><span class="sxs-lookup"><span data-stu-id="42218-104">The **FRAMETABLE** structure, a circular buffer of frame pointers, is handed back to applications attached to the **ITRC** interface of the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="42218-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42218-105">Syntax</span></span>


```C++
typedef struct _FRAMETABLE {
  DWORD            FrameTableLength;
  DWORD            StartIndex;
  DWORD            EndIndex;
  DWORD            FrameCount;
  FRAME_DESCRIPTOR Frames[1];
} FRAMETABLE, *LPFRAMETABLE;
```



## <a name="members"></a><span data-ttu-id="42218-106">Члены</span><span class="sxs-lookup"><span data-stu-id="42218-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="42218-107">**фраметаблеленгс**</span><span class="sxs-lookup"><span data-stu-id="42218-107">**FrameTableLength**</span></span>
</dt> <dd>

<span data-ttu-id="42218-108">Общая длина таблицы.</span><span class="sxs-lookup"><span data-stu-id="42218-108">The total length of the table.</span></span>

</dd> <dt>

<span data-ttu-id="42218-109">**StartIndex**</span><span class="sxs-lookup"><span data-stu-id="42218-109">**StartIndex**</span></span>
</dt> <dd>

<span data-ttu-id="42218-110">Первый индекс в таблице.</span><span class="sxs-lookup"><span data-stu-id="42218-110">The first index within the table.</span></span>

</dd> <dt>

<span data-ttu-id="42218-111">**EndIndex**</span><span class="sxs-lookup"><span data-stu-id="42218-111">**EndIndex**</span></span>
</dt> <dd>

<span data-ttu-id="42218-112">Последний индекс в таблице.</span><span class="sxs-lookup"><span data-stu-id="42218-112">The last index within the table.</span></span>

</dd> <dt>

<span data-ttu-id="42218-113">**FrameCount**</span><span class="sxs-lookup"><span data-stu-id="42218-113">**FrameCount**</span></span>
</dt> <dd>

<span data-ttu-id="42218-114">Число кадров, описываемых этой таблицей.</span><span class="sxs-lookup"><span data-stu-id="42218-114">The number of frames described by this table.</span></span>

</dd> <dt>

<span data-ttu-id="42218-115">**Получен**</span><span class="sxs-lookup"><span data-stu-id="42218-115">**Frames**</span></span>
</dt> <dd>

<span data-ttu-id="42218-116">Фактический массив дескрипторов кадров.</span><span class="sxs-lookup"><span data-stu-id="42218-116">The actual array of frame descriptors.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="42218-117">Требования</span><span class="sxs-lookup"><span data-stu-id="42218-117">Requirements</span></span>



| <span data-ttu-id="42218-118">Требование</span><span class="sxs-lookup"><span data-stu-id="42218-118">Requirement</span></span> | <span data-ttu-id="42218-119">Значение</span><span class="sxs-lookup"><span data-stu-id="42218-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="42218-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="42218-120">Minimum supported client</span></span><br/> | <span data-ttu-id="42218-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="42218-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="42218-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="42218-122">Minimum supported server</span></span><br/> | <span data-ttu-id="42218-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="42218-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="42218-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="42218-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="42218-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="42218-125"><dt>Netmon.h</dt></span></span> </dl> |



 

 




