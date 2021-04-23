---
title: Структура MPCOMPONENT_STATUS (Мпклиент. h)
description: Сведения о состоянии компонента.
ms.assetid: 0E589E52-A204-425C-880B-CF13C16893F3
keywords:
- MPCOMPONENT_STATUS структуры устаревшие функции среды Windows
- Функции PMPCOMPONENT_STATUS указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPCOMPONENT_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2923136d2599440bc6ccfe863af9795f7d7ff96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801918"
---
# <a name="mpcomponent_status-structure"></a><span data-ttu-id="ac4b3-105">\_Структура состояния мпкомпонент</span><span class="sxs-lookup"><span data-stu-id="ac4b3-105">MPCOMPONENT\_STATUS structure</span></span>

<span data-ttu-id="ac4b3-106">Сведения о состоянии компонента.</span><span class="sxs-lookup"><span data-stu-id="ac4b3-106">Component status information.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac4b3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac4b3-107">Syntax</span></span>


```C++
typedef struct tagMPCOMPONENT_STATUS {
  BOOL    fEnable;
  HRESULT hResult;
} MPCOMPONENT_STATUS, *PMPCOMPONENT_STATUS;
```



## <a name="members"></a><span data-ttu-id="ac4b3-108">Члены</span><span class="sxs-lookup"><span data-stu-id="ac4b3-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ac4b3-109">**фенабле**</span><span class="sxs-lookup"><span data-stu-id="ac4b3-109">**fEnable**</span></span>
</dt> <dd>

<span data-ttu-id="ac4b3-110">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="ac4b3-110">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="ac4b3-111">Состояние компонента.</span><span class="sxs-lookup"><span data-stu-id="ac4b3-111">Status for the component.</span></span>

</dd> <dt>

<span data-ttu-id="ac4b3-112">**Состав**</span><span class="sxs-lookup"><span data-stu-id="ac4b3-112">**hResult**</span></span>
</dt> <dd>

<span data-ttu-id="ac4b3-113">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ac4b3-113">Type: **HRESULT**</span></span>

</dd> <dd>

<span data-ttu-id="ac4b3-114">Код успешного выполнения или ошибки, связанный с состоянием.</span><span class="sxs-lookup"><span data-stu-id="ac4b3-114">Success or failure code associated with the status.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ac4b3-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ac4b3-115">Requirements</span></span>



| <span data-ttu-id="ac4b3-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ac4b3-116">Requirement</span></span> | <span data-ttu-id="ac4b3-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ac4b3-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ac4b3-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ac4b3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ac4b3-119">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ac4b3-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ac4b3-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ac4b3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ac4b3-121">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ac4b3-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ac4b3-122">Header</span><span class="sxs-lookup"><span data-stu-id="ac4b3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac4b3-123"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac4b3-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





