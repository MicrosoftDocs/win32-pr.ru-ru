---
title: Интерфейс ID3DX11DataLoader (D3DX11core. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Объект загрузки данных, используемый интерфейсом ID3DX11ThreadPump для асинхронной загрузки данных.
ms.assetid: 878929ea-0228-4650-9ca0-f83d60d9f915
keywords:
- Интерфейс ID3DX11DataLoader Direct3D 11
- Интерфейс ID3DX11DataLoader Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11DataLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68236451bf2ba6f491d17541f7d4ca627f5063c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135306"
---
# <a name="id3dx11dataloader-interface"></a><span data-ttu-id="4e0b7-106">Интерфейс ID3DX11DataLoader</span><span class="sxs-lookup"><span data-stu-id="4e0b7-106">ID3DX11DataLoader interface</span></span>

> [!Note]  
> <span data-ttu-id="4e0b7-107">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="4e0b7-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="4e0b7-108">Объект загрузки данных, используемый [**интерфейсом ID3DX11ThreadPump**](id3dx11threadpump.md) для асинхронной загрузки данных.</span><span class="sxs-lookup"><span data-stu-id="4e0b7-108">Data loading object used by [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md) for loading data asynchronously.</span></span>

## <a name="members"></a><span data-ttu-id="4e0b7-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="4e0b7-109">Members</span></span>

<span data-ttu-id="4e0b7-110">Интерфейс **ID3DX11DataLoader** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4e0b7-110">The **ID3DX11DataLoader** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4e0b7-111">**ID3DX11DataLoader** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4e0b7-111">**ID3DX11DataLoader** also has these types of members:</span></span>

-   [<span data-ttu-id="4e0b7-112">Методы</span><span class="sxs-lookup"><span data-stu-id="4e0b7-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4e0b7-113">Методы</span><span class="sxs-lookup"><span data-stu-id="4e0b7-113">Methods</span></span>

<span data-ttu-id="4e0b7-114">Интерфейс **ID3DX11DataLoader** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="4e0b7-114">The **ID3DX11DataLoader** interface has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="4e0b7-115">Метод</span><span class="sxs-lookup"><span data-stu-id="4e0b7-115">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="4e0b7-116">Описание</span><span class="sxs-lookup"><span data-stu-id="4e0b7-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4e0b7-117"><a href="id3dx11dataloader-decompress.md"><strong>Распаковки</strong></a></span><span class="sxs-lookup"><span data-stu-id="4e0b7-117"><a href="id3dx11dataloader-decompress.md"><strong>Decompress</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="4e0b7-118">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="4e0b7-118">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="4e0b7-119">Распаковывает закодированные данные.</span><span class="sxs-lookup"><span data-stu-id="4e0b7-119">Decompresses encoded data.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4e0b7-120"><a href="id3dx11dataloader-destroy.md"><strong>Завершить</strong></a></span><span class="sxs-lookup"><span data-stu-id="4e0b7-120"><a href="id3dx11dataloader-destroy.md"><strong>Destroy</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="4e0b7-121">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="4e0b7-121">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="4e0b7-122">Уничтожает загрузчик после завершения рабочего элемента.</span><span class="sxs-lookup"><span data-stu-id="4e0b7-122">Destroys the loader after a work item completes.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4e0b7-123"><a href="id3dx11dataloader-load.md"><strong>Загрузить</strong></a></span><span class="sxs-lookup"><span data-stu-id="4e0b7-123"><a href="id3dx11dataloader-load.md"><strong>Load</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="4e0b7-124">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="4e0b7-124">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="4e0b7-125">Загружает данные с диска.</span><span class="sxs-lookup"><span data-stu-id="4e0b7-125">Loads data from a disk.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="4e0b7-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="4e0b7-126">Remarks</span></span>

<span data-ttu-id="4e0b7-127">Этот объект может быть унаследован и его члены переопределены.</span><span class="sxs-lookup"><span data-stu-id="4e0b7-127">This object can be inherited and its members redefined.</span></span> <span data-ttu-id="4e0b7-128">Это позволит вам настроить API для загрузки и распаковки собственных пользовательских форматов файлов.</span><span class="sxs-lookup"><span data-stu-id="4e0b7-128">Doing so would enable you to customize the API for loading and decompressing your own custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e0b7-129">Требования</span><span class="sxs-lookup"><span data-stu-id="4e0b7-129">Requirements</span></span>



| <span data-ttu-id="4e0b7-130">Требование</span><span class="sxs-lookup"><span data-stu-id="4e0b7-130">Requirement</span></span> | <span data-ttu-id="4e0b7-131">Значение</span><span class="sxs-lookup"><span data-stu-id="4e0b7-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e0b7-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4e0b7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4e0b7-133">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4e0b7-133">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="4e0b7-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4e0b7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4e0b7-135">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4e0b7-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4e0b7-136">Header</span><span class="sxs-lookup"><span data-stu-id="4e0b7-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e0b7-137"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e0b7-137"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="4e0b7-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4e0b7-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="4e0b7-139"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e0b7-139"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4e0b7-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e0b7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e0b7-141">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="4e0b7-141">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

