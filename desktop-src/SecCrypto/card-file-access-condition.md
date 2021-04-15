---
description: Указывает разрешения на управление доступом для файла на смарт-карте.
ms.assetid: 995d959f-30dc-4e5c-be2d-6b447499415a
title: Перечисление CARD_FILE_ACCESS_CONDITION (Cardmod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CARD_FILE_ACCESS_CONDITION
api_type:
- HeaderDef
api_location:
- Cardmod.h
ms.openlocfilehash: d3ef9fc81c9ab3bff5f3992c3aedeb3f923648ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662365"
---
# <a name="card_file_access_condition-enumeration"></a><span data-ttu-id="e8ff0-103">\_ \_ Перечисление условий доступа к файлу карты \_</span><span class="sxs-lookup"><span data-stu-id="e8ff0-103">CARD\_FILE\_ACCESS\_CONDITION enumeration</span></span>

<span data-ttu-id="e8ff0-104">Перечисление **\_ \_ \_ условий доступа к файлу карты** определяет разрешения на управление доступом для файла на [*смарт-карте*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e8ff0-104">The **CARD\_FILE\_ACCESS\_CONDITION** enumeration specifies access control permissions for a file on a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e8ff0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8ff0-105">Syntax</span></span>


```C++
typedef enum  { 
  InvalidAc                 = 0,
  EveryoneReadUserWriteAc   = 1,
  UserWriteExecuteAc        = 2,
  EveryoneReadAdminWriteAc  = 3,
  UnknownAc                 = 4
} CARD_FILE_ACCESS_CONDITION;
```



## <a name="constants"></a><span data-ttu-id="e8ff0-106">Константы</span><span class="sxs-lookup"><span data-stu-id="e8ff0-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e8ff0-107"><span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**инвалидак**</span><span class="sxs-lookup"><span data-stu-id="e8ff0-107"><span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**</span></span>
</dt> <dd>

<span data-ttu-id="e8ff0-108">Недопустимое значение.</span><span class="sxs-lookup"><span data-stu-id="e8ff0-108">This value is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="e8ff0-109"><span id="EveryoneReadUserWriteAc"></span><span id="everyonereaduserwriteac"></span><span id="EVERYONEREADUSERWRITEAC"></span>**еверйонереадусервритеак**</span><span class="sxs-lookup"><span data-stu-id="e8ff0-109"><span id="EveryoneReadUserWriteAc"></span><span id="everyonereaduserwriteac"></span><span id="EVERYONEREADUSERWRITEAC"></span>**EveryoneReadUserWriteAc**</span></span>
</dt> <dd>

<span data-ttu-id="e8ff0-110">Все могут читать файл.</span><span class="sxs-lookup"><span data-stu-id="e8ff0-110">Everyone can read the file.</span></span> <span data-ttu-id="e8ff0-111">Определенные пользователи могут записывать в файл.</span><span class="sxs-lookup"><span data-stu-id="e8ff0-111">Specific users can write to the file.</span></span>

</dd> <dt>

<span data-ttu-id="e8ff0-112"><span id="UserWriteExecuteAc"></span><span id="userwriteexecuteac"></span><span id="USERWRITEEXECUTEAC"></span>**усервритиксекутеак**</span><span class="sxs-lookup"><span data-stu-id="e8ff0-112"><span id="UserWriteExecuteAc"></span><span id="userwriteexecuteac"></span><span id="USERWRITEEXECUTEAC"></span>**UserWriteExecuteAc**</span></span>
</dt> <dd>

<span data-ttu-id="e8ff0-113">Только определенные пользователи могут выполнять чтение и запись в файл.</span><span class="sxs-lookup"><span data-stu-id="e8ff0-113">Only specific users can read or write to the file.</span></span>

</dd> <dt>

<span data-ttu-id="e8ff0-114"><span id="EveryoneReadAdminWriteAc"></span><span id="everyonereadadminwriteac"></span><span id="EVERYONEREADADMINWRITEAC"></span>**еверйонереададминвритеак**</span><span class="sxs-lookup"><span data-stu-id="e8ff0-114"><span id="EveryoneReadAdminWriteAc"></span><span id="everyonereadadminwriteac"></span><span id="EVERYONEREADADMINWRITEAC"></span>**EveryoneReadAdminWriteAc**</span></span>
</dt> <dd>

<span data-ttu-id="e8ff0-115">Все могут читать файл.</span><span class="sxs-lookup"><span data-stu-id="e8ff0-115">Everyone can read the file.</span></span> <span data-ttu-id="e8ff0-116">Администраторы могут записывать в файл.</span><span class="sxs-lookup"><span data-stu-id="e8ff0-116">Administrators can write to the file.</span></span>

</dd> <dt>

<span data-ttu-id="e8ff0-117"><span id="UnknownAc"></span><span id="unknownac"></span><span id="UNKNOWNAC"></span>**ункновнак**</span><span class="sxs-lookup"><span data-stu-id="e8ff0-117"><span id="UnknownAc"></span><span id="unknownac"></span><span id="UNKNOWNAC"></span>**UnknownAc**</span></span>
</dt> <dd>

<span data-ttu-id="e8ff0-118">Разрешения на доступ к файлу неизвестны.</span><span class="sxs-lookup"><span data-stu-id="e8ff0-118">Access permissions for the file are unknown.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e8ff0-119">Требования</span><span class="sxs-lookup"><span data-stu-id="e8ff0-119">Requirements</span></span>



| <span data-ttu-id="e8ff0-120">Требование</span><span class="sxs-lookup"><span data-stu-id="e8ff0-120">Requirement</span></span> | <span data-ttu-id="e8ff0-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e8ff0-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e8ff0-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8ff0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e8ff0-123">Windows XP, \[ только классические приложения Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e8ff0-123">Windows XP, Windows XP \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e8ff0-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8ff0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e8ff0-125">Windows Server 2003, \[ только для настольных приложений Windows server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e8ff0-125">Windows Server 2003, Windows Server 2003 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="e8ff0-126">Header</span><span class="sxs-lookup"><span data-stu-id="e8ff0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8ff0-127"><dt>Cardmod. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8ff0-127"><dt>Cardmod.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8ff0-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8ff0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8ff0-129">Поставщик службы криптографии для смарт-карт (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="e8ff0-129">Microsoft Base Smart Card Cryptographic Service Provider</span></span>](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider)
</dt> <dt>

[<span data-ttu-id="e8ff0-130">**\_ \_ сведения о файле карты**</span><span class="sxs-lookup"><span data-stu-id="e8ff0-130">**CARD\_FILE\_INFO**</span></span>](/previous-versions/windows/desktop/secsmart/card-file-info)
</dt> <dt>

[<span data-ttu-id="e8ff0-131">**кардкреатефиле**</span><span class="sxs-lookup"><span data-stu-id="e8ff0-131">**CardCreateFile**</span></span>](/previous-versions/windows/desktop/secsmart/cardcreatefile)
</dt> </dl>

 

 
