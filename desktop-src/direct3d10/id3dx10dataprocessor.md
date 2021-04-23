---
description: Объект обработки данных, используемый интерфейсом ID3DX10ThreadPump для асинхронной обработки загруженных данных.
ms.assetid: c932f558-10da-45fc-a833-8ed86fa065ab
title: Интерфейс ID3DX10DataProcessor (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataProcessor
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: de573e50a1442396df78dd6a3c8f0bd09c1cbf6d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914831"
---
# <a name="id3dx10dataprocessor-interface"></a><span data-ttu-id="a7f9e-103">Интерфейс ID3DX10DataProcessor</span><span class="sxs-lookup"><span data-stu-id="a7f9e-103">ID3DX10DataProcessor interface</span></span>

<span data-ttu-id="a7f9e-104">Объект обработки данных, используемый [**интерфейсом ID3DX10ThreadPump**](id3dx10threadpump.md) для асинхронной обработки загруженных данных.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-104">Data processing object used by [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) for processing loaded data asynchronously.</span></span>

## <a name="members"></a><span data-ttu-id="a7f9e-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="a7f9e-105">Members</span></span>

<span data-ttu-id="a7f9e-106">Интерфейс **ID3DX10DataProcessor** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a7f9e-106">The **ID3DX10DataProcessor** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a7f9e-107">**ID3DX10DataProcessor** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a7f9e-107">**ID3DX10DataProcessor** also has these types of members:</span></span>

-   [<span data-ttu-id="a7f9e-108">Методы</span><span class="sxs-lookup"><span data-stu-id="a7f9e-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a7f9e-109">Методы</span><span class="sxs-lookup"><span data-stu-id="a7f9e-109">Methods</span></span>

<span data-ttu-id="a7f9e-110">Интерфейс **ID3DX10DataProcessor** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-110">The **ID3DX10DataProcessor** interface has these methods.</span></span>



| <span data-ttu-id="a7f9e-111">Метод</span><span class="sxs-lookup"><span data-stu-id="a7f9e-111">Method</span></span>                                                                | <span data-ttu-id="a7f9e-112">Описание</span><span class="sxs-lookup"><span data-stu-id="a7f9e-112">Description</span></span>                                                                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a7f9e-113">**креатедевицеобжект**</span><span class="sxs-lookup"><span data-stu-id="a7f9e-113">**CreateDeviceObject**</span></span>](id3dx10dataprocessor-createdeviceobject.md) | <span data-ttu-id="a7f9e-114">Создайте объект устройства.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-114">Create a device object.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="a7f9e-115">**Завершить**</span><span class="sxs-lookup"><span data-stu-id="a7f9e-115">**Destroy**</span></span>](id3dx10dataprocessor-destroy.md)                       | <span data-ttu-id="a7f9e-116">Используется [**интерфейсом ID3DX10ThreadPump**](id3dx10threadpump.md) для уничтожения процессора после завершения рабочего элемента.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-116">Used by a [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) to destroy the processor after a work item completes.</span></span><br/> |
| [<span data-ttu-id="a7f9e-117">**Процесс**</span><span class="sxs-lookup"><span data-stu-id="a7f9e-117">**Process**</span></span>](id3dx10dataprocessor-process.md)                       | <span data-ttu-id="a7f9e-118">Обработка некоторых данных.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-118">Process some data.</span></span><br/>                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="a7f9e-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a7f9e-119">Remarks</span></span>

<span data-ttu-id="a7f9e-120">Этот объект может быть унаследован и его члены переопределены.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-120">This object can be inherited and its members redefined.</span></span> <span data-ttu-id="a7f9e-121">Это позволит настроить API для обработки собственных пользовательских форматов файлов.</span><span class="sxs-lookup"><span data-stu-id="a7f9e-121">Doing so would enable you to customize the API for processing your own custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7f9e-122">Требования</span><span class="sxs-lookup"><span data-stu-id="a7f9e-122">Requirements</span></span>



| <span data-ttu-id="a7f9e-123">Требование</span><span class="sxs-lookup"><span data-stu-id="a7f9e-123">Requirement</span></span> | <span data-ttu-id="a7f9e-124">Значение</span><span class="sxs-lookup"><span data-stu-id="a7f9e-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a7f9e-125">Header</span><span class="sxs-lookup"><span data-stu-id="a7f9e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a7f9e-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7f9e-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="a7f9e-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a7f9e-127">Library</span></span><br/> | <dl> <span data-ttu-id="a7f9e-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7f9e-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7f9e-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a7f9e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7f9e-130">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="a7f9e-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
