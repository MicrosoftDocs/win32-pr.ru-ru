---
title: Метод выделения Имеморяллокатор
description: Метод Allocate выделяет память для функции Стгконвертпропертитовариант, когда функция преобразует тип данных СЕРИАЛИЗЕДПРОПЕРТИВАЛУЕ в тип данных ПРОПВАРИАНТ.
ms.assetid: aa9c9308-fb55-405c-901a-9d5abfac5395
keywords:
- Выделить структурированное хранилище методов
- Выделить структурированное хранилище методов, интерфейс Имеморяллокатор
- Структурированное хранилище интерфейса Имеморяллокатор, метод Allocate
topic_type:
- apiref
api_name:
- IMemoryAllocator.Allocate
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7ee4b220e1c1e14ceed685e9b2adc694a44d2e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661819"
---
# <a name="imemoryallocatorallocate-method"></a><span data-ttu-id="4e0ac-106">Метод Имеморяллокатор:: allocate</span><span class="sxs-lookup"><span data-stu-id="4e0ac-106">IMemoryAllocator::Allocate method</span></span>

<span data-ttu-id="4e0ac-107">Метод **allocate** выделяет память для функции [**стгконвертпропертитовариант**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) , когда функция преобразует тип данных **сериализедпропертивалуе** в тип данных **пропвариант** .</span><span class="sxs-lookup"><span data-stu-id="4e0ac-107">The **Allocate** method allocates memory for the [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) function when the function converts a **SERIALIZEDPROPERTYVALUE** data type to a **PROPVARIANT** data type.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e0ac-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e0ac-108">Syntax</span></span>


```C++
virtual void* Allocate(
  [in] ULONG cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="4e0ac-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4e0ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e0ac-110">*кбсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4e0ac-110">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e0ac-111">Задает размер выделяемой памяти.</span><span class="sxs-lookup"><span data-stu-id="4e0ac-111">Specifies the size of memory to be allocated.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4e0ac-112">Требования</span><span class="sxs-lookup"><span data-stu-id="4e0ac-112">Requirements</span></span>



| <span data-ttu-id="4e0ac-113">Требование</span><span class="sxs-lookup"><span data-stu-id="4e0ac-113">Requirement</span></span> | <span data-ttu-id="4e0ac-114">Значение</span><span class="sxs-lookup"><span data-stu-id="4e0ac-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4e0ac-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4e0ac-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4e0ac-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4e0ac-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="4e0ac-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4e0ac-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4e0ac-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4e0ac-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4e0ac-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4e0ac-119">Library</span></span><br/>                  | <dl> <span data-ttu-id="4e0ac-120"><dt>Ole32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e0ac-120"><dt>Ole32.lib</dt></span></span> </dl> |



 

