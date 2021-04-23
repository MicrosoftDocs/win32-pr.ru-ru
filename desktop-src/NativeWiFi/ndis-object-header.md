---
description: Упаковывает сведения о типе объекта, версии и размере, необходимые для многих структур NDIS 6,0.
ms.assetid: 0dfb6022-1d8d-4bd9-bde3-2ee6d683f223
title: Структура NDIS_OBJECT_HEADER (Нтддндис. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDIS_OBJECT_HEADER
api_type:
- HeaderDef
api_location:
- ntddndis.h
ms.openlocfilehash: fe28a87eeb1457bace0b72a386bcb07667b24a64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683340"
---
# <a name="ndis_object_header-structure"></a><span data-ttu-id="ff240-103">\_ \_ Структура заголовка объекта NDIS</span><span class="sxs-lookup"><span data-stu-id="ff240-103">NDIS\_OBJECT\_HEADER structure</span></span>

<span data-ttu-id="ff240-104">Структура **\_ \_ заголовка объекта NDIS** упаковывает тип объекта, версию и сведения о размере, которые требуются во многих структурах NDIS 6,0.</span><span class="sxs-lookup"><span data-stu-id="ff240-104">The **NDIS\_OBJECT\_HEADER** structure packages the object type, version, and size information that is required in many NDIS 6.0 structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff240-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff240-105">Syntax</span></span>


```C++
typedef struct _NDIS_OBJECT_HEADER {
  UCHAR  Type;
  UCHAR  Revision;
  USHORT Size;
} NDIS_OBJECT_HEADER, *PNDIS_OBJECT_HEADER;
```



## <a name="members"></a><span data-ttu-id="ff240-106">Члены</span><span class="sxs-lookup"><span data-stu-id="ff240-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ff240-107">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ff240-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="ff240-108">Указывает тип объекта NDIS, который описывает структура.</span><span class="sxs-lookup"><span data-stu-id="ff240-108">Specifies the type of NDIS object that a structure describes.</span></span>

</dd> <dt>

<span data-ttu-id="ff240-109">**Редакции**</span><span class="sxs-lookup"><span data-stu-id="ff240-109">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="ff240-110">Указывает номер редакции этой структуры.</span><span class="sxs-lookup"><span data-stu-id="ff240-110">Specifies the revision number of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="ff240-111">**Размер**</span><span class="sxs-lookup"><span data-stu-id="ff240-111">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="ff240-112">Задает общий размер (в байтах) структуры NDIS, содержащей **\_ \_ заголовок объекта NDIS**.</span><span class="sxs-lookup"><span data-stu-id="ff240-112">Specifies the total size, in bytes, of the NDIS structure that contains the **NDIS\_OBJECT\_HEADER**.</span></span> <span data-ttu-id="ff240-113">Этот размер включает в себя размер элемента **\_ \_ заголовка объекта NDIS** и всех остальных элементов структуры.</span><span class="sxs-lookup"><span data-stu-id="ff240-113">This size includes the size of the **NDIS\_OBJECT\_HEADER** member and all other members of the structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ff240-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ff240-114">Requirements</span></span>



| <span data-ttu-id="ff240-115">Требование</span><span class="sxs-lookup"><span data-stu-id="ff240-115">Requirement</span></span> | <span data-ttu-id="ff240-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ff240-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff240-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ff240-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ff240-118">Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ff240-118">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ff240-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ff240-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ff240-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ff240-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ff240-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="ff240-121">Redistributable</span></span><br/>          | <span data-ttu-id="ff240-122">Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="ff240-122">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                        |
| <span data-ttu-id="ff240-123">Header</span><span class="sxs-lookup"><span data-stu-id="ff240-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff240-124"><dt>Нтддндис. h (включение Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ff240-124"><dt>Ntddndis.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff240-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ff240-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff240-126">**DOT11 \_ BSSID, \_ список**</span><span class="sxs-lookup"><span data-stu-id="ff240-126">**DOT11\_BSSID\_LIST**</span></span>](dot11-bssid-list.md)
</dt> </dl>

 

 




