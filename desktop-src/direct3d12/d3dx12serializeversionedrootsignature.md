---
title: Функция D3DX12SerializeVersionedRootSignature (D3dx12. h)
description: Помогает включить функции корневой подписи 1,1, когда они доступны, и не требует поддержки двух путей кода для сборки корневых подписей. Этот вспомогательный метод восстанавливает корневую подпись версии 1,0, если версия 1,1 не поддерживается.
ms.assetid: 0F6BA6C1-9A33-4E99-BF34-4A0358E7427D
keywords:
- Функция D3DX12SerializeVersionedRootSignature
topic_type:
- apiref
api_name:
- D3DX12SerializeVersionedRootSignature
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70a9d0424f7f7a7f89edde18273c5d1fa22fae28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703658"
---
# <a name="d3dx12serializeversionedrootsignature-function"></a><span data-ttu-id="8c0f4-105">Функция D3DX12SerializeVersionedRootSignature</span><span class="sxs-lookup"><span data-stu-id="8c0f4-105">D3DX12SerializeVersionedRootSignature function</span></span>

<span data-ttu-id="8c0f4-106">Помогает включить функции корневой подписи 1,1, когда они доступны, и не требует поддержки двух путей кода для сборки корневых подписей.</span><span class="sxs-lookup"><span data-stu-id="8c0f4-106">Helps enable root signature 1.1 features when they are available, and does not require maintaining two code paths for building root signatures.</span></span> <span data-ttu-id="8c0f4-107">Этот вспомогательный метод восстанавливает корневую подпись версии 1,0, если версия 1,1 не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8c0f4-107">This helper method reconstructs a version 1.0 root signature when version 1.1 is not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c0f4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8c0f4-108">Syntax</span></span>


```C++
HRESULT inline D3DX12SerializeVersionedRootSignature(
  _In_      const D3D12_VERSIONED_ROOT_SIGNATURE_DESC *pRootSignatureDesc,
                  D3D_ROOT_SIGNATURE_VERSION          MaxVersion,
  _Out_           ID3DBlob                            **ppBlob,
  _Out_opt_       ID3DBlob                            **ppErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="8c0f4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c0f4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c0f4-110">*прутсигнатуредеск* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8c0f4-110">*pRootSignatureDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c0f4-111">Тип: **const D3D12 с \_ версией \_ корневая \_ подпись \_ DESC \***</span><span class="sxs-lookup"><span data-stu-id="8c0f4-111">Type: **const D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC\***</span></span>

<span data-ttu-id="8c0f4-112">Указывает [**D3D12 \_ \_ корневую \_ подпись \_ с версией**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) , которая содержит описание любой версии корневой подписи.</span><span class="sxs-lookup"><span data-stu-id="8c0f4-112">Specifies a [**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) that contains a description of any version of a root signature.</span></span>

</dd> <dt>

<span data-ttu-id="8c0f4-113">*MaxVersion*</span><span class="sxs-lookup"><span data-stu-id="8c0f4-113">*MaxVersion*</span></span> 
</dt> <dd>

<span data-ttu-id="8c0f4-114">Тип: **\_ версия " \_ корневая \_ сигнатура D3D** "</span><span class="sxs-lookup"><span data-stu-id="8c0f4-114">Type: **D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>

<span data-ttu-id="8c0f4-115">Указывает максимальную поддерживаемую [**\_ версию для корневой \_ сигнатуры \_ D3D**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version).</span><span class="sxs-lookup"><span data-stu-id="8c0f4-115">Specifies the maximum supported [**D3D\_ROOT\_SIGNATURE\_VERSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version).</span></span>

</dd> <dt>

<span data-ttu-id="8c0f4-116">*ппблоб* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8c0f4-116">*ppBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c0f4-117">Тип: **ID3DBlob \* \***</span><span class="sxs-lookup"><span data-stu-id="8c0f4-117">Type: **ID3DBlob\*\***</span></span>

<span data-ttu-id="8c0f4-118">Указатель на блок памяти, который получает указатель на интерфейс [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) , который можно использовать для доступа к сериализованной корневой подписи.</span><span class="sxs-lookup"><span data-stu-id="8c0f4-118">A pointer to a memory block that receives a pointer to the [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) interface that you can use to access the serialized root signature.</span></span>

</dd> <dt>

<span data-ttu-id="8c0f4-119">*пперрорблоб* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="8c0f4-119">*ppErrorBlob* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8c0f4-120">Тип: **ID3DBlob \* \***</span><span class="sxs-lookup"><span data-stu-id="8c0f4-120">Type: **ID3DBlob\*\***</span></span>

<span data-ttu-id="8c0f4-121">Указатель на блок памяти, который получает указатель на интерфейс [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) , который можно использовать для доступа к сообщениям об ошибках сериализатора, или **значение NULL** , если ошибок нет.</span><span class="sxs-lookup"><span data-stu-id="8c0f4-121">A pointer to a memory block that receives a pointer to the [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) interface that you can use to access serializer error messages, or **NULL** if there are no errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c0f4-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8c0f4-122">Return value</span></span>

<span data-ttu-id="8c0f4-123">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8c0f4-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8c0f4-124">Возвращает **значение \_ ОК** , если выполнено успешно; в противном случае возвращает один из [кодов возврата Direct3D 12](d3d12-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="8c0f4-124">Returns **S\_OK** if successful; otherwise, returns one of the [Direct3D 12 Return Codes](d3d12-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8c0f4-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8c0f4-125">Remarks</span></span>

<span data-ttu-id="8c0f4-126">Эта функция была выпущена и совпадает с годовщиной обновления Windows 10 (14393).</span><span class="sxs-lookup"><span data-stu-id="8c0f4-126">This function was released to coincide with the Windows 10 Anniversary Update (14393).</span></span> <span data-ttu-id="8c0f4-127">Для поддержки версий Windows 10 до этого для использования этой функции требуется настроить d3d12. lib для *отложенной загрузки*.</span><span class="sxs-lookup"><span data-stu-id="8c0f4-127">In order to support Windows 10 versions prior to this, use of this function requires d3d12.lib be set up for *delay loading*.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c0f4-128">Требования</span><span class="sxs-lookup"><span data-stu-id="8c0f4-128">Requirements</span></span>



| <span data-ttu-id="8c0f4-129">Требование</span><span class="sxs-lookup"><span data-stu-id="8c0f4-129">Requirement</span></span> | <span data-ttu-id="8c0f4-130">Значение</span><span class="sxs-lookup"><span data-stu-id="8c0f4-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8c0f4-131">Header</span><span class="sxs-lookup"><span data-stu-id="8c0f4-131">Header</span></span><br/>  | <dl> <span data-ttu-id="8c0f4-132"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c0f4-132"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="8c0f4-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8c0f4-133">Library</span></span><br/> | <dl> <span data-ttu-id="8c0f4-134"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c0f4-134"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="8c0f4-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8c0f4-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="8c0f4-136"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c0f4-136"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c0f4-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c0f4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c0f4-138">**D3D12SerializeVersionedRootSignature**</span><span class="sxs-lookup"><span data-stu-id="8c0f4-138">**D3D12SerializeVersionedRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature)
</dt> <dt>

[<span data-ttu-id="8c0f4-139">Вспомогательные функции для D3D12</span><span class="sxs-lookup"><span data-stu-id="8c0f4-139">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

