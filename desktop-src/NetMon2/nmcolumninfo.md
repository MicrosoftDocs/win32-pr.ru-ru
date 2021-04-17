---
description: Структура НМКОЛУМНИНФО определяет один столбец в верхней области Просмотр событий.
ms.assetid: 21e0a129-464b-45b3-9c6b-6594e62fbce9
title: Структура НМКОЛУМНИНФО (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EVENTCOLUMNINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 2597b486590871f0af28736717d4c2f332aae342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684540"
---
# <a name="nmcolumninfo-structure"></a><span data-ttu-id="8a0b2-103">Структура НМКОЛУМНИНФО</span><span class="sxs-lookup"><span data-stu-id="8a0b2-103">NMCOLUMNINFO structure</span></span>

<span data-ttu-id="8a0b2-104">Структура **нмколумнинфо** определяет один столбец в верхней области Просмотр событий.</span><span class="sxs-lookup"><span data-stu-id="8a0b2-104">The **NMCOLUMNINFO** structure defines one column in the top pane of the Event Viewer.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a0b2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a0b2-105">Syntax</span></span>


```C++
typedef struct {
  LPSTR           szColumnName;
  NMCOLUMNVARIANT VariantData;
} EVENTCOLUMNINFO;
```



## <a name="members"></a><span data-ttu-id="8a0b2-106">Члены</span><span class="sxs-lookup"><span data-stu-id="8a0b2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8a0b2-107">**сзколумннаме**</span><span class="sxs-lookup"><span data-stu-id="8a0b2-107">**szColumnName**</span></span>
</dt> <dd>

<span data-ttu-id="8a0b2-108">Отображаемое имя определенного столбца.</span><span class="sxs-lookup"><span data-stu-id="8a0b2-108">Displayable name of a specific column.</span></span> <span data-ttu-id="8a0b2-109">Если имя слишком длинное, оно не будет полностью видимо в конфигурации Просмотр событий по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8a0b2-109">If the name is too long, it will not be completely visible in the default Event Viewer configuration.</span></span>

</dd> <dt>

<span data-ttu-id="8a0b2-110">**вариантдата**</span><span class="sxs-lookup"><span data-stu-id="8a0b2-110">**VariantData**</span></span>
</dt> <dd>

<span data-ttu-id="8a0b2-111">Данные, вставленные в столбец.</span><span class="sxs-lookup"><span data-stu-id="8a0b2-111">The data inserted into the column.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8a0b2-112">Требования</span><span class="sxs-lookup"><span data-stu-id="8a0b2-112">Requirements</span></span>



| <span data-ttu-id="8a0b2-113">Требование</span><span class="sxs-lookup"><span data-stu-id="8a0b2-113">Requirement</span></span> | <span data-ttu-id="8a0b2-114">Значение</span><span class="sxs-lookup"><span data-stu-id="8a0b2-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8a0b2-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8a0b2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8a0b2-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8a0b2-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8a0b2-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8a0b2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8a0b2-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8a0b2-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8a0b2-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8a0b2-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a0b2-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a0b2-120"><dt>Netmon.h</dt></span></span> </dl> |



 

 




