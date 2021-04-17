---
description: Определяет структуру файла заголовка сетевой монитор.
ms.assetid: 944980c9-ebaa-4042-a112-d32b7a28ba21
title: Структура CAPTUREFILE_HEADER_VALUES (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPTUREFILE_HEADER_VALUES
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 2597b3f83a65dafd2da0198aade5243acc1184fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650774"
---
# <a name="capturefile_header_values-structure"></a><span data-ttu-id="7dce8-103">\_ \_ Структура значений заголовка каптурефиле</span><span class="sxs-lookup"><span data-stu-id="7dce8-103">CAPTUREFILE\_HEADER\_VALUES structure</span></span>

<span data-ttu-id="7dce8-104">Структура **\_ \_ значений заголовка каптурефиле** определяет структуру файла заголовка сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="7dce8-104">The **CAPTUREFILE\_HEADER\_VALUES** structure defines the Network Monitor header file structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dce8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7dce8-105">Syntax</span></span>


```C++
typedef struct _CAPTUREFILE_HEADER_VALUES {
  DWORD      Signature;
  BYTE       BCDVerMinor;
  BYTE       BCDVerMajor;
  WORD       MacType;
  SYSTEMTIME TimeStamp;
  DWORD      FrameTableOffset;
  DWORD      FrameTableLength;
  DWORD      UserDataOffset;
  DWORD      UserDataLength;
  DWORD      CommentDataOffset;
  DWORD      CommentDataLength;
  DWORD      StatisticsOffset;
  DWORD      StatisticsLength;
  DWORD      NetworkInfoOffset;
  DWORD      NetworkInfoLength;
  DWORD      ConversationStatsOffset;
  DWORD      ConversationStatsLength;
} CAPTUREFILE_HEADER_VALUES, *LPCAPTUREFILE_HEADER_VALUES;
```



## <a name="members"></a><span data-ttu-id="7dce8-106">Члены</span><span class="sxs-lookup"><span data-stu-id="7dce8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7dce8-107">**Образец**</span><span class="sxs-lookup"><span data-stu-id="7dce8-107">**Signature**</span></span>
</dt> <dd>

<span data-ttu-id="7dce8-108">Уникальный идентификатор: ' ГМБУ.</span><span class="sxs-lookup"><span data-stu-id="7dce8-108">Unique identifier: 'GMBU.</span></span>

</dd> <dt>

<span data-ttu-id="7dce8-109">**бкдверминор**</span><span class="sxs-lookup"><span data-stu-id="7dce8-109">**BCDVerMinor**</span></span>
</dt> <dd>

<span data-ttu-id="7dce8-110">Двоичное, закодированное десятичное число (минор).</span><span class="sxs-lookup"><span data-stu-id="7dce8-110">Binary, coded decimal (minor).</span></span> <span data-ttu-id="7dce8-111">Значение этого элемента должно быть равно нулю (0).</span><span class="sxs-lookup"><span data-stu-id="7dce8-111">The value of this member should be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="7dce8-112">**бкдвермажор**</span><span class="sxs-lookup"><span data-stu-id="7dce8-112">**BCDVerMajor**</span></span>
</dt> <dd>

<span data-ttu-id="7dce8-113">Двоично-кодированное десятичное число (основной).</span><span class="sxs-lookup"><span data-stu-id="7dce8-113">Binary coded decimal (major).</span></span> <span data-ttu-id="7dce8-114">Это значение должно быть равно 2.</span><span class="sxs-lookup"><span data-stu-id="7dce8-114">This value should be 2.</span></span>

</dd> <dt>

<span data-ttu-id="7dce8-115">**MacType**</span><span class="sxs-lookup"><span data-stu-id="7dce8-115">**MacType**</span></span>
</dt> <dd>

<span data-ttu-id="7dce8-116">Тип топологии.</span><span class="sxs-lookup"><span data-stu-id="7dce8-116">Topology type.</span></span>

</dd> <dt>

<span data-ttu-id="7dce8-117">**TimeStamp**</span><span class="sxs-lookup"><span data-stu-id="7dce8-117">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="7dce8-118">Время записи.</span><span class="sxs-lookup"><span data-stu-id="7dce8-118">Time of capture.</span></span>

</dd> <dt>

<span data-ttu-id="7dce8-119">**фраметаблеоффсет**</span><span class="sxs-lookup"><span data-stu-id="7dce8-119">**FrameTableOffset**</span></span>
</dt> <dd>

<span data-ttu-id="7dce8-120">Таблица индексов кадров.</span><span class="sxs-lookup"><span data-stu-id="7dce8-120">Frame index table.</span></span>

</dd> <dt>

<span data-ttu-id="7dce8-121">**фраметаблеленгс**</span><span class="sxs-lookup"><span data-stu-id="7dce8-121">**FrameTableLength**</span></span>
</dt> <dd>

<span data-ttu-id="7dce8-122">Размер таблицы индексов кадров.</span><span class="sxs-lookup"><span data-stu-id="7dce8-122">Frame index table size.</span></span>

</dd> <dt>

<span data-ttu-id="7dce8-123">**усердатаоффсет**</span><span class="sxs-lookup"><span data-stu-id="7dce8-123">**UserDataOffset**</span></span>
</dt> <dd>

<span data-ttu-id="7dce8-124">Смещение данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="7dce8-124">User data offset.</span></span>

</dd> <dt>

<span data-ttu-id="7dce8-125">**усердаталенгс**</span><span class="sxs-lookup"><span data-stu-id="7dce8-125">**UserDataLength**</span></span>
</dt> <dd>

<span data-ttu-id="7dce8-126">Длина данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="7dce8-126">User data length.</span></span>

</dd> <dt>

<span data-ttu-id="7dce8-127">**комментдатаоффсет**</span><span class="sxs-lookup"><span data-stu-id="7dce8-127">**CommentDataOffset**</span></span>
</dt> <dd>

<span data-ttu-id="7dce8-128">Смещение данных комментария.</span><span class="sxs-lookup"><span data-stu-id="7dce8-128">Comment data offset.</span></span>

</dd> <dt>

<span data-ttu-id="7dce8-129">**комментдаталенгс**</span><span class="sxs-lookup"><span data-stu-id="7dce8-129">**CommentDataLength**</span></span>
</dt> <dd>

<span data-ttu-id="7dce8-130">Длина данных комментария.</span><span class="sxs-lookup"><span data-stu-id="7dce8-130">Length of comment data.</span></span>

</dd> <dt>

<span data-ttu-id="7dce8-131">**статистиксоффсет**</span><span class="sxs-lookup"><span data-stu-id="7dce8-131">**StatisticsOffset**</span></span>
</dt> <dd>

<span data-ttu-id="7dce8-132">Смещение структуры **статистики** .</span><span class="sxs-lookup"><span data-stu-id="7dce8-132">Offset to the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="7dce8-133">**статистиксленгс**</span><span class="sxs-lookup"><span data-stu-id="7dce8-133">**StatisticsLength**</span></span>
</dt> <dd>

<span data-ttu-id="7dce8-134">Длина структуры **статистики** .</span><span class="sxs-lookup"><span data-stu-id="7dce8-134">Length of the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="7dce8-135">**нетворкинфуффсет**</span><span class="sxs-lookup"><span data-stu-id="7dce8-135">**NetworkInfoOffset**</span></span>
</dt> <dd>

<span data-ttu-id="7dce8-136">Смещение к структуре **нетворкинфо** .</span><span class="sxs-lookup"><span data-stu-id="7dce8-136">Offset to the **NETWORKINFO** structure.</span></span>

</dd> <dt>

<span data-ttu-id="7dce8-137">**нетворкинфоленгс**</span><span class="sxs-lookup"><span data-stu-id="7dce8-137">**NetworkInfoLength**</span></span>
</dt> <dd>

<span data-ttu-id="7dce8-138">Длина структуры **нетворкинфо** .</span><span class="sxs-lookup"><span data-stu-id="7dce8-138">Length of the **NETWORKINFO** structure.</span></span>

</dd> <dt>

<span data-ttu-id="7dce8-139">**конверсатионстатсоффсет**</span><span class="sxs-lookup"><span data-stu-id="7dce8-139">**ConversationStatsOffset**</span></span>
</dt> <dd>

<span data-ttu-id="7dce8-140">Этот элемент не используется.</span><span class="sxs-lookup"><span data-stu-id="7dce8-140">This member is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7dce8-141">**конверсатионстатсленгс**</span><span class="sxs-lookup"><span data-stu-id="7dce8-141">**ConversationStatsLength**</span></span>
</dt> <dd>

<span data-ttu-id="7dce8-142">Этот элемент не используется.</span><span class="sxs-lookup"><span data-stu-id="7dce8-142">This member is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7dce8-143">Требования</span><span class="sxs-lookup"><span data-stu-id="7dce8-143">Requirements</span></span>



| <span data-ttu-id="7dce8-144">Требование</span><span class="sxs-lookup"><span data-stu-id="7dce8-144">Requirement</span></span> | <span data-ttu-id="7dce8-145">Значение</span><span class="sxs-lookup"><span data-stu-id="7dce8-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7dce8-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7dce8-146">Minimum supported client</span></span><br/> | <span data-ttu-id="7dce8-147">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7dce8-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7dce8-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7dce8-148">Minimum supported server</span></span><br/> | <span data-ttu-id="7dce8-149">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7dce8-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7dce8-150">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7dce8-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dce8-151"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7dce8-151"><dt>Netmon.h</dt></span></span> </dl> |



 

 




