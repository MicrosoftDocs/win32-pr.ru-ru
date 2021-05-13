---
description: Задает или возвращает состояние дисковых квот тома.
title: Дисккуотаконтрол. Куотастате, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.QuotaState
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b0766ecf-6e22-4481-a6a7-df873a277bc2
ms.openlocfilehash: 3580ad47a5ec6a5d0276dc0e30a4a6463aca2fb3
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843195"
---
# <a name="diskquotacontrolquotastate-property"></a><span data-ttu-id="4f8c6-103">Дисккуотаконтрол. Куотастате, свойство</span><span class="sxs-lookup"><span data-stu-id="4f8c6-103">DiskQuotaControl.QuotaState property</span></span>

<span data-ttu-id="4f8c6-104">Задает или возвращает состояние дисковых квот тома.</span><span class="sxs-lookup"><span data-stu-id="4f8c6-104">Sets or gets the state of the volume's disk quotas.</span></span>

<span data-ttu-id="4f8c6-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="4f8c6-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f8c6-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f8c6-106">Syntax</span></span>


```JScript
iQuotaState = DiskQuotaControl.QuotaState
DiskQuotaControl.QuotaState = iQuotaState
```



## <a name="property-value"></a><span data-ttu-id="4f8c6-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4f8c6-107">Property value</span></span>

<span data-ttu-id="4f8c6-108">Этому свойству можно присвоить одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="4f8c6-108">This property can be set to one of the following values.</span></span>



| <span data-ttu-id="4f8c6-109">Состояние</span><span class="sxs-lookup"><span data-stu-id="4f8c6-109">State</span></span>          | <span data-ttu-id="4f8c6-110">Значение</span><span class="sxs-lookup"><span data-stu-id="4f8c6-110">Value</span></span> | <span data-ttu-id="4f8c6-111">Описание</span><span class="sxs-lookup"><span data-stu-id="4f8c6-111">Description</span></span>               |
|----------------|-------|---------------------------|
| <span data-ttu-id="4f8c6-112">дкстатедисабле</span><span class="sxs-lookup"><span data-stu-id="4f8c6-112">dqStateDisable</span></span> | <span data-ttu-id="4f8c6-113">0</span><span class="sxs-lookup"><span data-stu-id="4f8c6-113">0</span></span>     | <span data-ttu-id="4f8c6-114">Квоты диска отключены.</span><span class="sxs-lookup"><span data-stu-id="4f8c6-114">Disk quotas are disabled.</span></span> |
| <span data-ttu-id="4f8c6-115">дкстатетракк</span><span class="sxs-lookup"><span data-stu-id="4f8c6-115">dqStateTrack</span></span>   | <span data-ttu-id="4f8c6-116">1</span><span class="sxs-lookup"><span data-stu-id="4f8c6-116">1</span></span>     | <span data-ttu-id="4f8c6-117">Квоты диска отключены.</span><span class="sxs-lookup"><span data-stu-id="4f8c6-117">Disk quotas are disabled.</span></span> |
| <span data-ttu-id="4f8c6-118">дкстатинфорце</span><span class="sxs-lookup"><span data-stu-id="4f8c6-118">dqStateEnforce</span></span> | <span data-ttu-id="4f8c6-119">2</span><span class="sxs-lookup"><span data-stu-id="4f8c6-119">2</span></span>     | <span data-ttu-id="4f8c6-120">Применить ограничение квоты.</span><span class="sxs-lookup"><span data-stu-id="4f8c6-120">Enforce quota limit.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="4f8c6-121">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="4f8c6-121">Requirements</span></span>



| <span data-ttu-id="4f8c6-122">Требование</span><span class="sxs-lookup"><span data-stu-id="4f8c6-122">Requirement</span></span> | <span data-ttu-id="4f8c6-123">Значение</span><span class="sxs-lookup"><span data-stu-id="4f8c6-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f8c6-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4f8c6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4f8c6-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4f8c6-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4f8c6-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4f8c6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4f8c6-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4f8c6-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4f8c6-128">DLL</span><span class="sxs-lookup"><span data-stu-id="4f8c6-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f8c6-129"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="4f8c6-129"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f8c6-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f8c6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f8c6-131">**Объект Дисккуотаконтрол**</span><span class="sxs-lookup"><span data-stu-id="4f8c6-131">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




