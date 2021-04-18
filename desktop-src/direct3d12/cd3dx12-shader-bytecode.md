---
title: Структура CD3DX12_SHADER_BYTECODE (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию \_ структуры байт-кода шейдера D3D12 \_ .
ms.assetid: 09CEFCCE-C499-493D-ACDE-806E09995315
keywords:
- Структура CD3DX12_SHADER_BYTECODE
topic_type:
- apiref
api_name:
- CD3DX12_SHADER_BYTECODE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1227c18913492d6533b08f49f5761fab1b93e97b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713503"
---
# <a name="cd3dx12_shader_bytecode-structure"></a><span data-ttu-id="8cd17-104">\_ \_ Структура байта ШЕЙДЕРа CD3DX12</span><span class="sxs-lookup"><span data-stu-id="8cd17-104">CD3DX12\_SHADER\_BYTECODE structure</span></span>

<span data-ttu-id="8cd17-105">Вспомогательная структура, позволяющая упростить инициализацию [**структуры \_ байт- \_ кода шейдера D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .</span><span class="sxs-lookup"><span data-stu-id="8cd17-105">A helper structure to enable easy initialization of a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cd17-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8cd17-106">Syntax</span></span>


```C++
struct CD3DX12_SHADER_BYTECODE  : public D3D12_SHADER_BYTECODE{
   CD3DX12_SHADER_BYTECODE();
   explicit CD3DX12_SHADER_BYTECODE(const D3D12_SHADER_BYTECODE &o);
   CD3DX12_SHADER_BYTECODE(ID3DBlob* pShaderBlob);
   CD3DX12_SHADER_BYTECODE(const void* _pShaderBytecode, SIZE_T bytecodeLength);
   operator const D3D12_SHADER_BYTECODE&() const;
};
```



## <a name="members"></a><span data-ttu-id="8cd17-107">Члены</span><span class="sxs-lookup"><span data-stu-id="8cd17-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8cd17-108">**\_Байт-код шейдера CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="8cd17-108">**CD3DX12\_SHADER\_BYTECODE()**</span></span>
</dt> <dd>

<span data-ttu-id="8cd17-109">Создает новый, неинициализированный экземпляр \_ байт-кода шейдера CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="8cd17-109">Creates a new, uninitialized, instance of a CD3DX12\_SHADER\_BYTECODE.</span></span>

</dd> <dt>

<span data-ttu-id="8cd17-110">**явный \_ байт-код шейдера CD3DX12 \_ (const D3D12, \_ байтовый код шейдера \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="8cd17-110">**explicit CD3DX12\_SHADER\_BYTECODE(const D3D12\_SHADER\_BYTECODE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="8cd17-111">Создает новый экземпляр \_ байт-кода шейдера CD3DX12 \_ , инициализированного с содержимым другой структуры [**байт- \_ \_ кода шейдера D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .</span><span class="sxs-lookup"><span data-stu-id="8cd17-111">Creates a new instance of a CD3DX12\_SHADER\_BYTECODE, initialized with the contents of another [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8cd17-112">**\_Байт-код шейдера CD3DX12 \_ (ID3DBlob \* пшадерблоб)**</span><span class="sxs-lookup"><span data-stu-id="8cd17-112">**CD3DX12\_SHADER\_BYTECODE(ID3DBlob\* pShaderBlob)**</span></span>
</dt> <dd>

<span data-ttu-id="8cd17-113">Создает новый экземпляр \_ байт-кода шейдера CD3DX12 \_ , инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="8cd17-113">Creates a new instance of a CD3DX12\_SHADER\_BYTECODE, initializing the following parameters:</span></span>

<span data-ttu-id="8cd17-114">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) \* пшадерблоб</span><span class="sxs-lookup"><span data-stu-id="8cd17-114">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))\* pShaderBlob</span></span>

</dd> <dt>

<span data-ttu-id="8cd17-115">**\_Байт-код шейдера CD3DX12 \_ (const void \* \_ Пшадербитекоде, Size \_ T битекоделенгс)**</span><span class="sxs-lookup"><span data-stu-id="8cd17-115">**CD3DX12\_SHADER\_BYTECODE(const void\* \_pShaderBytecode, SIZE\_T bytecodeLength)**</span></span>
</dt> <dd>

<span data-ttu-id="8cd17-116">Создает новый экземпляр \_ байт-кода шейдера CD3DX12 \_ , инициализируя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="8cd17-116">Creates a new instance of a CD3DX12\_SHADER\_BYTECODE, initializing the following parameters:</span></span>

<span data-ttu-id="8cd17-117">void \* \_ пшадербитекоде</span><span class="sxs-lookup"><span data-stu-id="8cd17-117">void\* \_pShaderBytecode</span></span>

<span data-ttu-id="8cd17-118">РАЗМЕР \_ T битекоделенгс</span><span class="sxs-lookup"><span data-stu-id="8cd17-118">SIZE\_T bytecodeLength</span></span>

</dd> <dt>

<span data-ttu-id="8cd17-119">**D3D12-байта оператора const константы \_ шейдера \_& () const**</span><span class="sxs-lookup"><span data-stu-id="8cd17-119">**operator const D3D12\_SHADER\_BYTECODE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="8cd17-120">Определяет & оператором передачи по ссылке для типа родительской структуры.</span><span class="sxs-lookup"><span data-stu-id="8cd17-120">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8cd17-121">Требования</span><span class="sxs-lookup"><span data-stu-id="8cd17-121">Requirements</span></span>



| <span data-ttu-id="8cd17-122">Требование</span><span class="sxs-lookup"><span data-stu-id="8cd17-122">Requirement</span></span> | <span data-ttu-id="8cd17-123">Значение</span><span class="sxs-lookup"><span data-stu-id="8cd17-123">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8cd17-124">Header</span><span class="sxs-lookup"><span data-stu-id="8cd17-124">Header</span></span><br/> | <dl> <span data-ttu-id="8cd17-125"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cd17-125"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cd17-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8cd17-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cd17-127">**\_Байтовый код шейдера D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="8cd17-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> <dt>

[<span data-ttu-id="8cd17-128">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="8cd17-128">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

