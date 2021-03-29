---
description: Указывает текущее состояние работающего эксперта.
ms.assetid: 49107459-599c-4710-8935-4b2c789081de
title: Структура ЕКСПЕРТСТАТУС (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTSTATUS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a9e201b692bb82c78f88a35f22f2688d096f1771
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540234"
---
# <a name="expertstatus-structure"></a><span data-ttu-id="41f4c-103">Структура ЕКСПЕРТСТАТУС</span><span class="sxs-lookup"><span data-stu-id="41f4c-103">EXPERTSTATUS structure</span></span>

<span data-ttu-id="41f4c-104">Структура **експертстатус** указывает текущее состояние работающего эксперта.</span><span class="sxs-lookup"><span data-stu-id="41f4c-104">The **EXPERTSTATUS** structure indicates the current status of a running expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="41f4c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="41f4c-105">Syntax</span></span>


```C++
typedef struct {
  EXPERTSTATUSENUMERATION Status;
  DWORD                   SubStatus;
  DWORD                   PercentDone;
  DWORD                   Frame;
  char                    szStatusText[EXPERTSTRINGLENGTH];
} EXPERTSTATUS, *PEXPERTSTATUS;
```



## <a name="members"></a><span data-ttu-id="41f4c-106">Члены</span><span class="sxs-lookup"><span data-stu-id="41f4c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="41f4c-107">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="41f4c-107">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="41f4c-108">Текущее значение состояния эксперта, определенное перечислением [**експертстатусенумератион**](expertstatusenumeration.md) .</span><span class="sxs-lookup"><span data-stu-id="41f4c-108">Current expert status value defined by the [**EXPERTSTATUSENUMERATION**](expertstatusenumeration.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="41f4c-109">**Подсостояние**</span><span class="sxs-lookup"><span data-stu-id="41f4c-109">**SubStatus**</span></span>
</dt> <dd>

<span data-ttu-id="41f4c-110">Значение подсостояния.</span><span class="sxs-lookup"><span data-stu-id="41f4c-110">Sub-status value.</span></span>

</dd> <dt>

<span data-ttu-id="41f4c-111">**PercentDone**</span><span class="sxs-lookup"><span data-stu-id="41f4c-111">**PercentDone**</span></span>
</dt> <dd>

<span data-ttu-id="41f4c-112">Процент выполнения экспертного анализа сетевых данных.</span><span class="sxs-lookup"><span data-stu-id="41f4c-112">Percentage completion of the expert analysis of network data.</span></span>

</dd> <dt>

<span data-ttu-id="41f4c-113">**Frame**</span><span class="sxs-lookup"><span data-stu-id="41f4c-113">**Frame**</span></span>
</dt> <dd>

<span data-ttu-id="41f4c-114">Номер кадра.</span><span class="sxs-lookup"><span data-stu-id="41f4c-114">Frame number.</span></span>

</dd> <dt>

<span data-ttu-id="41f4c-115">**сзстатустекст**</span><span class="sxs-lookup"><span data-stu-id="41f4c-115">**szStatusText**</span></span>
</dt> <dd>

<span data-ttu-id="41f4c-116">Текст, описывающий состояние эксперта.</span><span class="sxs-lookup"><span data-stu-id="41f4c-116">Text that describes the expert status.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="41f4c-117">Требования</span><span class="sxs-lookup"><span data-stu-id="41f4c-117">Requirements</span></span>



| <span data-ttu-id="41f4c-118">Требование</span><span class="sxs-lookup"><span data-stu-id="41f4c-118">Requirement</span></span> | <span data-ttu-id="41f4c-119">Значение</span><span class="sxs-lookup"><span data-stu-id="41f4c-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="41f4c-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="41f4c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="41f4c-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="41f4c-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="41f4c-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="41f4c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="41f4c-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="41f4c-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="41f4c-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="41f4c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="41f4c-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="41f4c-125"><dt>Netmon.h</dt></span></span> </dl> |



 

 




