---
description: Интерфейс ID3DXPRTBuffer используется в качестве буфера данных для хранения данных вершин и точек для использования с предварительно вычисленными методами и функциями пересчета радианце (PRT).
ms.assetid: 36c1fd13-0949-4991-93cb-41ace458802d
title: Интерфейс ID3DXPRTBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: daadb5b0ad8155062e75ea4eca566a0afbf3631b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105704021"
---
# <a name="id3dxprtbuffer-interface"></a><span data-ttu-id="3fae9-103">Интерфейс ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="3fae9-103">ID3DXPRTBuffer interface</span></span>

<span data-ttu-id="3fae9-104">Интерфейс ID3DXPRTBuffer используется в качестве буфера данных для хранения данных вершин и точек для использования с предварительно вычисленными методами и функциями пересчета радианце (PRT).</span><span class="sxs-lookup"><span data-stu-id="3fae9-104">The ID3DXPRTBuffer interface is used as a data buffer to store vertex and pixel data for use with precomputed radiance transfer (PRT) methods and functions.</span></span>

## <a name="members"></a><span data-ttu-id="3fae9-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="3fae9-105">Members</span></span>

<span data-ttu-id="3fae9-106">Интерфейс **ID3DXPRTBuffer** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3fae9-106">The **ID3DXPRTBuffer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3fae9-107">**ID3DXPRTBuffer** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3fae9-107">**ID3DXPRTBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="3fae9-108">Методы</span><span class="sxs-lookup"><span data-stu-id="3fae9-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3fae9-109">Методы</span><span class="sxs-lookup"><span data-stu-id="3fae9-109">Methods</span></span>

<span data-ttu-id="3fae9-110">Интерфейс **ID3DXPRTBuffer** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="3fae9-110">The **ID3DXPRTBuffer** interface has these methods.</span></span>



| <span data-ttu-id="3fae9-111">Метод</span><span class="sxs-lookup"><span data-stu-id="3fae9-111">Method</span></span>                                                   | <span data-ttu-id="3fae9-112">Описание</span><span class="sxs-lookup"><span data-stu-id="3fae9-112">Description</span></span>                                                                                                                                                                                   |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3fae9-113">**аддбуффер**</span><span class="sxs-lookup"><span data-stu-id="3fae9-113">**AddBuffer**</span></span>](id3dxprtbuffer--addbuffer.md)           | <span data-ttu-id="3fae9-114">Добавляет еще один буфер в **ID3DXPRTBuffer** и сохраняет результаты в **ID3DXPRTBuffer**.</span><span class="sxs-lookup"><span data-stu-id="3fae9-114">Adds another buffer to the **ID3DXPRTBuffer** and stores the results in **ID3DXPRTBuffer**.</span></span><br/>                                                                                        |
| [<span data-ttu-id="3fae9-115">**аттачгх**</span><span class="sxs-lookup"><span data-stu-id="3fae9-115">**AttachGH**</span></span>](id3dxprtbuffer--attachgh.md)             | <span data-ttu-id="3fae9-116">Связывает объект [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) с объектом **ID3DXPRTBuffer** .</span><span class="sxs-lookup"><span data-stu-id="3fae9-116">Associates an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object with the **ID3DXPRTBuffer** object.</span></span><br/>                                                              |
| [<span data-ttu-id="3fae9-117">**евалгх**</span><span class="sxs-lookup"><span data-stu-id="3fae9-117">**EvalGH**</span></span>](id3dxprtbuffer--evalgh.md)                 | <span data-ttu-id="3fae9-118">Применяет сохраненные данные для переплета текстуры в буфер текстуры **ID3DXPRTBuffer** .</span><span class="sxs-lookup"><span data-stu-id="3fae9-118">Applies stored texture gutter data to an **ID3DXPRTBuffer** texture buffer.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="3fae9-119">**екстракттекстуре**</span><span class="sxs-lookup"><span data-stu-id="3fae9-119">**ExtractTexture**</span></span>](id3dxprtbuffer--extracttexture.md) | <span data-ttu-id="3fae9-120">Извлекает данные коэффициента из цветового канала буфера для указанного диапазона коэффициентов и добавляет данные в объект [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .</span><span class="sxs-lookup"><span data-stu-id="3fae9-120">Extracts coefficient data from a color channel of the buffer for a specified range of coefficients, and adds the data to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object.</span></span><br/> |
| [<span data-ttu-id="3fae9-121">**екстракттомеш**</span><span class="sxs-lookup"><span data-stu-id="3fae9-121">**ExtractToMesh**</span></span>](id3dxprtbuffer--extracttomesh.md)   | <span data-ttu-id="3fae9-122">Извлекает коэффициенты из одноканального буфера и добавляет данные в объект [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="3fae9-122">Extracts coefficient data from a single-channel buffer and adds the data to an [**ID3DXMesh**](id3dxmesh.md) object.</span></span><br/>                                                              |
| [<span data-ttu-id="3fae9-123">**Высота**</span><span class="sxs-lookup"><span data-stu-id="3fae9-123">**GetHeight**</span></span>](id3dxprtbuffer--getheight.md)           | <span data-ttu-id="3fae9-124">Получает высоту текстуры в пикселях.</span><span class="sxs-lookup"><span data-stu-id="3fae9-124">Retrieves the height of the texture, in pixels.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="3fae9-125">**жетнумчаннелс**</span><span class="sxs-lookup"><span data-stu-id="3fae9-125">**GetNumChannels**</span></span>](id3dxprtbuffer--getnumchannels.md) | <span data-ttu-id="3fae9-126">Возвращает количество цветовых каналов, используемых в памяти для хранения образцов.</span><span class="sxs-lookup"><span data-stu-id="3fae9-126">Retrieves the number of color channels used in memory to store samples.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="3fae9-127">**жетнумкоеффс**</span><span class="sxs-lookup"><span data-stu-id="3fae9-127">**GetNumCoeffs**</span></span>](id3dxprtbuffer--getnumcoeffs.md)     | <span data-ttu-id="3fae9-128">Возвращает число скаляров на цветовой канал, используемый в памяти для хранения выборок.</span><span class="sxs-lookup"><span data-stu-id="3fae9-128">Retrieves the number of scalars per color channel used in memory to store samples.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="3fae9-129">**жетнумсамплес**</span><span class="sxs-lookup"><span data-stu-id="3fae9-129">**GetNumSamples**</span></span>](id3dxprtbuffer--getnumsamples.md)   | <span data-ttu-id="3fae9-130">Возвращает число вершин (или пикселей текстуры) выборки.</span><span class="sxs-lookup"><span data-stu-id="3fae9-130">Retrieves the number of vertices (or texels) sampled.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="3fae9-131">**Полуширинные**</span><span class="sxs-lookup"><span data-stu-id="3fae9-131">**GetWidth**</span></span>](id3dxprtbuffer--getwidth.md)             | <span data-ttu-id="3fae9-132">Получает ширину текстуры в пикселях.</span><span class="sxs-lookup"><span data-stu-id="3fae9-132">Retrieves the width of the texture, in pixels.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="3fae9-133">**«Текстурирование»**</span><span class="sxs-lookup"><span data-stu-id="3fae9-133">**IsTexture**</span></span>](id3dxprtbuffer--istexture.md)           | <span data-ttu-id="3fae9-134">Указывает, содержит ли буфер текстуру.</span><span class="sxs-lookup"><span data-stu-id="3fae9-134">Indicates whether the buffer contains a texture.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="3fae9-135">**локкбуффер**</span><span class="sxs-lookup"><span data-stu-id="3fae9-135">**LockBuffer**</span></span>](id3dxprtbuffer--lockbuffer.md)         | <span data-ttu-id="3fae9-136">Блокирует диапазон демонстрационных данных вершин или шаг текселя и получает указатель на расположение в буферной памяти.</span><span class="sxs-lookup"><span data-stu-id="3fae9-136">Locks a range of vertex or texel sample data and obtains a pointer to the location in buffer memory.</span></span><br/>                                                                               |
| [<span data-ttu-id="3fae9-137">**релеасегх**</span><span class="sxs-lookup"><span data-stu-id="3fae9-137">**ReleaseGH**</span></span>](id3dxprtbuffer--releasegh.md)           | <span data-ttu-id="3fae9-138">Отменяет связь присоединенного объекта [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) с объектом **ID3DXPRTBuffer** .</span><span class="sxs-lookup"><span data-stu-id="3fae9-138">Unassociates an attached [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object with the **ID3DXPRTBuffer** object.</span></span><br/>                                                   |
| [<span data-ttu-id="3fae9-139">**Изменить размер**</span><span class="sxs-lookup"><span data-stu-id="3fae9-139">**Resize**</span></span>](id3dxprtbuffer--resize.md)                 | <span data-ttu-id="3fae9-140">Изменяет число выборок, содержащихся в буфере.</span><span class="sxs-lookup"><span data-stu-id="3fae9-140">Changes the number of samples contained in the buffer.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="3fae9-141">**скалебуффер**</span><span class="sxs-lookup"><span data-stu-id="3fae9-141">**ScaleBuffer**</span></span>](id3dxprtbuffer--scalebuffer.md)       | <span data-ttu-id="3fae9-142">Умножает каждое значение в буфере на постоянное значение.</span><span class="sxs-lookup"><span data-stu-id="3fae9-142">Multiplies every value in the buffer by a constant value.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="3fae9-143">**унлоккбуффер**</span><span class="sxs-lookup"><span data-stu-id="3fae9-143">**UnlockBuffer**</span></span>](id3dxprtbuffer--unlockbuffer.md)     | <span data-ttu-id="3fae9-144">Завершает срок существования указателя Ппдата, возвращенного [**ID3DXPRTBuffer:: локкбуффер**](id3dxprtbuffer--lockbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="3fae9-144">Ends the lifespan of the ppData pointer returned by [**ID3DXPRTBuffer::LockBuffer**](id3dxprtbuffer--lockbuffer.md).</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="3fae9-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3fae9-145">Remarks</span></span>

<span data-ttu-id="3fae9-146">Интерфейс **ID3DXPRTBuffer** получается путем вызова функций [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) или [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) .</span><span class="sxs-lookup"><span data-stu-id="3fae9-146">The **ID3DXPRTBuffer** interface is obtained by calling the [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) or [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) functions.</span></span>

<span data-ttu-id="3fae9-147">Тип LPD3DXPRTBUFFER определяется как указатель на интерфейс **ID3DXPRTBuffer** .</span><span class="sxs-lookup"><span data-stu-id="3fae9-147">The LPD3DXPRTBUFFER type is defined as a pointer to the **ID3DXPRTBuffer** interface.</span></span>


```
typedef interface ID3DXPRTBuffer ID3DXPRTBuffer;
typedef interface ID3DXPRTBuffer *LPD3DXPRTBUFFER;
```



## <a name="requirements"></a><span data-ttu-id="3fae9-148">Требования</span><span class="sxs-lookup"><span data-stu-id="3fae9-148">Requirements</span></span>



| <span data-ttu-id="3fae9-149">Требование</span><span class="sxs-lookup"><span data-stu-id="3fae9-149">Requirement</span></span> | <span data-ttu-id="3fae9-150">Значение</span><span class="sxs-lookup"><span data-stu-id="3fae9-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3fae9-151">Header</span><span class="sxs-lookup"><span data-stu-id="3fae9-151">Header</span></span><br/>  | <dl> <span data-ttu-id="3fae9-152"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fae9-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3fae9-153">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3fae9-153">Library</span></span><br/> | <dl> <span data-ttu-id="3fae9-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3fae9-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3fae9-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3fae9-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fae9-156">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="3fae9-156">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[<span data-ttu-id="3fae9-157">**D3DXCreatePRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="3fae9-157">**D3DXCreatePRTBuffer**</span></span>](d3dxcreateprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="3fae9-158">**D3DXCreatePRTBufferTex**</span><span class="sxs-lookup"><span data-stu-id="3fae9-158">**D3DXCreatePRTBufferTex**</span></span>](d3dxcreateprtbuffertex.md)
</dt> <dt>

[<span data-ttu-id="3fae9-159">**ID3DXPRTCompBuffer**</span><span class="sxs-lookup"><span data-stu-id="3fae9-159">**ID3DXPRTCompBuffer**</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
