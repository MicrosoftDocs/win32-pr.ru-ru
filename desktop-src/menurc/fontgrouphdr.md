---
title: Структура ФОНТГРАУФДР
description: Содержит сведения, необходимые приложению для доступа к определенному шрифту. Приведенное здесь определение структуры предназначено только для объяснения. он отсутствует в любом стандартном файле заголовка.
ms.assetid: 180b3dfd-3f20-4100-b45b-2f253b7c0582
keywords:
- Меню структуры ФОНТГРАУФДР и другие ресурсы
topic_type:
- apiref
api_name:
- FONTGROUPHDR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1d67d9ecfa451970422f21d05817f26170a9c8eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104262213"
---
# <a name="fontgrouphdr-structure"></a><span data-ttu-id="d8c1c-105">Структура ФОНТГРАУФДР</span><span class="sxs-lookup"><span data-stu-id="d8c1c-105">FONTGROUPHDR structure</span></span>

<span data-ttu-id="d8c1c-106">Содержит сведения, необходимые приложению для доступа к определенному шрифту.</span><span class="sxs-lookup"><span data-stu-id="d8c1c-106">Contains the information necessary for an application to access a specific font.</span></span> <span data-ttu-id="d8c1c-107">Приведенное здесь определение структуры предназначено только для объяснения. он отсутствует в любом стандартном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="d8c1c-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8c1c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d8c1c-108">Syntax</span></span>


```C++
typedef struct {
  WORD     NumberOfFonts;
  DIRENTRY DE;
} FONTGROUPHDR;
```



## <a name="members"></a><span data-ttu-id="d8c1c-109">Члены</span><span class="sxs-lookup"><span data-stu-id="d8c1c-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="d8c1c-110">**нумбероффонтс**</span><span class="sxs-lookup"><span data-stu-id="d8c1c-110">**NumberOfFonts**</span></span>
</dt> <dd>

<span data-ttu-id="d8c1c-111">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="d8c1c-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="d8c1c-112">Число отдельных шрифтов, связанных с этим ресурсом.</span><span class="sxs-lookup"><span data-stu-id="d8c1c-112">The number of individual fonts associated with this resource.</span></span>

</dd> <dt>

<span data-ttu-id="d8c1c-113">**RU**</span><span class="sxs-lookup"><span data-stu-id="d8c1c-113">**DE**</span></span>
</dt> <dd>

<span data-ttu-id="d8c1c-114">Тип: **[ **Аренда**](direntry.md)**</span><span class="sxs-lookup"><span data-stu-id="d8c1c-114">Type: **[**DIRENTRY**](direntry.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d8c1c-115">Структура, которая содержит уникальный порядковый идентификатор для каждого шрифта в ресурсе.</span><span class="sxs-lookup"><span data-stu-id="d8c1c-115">A structure that contains a unique ordinal identifier for each font in the resource.</span></span> <span data-ttu-id="d8c1c-116">Элемент **de** — это заполнитель для массива с переменной длиной из [**неарендных**](direntry.md) структур.</span><span class="sxs-lookup"><span data-stu-id="d8c1c-116">The **DE** member is a placeholder for the variable-length array of [**DIRENTRY**](direntry.md) structures.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8c1c-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d8c1c-117">Remarks</span></span>

<span data-ttu-id="d8c1c-118">Структура **фонтграуфдр** соответствует данным для отдельных шрифтов в. RES — файл.</span><span class="sxs-lookup"><span data-stu-id="d8c1c-118">The **FONTGROUPHDR** structure follows the data for the individual fonts in the .Res file.</span></span> <span data-ttu-id="d8c1c-119">Компилятор ресурсов автоматически добавляет структуру **фонтграуфдр** , как правило, в качестве последней записи в файле.</span><span class="sxs-lookup"><span data-stu-id="d8c1c-119">The resource compiler automatically adds the **FONTGROUPHDR** structure, generally as the last entry in the file.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8c1c-120">Требования</span><span class="sxs-lookup"><span data-stu-id="d8c1c-120">Requirements</span></span>



| <span data-ttu-id="d8c1c-121">Требование</span><span class="sxs-lookup"><span data-stu-id="d8c1c-121">Requirement</span></span> | <span data-ttu-id="d8c1c-122">Значение</span><span class="sxs-lookup"><span data-stu-id="d8c1c-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d8c1c-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d8c1c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d8c1c-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d8c1c-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d8c1c-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d8c1c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d8c1c-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d8c1c-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d8c1c-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d8c1c-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="d8c1c-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="d8c1c-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d8c1c-129">**Аренда**</span><span class="sxs-lookup"><span data-stu-id="d8c1c-129">**DIRENTRY**</span></span>](direntry.md)
</dt> <dt>

[<span data-ttu-id="d8c1c-130">**фонтдирентри**</span><span class="sxs-lookup"><span data-stu-id="d8c1c-130">**FONTDIRENTRY**</span></span>](fontdirentry.md)
</dt> <dt>

<span data-ttu-id="d8c1c-131">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="d8c1c-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d8c1c-132">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="d8c1c-132">Resources</span></span>](resources.md)
</dt> </dl>

 

 





