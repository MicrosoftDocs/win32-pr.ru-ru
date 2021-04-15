---
title: Структура ИКОНРЕСДИР
description: Содержит измерения и формат цвета отдельного изображения значка в группе ресурсов. Приведенное здесь определение структуры предназначено только для объяснения. он отсутствует в любом стандартном файле заголовка.
ms.assetid: 4c727369-2e90-40ad-85af-96d7e060b97a
keywords:
- Меню структуры ИКОНРЕСДИР и другие ресурсы
topic_type:
- apiref
api_name:
- ICONRESDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: de3d15bf250685e0b0cad935cd5e8094b2f2ceee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661925"
---
# <a name="iconresdir-structure"></a><span data-ttu-id="6fad4-105">Структура ИКОНРЕСДИР</span><span class="sxs-lookup"><span data-stu-id="6fad4-105">ICONRESDIR structure</span></span>

<span data-ttu-id="6fad4-106">Содержит измерения и формат цвета отдельного изображения значка в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6fad4-106">Contains the dimensions and color format of an individual icon image in a resource group.</span></span> <span data-ttu-id="6fad4-107">Приведенное здесь определение структуры предназначено только для объяснения. он отсутствует в любом стандартном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="6fad4-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fad4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6fad4-108">Syntax</span></span>


```C++
typedef struct {
  BYTE Width;
  BYTE Height;
  BYTE ColorCount;
  BYTE reserved;
} ICONRESDIR;
```



## <a name="members"></a><span data-ttu-id="6fad4-109">Члены</span><span class="sxs-lookup"><span data-stu-id="6fad4-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="6fad4-110">**Width**</span><span class="sxs-lookup"><span data-stu-id="6fad4-110">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="6fad4-111">Тип: **Byte**</span><span class="sxs-lookup"><span data-stu-id="6fad4-111">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="6fad4-112">Ширина значка в пикселях.</span><span class="sxs-lookup"><span data-stu-id="6fad4-112">The width of the icon, in pixels.</span></span> <span data-ttu-id="6fad4-113">Допустимые значения: 16, 32 и 64.</span><span class="sxs-lookup"><span data-stu-id="6fad4-113">Acceptable values are 16, 32, and 64.</span></span>

</dd> <dt>

<span data-ttu-id="6fad4-114">**Height**</span><span class="sxs-lookup"><span data-stu-id="6fad4-114">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="6fad4-115">Тип: **Byte**</span><span class="sxs-lookup"><span data-stu-id="6fad4-115">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="6fad4-116">Высота значка в пикселях.</span><span class="sxs-lookup"><span data-stu-id="6fad4-116">The height of the icon, in pixels.</span></span> <span data-ttu-id="6fad4-117">Допустимые значения: 16, 32 и 64.</span><span class="sxs-lookup"><span data-stu-id="6fad4-117">Acceptable values are 16, 32, and 64.</span></span>

</dd> <dt>

<span data-ttu-id="6fad4-118">**колоркаунт**</span><span class="sxs-lookup"><span data-stu-id="6fad4-118">**ColorCount**</span></span>
</dt> <dd>

<span data-ttu-id="6fad4-119">Тип: **Byte**</span><span class="sxs-lookup"><span data-stu-id="6fad4-119">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="6fad4-120">Число цветов в значке.</span><span class="sxs-lookup"><span data-stu-id="6fad4-120">The number of colors in the icon.</span></span> <span data-ttu-id="6fad4-121">Допустимые значения: 2, 8 и 16.</span><span class="sxs-lookup"><span data-stu-id="6fad4-121">Acceptable values are 2, 8, and 16.</span></span>

</dd> <dt>

<span data-ttu-id="6fad4-122">**процессу**</span><span class="sxs-lookup"><span data-stu-id="6fad4-122">**reserved**</span></span>
</dt> <dd>

<span data-ttu-id="6fad4-123">Тип: **Byte**</span><span class="sxs-lookup"><span data-stu-id="6fad4-123">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="6fad4-124">Процессу необходимо задать то же значение, что и для зарезервированного поля в заголовке файла значка.</span><span class="sxs-lookup"><span data-stu-id="6fad4-124">Reserved; must be set to the same value as that of the reserved field in the icon file header.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6fad4-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6fad4-125">Remarks</span></span>

<span data-ttu-id="6fad4-126">Структура **иконресдир** передается в структуру [**ресдир**](resdir.md) , если структура **ресдир** описывает значок.</span><span class="sxs-lookup"><span data-stu-id="6fad4-126">The **ICONRESDIR** structure is passed in the [**RESDIR**](resdir.md) structure if the **RESDIR** structure describes an icon.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fad4-127">Требования</span><span class="sxs-lookup"><span data-stu-id="6fad4-127">Requirements</span></span>



| <span data-ttu-id="6fad4-128">Требование</span><span class="sxs-lookup"><span data-stu-id="6fad4-128">Requirement</span></span> | <span data-ttu-id="6fad4-129">Значение</span><span class="sxs-lookup"><span data-stu-id="6fad4-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="6fad4-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6fad4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6fad4-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6fad4-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6fad4-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6fad4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6fad4-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6fad4-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6fad4-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6fad4-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="6fad4-135">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="6fad4-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6fad4-136">**ресдир**</span><span class="sxs-lookup"><span data-stu-id="6fad4-136">**RESDIR**</span></span>](resdir.md)
</dt> <dt>

<span data-ttu-id="6fad4-137">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="6fad4-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6fad4-138">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="6fad4-138">Resources</span></span>](resources.md)
</dt> </dl>

 

 





