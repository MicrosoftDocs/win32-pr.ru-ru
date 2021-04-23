---
description: Объект загрузки данных, используемый интерфейсом ID3DX10ThreadPump для асинхронной загрузки данных.
ms.assetid: bda2414c-bbab-47ac-b23a-f58fb86e732d
title: Интерфейс ID3DX10DataLoader (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataLoader
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b0e45d24d663f0ba9a8978bc251a4adf0c7868fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000376"
---
# <a name="id3dx10dataloader-interface"></a><span data-ttu-id="f409b-103">Интерфейс ID3DX10DataLoader</span><span class="sxs-lookup"><span data-stu-id="f409b-103">ID3DX10DataLoader interface</span></span>

<span data-ttu-id="f409b-104">Объект загрузки данных, используемый [**интерфейсом ID3DX10ThreadPump**](id3dx10threadpump.md) для асинхронной загрузки данных.</span><span class="sxs-lookup"><span data-stu-id="f409b-104">Data loading object used by [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) for loading data asynchronously.</span></span>

## <a name="members"></a><span data-ttu-id="f409b-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="f409b-105">Members</span></span>

<span data-ttu-id="f409b-106">Интерфейс **ID3DX10DataLoader** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f409b-106">The **ID3DX10DataLoader** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f409b-107">**ID3DX10DataLoader** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f409b-107">**ID3DX10DataLoader** also has these types of members:</span></span>

-   [<span data-ttu-id="f409b-108">Методы</span><span class="sxs-lookup"><span data-stu-id="f409b-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f409b-109">Методы</span><span class="sxs-lookup"><span data-stu-id="f409b-109">Methods</span></span>

<span data-ttu-id="f409b-110">Интерфейс **ID3DX10DataLoader** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="f409b-110">The **ID3DX10DataLoader** interface has these methods.</span></span>



| <span data-ttu-id="f409b-111">Метод</span><span class="sxs-lookup"><span data-stu-id="f409b-111">Method</span></span>                                             | <span data-ttu-id="f409b-112">Описание</span><span class="sxs-lookup"><span data-stu-id="f409b-112">Description</span></span>                                                                                                                                                                                                                        |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f409b-113">**Распаковки**</span><span class="sxs-lookup"><span data-stu-id="f409b-113">**Decompress**</span></span>](id3dx10dataloader-decompress.md) | <span data-ttu-id="f409b-114">Используется для распаковки закодированных данных.</span><span class="sxs-lookup"><span data-stu-id="f409b-114">Used to decompress encoded data.</span></span> <span data-ttu-id="f409b-115">Обычно это используется для загрузки ресурсов из файловых систем, таких как ZIP-файлы.</span><span class="sxs-lookup"><span data-stu-id="f409b-115">Typically this would be used to load resources from file systems, such as ZIP files.</span></span> <span data-ttu-id="f409b-116">При загрузке из несжатого ресурса стадия распаковки не должна выполнять никаких действий.</span><span class="sxs-lookup"><span data-stu-id="f409b-116">When loading from an uncompressed resource, the decompression stage does not have to do any work.</span></span><br/> |
| [<span data-ttu-id="f409b-117">**Завершить**</span><span class="sxs-lookup"><span data-stu-id="f409b-117">**Destroy**</span></span>](id3dx10dataloader-destroy.md)       | <span data-ttu-id="f409b-118">Используется [**интерфейсом ID3DX10ThreadPump**](id3dx10threadpump.md) для уничтожения загрузчика после завершения рабочего элемента.</span><span class="sxs-lookup"><span data-stu-id="f409b-118">Used by a [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) to destroy the loader after a work item completes.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="f409b-119">**Загрузить**</span><span class="sxs-lookup"><span data-stu-id="f409b-119">**Load**</span></span>](id3dx10dataloader-load.md)             | <span data-ttu-id="f409b-120">Используется [**интерфейсом ID3DX10ThreadPump**](id3dx10threadpump.md) для загрузки данных с диска.</span><span class="sxs-lookup"><span data-stu-id="f409b-120">Used by a [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) to load data from a disk.</span></span><br/>                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="f409b-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f409b-121">Remarks</span></span>

<span data-ttu-id="f409b-122">Этот объект может быть унаследован и его члены переопределены.</span><span class="sxs-lookup"><span data-stu-id="f409b-122">This object can be inherited and its members redefined.</span></span> <span data-ttu-id="f409b-123">Это позволит вам настроить API для загрузки и распаковки собственных пользовательских форматов файлов.</span><span class="sxs-lookup"><span data-stu-id="f409b-123">Doing so would enable you to customize the API for loading and decompressing your own custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="f409b-124">Требования</span><span class="sxs-lookup"><span data-stu-id="f409b-124">Requirements</span></span>



| <span data-ttu-id="f409b-125">Требование</span><span class="sxs-lookup"><span data-stu-id="f409b-125">Requirement</span></span> | <span data-ttu-id="f409b-126">Значение</span><span class="sxs-lookup"><span data-stu-id="f409b-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f409b-127">Header</span><span class="sxs-lookup"><span data-stu-id="f409b-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f409b-128"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="f409b-128"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f409b-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f409b-129">Library</span></span><br/> | <dl> <span data-ttu-id="f409b-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f409b-130"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f409b-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f409b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f409b-132">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="f409b-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
