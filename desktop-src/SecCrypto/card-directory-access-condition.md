---
description: Указывает разрешения на управление доступом для каталога на смарт-карте.
ms.assetid: 361d9fa0-286e-4d2c-8452-3b5f48e77779
title: Перечисление CARD_DIRECTORY_ACCESS_CONDITION (Cardmod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CARD_DIRECTORY_ACCESS_CONDITION
api_type:
- HeaderDef
api_location:
- Cardmod.h
ms.openlocfilehash: 9879fa73f6bb45b56f433d7bca7765ab5fc0daef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263007"
---
# <a name="card_directory_access_condition-enumeration"></a><span data-ttu-id="02135-103">\_ \_ Перечисление условий доступа к КАТАЛОГу карты \_</span><span class="sxs-lookup"><span data-stu-id="02135-103">CARD\_DIRECTORY\_ACCESS\_CONDITION enumeration</span></span>

<span data-ttu-id="02135-104">Перечисление **\_ \_ \_ условий доступа к каталогу карты** определяет разрешения на управление доступом для каталога на [*смарт-карте*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="02135-104">The **CARD\_DIRECTORY\_ACCESS\_CONDITION** enumeration specifies access control permissions for a directory on a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="02135-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02135-105">Syntax</span></span>


```C++
typedef enum  { 
  InvalidAc               = 0,
  UserCreateDeleteDirAc   = 1,
  AdminCreateDeleteDirAc  = 2
} CARD_DIRECTORY_ACCESS_CONDITION;
```



## <a name="constants"></a><span data-ttu-id="02135-106">Константы</span><span class="sxs-lookup"><span data-stu-id="02135-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="02135-107"><span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**инвалидак**</span><span class="sxs-lookup"><span data-stu-id="02135-107"><span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**</span></span>
</dt> <dd>

<span data-ttu-id="02135-108">Недопустимое значение.</span><span class="sxs-lookup"><span data-stu-id="02135-108">This value is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="02135-109"><span id="UserCreateDeleteDirAc"></span><span id="usercreatedeletedirac"></span><span id="USERCREATEDELETEDIRAC"></span>**усеркреатеделетедирак**</span><span class="sxs-lookup"><span data-stu-id="02135-109"><span id="UserCreateDeleteDirAc"></span><span id="usercreatedeletedirac"></span><span id="USERCREATEDELETEDIRAC"></span>**UserCreateDeleteDirAc**</span></span>
</dt> <dd>

<span data-ttu-id="02135-110">Конкретные пользователи могут читать, записывать и удалять каталог.</span><span class="sxs-lookup"><span data-stu-id="02135-110">Specific users can read, write, and delete the directory.</span></span>

</dd> <dt>

<span data-ttu-id="02135-111"><span id="AdminCreateDeleteDirAc"></span><span id="admincreatedeletedirac"></span><span id="ADMINCREATEDELETEDIRAC"></span>**админкреатеделетедирак**</span><span class="sxs-lookup"><span data-stu-id="02135-111"><span id="AdminCreateDeleteDirAc"></span><span id="admincreatedeletedirac"></span><span id="ADMINCREATEDELETEDIRAC"></span>**AdminCreateDeleteDirAc**</span></span>
</dt> <dd>

<span data-ttu-id="02135-112">Администраторы могут читать, записывать и удалять каталог.</span><span class="sxs-lookup"><span data-stu-id="02135-112">Administrators can read, write, and delete the directory.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="02135-113">Требования</span><span class="sxs-lookup"><span data-stu-id="02135-113">Requirements</span></span>



| <span data-ttu-id="02135-114">Требование</span><span class="sxs-lookup"><span data-stu-id="02135-114">Requirement</span></span> | <span data-ttu-id="02135-115">Значение</span><span class="sxs-lookup"><span data-stu-id="02135-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="02135-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="02135-116">Minimum supported client</span></span><br/> | <span data-ttu-id="02135-117">Windows XP, \[ только классические приложения Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="02135-117">Windows XP, Windows XP \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="02135-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="02135-118">Minimum supported server</span></span><br/> | <span data-ttu-id="02135-119">Windows Server 2003, \[ только для настольных приложений Windows server 2003\]</span><span class="sxs-lookup"><span data-stu-id="02135-119">Windows Server 2003, Windows Server 2003 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="02135-120">Header</span><span class="sxs-lookup"><span data-stu-id="02135-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="02135-121"><dt>Cardmod. h</dt></span><span class="sxs-lookup"><span data-stu-id="02135-121"><dt>Cardmod.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02135-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02135-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02135-123">Поставщик службы криптографии для смарт-карт (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="02135-123">Microsoft Base Smart Card Cryptographic Service Provider</span></span>](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider)
</dt> <dt>

[<span data-ttu-id="02135-124">**кардкреатедиректори**</span><span class="sxs-lookup"><span data-stu-id="02135-124">**CardCreateDirectory**</span></span>](/previous-versions/windows/desktop/secsmart/cardcreatedirectory)
</dt> <dt>

[<span data-ttu-id="02135-125">**кардделетедиректори**</span><span class="sxs-lookup"><span data-stu-id="02135-125">**CardDeleteDirectory**</span></span>](/previous-versions/windows/desktop/secsmart/carddeletedirectory)
</dt> </dl>

 

 
