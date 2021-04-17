---
description: Добавьте рабочий элемент в конвейер потоков.
ms.assetid: f07789dc-a3d5-4bad-9768-527e701271b8
title: 'Метод ID3DX10ThreadPump:: Аддворкитем (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.AddWorkItem
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: aaf5286ca6cf7b61b0027b176d9a9261bd0beaa8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105704016"
---
# <a name="id3dx10threadpumpaddworkitem-method"></a><span data-ttu-id="c7e34-103">Метод ID3DX10ThreadPump:: Аддворкитем</span><span class="sxs-lookup"><span data-stu-id="c7e34-103">ID3DX10ThreadPump::AddWorkItem method</span></span>

<span data-ttu-id="c7e34-104">Добавьте рабочий элемент в конвейер потоков.</span><span class="sxs-lookup"><span data-stu-id="c7e34-104">Add a work item to the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7e34-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c7e34-105">Syntax</span></span>


```C++
HRESULT AddWorkItem(
  [in]  ID3DX10DataLoader    *pDataLoader,
  [in]  ID3DX10DataProcessor *pDataProcessor,
  [in]  HRESULT              *pHResult,
  [out] void                 **ppDeviceObject
);
```



## <a name="parameters"></a><span data-ttu-id="c7e34-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7e34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7e34-107">*пдаталоадер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7e34-107">*pDataLoader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7e34-108">Тип: **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\***</span><span class="sxs-lookup"><span data-stu-id="c7e34-108">Type: **[**ID3DX10DataLoader**](id3dx10dataloader.md)\***</span></span>

<span data-ttu-id="c7e34-109">Загрузчик, который будет использоваться генератором потоков, когда для рабочего элемента требуется загрузка данных.</span><span class="sxs-lookup"><span data-stu-id="c7e34-109">The loader that the thread pump will use when a work item requires data to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="c7e34-110">*пдатапроцессор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7e34-110">*pDataProcessor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7e34-111">Тип: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\***</span><span class="sxs-lookup"><span data-stu-id="c7e34-111">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\***</span></span>

<span data-ttu-id="c7e34-112">Процессор, который будет использоваться генератором потоков, когда для рабочего элемента требуются данные для обработки.</span><span class="sxs-lookup"><span data-stu-id="c7e34-112">The processor that the thread pump will use when a work item requires data to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="c7e34-113">*фресулт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7e34-113">*pHResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7e34-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="c7e34-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="c7e34-115">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="c7e34-115">A pointer to the return value.</span></span> <span data-ttu-id="c7e34-116">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c7e34-116">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c7e34-117">*ппдевицеобжект* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c7e34-117">*ppDeviceObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7e34-118">Тип: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="c7e34-118">Type: **void\*\***</span></span>

<span data-ttu-id="c7e34-119">Устройство, использующее объект.</span><span class="sxs-lookup"><span data-stu-id="c7e34-119">The device that uses the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7e34-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c7e34-120">Return value</span></span>

<span data-ttu-id="c7e34-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c7e34-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c7e34-122">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c7e34-122">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7e34-123">Требования</span><span class="sxs-lookup"><span data-stu-id="c7e34-123">Requirements</span></span>



| <span data-ttu-id="c7e34-124">Требование</span><span class="sxs-lookup"><span data-stu-id="c7e34-124">Requirement</span></span> | <span data-ttu-id="c7e34-125">Значение</span><span class="sxs-lookup"><span data-stu-id="c7e34-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c7e34-126">Header</span><span class="sxs-lookup"><span data-stu-id="c7e34-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c7e34-127"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7e34-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="c7e34-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c7e34-128">Library</span></span><br/> | <dl> <span data-ttu-id="c7e34-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7e34-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7e34-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7e34-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7e34-131">ID3DX10ThreadPump</span><span class="sxs-lookup"><span data-stu-id="c7e34-131">ID3DX10ThreadPump</span></span>](id3dx10threadpump.md)
</dt> <dt>

[<span data-ttu-id="c7e34-132">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="c7e34-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




