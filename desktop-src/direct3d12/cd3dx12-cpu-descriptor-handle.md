---
title: Структура CD3DX12_CPU_DESCRIPTOR_HANDLE (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию \_ \_ \_ структуры дескриптора дескриптора ЦП D3D12.
ms.assetid: 91736069-7D13-47B0-B78C-0F6F104F97EB
keywords:
- Структура CD3DX12_CPU_DESCRIPTOR_HANDLE
topic_type:
- apiref
api_name:
- CD3DX12_CPU_DESCRIPTOR_HANDLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d1045202c531aa200745fc89ed067628a175486
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647822"
---
# <a name="cd3dx12_cpu_descriptor_handle-structure"></a><span data-ttu-id="3febf-104">\_ \_ \_ Структура дескриптора ДЕСКРИПТОРа ЦП CD3DX12</span><span class="sxs-lookup"><span data-stu-id="3febf-104">CD3DX12\_CPU\_DESCRIPTOR\_HANDLE structure</span></span>

<span data-ttu-id="3febf-105">Вспомогательная структура, позволяющая упростить инициализацию [**структуры \_ \_ \_ дескриптора дескриптора ЦП D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) .</span><span class="sxs-lookup"><span data-stu-id="3febf-105">A helper structure to enable easy initialization of a [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="3febf-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3febf-106">Syntax</span></span>


```C++
struct CD3DX12_CPU_DESCRIPTOR_HANDLE  : public D3D12_CPU_DESCRIPTOR_HANDLE{
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE();
                                  explicit CD3DX12_CPU_DESCRIPTOR_HANDLE(const D3D12_CPU_DESCRIPTOR_HANDLE &o);
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE(CD3DX12_DEFAULT);
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE(const D3D12_CPU_DESCRIPTOR_HANDLE &other, INT offsetScaledByIncrementSize);
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE(const D3D12_CPU_DESCRIPTOR_HANDLE &other, INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_CPU_DESCRIPTOR_HANDLE&  Offset(INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_CPU_DESCRIPTOR_HANDLE&  Offset(INT offsetScaledByIncrementSize);
  bool                            operator==( _In_ const D3D12_CPU_DESCRIPTOR_HANDLE& other) const;
  bool                            operator!=(_In_ const D3D12_CPU_DESCRIPTOR_HANDLE& other) const;
  CD3DX12_CPU_DESCRIPTOR_HANDLE & operator=(const D3D12_CPU_DESCRIPTOR_HANDLE &other);
  void                            inline InitOffsetted(_In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            inline InitOffsetted(_In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_CPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_CPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
};
```



## <a name="members"></a><span data-ttu-id="3febf-107">Члены</span><span class="sxs-lookup"><span data-stu-id="3febf-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="3febf-108">**\_ \_ Дескриптор дескриптора ЦП CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="3febf-108">**CD3DX12\_CPU\_DESCRIPTOR\_HANDLE()**</span></span>
</dt> <dd>

<span data-ttu-id="3febf-109">Создает новый, неинициализированный экземпляр \_ \_ дескриптора дескриптора ЦП CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="3febf-109">Creates a new, uninitialized, instance of a CD3DX12\_CPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="3febf-110">**явный дескриптор \_ ЦП \_ CD3DX12 \_ (дескриптор дескриптора \_ ЦП const D3D12 \_ \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="3febf-110">**explicit CD3DX12\_CPU\_DESCRIPTOR\_HANDLE(const D3D12\_CPU\_DESCRIPTOR\_HANDLE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="3febf-111">Создает новый экземпляр \_ \_ дескриптора дескриптора ЦП CD3DX12 \_ , инициализированного с содержимым другой структуры дескриптора [**\_ процессора \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) .</span><span class="sxs-lookup"><span data-stu-id="3febf-111">Creates a new instance of a CD3DX12\_CPU\_DESCRIPTOR\_HANDLE, initialized with the contents of another [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3febf-112">**\_ \_ Дескриптор дескриптора ЦП CD3DX12 \_ ( \_ по умолчанию CD3DX12)**</span><span class="sxs-lookup"><span data-stu-id="3febf-112">**CD3DX12\_CPU\_DESCRIPTOR\_HANDLE(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="3febf-113">Создает новый экземпляр \_ \_ дескриптора дескриптора ЦП CD3DX12 \_ , инициализированного с параметрами по умолчанию (указатель имеет нулевое значение).</span><span class="sxs-lookup"><span data-stu-id="3febf-113">Creates a new instance of a CD3DX12\_CPU\_DESCRIPTOR\_HANDLE, initialized with default parameters (pointer set to zero).</span></span>

</dd> <dt>

<span data-ttu-id="3febf-114">**Дескриптор CD3DX12 дескриптора \_ ЦП \_ \_ (константа дескриптора цп const D3D12 \_ \_ \_ &other, int оффсетскаледбинкрементсизе)**</span><span class="sxs-lookup"><span data-stu-id="3febf-114">**CD3DX12\_CPU\_DESCRIPTOR\_HANDLE(const D3D12\_CPU\_DESCRIPTOR\_HANDLE &other, INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="3febf-115">Создает новый экземпляр \_ \_ дескриптора дескриптора ЦП CD3DX12 \_ , инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="3febf-115">Creates a new instance of a CD3DX12\_CPU\_DESCRIPTOR\_HANDLE, initializing the following parameters:</span></span>

<span data-ttu-id="3febf-116">Дескриптор D3D12 дескриптора \_ цп \_ \_ &другой</span><span class="sxs-lookup"><span data-stu-id="3febf-116">D3D12\_CPU\_DESCRIPTOR\_HANDLE &other</span></span>

<span data-ttu-id="3febf-117">INT Оффсетскаледбинкрементсизе: число инкрементов, на которое смещается смещение.</span><span class="sxs-lookup"><span data-stu-id="3febf-117">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="3febf-118">**Дескриптор CD3DX12 дескриптора \_ ЦП \_ \_ (константа дескриптора цп const D3D12 \_ \_ \_ &other, int оффсетиндескрипторс, uint дескрипторинкрементсизе)**</span><span class="sxs-lookup"><span data-stu-id="3febf-118">**CD3DX12\_CPU\_DESCRIPTOR\_HANDLE(const D3D12\_CPU\_DESCRIPTOR\_HANDLE &other, INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="3febf-119">Создает новый экземпляр \_ \_ дескриптора дескриптора ЦП CD3DX12 \_ , инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="3febf-119">Creates a new instance of a CD3DX12\_CPU\_DESCRIPTOR\_HANDLE, initializing the following parameters:</span></span>

<span data-ttu-id="3febf-120">Дескриптор D3D12 дескриптора \_ цп \_ \_ &другой</span><span class="sxs-lookup"><span data-stu-id="3febf-120">D3D12\_CPU\_DESCRIPTOR\_HANDLE &other</span></span>

<span data-ttu-id="3febf-121">INT Оффсетиндескрипторс: количество дескрипторов, с помощью которых увеличивается значение.</span><span class="sxs-lookup"><span data-stu-id="3febf-121">INT offsetInDescriptors: The number of descriptors by which to increment.</span></span>

<span data-ttu-id="3febf-122">UINT Дескрипторинкрементсизе: величина приращения для каждого дескриптора, включая заполнение.</span><span class="sxs-lookup"><span data-stu-id="3febf-122">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> <dt>

<span data-ttu-id="3febf-123">**Offset (INT Оффсетиндескрипторс, UINT Дескрипторинкрементсизе)**</span><span class="sxs-lookup"><span data-stu-id="3febf-123">**Offset(INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="3febf-124">Задает смещение на основе указанного числа дескрипторов и величины приращения каждого из них.</span><span class="sxs-lookup"><span data-stu-id="3febf-124">Sets the offset based on the specified number of descriptors and how much to increment for each descriptor.</span></span> <span data-ttu-id="3febf-125">Использует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="3febf-125">Uses the following parameters:</span></span>

<span data-ttu-id="3febf-126">INT Оффсетиндескрипторс: количество дескрипторов, с помощью которых увеличивается значение.</span><span class="sxs-lookup"><span data-stu-id="3febf-126">INT offsetInDescriptors: The number of descriptors by which to increment.</span></span>

<span data-ttu-id="3febf-127">UINT Дескрипторинкрементсизе: величина приращения для каждого дескриптора, включая заполнение.</span><span class="sxs-lookup"><span data-stu-id="3febf-127">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> <dt>

<span data-ttu-id="3febf-128">**Offset (INT Оффсетскаледбинкрементсизе)**</span><span class="sxs-lookup"><span data-stu-id="3febf-128">**Offset(INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="3febf-129">Задает смещение на основе указанного числа приращений.</span><span class="sxs-lookup"><span data-stu-id="3febf-129">Sets the offset based on the specified number of increments.</span></span> <span data-ttu-id="3febf-130">Использует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="3febf-130">Uses the following parameters:</span></span>

<span data-ttu-id="3febf-131">INT Оффсетскаледбинкрементсизе: число инкрементов, на которое смещается смещение.</span><span class="sxs-lookup"><span data-stu-id="3febf-131">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="3febf-132">**оператор = = ( \_ в \_ константном дескрипторе \_ дескриптора цп const D3D12 \_ \_& Other) const**</span><span class="sxs-lookup"><span data-stu-id="3febf-132">**operator==( \_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE& other) const**</span></span>
</dt> <dd>

<span data-ttu-id="3febf-133">Проверяет на равенство между текущим \_ \_ дескриптором дескриптора ЦП CD3DX12 и указанным дескриптором дескриптора \_ ЦП D3D12 или дескриптором дескриптора ЦП \_ \_ \_ CD3DX12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="3febf-133">Tests for equality between the current CD3DX12\_CPU\_DESCRIPTOR\_HANDLE and the specified D3D12\_CPU\_DESCRIPTOR\_HANDLE or CD3DX12\_CPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="3febf-134">**operator! = ( \_ в \_ константном дескрипторе \_ дескриптора цп const D3D12 \_ \_& Other) const**</span><span class="sxs-lookup"><span data-stu-id="3febf-134">**operator!=(\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE& other) const**</span></span>
</dt> <dd>

<span data-ttu-id="3febf-135">Проверяет на неравенство между текущим \_ \_ дескриптором дескриптора ЦП CD3DX12 и указанным дескриптором дескриптора \_ ЦП D3D12 или дескриптором дескриптора ЦП \_ \_ \_ CD3DX12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="3febf-135">Tests for inequality between the current CD3DX12\_CPU\_DESCRIPTOR\_HANDLE and the specified D3D12\_CPU\_DESCRIPTOR\_HANDLE or CD3DX12\_CPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="3febf-136">**operator = (const дескриптор D3D12 дескриптора \_ цп \_ \_ &другой)**</span><span class="sxs-lookup"><span data-stu-id="3febf-136">**operator=(const D3D12\_CPU\_DESCRIPTOR\_HANDLE &other)**</span></span>
</dt> <dd>

<span data-ttu-id="3febf-137">Задает \_ \_ дескриптору дескриптора ЦП текущего CD3DX12 \_ те же значения, что и указанный дескриптор дескриптора ЦП D3D12 или дескриптор CD3DX12 дескриптора \_ \_ \_ \_ ЦП \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="3febf-137">Sets the current CD3DX12\_CPU\_DESCRIPTOR\_HANDLE to the same values as the specified D3D12\_CPU\_DESCRIPTOR\_HANDLE or CD3DX12\_CPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="3febf-138">**Встроенный Инитоффсеттед ( \_ в \_ дескрипторе дескриптора ЦП const D3D12 \_ \_ \_ &Base, int оффсетскаледбинкрементсизе)**</span><span class="sxs-lookup"><span data-stu-id="3febf-138">**inline InitOffsetted(\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base, INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="3febf-139">Инициализирует структуру [**\_ \_ \_ дескриптора дескриптора ЦП D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) с указанным числом элементов.</span><span class="sxs-lookup"><span data-stu-id="3febf-139">Initializes a [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure with the specified number of items.</span></span> <span data-ttu-id="3febf-140">Использует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="3febf-140">Uses the following parameters:</span></span>

<span data-ttu-id="3febf-141">\_В \_ константном \_ \_ дескрипторе дескриптора ЦП D3D12 \_ &Base: базовый адрес, по которому производится смещение.</span><span class="sxs-lookup"><span data-stu-id="3febf-141">\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="3febf-142">INT Оффсетскаледбинкрементсизе: число инкрементов, на которое смещается смещение.</span><span class="sxs-lookup"><span data-stu-id="3febf-142">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="3febf-143">**Встроенный Инитоффсеттед ( \_ в \_ дескрипторе дескриптора ЦП const D3D12 \_ \_ \_ &Base, int оффсетиндескрипторс, uint дескрипторинкрементсизе)**</span><span class="sxs-lookup"><span data-stu-id="3febf-143">**inline InitOffsetted(\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="3febf-144">Инициализирует структуру [**\_ \_ \_ дескриптора дескриптора ЦП D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) со смещением, используя указанное число дескрипторов заданного размера.</span><span class="sxs-lookup"><span data-stu-id="3febf-144">Initializes a [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure with an offset, using the specified number of descriptors of the given size.</span></span> <span data-ttu-id="3febf-145">Использует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="3febf-145">Uses the following parameters:</span></span>

<span data-ttu-id="3febf-146">\_В \_ константном \_ \_ дескрипторе дескриптора ЦП D3D12 \_ &Base: базовый адрес, по которому производится смещение.</span><span class="sxs-lookup"><span data-stu-id="3febf-146">\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="3febf-147">INT Оффсетиндескрипторс: количество дескрипторов, по которым производится смещение.</span><span class="sxs-lookup"><span data-stu-id="3febf-147">INT offsetInDescriptors: The number of descriptors by which to offset.</span></span>

<span data-ttu-id="3febf-148">UINT Дескрипторинкрементсизе: величина приращения для каждого дескриптора, включая заполнение.</span><span class="sxs-lookup"><span data-stu-id="3febf-148">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> <dt>

<span data-ttu-id="3febf-149">**статический встроенный Инитоффсеттед дескриптор \_ ЦП (out D3D12) дескриптор обработчика \_ \_ &в константном дескрипторе дескриптора \_ \_ \_ \_ \_ ЦП D3D12 \_ \_ &Base, int оффсетскаледбинкрементсизе)**</span><span class="sxs-lookup"><span data-stu-id="3febf-149">**static inline InitOffsetted(\_Out\_ D3D12\_CPU\_DESCRIPTOR\_HANDLE &handle, \_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base, INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="3febf-150">Инициализирует структуру [**\_ \_ \_ дескриптора дескриптора ЦП D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) со смещением, используя указанное число дескрипторов заданного размера.</span><span class="sxs-lookup"><span data-stu-id="3febf-150">Initializes a [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure with an offset, using the specified number of descriptors of the given size.</span></span> <span data-ttu-id="3febf-151">Использует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="3febf-151">Uses the following parameters:</span></span>

<span data-ttu-id="3febf-152">\_Дескриптор \_ обработчика дескрипторов ЦП D3D12 дескриптора \_ \_ \_ &: выводит результирующий \_ дескриптор ЦП D3D12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="3febf-152">\_Out\_ D3D12\_CPU\_DESCRIPTOR\_HANDLE &handle: Outputs the resulting D3D12\_CPU\_DESCRIPTOR\_HANDLE.</span></span>

<span data-ttu-id="3febf-153">\_В \_ константном \_ \_ дескрипторе дескриптора ЦП D3D12 \_ &Base: базовый адрес, по которому производится смещение.</span><span class="sxs-lookup"><span data-stu-id="3febf-153">\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="3febf-154">INT Оффсетскаледбинкрементсизе: число инкрементов, на которое смещается смещение.</span><span class="sxs-lookup"><span data-stu-id="3febf-154">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="3febf-155">**статический встроенный Инитоффсеттед дескриптор \_ процессора (out D3D12 дескриптора \_ \_ ЦП \_ \_ &дескриптор, \_ в дескрипторе дескриптора \_ ЦП const D3D12 \_ \_ \_ &Base, int оффсетиндескрипторс, uint дескрипторинкрементсизе)**</span><span class="sxs-lookup"><span data-stu-id="3febf-155">**static inline InitOffsetted(\_Out\_ D3D12\_CPU\_DESCRIPTOR\_HANDLE &handle, \_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="3febf-156">Инициализирует структуру [**\_ \_ \_ дескриптора дескриптора ЦП D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) со смещением, используя указанное число дескрипторов заданного размера.</span><span class="sxs-lookup"><span data-stu-id="3febf-156">Initializes a [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure with an offset, using the specified number of descriptors of the given size.</span></span> <span data-ttu-id="3febf-157">Использует следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="3febf-157">Uses the following parameters:</span></span>

<span data-ttu-id="3febf-158">\_Дескриптор \_ обработчика дескрипторов ЦП D3D12 дескриптора \_ \_ \_ &: выводит результирующий \_ дескриптор ЦП D3D12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="3febf-158">\_Out\_ D3D12\_CPU\_DESCRIPTOR\_HANDLE &handle: Outputs the resulting D3D12\_CPU\_DESCRIPTOR\_HANDLE.</span></span>

<span data-ttu-id="3febf-159">\_В \_ константном \_ \_ дескрипторе дескриптора ЦП D3D12 \_ &Base: базовый адрес, по которому производится смещение.</span><span class="sxs-lookup"><span data-stu-id="3febf-159">\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="3febf-160">INT Оффсетиндескрипторс: количество дескрипторов, по которым производится смещение.</span><span class="sxs-lookup"><span data-stu-id="3febf-160">INT offsetInDescriptors: The number of descriptors by which to offset.</span></span>

<span data-ttu-id="3febf-161">UINT Дескрипторинкрементсизе: величина приращения для каждого дескриптора, включая заполнение.</span><span class="sxs-lookup"><span data-stu-id="3febf-161">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3febf-162">Требования</span><span class="sxs-lookup"><span data-stu-id="3febf-162">Requirements</span></span>



| <span data-ttu-id="3febf-163">Требование</span><span class="sxs-lookup"><span data-stu-id="3febf-163">Requirement</span></span> | <span data-ttu-id="3febf-164">Значение</span><span class="sxs-lookup"><span data-stu-id="3febf-164">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3febf-165">Header</span><span class="sxs-lookup"><span data-stu-id="3febf-165">Header</span></span><br/> | <dl> <span data-ttu-id="3febf-166"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="3febf-166"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3febf-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3febf-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3febf-168">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="3febf-168">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





