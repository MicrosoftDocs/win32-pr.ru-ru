---
title: Класс Имеморяллокатор
description: Реализуется механизмом выделения памяти для функции Стгконвертпропертитовариант.
ms.assetid: a0735b62-5ed3-42df-a320-b58c742645a8
keywords:
- Структурированное хранилище класса Имеморяллокатор
- Структурированное хранилище класса Имеморяллокатор, описание
topic_type:
- apiref
api_name:
- IMemoryAllocator
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 421162fd0ee6228f1dbae03eeb52e5643b0e0b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415640"
---
# <a name="imemoryallocator-class"></a><span data-ttu-id="083f5-105">Класс Имеморяллокатор</span><span class="sxs-lookup"><span data-stu-id="083f5-105">IMemoryAllocator class</span></span>

<span data-ttu-id="083f5-106">Класс **имеморяллокатор** реализуется механизмом выделения памяти для функции [**стгконвертпропертитовариант**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) .</span><span class="sxs-lookup"><span data-stu-id="083f5-106">The **IMemoryAllocator** class is implemented by the memory allocator for the [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) function.</span></span>

## <a name="methods"></a><span data-ttu-id="083f5-107">Методы</span><span class="sxs-lookup"><span data-stu-id="083f5-107">Methods</span></span>



| <span data-ttu-id="083f5-108">Имя</span><span class="sxs-lookup"><span data-stu-id="083f5-108">Name</span></span>                                                     | <span data-ttu-id="083f5-109">Описание</span><span class="sxs-lookup"><span data-stu-id="083f5-109">Description</span></span>                                                                                                                                                                                                        |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="083f5-110">**Памяти**</span><span class="sxs-lookup"><span data-stu-id="083f5-110">**Allocate**</span></span>](imemoryallocator-allocate.md)<br/> | <span data-ttu-id="083f5-111">Выделяет память для функции [**стгконвертпропертитовариант**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) , когда функция преобразует тип данных **сериализедпропертивалуе** в тип данных **пропвариант** .</span><span class="sxs-lookup"><span data-stu-id="083f5-111">Allocates memory for the [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) function when the function converts a **SERIALIZEDPROPERTYVALUE** data type to a **PROPVARIANT** data type.</span></span><br/> |
| [<span data-ttu-id="083f5-112">**Бесплатный**</span><span class="sxs-lookup"><span data-stu-id="083f5-112">**Free**</span></span>](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize)<br/>        | <span data-ttu-id="083f5-113">Освобождает память, выделенную методом [**выделения**](imemoryallocator-allocate.md) .</span><span class="sxs-lookup"><span data-stu-id="083f5-113">Frees the memory allocated by the [**Allocate**](imemoryallocator-allocate.md) method.</span></span><br/>                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="083f5-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="083f5-114">Remarks</span></span>

<span data-ttu-id="083f5-115">Этот класс используется только функцией [**стгконвертпропертитовариант**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) .</span><span class="sxs-lookup"><span data-stu-id="083f5-115">This class is only used by the [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="083f5-116">Требования</span><span class="sxs-lookup"><span data-stu-id="083f5-116">Requirements</span></span>



| <span data-ttu-id="083f5-117">Требование</span><span class="sxs-lookup"><span data-stu-id="083f5-117">Requirement</span></span> | <span data-ttu-id="083f5-118">Значение</span><span class="sxs-lookup"><span data-stu-id="083f5-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="083f5-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="083f5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="083f5-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="083f5-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="083f5-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="083f5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="083f5-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="083f5-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="083f5-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="083f5-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="083f5-124"><dt>Ole32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="083f5-124"><dt>Ole32.lib</dt></span></span> </dl> |



 

