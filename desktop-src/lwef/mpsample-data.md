---
title: Структура MPSAMPLE_DATA (Мпклиент. h)
description: Данные уведомления передаются в функцию обратного вызова отправки образца.
ms.assetid: 58F348C6-411D-4545-9D4D-A80095FD139B
keywords:
- MPSAMPLE_DATA структуры устаревшие функции среды Windows
- Функции PMPSAMPLE_DATA указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPSAMPLE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24a894638465c0362069b8fdcbacddf98bfdd2c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137643"
---
# <a name="mpsample_data-structure"></a><span data-ttu-id="73c21-105">\_Структура данных мпсампле</span><span class="sxs-lookup"><span data-stu-id="73c21-105">MPSAMPLE\_DATA structure</span></span>

<span data-ttu-id="73c21-106">Данные уведомления передаются в функцию обратного вызова отправки образца.</span><span class="sxs-lookup"><span data-stu-id="73c21-106">Notification data passed to the sample submission callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="73c21-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73c21-107">Syntax</span></span>


```C++
typedef struct tagMPSAMPLE_DATA {
  DWORD dwSampleIndex;
} MPSAMPLE_DATA, *PMPSAMPLE_DATA;
```



## <a name="members"></a><span data-ttu-id="73c21-108">Члены</span><span class="sxs-lookup"><span data-stu-id="73c21-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="73c21-109">**двсамплеиндекс**</span><span class="sxs-lookup"><span data-stu-id="73c21-109">**dwSampleIndex**</span></span>
</dt> <dd>

<span data-ttu-id="73c21-110">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="73c21-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="73c21-111">Индекс образца элемента, для которого сообщается состояние отправки.</span><span class="sxs-lookup"><span data-stu-id="73c21-111">Index of the sample item for which the submission status is reported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="73c21-112">Требования</span><span class="sxs-lookup"><span data-stu-id="73c21-112">Requirements</span></span>



| <span data-ttu-id="73c21-113">Требование</span><span class="sxs-lookup"><span data-stu-id="73c21-113">Requirement</span></span> | <span data-ttu-id="73c21-114">Значение</span><span class="sxs-lookup"><span data-stu-id="73c21-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="73c21-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="73c21-115">Minimum supported client</span></span><br/> | <span data-ttu-id="73c21-116">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="73c21-116">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="73c21-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="73c21-117">Minimum supported server</span></span><br/> | <span data-ttu-id="73c21-118">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="73c21-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="73c21-119">Header</span><span class="sxs-lookup"><span data-stu-id="73c21-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="73c21-120"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="73c21-120"><dt>MpClient.h</dt></span></span> </dl> |



 

 





