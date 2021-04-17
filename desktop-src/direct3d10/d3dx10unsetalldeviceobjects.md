---
description: Удаляет все ресурсы с устройства, присвоив их указателям значение NULL. Этот метод должен вызываться во время завершения работы приложения. Это гарантирует, что когда один из них освобождает все ресурсы, которые не привязаны к устройству.
ms.assetid: f41ce97e-5a81-43a4-a8c7-7411b43c0d61
title: Функция D3DX10UnsetAllDeviceObjects (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10UnsetAllDeviceObjects
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4d3a113be935f77dbd62b2f3fac4c16c7cac9881
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694174"
---
# <a name="d3dx10unsetalldeviceobjects-function"></a><span data-ttu-id="476dd-105">Функция D3DX10UnsetAllDeviceObjects</span><span class="sxs-lookup"><span data-stu-id="476dd-105">D3DX10UnsetAllDeviceObjects function</span></span>

<span data-ttu-id="476dd-106">Удаляет все ресурсы с устройства, присвоив их указателям **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="476dd-106">Removes all resources from the device by setting their pointers to **NULL**.</span></span> <span data-ttu-id="476dd-107">Этот метод должен вызываться во время завершения работы приложения.</span><span class="sxs-lookup"><span data-stu-id="476dd-107">This should be called during shutdown of your application.</span></span> <span data-ttu-id="476dd-108">Это гарантирует, что когда один из них освобождает все ресурсы, которые не привязаны к устройству.</span><span class="sxs-lookup"><span data-stu-id="476dd-108">It helps ensure that when one is releasing all of their resources that none of them are bound to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="476dd-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="476dd-109">Syntax</span></span>


```C++
HRESULT D3DX10UnsetAllDeviceObjects(
  _In_ ID3D10Device *pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="476dd-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="476dd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="476dd-111">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="476dd-111">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="476dd-112">Тип: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="476dd-112">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="476dd-113">Указатель на устройство.</span><span class="sxs-lookup"><span data-stu-id="476dd-113">Pointer to the device.</span></span> <span data-ttu-id="476dd-114">См. раздел [**интерфейс ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device).</span><span class="sxs-lookup"><span data-stu-id="476dd-114">See [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="476dd-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="476dd-115">Return value</span></span>

<span data-ttu-id="476dd-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="476dd-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="476dd-117">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="476dd-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="476dd-118">Требования</span><span class="sxs-lookup"><span data-stu-id="476dd-118">Requirements</span></span>



| <span data-ttu-id="476dd-119">Требование</span><span class="sxs-lookup"><span data-stu-id="476dd-119">Requirement</span></span> | <span data-ttu-id="476dd-120">Значение</span><span class="sxs-lookup"><span data-stu-id="476dd-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="476dd-121">Header</span><span class="sxs-lookup"><span data-stu-id="476dd-121">Header</span></span><br/>  | <dl> <span data-ttu-id="476dd-122"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="476dd-122"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="476dd-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="476dd-123">Library</span></span><br/> | <dl> <span data-ttu-id="476dd-124"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="476dd-124"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="476dd-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="476dd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="476dd-126">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="476dd-126">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




