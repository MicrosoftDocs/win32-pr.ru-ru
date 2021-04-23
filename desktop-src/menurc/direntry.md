---
title: Структура аренды
description: Содержит уникальный порядковый номер, определяющий отдельный шрифт в группе ресурсов Font. Приведенное здесь определение структуры предназначено только для объяснения. он отсутствует в любом стандартном файле заголовка.
ms.assetid: 4afc561e-bc98-4968-9a00-5002870b0c5e
keywords:
- Меню "структура аренды" и другие ресурсы
topic_type:
- apiref
api_name:
- DIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caed8f05a92abbeda39084b99b6806c2e28777a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802674"
---
# <a name="direntry-structure"></a><span data-ttu-id="67517-105">Структура аренды</span><span class="sxs-lookup"><span data-stu-id="67517-105">DIRENTRY structure</span></span>

<span data-ttu-id="67517-106">Содержит уникальный порядковый номер, определяющий отдельный шрифт в группе ресурсов Font.</span><span class="sxs-lookup"><span data-stu-id="67517-106">Contains a unique ordinal that identifies an individual font in the font resource group.</span></span> <span data-ttu-id="67517-107">Приведенное здесь определение структуры предназначено только для объяснения. он отсутствует в любом стандартном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="67517-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="67517-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="67517-108">Syntax</span></span>


```C++
typedef struct {
  WORD fontOrdinal;
} DIRENTRY;
```



## <a name="members"></a><span data-ttu-id="67517-109">Члены</span><span class="sxs-lookup"><span data-stu-id="67517-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="67517-110">**фонтординал**</span><span class="sxs-lookup"><span data-stu-id="67517-110">**fontOrdinal**</span></span>
</dt> <dd>

<span data-ttu-id="67517-111">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="67517-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="67517-112">Уникальный порядковый идентификатор для отдельного шрифта в группе ресурсов шрифтов.</span><span class="sxs-lookup"><span data-stu-id="67517-112">A unique ordinal identifier for an individual font in a font resource group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67517-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="67517-113">Remarks</span></span>

<span data-ttu-id="67517-114">Структура [**фонтдирентри**](fontdirentry.md) для указанного шрифта непосредственно соответствует структуре **аренды** для этого шрифта.</span><span class="sxs-lookup"><span data-stu-id="67517-114">The [**FONTDIRENTRY**](fontdirentry.md) structure for the specified font directly follows the **DIRENTRY** structure for that font.</span></span>

## <a name="requirements"></a><span data-ttu-id="67517-115">Требования</span><span class="sxs-lookup"><span data-stu-id="67517-115">Requirements</span></span>



| <span data-ttu-id="67517-116">Требование</span><span class="sxs-lookup"><span data-stu-id="67517-116">Requirement</span></span> | <span data-ttu-id="67517-117">Значение</span><span class="sxs-lookup"><span data-stu-id="67517-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="67517-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="67517-118">Minimum supported client</span></span><br/> | <span data-ttu-id="67517-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="67517-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="67517-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="67517-120">Minimum supported server</span></span><br/> | <span data-ttu-id="67517-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="67517-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="67517-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="67517-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="67517-123">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="67517-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="67517-124">**фонтдирентри**</span><span class="sxs-lookup"><span data-stu-id="67517-124">**FONTDIRENTRY**</span></span>](fontdirentry.md)
</dt> <dt>

[<span data-ttu-id="67517-125">**фонтграуфдр**</span><span class="sxs-lookup"><span data-stu-id="67517-125">**FONTGROUPHDR**</span></span>](fontgrouphdr.md)
</dt> <dt>

<span data-ttu-id="67517-126">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="67517-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="67517-127">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="67517-127">Resources</span></span>](resources.md)
</dt> </dl>

 

 





