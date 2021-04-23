---
title: Структура ЛОКАЛХЕАДЕР
description: Содержит координаты x и y активной точки, связанной с курсором, идентифицируемым структурой РЕСДИР. Приведенное здесь определение структуры предназначено только для объяснения. он отсутствует в любом стандартном файле заголовка.
ms.assetid: 8cf74040-8b8f-447e-a881-1bcf05b151e2
keywords:
- Меню структуры ЛОКАЛХЕАДЕР и другие ресурсы
topic_type:
- apiref
api_name:
- LOCALHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7aa2ee51e1a9e456398a42d8190781b5dbec8d14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415724"
---
# <a name="localheader-structure"></a><span data-ttu-id="1036f-105">Структура ЛОКАЛХЕАДЕР</span><span class="sxs-lookup"><span data-stu-id="1036f-105">LOCALHEADER structure</span></span>

<span data-ttu-id="1036f-106">Содержит координаты x и y активной точки, связанной с курсором, идентифицируемым структурой [**ресдир**](resdir.md) .</span><span class="sxs-lookup"><span data-stu-id="1036f-106">Contains the x- and y-coordinates of a hotspot associated with the cursor identified by a [**RESDIR**](resdir.md) structure.</span></span> <span data-ttu-id="1036f-107">Приведенное здесь определение структуры предназначено только для объяснения. он отсутствует в любом стандартном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="1036f-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1036f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1036f-108">Syntax</span></span>


```C++
typedef struct {
  WORD xHotSpot;
  WORD yHotSpot;
} LOCALHEADER;
```



## <a name="members"></a><span data-ttu-id="1036f-109">Члены</span><span class="sxs-lookup"><span data-stu-id="1036f-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="1036f-110">**ксхотспот**</span><span class="sxs-lookup"><span data-stu-id="1036f-110">**xHotSpot**</span></span>
</dt> <dd>

<span data-ttu-id="1036f-111">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="1036f-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="1036f-112">Координата по оси x активной точки курсора в пикселях.</span><span class="sxs-lookup"><span data-stu-id="1036f-112">The x-coordinate of the cursor hot spot, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="1036f-113">**ихотспот**</span><span class="sxs-lookup"><span data-stu-id="1036f-113">**yHotSpot**</span></span>
</dt> <dd>

<span data-ttu-id="1036f-114">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="1036f-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="1036f-115">Координата по оси y активной точки курсора в пикселях.</span><span class="sxs-lookup"><span data-stu-id="1036f-115">The y-coordinate of the cursor hot spot, in pixels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1036f-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1036f-116">Remarks</span></span>

<span data-ttu-id="1036f-117">Структура **локалхеадер** — это первые данные, записываемые в [ресурс \_ курсора RT](/windows/desktop/menurc/resource-types) , если структура [**ресдир**](resdir.md) содержит сведения о курсоре.</span><span class="sxs-lookup"><span data-stu-id="1036f-117">The **LOCALHEADER** structure is the first data written to the [RT\_CURSOR](/windows/desktop/menurc/resource-types) resource if a [**RESDIR**](resdir.md) structure contains information about a cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="1036f-118">Требования</span><span class="sxs-lookup"><span data-stu-id="1036f-118">Requirements</span></span>



| <span data-ttu-id="1036f-119">Требование</span><span class="sxs-lookup"><span data-stu-id="1036f-119">Requirement</span></span> | <span data-ttu-id="1036f-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1036f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="1036f-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1036f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1036f-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1036f-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1036f-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1036f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1036f-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1036f-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="1036f-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1036f-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="1036f-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="1036f-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1036f-127">**курсордир**</span><span class="sxs-lookup"><span data-stu-id="1036f-127">**CURSORDIR**</span></span>](cursordir.md)
</dt> <dt>

[<span data-ttu-id="1036f-128">**ресдир**</span><span class="sxs-lookup"><span data-stu-id="1036f-128">**RESDIR**</span></span>](resdir.md)
</dt> <dt>

<span data-ttu-id="1036f-129">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="1036f-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1036f-130">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="1036f-130">Resources</span></span>](resources.md)
</dt> </dl>

 

