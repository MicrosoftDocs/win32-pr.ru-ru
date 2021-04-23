---
title: Метод ID3DX11ThreadPump Аддворкитем (D3DX11core. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Добавляет рабочий элемент в конвейер потока.
ms.assetid: 2578506c-6175-457a-bf10-94929bb3c0c4
keywords:
- Метод Аддворкитем Direct3D 11
- Метод Аддворкитем Direct3D 11, интерфейс ID3DX11ThreadPump
- Интерфейс ID3DX11ThreadPump Direct3D 11, метод Аддворкитем
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.AddWorkItem
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebf249405bd71287f93444ae8d23dab694027360
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354273"
---
# <a name="id3dx11threadpumpaddworkitem-method"></a><span data-ttu-id="bce67-107">Метод ID3DX11ThreadPump:: Аддворкитем</span><span class="sxs-lookup"><span data-stu-id="bce67-107">ID3DX11ThreadPump::AddWorkItem method</span></span>

> [!Note]  
> <span data-ttu-id="bce67-108">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="bce67-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="bce67-109">Добавляет рабочий элемент в конвейер потока.</span><span class="sxs-lookup"><span data-stu-id="bce67-109">Adds a work item to the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="bce67-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bce67-110">Syntax</span></span>


```C++
HRESULT AddWorkItem(
  [in]  ID3DX11DataLoader    *pDataLoader,
  [in]  ID3DX11DataProcessor *pDataProcessor,
  [in]  HRESULT              *pHResult,
  [out] void                 **ppDeviceObject
);
```



## <a name="parameters"></a><span data-ttu-id="bce67-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="bce67-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bce67-112">*пдаталоадер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bce67-112">*pDataLoader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bce67-113">Тип: **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\***</span><span class="sxs-lookup"><span data-stu-id="bce67-113">Type: **[**ID3DX11DataLoader**](id3dx11dataloader.md)\***</span></span>

<span data-ttu-id="bce67-114">Загрузчик, который будет использоваться генератором потоков, когда для рабочего элемента требуется загрузка данных.</span><span class="sxs-lookup"><span data-stu-id="bce67-114">The loader that the thread pump will use when a work item requires data to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="bce67-115">*пдатапроцессор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bce67-115">*pDataProcessor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bce67-116">Тип: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\***</span><span class="sxs-lookup"><span data-stu-id="bce67-116">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\***</span></span>

<span data-ttu-id="bce67-117">Процессор, который будет использоваться генератором потоков, когда для рабочего элемента требуются данные для обработки.</span><span class="sxs-lookup"><span data-stu-id="bce67-117">The processor that the thread pump will use when a work item requires data to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="bce67-118">*фресулт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bce67-118">*pHResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bce67-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="bce67-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="bce67-120">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="bce67-120">A pointer to the return value.</span></span> <span data-ttu-id="bce67-121">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="bce67-121">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bce67-122">*ппдевицеобжект* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bce67-122">*ppDeviceObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bce67-123">Тип: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="bce67-123">Type: **void\*\***</span></span>

<span data-ttu-id="bce67-124">Устройство, использующее объект.</span><span class="sxs-lookup"><span data-stu-id="bce67-124">The device that uses the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bce67-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bce67-125">Return value</span></span>

<span data-ttu-id="bce67-126">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bce67-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bce67-127">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="bce67-127">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bce67-128">Требования</span><span class="sxs-lookup"><span data-stu-id="bce67-128">Requirements</span></span>



| <span data-ttu-id="bce67-129">Требование</span><span class="sxs-lookup"><span data-stu-id="bce67-129">Requirement</span></span> | <span data-ttu-id="bce67-130">Значение</span><span class="sxs-lookup"><span data-stu-id="bce67-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bce67-131">Header</span><span class="sxs-lookup"><span data-stu-id="bce67-131">Header</span></span><br/>  | <dl> <span data-ttu-id="bce67-132"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="bce67-132"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="bce67-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bce67-133">Library</span></span><br/> | <dl> <span data-ttu-id="bce67-134"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bce67-134"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bce67-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bce67-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bce67-136">ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="bce67-136">ID3DX11ThreadPump</span></span>](id3dx11threadpump.md)
</dt> <dt>

[<span data-ttu-id="bce67-137">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="bce67-137">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





