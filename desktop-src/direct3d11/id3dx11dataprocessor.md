---
title: Интерфейс ID3DX11DataProcessor (D3DX11core. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Объект обработки данных, используемый интерфейсом ID3DX11ThreadPump для асинхронной загрузки данных.
ms.assetid: ab893879-416f-4b17-9035-a7f03a62b753
keywords:
- Интерфейс ID3DX11DataProcessor Direct3D 11
- Интерфейс ID3DX11DataProcessor Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e421a6e840665220311e5a27c0692cd7f347e7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104984148"
---
# <a name="id3dx11dataprocessor-interface"></a><span data-ttu-id="f19d2-106">Интерфейс ID3DX11DataProcessor</span><span class="sxs-lookup"><span data-stu-id="f19d2-106">ID3DX11DataProcessor interface</span></span>

> [!Note]  
> <span data-ttu-id="f19d2-107">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="f19d2-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="f19d2-108">Объект обработки данных, используемый [**интерфейсом ID3DX11ThreadPump**](id3dx11threadpump.md) для асинхронной загрузки данных.</span><span class="sxs-lookup"><span data-stu-id="f19d2-108">Data processing object used by [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md) for loading data asynchronously.</span></span>

## <a name="members"></a><span data-ttu-id="f19d2-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="f19d2-109">Members</span></span>

<span data-ttu-id="f19d2-110">Интерфейс **ID3DX11DataProcessor** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f19d2-110">The **ID3DX11DataProcessor** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f19d2-111">**ID3DX11DataProcessor** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f19d2-111">**ID3DX11DataProcessor** also has these types of members:</span></span>

-   [<span data-ttu-id="f19d2-112">Методы</span><span class="sxs-lookup"><span data-stu-id="f19d2-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f19d2-113">Методы</span><span class="sxs-lookup"><span data-stu-id="f19d2-113">Methods</span></span>

<span data-ttu-id="f19d2-114">Интерфейс **ID3DX11DataProcessor** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="f19d2-114">The **ID3DX11DataProcessor** interface has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="f19d2-115">Метод</span><span class="sxs-lookup"><span data-stu-id="f19d2-115">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="f19d2-116">Описание</span><span class="sxs-lookup"><span data-stu-id="f19d2-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="f19d2-117"><a href="id3dx11dataprocessor-createdeviceobject.md"><strong>креатедевицеобжект</strong></a></span><span class="sxs-lookup"><span data-stu-id="f19d2-117"><a href="id3dx11dataprocessor-createdeviceobject.md"><strong>CreateDeviceObject</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="f19d2-118">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="f19d2-118">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="f19d2-119">Создает объект устройства.</span><span class="sxs-lookup"><span data-stu-id="f19d2-119">Creates a device object.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="f19d2-120"><a href="id3dx11dataprocessor-destroy.md"><strong>Завершить</strong></a></span><span class="sxs-lookup"><span data-stu-id="f19d2-120"><a href="id3dx11dataprocessor-destroy.md"><strong>Destroy</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="f19d2-121">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="f19d2-121">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="f19d2-122">Уничтожает процессор после завершения рабочего элемента.</span><span class="sxs-lookup"><span data-stu-id="f19d2-122">Destroys the processor after a work item completes.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="f19d2-123"><a href="id3dx11dataprocessor-process.md"><strong>Процесс</strong></a></span><span class="sxs-lookup"><span data-stu-id="f19d2-123"><a href="id3dx11dataprocessor-process.md"><strong>Process</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="f19d2-124">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="f19d2-124">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="f19d2-125">Обрабатывает данные.</span><span class="sxs-lookup"><span data-stu-id="f19d2-125">Processes data.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="f19d2-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="f19d2-126">Remarks</span></span>

<span data-ttu-id="f19d2-127">Этот объект может быть унаследован и его члены переопределяются для обработки пользовательских форматов файлов.</span><span class="sxs-lookup"><span data-stu-id="f19d2-127">This object can be inherited and its members redefined for processing custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="f19d2-128">Требования</span><span class="sxs-lookup"><span data-stu-id="f19d2-128">Requirements</span></span>



| <span data-ttu-id="f19d2-129">Требование</span><span class="sxs-lookup"><span data-stu-id="f19d2-129">Requirement</span></span> | <span data-ttu-id="f19d2-130">Значение</span><span class="sxs-lookup"><span data-stu-id="f19d2-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f19d2-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f19d2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f19d2-132">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f19d2-132">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="f19d2-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f19d2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f19d2-134">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f19d2-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f19d2-135">Header</span><span class="sxs-lookup"><span data-stu-id="f19d2-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="f19d2-136"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="f19d2-136"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="f19d2-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f19d2-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="f19d2-138"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f19d2-138"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f19d2-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f19d2-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f19d2-140">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="f19d2-140">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

