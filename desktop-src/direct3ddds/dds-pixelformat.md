---
title: Структура DDS_PIXELFORMAT (DDS. h)
description: Формат пикселей поверхности.
ms.assetid: 39c5e48d-cf20-4d77-80d5-a67f04de4883
keywords:
- DDS структуры DDS_PIXELFORMAT
topic_type:
- apiref
api_name:
- DDS_PIXELFORMAT
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd909d62a1be212f9ed4ef9af243a27f28be818
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713529"
---
# <a name="dds_pixelformat-structure"></a><span data-ttu-id="d692b-104">\_Структура PIXELFORMAT DDS</span><span class="sxs-lookup"><span data-stu-id="d692b-104">DDS\_PIXELFORMAT structure</span></span>

<span data-ttu-id="d692b-105">Формат пикселей поверхности.</span><span class="sxs-lookup"><span data-stu-id="d692b-105">Surface pixel format.</span></span>

## <a name="syntax"></a><span data-ttu-id="d692b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d692b-106">Syntax</span></span>


```C++
struct DDS_PIXELFORMAT {
  DWORD dwSize;
  DWORD dwFlags;
  DWORD dwFourCC;
  DWORD dwRGBBitCount;
  DWORD dwRBitMask;
  DWORD dwGBitMask;
  DWORD dwBBitMask;
  DWORD dwABitMask;
};
```



## <a name="members"></a><span data-ttu-id="d692b-107">Члены</span><span class="sxs-lookup"><span data-stu-id="d692b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d692b-108">**двсизе**</span><span class="sxs-lookup"><span data-stu-id="d692b-108">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="d692b-109">Тип: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d692b-109">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d692b-110">Размер структуры; Задайте значение 32 (байт).</span><span class="sxs-lookup"><span data-stu-id="d692b-110">Structure size; set to 32 (bytes).</span></span>

</dd> <dt>

<span data-ttu-id="d692b-111">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="d692b-111">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="d692b-112">Тип: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d692b-112">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d692b-113">Значения, указывающие тип данных на поверхности.</span><span class="sxs-lookup"><span data-stu-id="d692b-113">Values which indicate what type of data is in the surface.</span></span>



| <span data-ttu-id="d692b-114">Flag</span><span class="sxs-lookup"><span data-stu-id="d692b-114">Flag</span></span>              | <span data-ttu-id="d692b-115">Описание</span><span class="sxs-lookup"><span data-stu-id="d692b-115">Description</span></span>                                                                                                                                                                                                                                | <span data-ttu-id="d692b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d692b-116">Value</span></span>   |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------|
| <span data-ttu-id="d692b-117">ДДПФ \_ алфапикселс</span><span class="sxs-lookup"><span data-stu-id="d692b-117">DDPF\_ALPHAPIXELS</span></span> | <span data-ttu-id="d692b-118">Текстура содержит альфа-данные; **двргбалфабитмаск** содержит допустимые данные.</span><span class="sxs-lookup"><span data-stu-id="d692b-118">Texture contains alpha data; **dwRGBAlphaBitMask** contains valid data.</span></span>                                                                                                                                                                    | <span data-ttu-id="d692b-119">0x1</span><span class="sxs-lookup"><span data-stu-id="d692b-119">0x1</span></span>     |
| <span data-ttu-id="d692b-120">ДДПФ \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="d692b-120">DDPF\_ALPHA</span></span>       | <span data-ttu-id="d692b-121">Используется в некоторых старых файлах DDS для несжатых данных только для альфа-канала (Двргббиткаунт содержит альфа-канал биткаунт; Двабитмаск содержит допустимые данные)</span><span class="sxs-lookup"><span data-stu-id="d692b-121">Used in some older DDS files for alpha channel only uncompressed data (dwRGBBitCount contains the alpha channel bitcount; dwABitMask contains valid data)</span></span>                                                                                  | <span data-ttu-id="d692b-122">0x2</span><span class="sxs-lookup"><span data-stu-id="d692b-122">0x2</span></span>     |
| <span data-ttu-id="d692b-123">ДДПФ \_ FourCC</span><span class="sxs-lookup"><span data-stu-id="d692b-123">DDPF\_FOURCC</span></span>      | <span data-ttu-id="d692b-124">Текстура содержит сжатые данные RGB. **двфауркк** содержит допустимые данные.</span><span class="sxs-lookup"><span data-stu-id="d692b-124">Texture contains compressed RGB data; **dwFourCC** contains valid data.</span></span>                                                                                                                                                                    | <span data-ttu-id="d692b-125">0x4</span><span class="sxs-lookup"><span data-stu-id="d692b-125">0x4</span></span>     |
| <span data-ttu-id="d692b-126">ДДПФ \_ RGB</span><span class="sxs-lookup"><span data-stu-id="d692b-126">DDPF\_RGB</span></span>         | <span data-ttu-id="d692b-127">Текстура содержит несжатые данные RGB; **двргббиткаунт** и маски RGB (**дврбитмаск**, **двгбитмаск**, **двббитмаск**) содержат допустимые данные.</span><span class="sxs-lookup"><span data-stu-id="d692b-127">Texture contains uncompressed RGB data; **dwRGBBitCount** and the RGB masks (**dwRBitMask**, **dwGBitMask**, **dwBBitMask**) contain valid data.</span></span>                                                                                           | <span data-ttu-id="d692b-128">0x40</span><span class="sxs-lookup"><span data-stu-id="d692b-128">0x40</span></span>    |
| <span data-ttu-id="d692b-129">ДДПФ \_ YUV</span><span class="sxs-lookup"><span data-stu-id="d692b-129">DDPF\_YUV</span></span>         | <span data-ttu-id="d692b-130">Используется в некоторых старых файлах DDS для несжатых данных YUV (Двргббиткаунт содержит число битов YUV, Дврбитмаск содержит маску Y, Двгбитмаск содержит маску U, Двббитмаск содержит маску V)</span><span class="sxs-lookup"><span data-stu-id="d692b-130">Used in some older DDS files for YUV uncompressed data (dwRGBBitCount contains the YUV bit count; dwRBitMask contains the Y mask, dwGBitMask contains the U mask, dwBBitMask contains the V mask)</span></span>                                          | <span data-ttu-id="d692b-131">0x200</span><span class="sxs-lookup"><span data-stu-id="d692b-131">0x200</span></span>   |
| <span data-ttu-id="d692b-132">\_светимость ддпф</span><span class="sxs-lookup"><span data-stu-id="d692b-132">DDPF\_LUMINANCE</span></span>   | <span data-ttu-id="d692b-133">Используется в некоторых старых файлах DDS для несжатых данных одноканального цвета (Двргббиткаунт содержит число битов канала светимости; Дврбитмаск содержит маску канала).</span><span class="sxs-lookup"><span data-stu-id="d692b-133">Used in some older DDS files for single channel color uncompressed data (dwRGBBitCount contains the luminance channel bit count; dwRBitMask contains the channel mask).</span></span> <span data-ttu-id="d692b-134">Можно сочетать с ДДПФ \_ алфапикселс для файла DDS из двух каналов.</span><span class="sxs-lookup"><span data-stu-id="d692b-134">Can be combined with DDPF\_ALPHAPIXELS for a two channel DDS file.</span></span> | <span data-ttu-id="d692b-135">0x20000</span><span class="sxs-lookup"><span data-stu-id="d692b-135">0x20000</span></span> |



 

</dd> <dt>

<span data-ttu-id="d692b-136">**двфауркк**</span><span class="sxs-lookup"><span data-stu-id="d692b-136">**dwFourCC**</span></span>
</dt> <dd>

<span data-ttu-id="d692b-137">Тип: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d692b-137">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d692b-138">Коды из четырех символов для указания сжатых или пользовательских форматов.</span><span class="sxs-lookup"><span data-stu-id="d692b-138">Four-character codes for specifying compressed or custom formats.</span></span> <span data-ttu-id="d692b-139">Возможные значения: *DXT1*, *DXT2*, *DXT3*, *DXT4* или *DXT5*.</span><span class="sxs-lookup"><span data-stu-id="d692b-139">Possible values include: *DXT1*, *DXT2*, *DXT3*, *DXT4*, or *DXT5*.</span></span> <span data-ttu-id="d692b-140">Объект FourCC СОДЕРЖИМЫМ DX10 указывает пресценсе из расширенного заголовка [**\_ \_ DXT10 заголовков**](dds-header-dxt10.md) , а элемент дксгиформат этой структуры — истинный формат.</span><span class="sxs-lookup"><span data-stu-id="d692b-140">A FourCC of DX10 indicates the prescense of the [**DDS\_HEADER\_DXT10**](dds-header-dxt10.md) extended header, and the dxgiFormat member of that structure indicates the true format.</span></span> <span data-ttu-id="d692b-141">При использовании кода из четырех символов dwFlags должен содержать *ддпф \_ FourCC*.</span><span class="sxs-lookup"><span data-stu-id="d692b-141">When using a four-character code, dwFlags must include *DDPF\_FOURCC*.</span></span>

</dd> <dt>

<span data-ttu-id="d692b-142">**двргббиткаунт**</span><span class="sxs-lookup"><span data-stu-id="d692b-142">**dwRGBBitCount**</span></span>
</dt> <dd>

<span data-ttu-id="d692b-143">Тип: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d692b-143">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d692b-144">Число битов в формате RGB (возможно, включая альфа).</span><span class="sxs-lookup"><span data-stu-id="d692b-144">Number of bits in an RGB (possibly including alpha) format.</span></span> <span data-ttu-id="d692b-145">Допустим, если **dwFlags** включает *ддпф \_ RGB*, *ддпф \_ светимость* или *ддпф \_ YUV*.</span><span class="sxs-lookup"><span data-stu-id="d692b-145">Valid when **dwFlags** includes *DDPF\_RGB*, *DDPF\_LUMINANCE*, or *DDPF\_YUV*.</span></span>

</dd> <dt>

<span data-ttu-id="d692b-146">**дврбитмаск**</span><span class="sxs-lookup"><span data-stu-id="d692b-146">**dwRBitMask**</span></span>
</dt> <dd>

<span data-ttu-id="d692b-147">Тип: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d692b-147">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d692b-148">Красный (или лумианнце или Y) маску для чтения цветовых данных.</span><span class="sxs-lookup"><span data-stu-id="d692b-148">Red (or lumiannce or Y) mask for reading color data.</span></span> <span data-ttu-id="d692b-149">Например, при наличии формата A8R8G8B8 красной маской будет 0x00ff0000.</span><span class="sxs-lookup"><span data-stu-id="d692b-149">For instance, given the A8R8G8B8 format, the red mask would be 0x00ff0000.</span></span>

</dd> <dt>

<span data-ttu-id="d692b-150">**двгбитмаск**</span><span class="sxs-lookup"><span data-stu-id="d692b-150">**dwGBitMask**</span></span>
</dt> <dd>

<span data-ttu-id="d692b-151">Тип: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d692b-151">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d692b-152">Зеленая (или U) маска для чтения данных цвета.</span><span class="sxs-lookup"><span data-stu-id="d692b-152">Green (or U) mask for reading color data.</span></span> <span data-ttu-id="d692b-153">Например, при наличии формата A8R8G8B8 Зеленая маска будет 0x0000FF00.</span><span class="sxs-lookup"><span data-stu-id="d692b-153">For instance, given the A8R8G8B8 format, the green mask would be 0x0000ff00.</span></span>

</dd> <dt>

<span data-ttu-id="d692b-154">**двббитмаск**</span><span class="sxs-lookup"><span data-stu-id="d692b-154">**dwBBitMask**</span></span>
</dt> <dd>

<span data-ttu-id="d692b-155">Тип: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d692b-155">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d692b-156">Синяя (или V) маска для чтения данных цвета.</span><span class="sxs-lookup"><span data-stu-id="d692b-156">Blue (or V) mask for reading color data.</span></span> <span data-ttu-id="d692b-157">Например, при наличии формата A8R8G8B8 синяя маска будет 0x000000ff.</span><span class="sxs-lookup"><span data-stu-id="d692b-157">For instance, given the A8R8G8B8 format, the blue mask would be 0x000000ff.</span></span>

</dd> <dt>

<span data-ttu-id="d692b-158">**двабитмаск**</span><span class="sxs-lookup"><span data-stu-id="d692b-158">**dwABitMask**</span></span>
</dt> <dd>

<span data-ttu-id="d692b-159">Тип: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d692b-159">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d692b-160">Альфа-маска для чтения альфа-данных.</span><span class="sxs-lookup"><span data-stu-id="d692b-160">Alpha mask for reading alpha data.</span></span> <span data-ttu-id="d692b-161">dwFlags должен включать *ддпф \_ Алфапикселс* или *ддпф \_ Alpha*.</span><span class="sxs-lookup"><span data-stu-id="d692b-161">dwFlags must include *DDPF\_ALPHAPIXELS* or *DDPF\_ALPHA*.</span></span> <span data-ttu-id="d692b-162">Например, при наличии формата A8R8G8B8 альфа-маска будет 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="d692b-162">For instance, given the A8R8G8B8 format, the alpha mask would be 0xff000000.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d692b-163">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d692b-163">Remarks</span></span>

<span data-ttu-id="d692b-164">Для хранения форматов DXGI, таких как данные с плавающей запятой, используйте **DWFLAGS** ддпф \_ FourCC и задайте **двфауркк** в качестве значения "," X "," 1 "," 0 ".</span><span class="sxs-lookup"><span data-stu-id="d692b-164">To store DXGI formats such as floating-point data, use a **dwFlags** of DDPF\_FOURCC and set **dwFourCC** to 'D','X','1','0'.</span></span> <span data-ttu-id="d692b-165">Используйте заголовок [**\_ \_ DXT10 Extension заголовков DDS**](dds-header-dxt10.md) для хранения формата DXGI в члене **дксгиформат** .</span><span class="sxs-lookup"><span data-stu-id="d692b-165">Use the [**DDS\_HEADER\_DXT10**](dds-header-dxt10.md) extension header to store the DXGI format in the **dxgiFormat** member.</span></span>

<span data-ttu-id="d692b-166">Обратите внимание, что существуют нестандартные разновидности файлов DDS, где **dwFlags** имеет ддпф \_ FourCC, а значение **двфауркк** устанавливается непосредственно в \_ значение перечисления формата D3DFORMAT или DXGI.</span><span class="sxs-lookup"><span data-stu-id="d692b-166">Note that there are non-standard variants of DDS files where **dwFlags** has DDPF\_FOURCC and the **dwFourCC** value is set directly to a D3DFORMAT or DXGI\_FORMAT enumeration value.</span></span> <span data-ttu-id="d692b-167">Невозможно устранить неоднозначность значений формата D3DFORMAT и DXGI \_ с помощью этой нестандартной схемы, поэтому вместо нее рекомендуется использовать заголовок расширения содержимым DX10.</span><span class="sxs-lookup"><span data-stu-id="d692b-167">It is not possible to disambiguate the D3DFORMAT versus DXGI\_FORMAT values using this non-standard scheme, so the DX10 extension header is recommended instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="d692b-168">Требования</span><span class="sxs-lookup"><span data-stu-id="d692b-168">Requirements</span></span>



| <span data-ttu-id="d692b-169">Требование</span><span class="sxs-lookup"><span data-stu-id="d692b-169">Requirement</span></span> | <span data-ttu-id="d692b-170">Значение</span><span class="sxs-lookup"><span data-stu-id="d692b-170">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d692b-171">Header</span><span class="sxs-lookup"><span data-stu-id="d692b-171">Header</span></span><br/> | <dl> <span data-ttu-id="d692b-172"><dt>DDS. h</dt></span><span class="sxs-lookup"><span data-stu-id="d692b-172"><dt>Dds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d692b-173">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d692b-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d692b-174">Справочник по DDS</span><span class="sxs-lookup"><span data-stu-id="d692b-174">Reference for DDS</span></span>](dx-graphics-dds-reference.md)
</dt> </dl>

 

