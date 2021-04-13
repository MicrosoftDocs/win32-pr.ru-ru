---
title: Интерфейс IDWriteFont2
description: Представляет физический шрифт в коллекции шрифтов.
ms.assetid: 4E3069AE-5882-4A26-A36D-BE7D7EE1B0C3
keywords:
- Непосредственная запись интерфейса IDWriteFont2
- Непосредственная запись интерфейса IDWriteFont2, описание
topic_type:
- apiref
api_name:
- IDWriteFont2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f82a47e56915747b0e118a6f63484b9dd3dcdbd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340840"
---
# <a name="idwritefont2-interface"></a><span data-ttu-id="04e3b-105">Интерфейс IDWriteFont2</span><span class="sxs-lookup"><span data-stu-id="04e3b-105">IDWriteFont2 interface</span></span>

<span data-ttu-id="04e3b-106">Представляет физический шрифт в коллекции шрифтов.</span><span class="sxs-lookup"><span data-stu-id="04e3b-106">Represents a physical font in a font collection.</span></span>

<span data-ttu-id="04e3b-107">Этот интерфейс добавляет возможность проверки того, является ли путь визуализации цвета потенциально необходимым.</span><span class="sxs-lookup"><span data-stu-id="04e3b-107">This interface adds the ability to check if a color rendering path is potentially necessary.</span></span>

## <a name="members"></a><span data-ttu-id="04e3b-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="04e3b-108">Members</span></span>

<span data-ttu-id="04e3b-109">Интерфейс **IDWriteFont2** наследует от [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1).</span><span class="sxs-lookup"><span data-stu-id="04e3b-109">The **IDWriteFont2** interface inherits from [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1).</span></span> <span data-ttu-id="04e3b-110">**IDWriteFont2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="04e3b-110">**IDWriteFont2** also has these types of members:</span></span>

-   [<span data-ttu-id="04e3b-111">Методы</span><span class="sxs-lookup"><span data-stu-id="04e3b-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="04e3b-112">Методы</span><span class="sxs-lookup"><span data-stu-id="04e3b-112">Methods</span></span>

<span data-ttu-id="04e3b-113">Интерфейс **IDWriteFont2** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="04e3b-113">The **IDWriteFont2** interface has these methods.</span></span>



| <span data-ttu-id="04e3b-114">Метод</span><span class="sxs-lookup"><span data-stu-id="04e3b-114">Method</span></span>                                          | <span data-ttu-id="04e3b-115">Описание</span><span class="sxs-lookup"><span data-stu-id="04e3b-115">Description</span></span>                                                                        |
|:------------------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="04e3b-116">**исколорфонт**</span><span class="sxs-lookup"><span data-stu-id="04e3b-116">**IsColorFont**</span></span>](idwritefont2-iscolorfont.md) | <span data-ttu-id="04e3b-117">Позволяет определить, является ли путь визуализации цвета потенциально необходимым.</span><span class="sxs-lookup"><span data-stu-id="04e3b-117">Enables determining if a color rendering path is potentially necessary.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="04e3b-118">Требования</span><span class="sxs-lookup"><span data-stu-id="04e3b-118">Requirements</span></span>



| <span data-ttu-id="04e3b-119">Требование</span><span class="sxs-lookup"><span data-stu-id="04e3b-119">Requirement</span></span> | <span data-ttu-id="04e3b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="04e3b-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04e3b-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="04e3b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="04e3b-122">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="04e3b-122">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="04e3b-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="04e3b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="04e3b-124">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="04e3b-124">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="04e3b-125">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="04e3b-125">Minimum supported phone</span></span><br/>  | <span data-ttu-id="04e3b-126">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="04e3b-126">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="04e3b-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="04e3b-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="04e3b-128"><dt>Дврите. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04e3b-128"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="04e3b-129">DLL</span><span class="sxs-lookup"><span data-stu-id="04e3b-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04e3b-130"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04e3b-130"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="04e3b-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="04e3b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04e3b-132">**IDWriteFont1**</span><span class="sxs-lookup"><span data-stu-id="04e3b-132">**IDWriteFont1**</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1)
</dt> </dl>

 

