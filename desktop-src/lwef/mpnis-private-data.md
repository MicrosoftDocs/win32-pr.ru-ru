---
title: Структура MPNIS_PRIVATE_DATA (Мпклиент. h)
description: Частные уведомления NIS.
ms.assetid: 19B4928F-BC78-4DEA-A563-1516B6454465
keywords:
- MPNIS_PRIVATE_DATA структуры устаревшие функции среды Windows
- Функции PMPNIS_PRIVATE_DATA указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPNIS_PRIVATE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21340665a32b619c42d7909e8cd1b72ca6d09fb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801253"
---
# <a name="mpnis_private_data-structure"></a><span data-ttu-id="c4033-105">\_Структура закрытых \_ данных мпнис</span><span class="sxs-lookup"><span data-stu-id="c4033-105">MPNIS\_PRIVATE\_DATA structure</span></span>

<span data-ttu-id="c4033-106">Частные уведомления NIS.</span><span class="sxs-lookup"><span data-stu-id="c4033-106">Private NIS notifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4033-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4033-107">Syntax</span></span>


```C++
typedef struct tagMPNIS_PRIVATE_DATA {
  DWORD dwNotificationType;
  DWORD cbDataSize;
  BYTE  *pbData;
} MPNIS_PRIVATE_DATA, *PMPNIS_PRIVATE_DATA;
```



## <a name="members"></a><span data-ttu-id="c4033-108">Члены</span><span class="sxs-lookup"><span data-stu-id="c4033-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c4033-109">**двнотификатионтипе**</span><span class="sxs-lookup"><span data-stu-id="c4033-109">**dwNotificationType**</span></span>
</dt> <dd>

<span data-ttu-id="c4033-110">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c4033-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="c4033-111">Тип уведомления.</span><span class="sxs-lookup"><span data-stu-id="c4033-111">Type of notification.</span></span>

</dd> <dt>

<span data-ttu-id="c4033-112">**кбдатасизе**</span><span class="sxs-lookup"><span data-stu-id="c4033-112">**cbDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="c4033-113">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c4033-113">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="c4033-114">Размер зарезервированных данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="c4033-114">Size of reserved data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c4033-115">**pbData**</span><span class="sxs-lookup"><span data-stu-id="c4033-115">**pbData**</span></span>
</dt> <dd>

<span data-ttu-id="c4033-116">Тип: **Byte \***</span><span class="sxs-lookup"><span data-stu-id="c4033-116">Type: **BYTE\***</span></span>

</dd> <dd>

<span data-ttu-id="c4033-117">Указатель на зарезервированные данные.</span><span class="sxs-lookup"><span data-stu-id="c4033-117">Pointer to reserved data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c4033-118">Требования</span><span class="sxs-lookup"><span data-stu-id="c4033-118">Requirements</span></span>



| <span data-ttu-id="c4033-119">Требование</span><span class="sxs-lookup"><span data-stu-id="c4033-119">Requirement</span></span> | <span data-ttu-id="c4033-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c4033-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4033-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c4033-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c4033-122">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c4033-122">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c4033-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c4033-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c4033-124">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c4033-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c4033-125">Header</span><span class="sxs-lookup"><span data-stu-id="c4033-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4033-126"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4033-126"><dt>MpClient.h</dt></span></span> </dl> |



 

 





