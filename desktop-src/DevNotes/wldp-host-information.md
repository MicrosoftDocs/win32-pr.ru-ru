---
description: Структура, идентифицирующая узел и исходный файл для оценки.
ms.assetid: 547EF59E-7DE5-45E4-948F-109547FAAEE7
title: Структура WLDP_HOST_INFORMATION (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_HOST_INFORMATION
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: ad20be7fa5887e42c09248d04e14f5ff8cffcd54
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072357"
---
# <a name="wldp_host_information-structure"></a><span data-ttu-id="ee9e1-103">\_ \_ Структура сведений о узле WLDP</span><span class="sxs-lookup"><span data-stu-id="ee9e1-103">WLDP\_HOST\_INFORMATION structure</span></span>

<span data-ttu-id="ee9e1-104">Структура, идентифицирующая узел и исходный файл для оценки.</span><span class="sxs-lookup"><span data-stu-id="ee9e1-104">A structure identifying the host and source file to be evaluated.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee9e1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ee9e1-105">Syntax</span></span>


```C++
typedef struct _WLDP_HOST_INFORMATION {
  DWORD        dwRevision;
  WLDP_HOST_ID dwHostId;
  PCWSTR       szSource;
  HANDLE       hSource;
} WLDP_HOST_INFORMATION, *PWLDP_HOST_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="ee9e1-106">Члены</span><span class="sxs-lookup"><span data-stu-id="ee9e1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ee9e1-107">**двревисион**</span><span class="sxs-lookup"><span data-stu-id="ee9e1-107">**dwRevision**</span></span>
</dt> <dd>

<span data-ttu-id="ee9e1-108">Должна быть **WLDPа \_ \_ \_ версия сведений об узле**.</span><span class="sxs-lookup"><span data-stu-id="ee9e1-108">Must be **WLDP\_HOST\_INFORMATION\_REVISION**.</span></span>

</dd> <dt>

<span data-ttu-id="ee9e1-109">**двхостид**</span><span class="sxs-lookup"><span data-stu-id="ee9e1-109">**dwHostId**</span></span>
</dt> <dd>

<span data-ttu-id="ee9e1-110">Значение перечисления из [**\_ \_ идентификатора узла WLDP**](wldp-host-id.md) , описывающее идентификатор узла.</span><span class="sxs-lookup"><span data-stu-id="ee9e1-110">Enumeration value from [**WLDP\_HOST\_ID**](wldp-host-id.md) that describes the host ID.</span></span>

</dd> <dt>

<span data-ttu-id="ee9e1-111">**сзсаурце**</span><span class="sxs-lookup"><span data-stu-id="ee9e1-111">**szSource**</span></span>
</dt> <dd>

<span data-ttu-id="ee9e1-112">Полный путь и имя скрипта с расширением.</span><span class="sxs-lookup"><span data-stu-id="ee9e1-112">Full path and script name with the extension.</span></span> <span data-ttu-id="ee9e1-113">Значение NULL **для \_ \_ \_ глобального идентификатора узла WLDP** или выполнение скрипта вручную.</span><span class="sxs-lookup"><span data-stu-id="ee9e1-113">NULL for **WLDP\_HOST\_ID\_GLOBAL**, or manual script execution.</span></span>

</dd> <dt>

<span data-ttu-id="ee9e1-114">**хсаурце**</span><span class="sxs-lookup"><span data-stu-id="ee9e1-114">**hSource**</span></span>
</dt> <dd>

<span data-ttu-id="ee9e1-115">В дополнение к имени вызывающий объект может указать обработчик для файла, используемого для проверки.</span><span class="sxs-lookup"><span data-stu-id="ee9e1-115">In addition to the name, the caller can specify a handle to the file used for validation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ee9e1-116">Требования</span><span class="sxs-lookup"><span data-stu-id="ee9e1-116">Requirements</span></span>



| <span data-ttu-id="ee9e1-117">Требование</span><span class="sxs-lookup"><span data-stu-id="ee9e1-117">Requirement</span></span> | <span data-ttu-id="ee9e1-118">Значение</span><span class="sxs-lookup"><span data-stu-id="ee9e1-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ee9e1-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ee9e1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ee9e1-120">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ee9e1-120">Windows 8 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ee9e1-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ee9e1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ee9e1-122">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ee9e1-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ee9e1-123">Header</span><span class="sxs-lookup"><span data-stu-id="ee9e1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee9e1-124"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee9e1-124"><dt>Wldp.h</dt></span></span> </dl> |



 

 




