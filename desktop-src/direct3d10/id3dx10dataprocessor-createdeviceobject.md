---
description: Создайте объект устройства.
ms.assetid: 5b9b00de-c744-43c7-b383-1d3358c80741
title: 'Метод ID3DX10DataProcessor:: Креатедевицеобжект (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataProcessor.CreateDeviceObject
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1ed362f992ca2b9d3ce6e561e08e5fe7fd0bdbe3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273801"
---
# <a name="id3dx10dataprocessorcreatedeviceobject-method"></a><span data-ttu-id="d27d0-103">Метод ID3DX10DataProcessor:: Креатедевицеобжект</span><span class="sxs-lookup"><span data-stu-id="d27d0-103">ID3DX10DataProcessor::CreateDeviceObject method</span></span>

<span data-ttu-id="d27d0-104">Создайте объект устройства.</span><span class="sxs-lookup"><span data-stu-id="d27d0-104">Create a device object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d27d0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d27d0-105">Syntax</span></span>


```C++
HRESULT CreateDeviceObject(
  [out] void **ppDataObject
);
```



## <a name="parameters"></a><span data-ttu-id="d27d0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d27d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d27d0-107">*ппдатаобжект* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d27d0-107">*ppDataObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d27d0-108">Тип: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="d27d0-108">Type: **void\*\***</span></span>

<span data-ttu-id="d27d0-109">Адрес указателя на созданный объект устройства.</span><span class="sxs-lookup"><span data-stu-id="d27d0-109">Address of a pointer to the created device object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d27d0-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d27d0-110">Return value</span></span>

<span data-ttu-id="d27d0-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d27d0-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d27d0-112">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="d27d0-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d27d0-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d27d0-113">Requirements</span></span>



| <span data-ttu-id="d27d0-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d27d0-114">Requirement</span></span> | <span data-ttu-id="d27d0-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d27d0-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d27d0-116">Header</span><span class="sxs-lookup"><span data-stu-id="d27d0-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d27d0-117"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="d27d0-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="d27d0-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d27d0-118">Library</span></span><br/> | <dl> <span data-ttu-id="d27d0-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d27d0-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d27d0-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d27d0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d27d0-121">ID3DX10DataProcessor</span><span class="sxs-lookup"><span data-stu-id="d27d0-121">ID3DX10DataProcessor</span></span>](id3dx10dataprocessor.md)
</dt> <dt>

[<span data-ttu-id="d27d0-122">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="d27d0-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




