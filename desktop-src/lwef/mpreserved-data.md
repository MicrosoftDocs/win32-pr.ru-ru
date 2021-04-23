---
title: Структура MPRESERVED_DATA (Мпклиент. h)
description: Зарезервированные данные уведомления.
ms.assetid: C92206BD-6E56-4B7D-ABB1-DC1149AE141D
keywords:
- MPRESERVED_DATA структуры устаревшие функции среды Windows
- Функции PMPRESERVED_DATA указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPRESERVED_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b1e08184da71fe857cb412ef986c986a0c59baa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136478"
---
# <a name="mpreserved_data-structure"></a><span data-ttu-id="8a832-105">\_Структура данных мпресервед</span><span class="sxs-lookup"><span data-stu-id="8a832-105">MPRESERVED\_DATA structure</span></span>

<span data-ttu-id="8a832-106">Зарезервированные данные уведомления.</span><span class="sxs-lookup"><span data-stu-id="8a832-106">Reserved notification data.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a832-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a832-107">Syntax</span></span>


```C++
typedef struct tagMPRESERVED_DATA {
  DWORD cbReservedData;
  BYTE  *pbReservedData;
} MPRESERVED_DATA, *PMPRESERVED_DATA;
```



## <a name="members"></a><span data-ttu-id="8a832-108">Члены</span><span class="sxs-lookup"><span data-stu-id="8a832-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8a832-109">**кбресерведдата**</span><span class="sxs-lookup"><span data-stu-id="8a832-109">**cbReservedData**</span></span>
</dt> <dd>

<span data-ttu-id="8a832-110">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8a832-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="8a832-111">Размер зарезервированных данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="8a832-111">Size of reserved data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="8a832-112">**пбресерведдата**</span><span class="sxs-lookup"><span data-stu-id="8a832-112">**pbReservedData**</span></span>
</dt> <dd>

<span data-ttu-id="8a832-113">Тип: **Byte \***</span><span class="sxs-lookup"><span data-stu-id="8a832-113">Type: **BYTE\***</span></span>

</dd> <dd>

<span data-ttu-id="8a832-114">Указатель на зарезервированные данные.</span><span class="sxs-lookup"><span data-stu-id="8a832-114">Pointer to reserved data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8a832-115">Требования</span><span class="sxs-lookup"><span data-stu-id="8a832-115">Requirements</span></span>



| <span data-ttu-id="8a832-116">Требование</span><span class="sxs-lookup"><span data-stu-id="8a832-116">Requirement</span></span> | <span data-ttu-id="8a832-117">Значение</span><span class="sxs-lookup"><span data-stu-id="8a832-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8a832-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8a832-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8a832-119">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8a832-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8a832-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8a832-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8a832-121">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8a832-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8a832-122">Header</span><span class="sxs-lookup"><span data-stu-id="8a832-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a832-123"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a832-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





