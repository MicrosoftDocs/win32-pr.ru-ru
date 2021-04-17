---
description: Связывает имя группы и ее маркер.
ms.assetid: 76f3fe37-cf85-42ab-8f9e-3ab2c6053dcd
title: Структура GROUPINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GROUPINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 5152b0a621a34e49d6f1024a81b7e91aed94a06b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662178"
---
# <a name="groupinfo-structure"></a><span data-ttu-id="df966-103">Структура GROUPINFO</span><span class="sxs-lookup"><span data-stu-id="df966-103">GROUPINFO structure</span></span>

<span data-ttu-id="df966-104">Структура **GROUPINFO** связывает имя группы и ее маркер.</span><span class="sxs-lookup"><span data-stu-id="df966-104">The **GROUPINFO** structure associates a group name and its handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="df966-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df966-105">Syntax</span></span>


```C++
typedef struct {
  char   szGroupName[EXPERTGROUPNAMELENGTH+1];
  HGROUP hGroup;
} GROUPINFO, *PGROUPINFO;
```



## <a name="members"></a><span data-ttu-id="df966-106">Члены</span><span class="sxs-lookup"><span data-stu-id="df966-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="df966-107">**сзграупнаме**</span><span class="sxs-lookup"><span data-stu-id="df966-107">**szGroupName**</span></span>
</dt> <dd>

<span data-ttu-id="df966-108">Увеличенное значение массива в структуре **GROUPNAME** .</span><span class="sxs-lookup"><span data-stu-id="df966-108">Incremented value of an array in the **GROUPNAME** structure.</span></span>

</dd> <dt>

<span data-ttu-id="df966-109">**hGroup**</span><span class="sxs-lookup"><span data-stu-id="df966-109">**hGroup**</span></span>
</dt> <dd>

<span data-ttu-id="df966-110">Обработчик для группы.</span><span class="sxs-lookup"><span data-stu-id="df966-110">Handle to a group.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="df966-111">Требования</span><span class="sxs-lookup"><span data-stu-id="df966-111">Requirements</span></span>



| <span data-ttu-id="df966-112">Требование</span><span class="sxs-lookup"><span data-stu-id="df966-112">Requirement</span></span> | <span data-ttu-id="df966-113">Значение</span><span class="sxs-lookup"><span data-stu-id="df966-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="df966-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="df966-114">Minimum supported client</span></span><br/> | <span data-ttu-id="df966-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="df966-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="df966-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="df966-116">Minimum supported server</span></span><br/> | <span data-ttu-id="df966-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="df966-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="df966-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="df966-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="df966-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="df966-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




