---
title: Структура MPVERSION_INFO (Мпклиент. h)
description: Сведения о версии для компонентов диспетчера защиты от вредоносных программ.
ms.assetid: C18EE6FE-57E1-4814-85CA-19C3ACE275D2
keywords:
- MPVERSION_INFO структуры устаревшие функции среды Windows
- Функции PMPVERSION_INFO указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPVERSION_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f30153c427b880600a3d8aeb3c411a8679cd64b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341045"
---
# <a name="mpversion_info-structure"></a><span data-ttu-id="1b913-105">\_Структура сведений о MPVERSION</span><span class="sxs-lookup"><span data-stu-id="1b913-105">MPVERSION\_INFO structure</span></span>

<span data-ttu-id="1b913-106">Сведения о версии для компонентов диспетчера защиты от вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="1b913-106">Version information for the malware protection manager's components.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b913-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1b913-107">Syntax</span></span>


```C++
typedef struct tagMPVERSION_INFO {
  MPCOMPONENT_VERSION Product;
  MPCOMPONENT_VERSION Service;
  MPCOMPONENT_VERSION FileSystemFilter;
  MPCOMPONENT_VERSION Engine;
  MPCOMPONENT_VERSION ASSignature;
  MPCOMPONENT_VERSION AVSignature;
  MPCOMPONENT_VERSION NISEngine;
  MPCOMPONENT_VERSION NISSignature;
  MPCOMPONENT_VERSION Reserved[4];
} MPVERSION_INFO, *PMPVERSION_INFO;
```



## <a name="members"></a><span data-ttu-id="1b913-108">Члены</span><span class="sxs-lookup"><span data-stu-id="1b913-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="1b913-109">**Продукт**</span><span class="sxs-lookup"><span data-stu-id="1b913-109">**Product**</span></span>
</dt> <dd>

<span data-ttu-id="1b913-110">Тип: **[ **мпкомпонент \_ версия**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="1b913-110">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1b913-111">Номер версии продукта.</span><span class="sxs-lookup"><span data-stu-id="1b913-111">Product version.</span></span>

</dd> <dt>

<span data-ttu-id="1b913-112">**Служба**</span><span class="sxs-lookup"><span data-stu-id="1b913-112">**Service**</span></span>
</dt> <dd>

<span data-ttu-id="1b913-113">Тип: **[ **мпкомпонент \_ версия**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="1b913-113">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1b913-114">Версия компонента службы.</span><span class="sxs-lookup"><span data-stu-id="1b913-114">Service component version.</span></span>

</dd> <dt>

<span data-ttu-id="1b913-115">**филесистемфилтер**</span><span class="sxs-lookup"><span data-stu-id="1b913-115">**FileSystemFilter**</span></span>
</dt> <dd>

<span data-ttu-id="1b913-116">Тип: **[ **мпкомпонент \_ версия**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="1b913-116">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1b913-117">Версия компонента фильтра файловой системы.</span><span class="sxs-lookup"><span data-stu-id="1b913-117">File system filter component version.</span></span>

</dd> <dt>

<span data-ttu-id="1b913-118">**Ядро**</span><span class="sxs-lookup"><span data-stu-id="1b913-118">**Engine**</span></span>
</dt> <dd>

<span data-ttu-id="1b913-119">Тип: **[ **мпкомпонент \_ версия**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="1b913-119">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1b913-120">Версия компонента ядра.</span><span class="sxs-lookup"><span data-stu-id="1b913-120">Engine component version.</span></span>

</dd> <dt>

<span data-ttu-id="1b913-121">**ассигнатуре**</span><span class="sxs-lookup"><span data-stu-id="1b913-121">**ASSignature**</span></span>
</dt> <dd>

<span data-ttu-id="1b913-122">Тип: **[ **мпкомпонент \_ версия**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="1b913-122">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1b913-123">Версия компонента подписи антишпионского по.</span><span class="sxs-lookup"><span data-stu-id="1b913-123">Antispyware signature component version.</span></span>

</dd> <dt>

<span data-ttu-id="1b913-124">**авсигнатуре**</span><span class="sxs-lookup"><span data-stu-id="1b913-124">**AVSignature**</span></span>
</dt> <dd>

<span data-ttu-id="1b913-125">Тип: **[ **мпкомпонент \_ версия**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="1b913-125">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1b913-126">Версия компонента сигнатур Антивируса.</span><span class="sxs-lookup"><span data-stu-id="1b913-126">Antivirus signature component version.</span></span>

</dd> <dt>

<span data-ttu-id="1b913-127">**нисенгине**</span><span class="sxs-lookup"><span data-stu-id="1b913-127">**NISEngine**</span></span>
</dt> <dd>

<span data-ttu-id="1b913-128">Тип: **[ **мпкомпонент \_ версия**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="1b913-128">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1b913-129">Версия подсистемы NIS.</span><span class="sxs-lookup"><span data-stu-id="1b913-129">NIS engine version.</span></span>

</dd> <dt>

<span data-ttu-id="1b913-130">**ниссигнатуре**</span><span class="sxs-lookup"><span data-stu-id="1b913-130">**NISSignature**</span></span>
</dt> <dd>

<span data-ttu-id="1b913-131">Тип: **[ **мпкомпонент \_ версия**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="1b913-131">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1b913-132">Версия компонента подписи NIS-подписи.</span><span class="sxs-lookup"><span data-stu-id="1b913-132">NIS Signature signature component version.</span></span>

</dd> <dt>

<span data-ttu-id="1b913-133">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="1b913-133">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="1b913-134">Тип: **[**мпкомпонент \_ версия**](mpcomponent-version.md) \[ 4.\]**</span><span class="sxs-lookup"><span data-stu-id="1b913-134">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)\[4\]**</span></span>

</dd> <dd>

<span data-ttu-id="1b913-135">Зарезервированные поля.</span><span class="sxs-lookup"><span data-stu-id="1b913-135">Reserved fields.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1b913-136">Требования</span><span class="sxs-lookup"><span data-stu-id="1b913-136">Requirements</span></span>



| <span data-ttu-id="1b913-137">Требование</span><span class="sxs-lookup"><span data-stu-id="1b913-137">Requirement</span></span> | <span data-ttu-id="1b913-138">Значение</span><span class="sxs-lookup"><span data-stu-id="1b913-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b913-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1b913-139">Minimum supported client</span></span><br/> | <span data-ttu-id="1b913-140">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1b913-140">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="1b913-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1b913-141">Minimum supported server</span></span><br/> | <span data-ttu-id="1b913-142">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1b913-142">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1b913-143">Header</span><span class="sxs-lookup"><span data-stu-id="1b913-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b913-144"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b913-144"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b913-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1b913-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b913-146">**\_версия мпкомпонент**</span><span class="sxs-lookup"><span data-stu-id="1b913-146">**MPCOMPONENT\_VERSION**</span></span>](mpcomponent-version.md)
</dt> </dl>

 

 





