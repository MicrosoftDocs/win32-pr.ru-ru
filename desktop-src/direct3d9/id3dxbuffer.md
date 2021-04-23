---
description: Интерфейс ID3DXBuffer используется в качестве буфера данных, сохраняя сведения о вершинах, соседях и материалах во время оптимизации сетки и операций загрузки.
ms.assetid: 63ee3b2d-c0e6-4ad4-9274-2b1dfd77f89d
title: Интерфейс ID3DXBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5fff273d2e38daeb003fb360f099e7a7b4985504
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674709"
---
# <a name="id3dxbuffer-interface"></a><span data-ttu-id="87464-103">Интерфейс ID3DXBuffer</span><span class="sxs-lookup"><span data-stu-id="87464-103">ID3DXBuffer interface</span></span>

<span data-ttu-id="87464-104">Интерфейс ID3DXBuffer используется в качестве буфера данных, сохраняя сведения о вершинах, соседях и материалах во время оптимизации сетки и операций загрузки.</span><span class="sxs-lookup"><span data-stu-id="87464-104">The ID3DXBuffer interface is used as a data buffer, storing vertex, adjacency, and material information during mesh optimization and loading operations.</span></span> <span data-ttu-id="87464-105">Объект buffer используется для возврата произвольных данных о длине.</span><span class="sxs-lookup"><span data-stu-id="87464-105">The buffer object is used to return arbitrary length data.</span></span> <span data-ttu-id="87464-106">Кроме того, объекты буфера используются для возврата объектного кода и сообщений об ошибках в методах, собирающих шейдеры вершин и пикселей.</span><span class="sxs-lookup"><span data-stu-id="87464-106">Also, buffer objects are used to return object code and error messages in methods that assemble vertex and pixel shaders.</span></span>

## <a name="members"></a><span data-ttu-id="87464-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="87464-107">Members</span></span>

<span data-ttu-id="87464-108">Интерфейс **ID3DXBuffer** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="87464-108">The **ID3DXBuffer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="87464-109">**ID3DXBuffer** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="87464-109">**ID3DXBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="87464-110">Методы</span><span class="sxs-lookup"><span data-stu-id="87464-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="87464-111">Методы</span><span class="sxs-lookup"><span data-stu-id="87464-111">Methods</span></span>

<span data-ttu-id="87464-112">Интерфейс **ID3DXBuffer** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="87464-112">The **ID3DXBuffer** interface has these methods.</span></span>



| <span data-ttu-id="87464-113">Метод</span><span class="sxs-lookup"><span data-stu-id="87464-113">Method</span></span>                                                    | <span data-ttu-id="87464-114">Описание</span><span class="sxs-lookup"><span data-stu-id="87464-114">Description</span></span>                                                    |
|:----------------------------------------------------------|:---------------------------------------------------------------|
| [<span data-ttu-id="87464-115">**жетбуфферпоинтер**</span><span class="sxs-lookup"><span data-stu-id="87464-115">**GetBufferPointer**</span></span>](id3dxbuffer--getbufferpointer.md) | <span data-ttu-id="87464-116">Извлекает указатель на данные в буфере.</span><span class="sxs-lookup"><span data-stu-id="87464-116">Retrieves a pointer to the data in the buffer.</span></span><br/>      |
| [<span data-ttu-id="87464-117">**жетбуфферсизе**</span><span class="sxs-lookup"><span data-stu-id="87464-117">**GetBufferSize**</span></span>](id3dxbuffer--getbuffersize.md)       | <span data-ttu-id="87464-118">Возвращает общий размер данных в буфере.</span><span class="sxs-lookup"><span data-stu-id="87464-118">Retrieves the total size of the data in the buffer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="87464-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87464-119">Remarks</span></span>

<span data-ttu-id="87464-120">Интерфейс **ID3DXBuffer** получается путем вызова функции [**D3DXCreateBuffer**](d3dxcreatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="87464-120">The **ID3DXBuffer** interface is obtained by calling the [**D3DXCreateBuffer**](d3dxcreatebuffer.md) function.</span></span>

<span data-ttu-id="87464-121">Тип LPD3DXBUFFER определяется как указатель на интерфейс **ID3DXBuffer** .</span><span class="sxs-lookup"><span data-stu-id="87464-121">The LPD3DXBUFFER type is defined as a pointer to the **ID3DXBuffer** interface.</span></span>


```
typedef interface ID3DXBuffer ID3DXBuffer;
typedef interface ID3DXBuffer *LPD3DXBUFFER;
```



## <a name="requirements"></a><span data-ttu-id="87464-122">Требования</span><span class="sxs-lookup"><span data-stu-id="87464-122">Requirements</span></span>



| <span data-ttu-id="87464-123">Требование</span><span class="sxs-lookup"><span data-stu-id="87464-123">Requirement</span></span> | <span data-ttu-id="87464-124">Значение</span><span class="sxs-lookup"><span data-stu-id="87464-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="87464-125">Header</span><span class="sxs-lookup"><span data-stu-id="87464-125">Header</span></span><br/>  | <dl> <span data-ttu-id="87464-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="87464-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="87464-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="87464-127">Library</span></span><br/> | <dl> <span data-ttu-id="87464-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87464-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="87464-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87464-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87464-130">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="87464-130">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
