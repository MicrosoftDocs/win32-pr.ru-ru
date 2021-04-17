---
title: Структура CD3DX12_GPU_DESCRIPTOR_HANDLE (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию \_ \_ \_ структуры дескриптора GPU D3D12.
ms.assetid: 6E405AD6-D370-4B87-849A-C52D64C79BF7
keywords:
- Структура CD3DX12_GPU_DESCRIPTOR_HANDLE
topic_type:
- apiref
api_name:
- CD3DX12_GPU_DESCRIPTOR_HANDLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429d41d401b7d3e928bc4ab76850b36ae41b1e8a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703679"
---
# <a name="cd3dx12_gpu_descriptor_handle-structure"></a><span data-ttu-id="cbacb-104">\_ \_ \_ Структура ДЕСКРИПТОРа GPU CD3DX12</span><span class="sxs-lookup"><span data-stu-id="cbacb-104">CD3DX12\_GPU\_DESCRIPTOR\_HANDLE structure</span></span>

<span data-ttu-id="cbacb-105">Вспомогательная структура, позволяющая упростить инициализацию [**структуры \_ \_ \_ дескриптора GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) .</span><span class="sxs-lookup"><span data-stu-id="cbacb-105">A helper structure to enable easy initialization of a [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbacb-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cbacb-106">Syntax</span></span>


```C++
struct CD3DX12_GPU_DESCRIPTOR_HANDLE  : public D3D12_GPU_DESCRIPTOR_HANDLE{
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE();
                                  explicit CD3DX12_GPU_DESCRIPTOR_HANDLE(const D3D12_GPU_DESCRIPTOR_HANDLE &o);
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE(CD3DX12_DEFAULT);
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE(const D3D12_GPU_DESCRIPTOR_HANDLE &other, INT offsetScaledByIncrementSize);
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE(const D3D12_GPU_DESCRIPTOR_HANDLE &other, INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_GPU_DESCRIPTOR_HANDLE&  Offset(INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_GPU_DESCRIPTOR_HANDLE&  Offset(INT offsetScaledByIncrementSize);
  bool                            inline operator==( _In_ const D3D12_GPU_DESCRIPTOR_HANDLE& other) const;
  bool                            inline operator!=( _In_ const D3D12_GPU_DESCRIPTOR_HANDLE& other) const;
  CD3DX12_GPU_DESCRIPTOR_HANDLE & operator=(const D3D12_GPU_DESCRIPTOR_HANDLE &other);
  void                            inline InitOffsetted(_In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            inline InitOffsetted(_In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_GPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_GPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
};
```



## <a name="members"></a><span data-ttu-id="cbacb-107">Члены</span><span class="sxs-lookup"><span data-stu-id="cbacb-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="cbacb-108">**\_Дескриптор CD3DX12 \_ GPU \_ ()**</span><span class="sxs-lookup"><span data-stu-id="cbacb-108">**CD3DX12\_GPU\_DESCRIPTOR\_HANDLE()**</span></span>
</dt> <dd>

<span data-ttu-id="cbacb-109">Создает новый, неинициализированный экземпляр \_ \_ \_ дескриптора CD3DX12 GPU.</span><span class="sxs-lookup"><span data-stu-id="cbacb-109">Creates a new, uninitialized, instance of a CD3DX12\_GPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="cbacb-110">**явный дескриптор \_ GPU \_ CD3DX12 \_ (константа дескриптора gpu const D3D12 \_ \_ \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="cbacb-110">**explicit CD3DX12\_GPU\_DESCRIPTOR\_HANDLE(const D3D12\_GPU\_DESCRIPTOR\_HANDLE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="cbacb-111">Создает новый экземпляр \_ \_ дескриптора дескриптора GPU CD3DX12 \_ , инициализированного с содержимым другой структуры [**\_ \_ \_ дескриптора GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) .</span><span class="sxs-lookup"><span data-stu-id="cbacb-111">Creates a new instance of a CD3DX12\_GPU\_DESCRIPTOR\_HANDLE, initialized with the contents of another [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cbacb-112">**\_Дескриптор CD3DX12 \_ GPU \_ ( \_ по умолчанию CD3DX12)**</span><span class="sxs-lookup"><span data-stu-id="cbacb-112">**CD3DX12\_GPU\_DESCRIPTOR\_HANDLE(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="cbacb-113">Создает новый экземпляр \_ \_ дескриптора дескриптора GPU CD3DX12 \_ , инициализируемый параметрами по умолчанию (устанавливает указатель на нуль).</span><span class="sxs-lookup"><span data-stu-id="cbacb-113">Creates a new instance of a CD3DX12\_GPU\_DESCRIPTOR\_HANDLE, initialized with default parameters (sets the pointer to zero).</span></span>

</dd> <dt>

<span data-ttu-id="cbacb-114">**Дескриптор \_ GPU \_ CD3DX12 \_ (константа дескриптора gpu const D3D12 \_ \_ \_ &other, int оффсетскаледбинкрементсизе)**</span><span class="sxs-lookup"><span data-stu-id="cbacb-114">**CD3DX12\_GPU\_DESCRIPTOR\_HANDLE(const D3D12\_GPU\_DESCRIPTOR\_HANDLE &other, INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="cbacb-115">Создает новый экземпляр \_ \_ дескриптора дескриптора GPU CD3DX12 \_ , инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="cbacb-115">Creates a new instance of a CD3DX12\_GPU\_DESCRIPTOR\_HANDLE, initializing the following parameters:</span></span>

<span data-ttu-id="cbacb-116">\_Дескриптор GPU \_ D3D12 \_ &другой</span><span class="sxs-lookup"><span data-stu-id="cbacb-116">D3D12\_GPU\_DESCRIPTOR\_HANDLE &other</span></span>

<span data-ttu-id="cbacb-117">INT Оффсетскаледбинкрементсизе: число инкрементов, на которое смещается смещение.</span><span class="sxs-lookup"><span data-stu-id="cbacb-117">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="cbacb-118">**Дескриптор \_ GPU \_ CD3DX12 \_ (константа дескриптора gpu const D3D12 \_ \_ \_ &other, int оффсетиндескрипторс, uint дескрипторинкрементсизе)**</span><span class="sxs-lookup"><span data-stu-id="cbacb-118">**CD3DX12\_GPU\_DESCRIPTOR\_HANDLE(const D3D12\_GPU\_DESCRIPTOR\_HANDLE &other, INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="cbacb-119">Создает новый экземпляр \_ \_ дескриптора дескриптора GPU CD3DX12 \_ , инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="cbacb-119">Creates a new instance of a CD3DX12\_GPU\_DESCRIPTOR\_HANDLE, initializing the following parameters:</span></span>

<span data-ttu-id="cbacb-120">\_Дескриптор GPU \_ D3D12 \_ &другой</span><span class="sxs-lookup"><span data-stu-id="cbacb-120">D3D12\_GPU\_DESCRIPTOR\_HANDLE &other</span></span>

<span data-ttu-id="cbacb-121">INT Оффсетиндескрипторс: количество дескрипторов, с помощью которых увеличивается значение.</span><span class="sxs-lookup"><span data-stu-id="cbacb-121">INT offsetInDescriptors: The number of descriptors by which to increment.</span></span>

<span data-ttu-id="cbacb-122">UINT Дескрипторинкрементсизе: величина приращения для каждого дескриптора, включая заполнение.</span><span class="sxs-lookup"><span data-stu-id="cbacb-122">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> <dt>

<span data-ttu-id="cbacb-123">**Offset (INT Оффсетиндескрипторс, UINT Дескрипторинкрементсизе)**</span><span class="sxs-lookup"><span data-stu-id="cbacb-123">**Offset(INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="cbacb-124">Задает смещение на основе указанного числа дескрипторов и величины приращения каждого из них.</span><span class="sxs-lookup"><span data-stu-id="cbacb-124">Sets the offset based on the specified number of descriptors and how much to increment for each descriptor.</span></span> <span data-ttu-id="cbacb-125">Использует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="cbacb-125">Uses the following parameters:</span></span>

<span data-ttu-id="cbacb-126">INT Оффсетиндескрипторс: количество дескрипторов, с помощью которых увеличивается значение.</span><span class="sxs-lookup"><span data-stu-id="cbacb-126">INT offsetInDescriptors: The number of descriptors by which to increment.</span></span>

<span data-ttu-id="cbacb-127">UINT Дескрипторинкрементсизе: величина приращения для каждого дескриптора, включая заполнение.</span><span class="sxs-lookup"><span data-stu-id="cbacb-127">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> <dt>

<span data-ttu-id="cbacb-128">**Offset (INT Оффсетскаледбинкрементсизе)**</span><span class="sxs-lookup"><span data-stu-id="cbacb-128">**Offset(INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="cbacb-129">Задает смещение на основе указанного числа приращений.</span><span class="sxs-lookup"><span data-stu-id="cbacb-129">Sets the offset based on the specified number of increments.</span></span> <span data-ttu-id="cbacb-130">Использует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="cbacb-130">Uses the following parameters:</span></span>

<span data-ttu-id="cbacb-131">INT Оффсетскаледбинкрементсизе: число инкрементов, на которое смещается смещение.</span><span class="sxs-lookup"><span data-stu-id="cbacb-131">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="cbacb-132">**встроенный оператор = = ( \_ в \_ константе дескриптора \_ GPU D3D12 \_ \_& Other) const**</span><span class="sxs-lookup"><span data-stu-id="cbacb-132">**inline operator==( \_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE& other) const**</span></span>
</dt> <dd>

<span data-ttu-id="cbacb-133">Проверяет на равенство между текущим \_ дескриптором CD3DX12 GPU и заданным дескриптором дескриптора \_ \_ GPU D3D12 или дескриптором \_ \_ \_ CD3DX12 \_ \_ \_ маркера GPU.</span><span class="sxs-lookup"><span data-stu-id="cbacb-133">Tests for equality between the current CD3DX12\_GPU\_DESCRIPTOR\_HANDLE and the specified D3D12\_GPU\_DESCRIPTOR\_HANDLE or CD3DX12\_GPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="cbacb-134">**встроенный оператор! = ( \_ в const D3D12 дескриптора GPU дескриптора \_ \_ \_ \_& Other) const**</span><span class="sxs-lookup"><span data-stu-id="cbacb-134">**inline operator!=( \_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE& other) const**</span></span>
</dt> <dd>

<span data-ttu-id="cbacb-135">Проверяет наличие неравенства между текущим \_ дескриптором CD3DX12 GPU \_ и заданным дескриптором дескриптора \_ GPU D3D12 или дескриптором \_ \_ \_ CD3DX12 \_ \_ \_ маркера GPU.</span><span class="sxs-lookup"><span data-stu-id="cbacb-135">Tests for inequality between the current CD3DX12\_GPU\_DESCRIPTOR\_HANDLE and the specified D3D12\_GPU\_DESCRIPTOR\_HANDLE or CD3DX12\_GPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="cbacb-136">**operator = (const D3D12 дескриптор GPU дескриптора \_ графического процессора \_ \_ &Other)**</span><span class="sxs-lookup"><span data-stu-id="cbacb-136">**operator=(const D3D12\_GPU\_DESCRIPTOR\_HANDLE &other)**</span></span>
</dt> <dd>

<span data-ttu-id="cbacb-137">Задает \_ \_ дескриптору текущего дескриптора GPU CD3DX12 \_ те же значения, что и указанный \_ дескриптор D3D12 или дескриптор GPU \_ \_ CD3DX12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cbacb-137">Sets the current CD3DX12\_GPU\_DESCRIPTOR\_HANDLE to the same values as the specified D3D12\_GPU\_DESCRIPTOR\_HANDLE or CD3DX12\_GPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="cbacb-138">**Встроенный Инитоффсеттед ( \_ в \_ \_ \_ дескрипторе дескриптора GPU const D3D12 \_ &Base, int оффсетскаледбинкрементсизе)**</span><span class="sxs-lookup"><span data-stu-id="cbacb-138">**inline InitOffsetted(\_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base, INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="cbacb-139">Инициализирует структуру [**\_ \_ \_ дескриптора GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) с указанным числом элементов.</span><span class="sxs-lookup"><span data-stu-id="cbacb-139">Initializes a [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure with the specified number of items.</span></span> <span data-ttu-id="cbacb-140">Использует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="cbacb-140">Uses the following parameters:</span></span>

<span data-ttu-id="cbacb-141">\_В \_ const D3D12 дескриптора GPU дескриптора \_ \_ \_ &Base: базовый адрес, по которому производится смещение.</span><span class="sxs-lookup"><span data-stu-id="cbacb-141">\_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="cbacb-142">INT Оффсетскаледбинкрементсизе: число инкрементов, на которое смещается смещение.</span><span class="sxs-lookup"><span data-stu-id="cbacb-142">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="cbacb-143">**Встроенный Инитоффсеттед ( \_ в \_ \_ \_ дескрипторе дескриптора GPU const D3D12 \_ &Base, int оффсетиндескрипторс, uint дескрипторинкрементсизе)**</span><span class="sxs-lookup"><span data-stu-id="cbacb-143">**inline InitOffsetted(\_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="cbacb-144">Инициализирует структуру [**\_ \_ \_ дескриптора GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) со смещением, используя указанное число дескрипторов заданного размера.</span><span class="sxs-lookup"><span data-stu-id="cbacb-144">Initializes a [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure with an offset, using the specified number of descriptors of the given size.</span></span> <span data-ttu-id="cbacb-145">Использует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="cbacb-145">Uses the following parameters:</span></span>

<span data-ttu-id="cbacb-146">\_В \_ const D3D12 дескриптора GPU дескриптора \_ \_ \_ &Base: базовый адрес, по которому производится смещение.</span><span class="sxs-lookup"><span data-stu-id="cbacb-146">\_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="cbacb-147">INT Оффсетиндескрипторс: количество дескрипторов, по которым производится смещение.</span><span class="sxs-lookup"><span data-stu-id="cbacb-147">INT offsetInDescriptors: The number of descriptors by which to offset.</span></span>

<span data-ttu-id="cbacb-148">UINT Дескрипторинкрементсизе: величина приращения для каждого дескриптора, включая заполнение.</span><span class="sxs-lookup"><span data-stu-id="cbacb-148">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> <dt>

<span data-ttu-id="cbacb-149">**статический встроенный Инитоффсеттед ( \_ out D3D12 Handle дескриптор \_ gpu дескриптор \_ \_ \_ &, в константном дескрипторе дескриптора \_ \_ \_ GPU D3D12 \_ \_ &Base, int оффсетскаледбинкрементсизе)**</span><span class="sxs-lookup"><span data-stu-id="cbacb-149">**static inline InitOffsetted(\_Out\_ D3D12\_GPU\_DESCRIPTOR\_HANDLE &handle, \_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base, INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="cbacb-150">Инициализирует структуру [**\_ \_ \_ дескриптора GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) со смещением, используя указанное число дескрипторов заданного размера.</span><span class="sxs-lookup"><span data-stu-id="cbacb-150">Initializes a [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure with an offset, using the specified number of descriptors of the given size.</span></span> <span data-ttu-id="cbacb-151">Использует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="cbacb-151">Uses the following parameters:</span></span>

<span data-ttu-id="cbacb-152">\_Выходной дескриптор GPU дескриптора D3D12 дескриптора \_ \_ \_ \_ &: выводит полученный \_ дескриптор GPU D3D12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cbacb-152">\_Out\_ D3D12\_GPU\_DESCRIPTOR\_HANDLE &handle: Outputs the resulting D3D12\_GPU\_DESCRIPTOR\_HANDLE.</span></span>

<span data-ttu-id="cbacb-153">\_В \_ const D3D12 дескриптора GPU дескриптора \_ \_ \_ &Base: базовый адрес, по которому производится смещение.</span><span class="sxs-lookup"><span data-stu-id="cbacb-153">\_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="cbacb-154">INT Оффсетскаледбинкрементсизе: число инкрементов, на которое смещается смещение.</span><span class="sxs-lookup"><span data-stu-id="cbacb-154">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="cbacb-155">**статический встроенный Инитоффсеттед ( \_ out D3D12 Handle дескриптор \_ \_ GPU \_ \_ &дескриптор, в дескрипторе \_ \_ \_ \_ маркера GPU D3D12 \_ &Base, int оффсетиндескрипторс, uint дескрипторинкрементсизе)**</span><span class="sxs-lookup"><span data-stu-id="cbacb-155">**static inline InitOffsetted(\_Out\_ D3D12\_GPU\_DESCRIPTOR\_HANDLE &handle, \_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="cbacb-156">Инициализирует структуру [**\_ \_ \_ дескриптора GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) со смещением, используя указанное число дескрипторов заданного размера.</span><span class="sxs-lookup"><span data-stu-id="cbacb-156">Initializes a [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure with an offset, using the specified number of descriptors of the given size.</span></span> <span data-ttu-id="cbacb-157">Использует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="cbacb-157">Uses the following parameters:</span></span>

<span data-ttu-id="cbacb-158">\_Выходной дескриптор GPU дескриптора D3D12 дескриптора \_ \_ \_ \_ &: выводит полученный \_ дескриптор GPU D3D12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cbacb-158">\_Out\_ D3D12\_GPU\_DESCRIPTOR\_HANDLE &handle: Outputs the resulting D3D12\_GPU\_DESCRIPTOR\_HANDLE.</span></span>

<span data-ttu-id="cbacb-159">\_В \_ const D3D12 дескриптора GPU дескриптора \_ \_ \_ &Base: базовый адрес, по которому производится смещение.</span><span class="sxs-lookup"><span data-stu-id="cbacb-159">\_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="cbacb-160">INT Оффсетиндескрипторс: количество дескрипторов, по которым производится смещение.</span><span class="sxs-lookup"><span data-stu-id="cbacb-160">INT offsetInDescriptors: The number of descriptors by which to offset.</span></span>

<span data-ttu-id="cbacb-161">UINT Дескрипторинкрементсизе: величина приращения для каждого дескриптора, включая заполнение.</span><span class="sxs-lookup"><span data-stu-id="cbacb-161">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cbacb-162">Требования</span><span class="sxs-lookup"><span data-stu-id="cbacb-162">Requirements</span></span>



| <span data-ttu-id="cbacb-163">Требование</span><span class="sxs-lookup"><span data-stu-id="cbacb-163">Requirement</span></span> | <span data-ttu-id="cbacb-164">Значение</span><span class="sxs-lookup"><span data-stu-id="cbacb-164">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cbacb-165">Header</span><span class="sxs-lookup"><span data-stu-id="cbacb-165">Header</span></span><br/> | <dl> <span data-ttu-id="cbacb-166"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbacb-166"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbacb-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cbacb-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbacb-168">**\_Дескриптор D3D12 \_ GPU \_**</span><span class="sxs-lookup"><span data-stu-id="cbacb-168">**D3D12\_GPU\_DESCRIPTOR\_HANDLE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle)
</dt> <dt>

[<span data-ttu-id="cbacb-169">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="cbacb-169">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





