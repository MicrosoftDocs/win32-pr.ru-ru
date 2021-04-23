---
title: Структура DDS_HEADER (DDS. h)
description: Описывает заголовок файла DDS.
ms.assetid: 7f8bde30-0ff9-4bb9-b444-5c875e6a0865
keywords:
- DDS структуры DDS_HEADER
topic_type:
- apiref
api_name:
- DDS_HEADER
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d70fa0c4b05b6655ce0329cc73651ea21d4d808
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713530"
---
# <a name="dds_header-structure"></a><span data-ttu-id="c7dc4-104">\_Структура заголовка DDS</span><span class="sxs-lookup"><span data-stu-id="c7dc4-104">DDS\_HEADER structure</span></span>

<span data-ttu-id="c7dc4-105">Описывает заголовок файла DDS.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-105">Describes a DDS file header.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7dc4-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c7dc4-106">Syntax</span></span>


```C++
typedef struct {
  DWORD           dwSize;
  DWORD           dwFlags;
  DWORD           dwHeight;
  DWORD           dwWidth;
  DWORD           dwPitchOrLinearSize;
  DWORD           dwDepth;
  DWORD           dwMipMapCount;
  DWORD           dwReserved1[11];
  DDS_PIXELFORMAT ddspf;
  DWORD           dwCaps;
  DWORD           dwCaps2;
  DWORD           dwCaps3;
  DWORD           dwCaps4;
  DWORD           dwReserved2;
} DDS_HEADER;
```



## <a name="members"></a><span data-ttu-id="c7dc4-107">Члены</span><span class="sxs-lookup"><span data-stu-id="c7dc4-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c7dc4-108">**двсизе**</span><span class="sxs-lookup"><span data-stu-id="c7dc4-108">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="c7dc4-109">Тип: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c7dc4-109">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="c7dc4-110">Размер структуры.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-110">Size of structure.</span></span> <span data-ttu-id="c7dc4-111">Этот элемент должен иметь значение 124.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-111">This member must be set to 124.</span></span>

</dd> <dt>

<span data-ttu-id="c7dc4-112">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="c7dc4-112">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="c7dc4-113">Тип: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c7dc4-113">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="c7dc4-114">Флаги, указывающие, какие элементы содержат допустимые данные.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-114">Flags to indicate which members contain valid data.</span></span>



| <span data-ttu-id="c7dc4-115">Flag</span><span class="sxs-lookup"><span data-stu-id="c7dc4-115">Flag</span></span>              | <span data-ttu-id="c7dc4-116">Описание</span><span class="sxs-lookup"><span data-stu-id="c7dc4-116">Description</span></span>                                                  | <span data-ttu-id="c7dc4-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c7dc4-117">Value</span></span>    |
|-------------------|--------------------------------------------------------------|----------|
| <span data-ttu-id="c7dc4-118">ДДСД \_ Cap</span><span class="sxs-lookup"><span data-stu-id="c7dc4-118">DDSD\_CAPS</span></span>        | <span data-ttu-id="c7dc4-119">Требуется в каждом файле. DDS.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-119">Required in every .dds file.</span></span>                                 | <span data-ttu-id="c7dc4-120">0x1</span><span class="sxs-lookup"><span data-stu-id="c7dc4-120">0x1</span></span>      |
| <span data-ttu-id="c7dc4-121">\_Высота ддсд</span><span class="sxs-lookup"><span data-stu-id="c7dc4-121">DDSD\_HEIGHT</span></span>      | <span data-ttu-id="c7dc4-122">Требуется в каждом файле. DDS.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-122">Required in every .dds file.</span></span>                                 | <span data-ttu-id="c7dc4-123">0x2</span><span class="sxs-lookup"><span data-stu-id="c7dc4-123">0x2</span></span>      |
| <span data-ttu-id="c7dc4-124">\_Ширина ддсд</span><span class="sxs-lookup"><span data-stu-id="c7dc4-124">DDSD\_WIDTH</span></span>       | <span data-ttu-id="c7dc4-125">Требуется в каждом файле. DDS.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-125">Required in every .dds file.</span></span>                                 | <span data-ttu-id="c7dc4-126">0x4</span><span class="sxs-lookup"><span data-stu-id="c7dc4-126">0x4</span></span>      |
| <span data-ttu-id="c7dc4-127">ДДСД \_ шаг</span><span class="sxs-lookup"><span data-stu-id="c7dc4-127">DDSD\_PITCH</span></span>       | <span data-ttu-id="c7dc4-128">Требуется, когда для несжатой текстуры указан шаг.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-128">Required when pitch is provided for an uncompressed texture.</span></span> | <span data-ttu-id="c7dc4-129">0x8</span><span class="sxs-lookup"><span data-stu-id="c7dc4-129">0x8</span></span>      |
| <span data-ttu-id="c7dc4-130">ДДСД \_ PIXELFORMAT</span><span class="sxs-lookup"><span data-stu-id="c7dc4-130">DDSD\_PIXELFORMAT</span></span> | <span data-ttu-id="c7dc4-131">Требуется в каждом файле. DDS.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-131">Required in every .dds file.</span></span>                                 | <span data-ttu-id="c7dc4-132">0x1000</span><span class="sxs-lookup"><span data-stu-id="c7dc4-132">0x1000</span></span>   |
| <span data-ttu-id="c7dc4-133">ДДСД \_ MIPMAPCOUNT</span><span class="sxs-lookup"><span data-stu-id="c7dc4-133">DDSD\_MIPMAPCOUNT</span></span> | <span data-ttu-id="c7dc4-134">Требуется в текстуре мипмаппед.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-134">Required in a mipmapped texture.</span></span>                             | <span data-ttu-id="c7dc4-135">0x20000</span><span class="sxs-lookup"><span data-stu-id="c7dc4-135">0x20000</span></span>  |
| <span data-ttu-id="c7dc4-136">ДДСД \_ линеарсизе</span><span class="sxs-lookup"><span data-stu-id="c7dc4-136">DDSD\_LINEARSIZE</span></span>  | <span data-ttu-id="c7dc4-137">Требуется, если для сжатой текстуры указан шаг.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-137">Required when pitch is provided for a compressed texture.</span></span>    | <span data-ttu-id="c7dc4-138">0x80000</span><span class="sxs-lookup"><span data-stu-id="c7dc4-138">0x80000</span></span>  |
| <span data-ttu-id="c7dc4-139">\_глубина ддсд</span><span class="sxs-lookup"><span data-stu-id="c7dc4-139">DDSD\_DEPTH</span></span>       | <span data-ttu-id="c7dc4-140">Требуется в текстуре глубины.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-140">Required in a depth texture.</span></span>                                 | <span data-ttu-id="c7dc4-141">0x800000</span><span class="sxs-lookup"><span data-stu-id="c7dc4-141">0x800000</span></span> |



 

> [!Note]  
> <span data-ttu-id="c7dc4-142">При записи файлов. DDS необходимо задать \_ Флаги ддсд Cap и ддсд \_ PIXELFORMAT, а для параметров мипмаппед — \_ флаг ддсд MIPMAPCOUNT.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-142">When you write .dds files, you should set the DDSD\_CAPS and DDSD\_PIXELFORMAT flags, and for mipmapped textures you should also set the DDSD\_MIPMAPCOUNT flag.</span></span> <span data-ttu-id="c7dc4-143">Однако при чтении DDS-файла не следует полагаться на \_ установленные флаги ддсд Cap, ддсд \_ PIXELFORMAT и ддсд \_ MIPMAPCOUNT, так как некоторые модули записи такого файла могут не устанавливать эти флаги.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-143">However, when you read a .dds file, you should not rely on the DDSD\_CAPS, DDSD\_PIXELFORMAT, and DDSD\_MIPMAPCOUNT flags being set because some writers of such a file might not set these flags.</span></span>

 

<span data-ttu-id="c7dc4-144">Флаг \_ текстуры заголовков DDS \_ \_ , определенный в DDS. h, является побитовым или сочетанием ДДСД \_ Caps, ддсд \_ Height, ддсд \_ Width и ддсд \_ PIXELFORMAT flags.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-144">The DDS\_HEADER\_FLAGS\_TEXTURE flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSD\_CAPS, DDSD\_HEIGHT, DDSD\_WIDTH, and DDSD\_PIXELFORMAT flags.</span></span>

<span data-ttu-id="c7dc4-145">\_ \_ Флаг mipmap заголовка DDS \_ , определенный в DDS. h, РАВЕН \_ флагу ддсд MIPMAPCOUNT.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-145">The DDS\_HEADER\_FLAGS\_MIPMAP flag, which is defined in Dds.h, is equal to the DDSD\_MIPMAPCOUNT flag.</span></span>

<span data-ttu-id="c7dc4-146">\_Флаг тома заголовков DDS \_ \_ , который определен в DDS. h, равен \_ флагу глубины ддсд.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-146">The DDS\_HEADER\_FLAGS\_VOLUME flag, which is defined in Dds.h, is equal to the DDSD\_DEPTH flag.</span></span>

<span data-ttu-id="c7dc4-147">\_ \_ Флаг высоты флагов заголовков DDS \_ , определенный в DDS. h, РАВЕН \_ флагу ддсд тон.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-147">The DDS\_HEADER\_FLAGS\_PITCH flag, which is defined in Dds.h, is equal to the DDSD\_PITCH flag.</span></span>

<span data-ttu-id="c7dc4-148">\_ \_ Флаг ЛИНЕАРСИЗЕ заголовка DDS \_ , определенный в DDS. h, РАВЕН \_ флагу ддсд линеарсизе.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-148">The DDS\_HEADER\_FLAGS\_LINEARSIZE flag, which is defined in Dds.h, is equal to the DDSD\_LINEARSIZE flag.</span></span>

</dd> <dt>

<span data-ttu-id="c7dc4-149">**двхеигхт**</span><span class="sxs-lookup"><span data-stu-id="c7dc4-149">**dwHeight**</span></span>
</dt> <dd>

<span data-ttu-id="c7dc4-150">Тип: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c7dc4-150">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="c7dc4-151">Высота поверхности (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="c7dc4-151">Surface height (in pixels).</span></span>

</dd> <dt>

<span data-ttu-id="c7dc4-152">**дввидс**</span><span class="sxs-lookup"><span data-stu-id="c7dc4-152">**dwWidth**</span></span>
</dt> <dd>

<span data-ttu-id="c7dc4-153">Тип: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c7dc4-153">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="c7dc4-154">Ширина поверхности (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="c7dc4-154">Surface width (in pixels).</span></span>

</dd> <dt>

<span data-ttu-id="c7dc4-155">**двпитчорлинеарсизе**</span><span class="sxs-lookup"><span data-stu-id="c7dc4-155">**dwPitchOrLinearSize**</span></span>
</dt> <dd>

<span data-ttu-id="c7dc4-156">Тип: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c7dc4-156">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="c7dc4-157">Шаг или количество байтов на строку развертки в несжатой текстуре; Общее число байтов в текстуре верхнего уровня для сжатой текстуры.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-157">The pitch or number of bytes per scan line in an uncompressed texture; the total number of bytes in the top level texture for a compressed texture.</span></span> <span data-ttu-id="c7dc4-158">Сведения о том, как вычислить шаг, см. в разделе Расположение файлов DDS [руководства по программированию для DDS](dx-graphics-dds-pguide.md).</span><span class="sxs-lookup"><span data-stu-id="c7dc4-158">For information about how to compute the pitch, see the DDS File Layout section of the [Programming Guide for DDS](dx-graphics-dds-pguide.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7dc4-159">**двдепс**</span><span class="sxs-lookup"><span data-stu-id="c7dc4-159">**dwDepth**</span></span>
</dt> <dd>

<span data-ttu-id="c7dc4-160">Тип: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c7dc4-160">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="c7dc4-161">Глубина текстуры тома (в пикселях), в противном случае неиспользуемая.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-161">Depth of a volume texture (in pixels), otherwise unused.</span></span>

</dd> <dt>

<span data-ttu-id="c7dc4-162">**двмипмапкаунт**</span><span class="sxs-lookup"><span data-stu-id="c7dc4-162">**dwMipMapCount**</span></span>
</dt> <dd>

<span data-ttu-id="c7dc4-163">Тип: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c7dc4-163">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="c7dc4-164">Количество уровней mipmap, в противном случае не используемое.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-164">Number of mipmap levels, otherwise unused.</span></span>

</dd> <dt>

<span data-ttu-id="c7dc4-165">**dwReserved1 \[ 11\]**</span><span class="sxs-lookup"><span data-stu-id="c7dc4-165">**dwReserved1\[11\]**</span></span>
</dt> <dd>

<span data-ttu-id="c7dc4-166">Тип: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c7dc4-166">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="c7dc4-167">Не используется.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-167">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="c7dc4-168">**ддспф**</span><span class="sxs-lookup"><span data-stu-id="c7dc4-168">**ddspf**</span></span>
</dt> <dd>

<span data-ttu-id="c7dc4-169">Тип: **[ **DDS \_ PIXELFORMAT**](dds-pixelformat.md)**</span><span class="sxs-lookup"><span data-stu-id="c7dc4-169">Type: **[**DDS\_PIXELFORMAT**](dds-pixelformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c7dc4-170">Формат пикселей (см. [**DDS \_ PIXELFORMAT**](dds-pixelformat.md)).</span><span class="sxs-lookup"><span data-stu-id="c7dc4-170">The pixel format (see [**DDS\_PIXELFORMAT**](dds-pixelformat.md)).</span></span>

</dd> <dt>

<span data-ttu-id="c7dc4-171">**двкапс**</span><span class="sxs-lookup"><span data-stu-id="c7dc4-171">**dwCaps**</span></span>
</dt> <dd>

<span data-ttu-id="c7dc4-172">Тип: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c7dc4-172">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="c7dc4-173">Указывает сложность хранимых поверхностей.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-173">Specifies the complexity of the surfaces stored.</span></span>



| <span data-ttu-id="c7dc4-174">Flag</span><span class="sxs-lookup"><span data-stu-id="c7dc4-174">Flag</span></span>             | <span data-ttu-id="c7dc4-175">Описание</span><span class="sxs-lookup"><span data-stu-id="c7dc4-175">Description</span></span>                                                                                                                              | <span data-ttu-id="c7dc4-176">Значение</span><span class="sxs-lookup"><span data-stu-id="c7dc4-176">Value</span></span>    |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------|----------|
| <span data-ttu-id="c7dc4-177">ДДСКАПС \_ сложный</span><span class="sxs-lookup"><span data-stu-id="c7dc4-177">DDSCAPS\_COMPLEX</span></span> | <span data-ttu-id="c7dc4-178">Используемых должен использоваться для любого файла, содержащего более одной поверхности (mipmap, карту кубической среды или текстуру тома мипмаппед).</span><span class="sxs-lookup"><span data-stu-id="c7dc4-178">Optional; must be used on any file that contains more than one surface (a mipmap, a cubic environment map, or mipmapped volume texture).</span></span> | <span data-ttu-id="c7dc4-179">0x8</span><span class="sxs-lookup"><span data-stu-id="c7dc4-179">0x8</span></span>      |
| <span data-ttu-id="c7dc4-180">ДДСКАПС \_ mipmap</span><span class="sxs-lookup"><span data-stu-id="c7dc4-180">DDSCAPS\_MIPMAP</span></span>  | <span data-ttu-id="c7dc4-181">Используемых должен использоваться для mipmap.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-181">Optional; should be used for a mipmap.</span></span>                                                                                                   | <span data-ttu-id="c7dc4-182">0x400000</span><span class="sxs-lookup"><span data-stu-id="c7dc4-182">0x400000</span></span> |
| <span data-ttu-id="c7dc4-183">\_текстура ддскапс</span><span class="sxs-lookup"><span data-stu-id="c7dc4-183">DDSCAPS\_TEXTURE</span></span> | <span data-ttu-id="c7dc4-184">Обязательно</span><span class="sxs-lookup"><span data-stu-id="c7dc4-184">Required</span></span>                                                                                                                                 | <span data-ttu-id="c7dc4-185">0x1000</span><span class="sxs-lookup"><span data-stu-id="c7dc4-185">0x1000</span></span>   |



 

> [!Note]  
> <span data-ttu-id="c7dc4-186">При записи файлов. DDS следует задать \_ флаг текстуры ддскапс, а для нескольких поверхностей также следует задать \_ сложный флаг ддскапс.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-186">When you write .dds files, you should set the DDSCAPS\_TEXTURE flag, and for multiple surfaces you should also set the DDSCAPS\_COMPLEX flag.</span></span> <span data-ttu-id="c7dc4-187">Однако при чтении DDS-файла не следует полагаться на ДДСКАПС \_ текстуры и ддскапс \_ сложные флаги, так как некоторые модули записи такого файла могут не устанавливать эти флаги.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-187">However, when you read a .dds file, you should not rely on the DDSCAPS\_TEXTURE and DDSCAPS\_COMPLEX flags being set because some writers of such a file might not set these flags.</span></span>

 

<span data-ttu-id="c7dc4-188">Флаг \_ \_ \_ mipmap, который определен в DDS. h, является побитовым или сочетанием ДДСКАПС \_ Complex и ддскапс \_ mipmap.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-188">The DDS\_SURFACE\_FLAGS\_MIPMAP flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS\_COMPLEX and DDSCAPS\_MIPMAP flags.</span></span>

<span data-ttu-id="c7dc4-189">Флаг \_ текстуры в области DDS \_ \_ , определенный в DDS. h, равен \_ флагу текстуры ддскапс.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-189">The DDS\_SURFACE\_FLAGS\_TEXTURE flag, which is defined in Dds.h, is equal to the DDSCAPS\_TEXTURE flag.</span></span>

<span data-ttu-id="c7dc4-190">Флаг \_ кубической карты в области DDS \_ \_ , определенный в DDS. h, равен \_ сложному флагу ддскапс.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-190">The DDS\_SURFACE\_FLAGS\_CUBEMAP flag, which is defined in Dds.h, is equal to the DDSCAPS\_COMPLEX flag.</span></span>

</dd> <dt>

<span data-ttu-id="c7dc4-191">**dwCaps2**</span><span class="sxs-lookup"><span data-stu-id="c7dc4-191">**dwCaps2**</span></span>
</dt> <dd>

<span data-ttu-id="c7dc4-192">Тип: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c7dc4-192">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="c7dc4-193">Дополнительные сведения о хранимых поверхностях.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-193">Additional detail about the surfaces stored.</span></span>



| <span data-ttu-id="c7dc4-194">Flag</span><span class="sxs-lookup"><span data-stu-id="c7dc4-194">Flag</span></span>                         | <span data-ttu-id="c7dc4-195">Описание</span><span class="sxs-lookup"><span data-stu-id="c7dc4-195">Description</span></span>                                            | <span data-ttu-id="c7dc4-196">Значение</span><span class="sxs-lookup"><span data-stu-id="c7dc4-196">Value</span></span>    |
|------------------------------|--------------------------------------------------------|----------|
| <span data-ttu-id="c7dc4-197">DDSCAPS2 \_ кубической карты</span><span class="sxs-lookup"><span data-stu-id="c7dc4-197">DDSCAPS2\_CUBEMAP</span></span>            | <span data-ttu-id="c7dc4-198">Требуется для схемы куба.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-198">Required for a cube map.</span></span>                               | <span data-ttu-id="c7dc4-199">0x200</span><span class="sxs-lookup"><span data-stu-id="c7dc4-199">0x200</span></span>    |
| <span data-ttu-id="c7dc4-200">DDSCAPS2 \_ кубической карты \_ поситивекс</span><span class="sxs-lookup"><span data-stu-id="c7dc4-200">DDSCAPS2\_CUBEMAP\_POSITIVEX</span></span> | <span data-ttu-id="c7dc4-201">Требуется, если эти поверхности хранятся в карте Куба.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-201">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="c7dc4-202">0x400</span><span class="sxs-lookup"><span data-stu-id="c7dc4-202">0x400</span></span>    |
| <span data-ttu-id="c7dc4-203">DDSCAPS2 \_ кубической карты \_ негативекс</span><span class="sxs-lookup"><span data-stu-id="c7dc4-203">DDSCAPS2\_CUBEMAP\_NEGATIVEX</span></span> | <span data-ttu-id="c7dc4-204">Требуется, если эти поверхности хранятся в карте Куба.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-204">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="c7dc4-205">0x800</span><span class="sxs-lookup"><span data-stu-id="c7dc4-205">0x800</span></span>    |
| <span data-ttu-id="c7dc4-206">DDSCAPS2 \_ кубической карты \_</span><span class="sxs-lookup"><span data-stu-id="c7dc4-206">DDSCAPS2\_CUBEMAP\_POSITIVEY</span></span> | <span data-ttu-id="c7dc4-207">Требуется, если эти поверхности хранятся в карте Куба.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-207">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="c7dc4-208">0x1000</span><span class="sxs-lookup"><span data-stu-id="c7dc4-208">0x1000</span></span>   |
| <span data-ttu-id="c7dc4-209">DDSCAPS2 \_ кубической карты \_ отрицательно</span><span class="sxs-lookup"><span data-stu-id="c7dc4-209">DDSCAPS2\_CUBEMAP\_NEGATIVEY</span></span> | <span data-ttu-id="c7dc4-210">Требуется, если эти поверхности хранятся в карте Куба.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-210">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="c7dc4-211">0x2000</span><span class="sxs-lookup"><span data-stu-id="c7dc4-211">0x2000</span></span>   |
| <span data-ttu-id="c7dc4-212">DDSCAPS2 \_ кубической карты \_ поситивез</span><span class="sxs-lookup"><span data-stu-id="c7dc4-212">DDSCAPS2\_CUBEMAP\_POSITIVEZ</span></span> | <span data-ttu-id="c7dc4-213">Требуется, если эти поверхности хранятся в карте Куба.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-213">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="c7dc4-214">0x4000</span><span class="sxs-lookup"><span data-stu-id="c7dc4-214">0x4000</span></span>   |
| <span data-ttu-id="c7dc4-215">DDSCAPS2 \_ кубической карты \_ негативез</span><span class="sxs-lookup"><span data-stu-id="c7dc4-215">DDSCAPS2\_CUBEMAP\_NEGATIVEZ</span></span> | <span data-ttu-id="c7dc4-216">Требуется, если эти поверхности хранятся в карте Куба.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-216">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="c7dc4-217">0x8000</span><span class="sxs-lookup"><span data-stu-id="c7dc4-217">0x8000</span></span>   |
| <span data-ttu-id="c7dc4-218">\_Том DDSCAPS2</span><span class="sxs-lookup"><span data-stu-id="c7dc4-218">DDSCAPS2\_VOLUME</span></span>             | <span data-ttu-id="c7dc4-219">Требуется для текстуры тома.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-219">Required for a volume texture.</span></span>                         | <span data-ttu-id="c7dc4-220">0x200000</span><span class="sxs-lookup"><span data-stu-id="c7dc4-220">0x200000</span></span> |



 

<span data-ttu-id="c7dc4-221">\_ \_ Флаг КУБИЧЕСКОЙ карты поситивекс DDS, который определен в DDS. h, представляет собой побитовое или сочетание \_ \_ флагов DDSCAPS2 кубической карты и DDSCAPS2 кубической карты поситивекс \_ .</span><span class="sxs-lookup"><span data-stu-id="c7dc4-221">The DDS\_CUBEMAP\_POSITIVEX flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_POSITIVEX flags.</span></span>

<span data-ttu-id="c7dc4-222">\_ \_ Флаг КУБИЧЕСКОЙ карты негативекс DDS, который определен в DDS. h, представляет собой побитовое или сочетание \_ \_ флагов DDSCAPS2 кубической карты и DDSCAPS2 кубической карты негативекс \_ .</span><span class="sxs-lookup"><span data-stu-id="c7dc4-222">The DDS\_CUBEMAP\_NEGATIVEX flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_NEGATIVEX flags.</span></span>

<span data-ttu-id="c7dc4-223">\_ \_ Флаг положительный кубической карты DDS, определенный в DDS. h, представляет собой побитовое или сочетание DDSCAPS2 \_ кубической карты и DDSCAPS2 \_ кубической карты \_ .</span><span class="sxs-lookup"><span data-stu-id="c7dc4-223">The DDS\_CUBEMAP\_POSITIVEY flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_POSITIVEY flags.</span></span>

<span data-ttu-id="c7dc4-224">\_ \_ Флаг отрицательного кубической карты DDS, определенный в DDS. h, представляет собой побитовое или сочетание DDSCAPS2 \_ кубической карты и DDSCAPS2 \_ кубической карты \_ негативных флагов.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-224">The DDS\_CUBEMAP\_NEGATIVEY flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_NEGATIVEY flags.</span></span>

<span data-ttu-id="c7dc4-225">\_ \_ Флаг КУБИЧЕСКОЙ карты поситивез DDS, который определен в DDS. h, представляет собой побитовое или сочетание \_ \_ флагов DDSCAPS2 кубической карты и DDSCAPS2 кубической карты поситивез \_ .</span><span class="sxs-lookup"><span data-stu-id="c7dc4-225">The DDS\_CUBEMAP\_POSITIVEZ flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_POSITIVEZ flags.</span></span>

<span data-ttu-id="c7dc4-226">\_ \_ Флаг КУБИЧЕСКОЙ карты негативез DDS, который определен в DDS. h, представляет собой побитовое или сочетание \_ \_ флагов DDSCAPS2 кубической карты и DDSCAPS2 кубической карты негативез \_ .</span><span class="sxs-lookup"><span data-stu-id="c7dc4-226">The DDS\_CUBEMAP\_NEGATIVEZ flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_NEGATIVEZ flags.</span></span>

<span data-ttu-id="c7dc4-227">\_ \_ Флаг КУБИЧЕСКОЙ карты аллфацес DDS, который определен в DDS. h, является побитовым или сочетанием DDS \_ КУБИЧЕСКОЙ карты \_ поситивекс, DDS \_ кубической карты \_ НЕГАТИВЕКС, DDS \_ КУБИЧЕСКОЙ карты \_ , DDS \_ кубической карты \_ негатив, DDS \_ кубической карты \_ поситивез и DDSCAPS2 \_ кубической карты \_ негативез flags.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-227">The DDS\_CUBEMAP\_ALLFACES flag, which is defined in Dds.h, is a bitwise-OR combination of the DDS\_CUBEMAP\_POSITIVEX, DDS\_CUBEMAP\_NEGATIVEX, DDS\_CUBEMAP\_POSITIVEY, DDS\_CUBEMAP\_NEGATIVEY, DDS\_CUBEMAP\_POSITIVEZ, and DDSCAPS2\_CUBEMAP\_NEGATIVEZ flags.</span></span>

<span data-ttu-id="c7dc4-228">\_Флаг тома DDS flags \_ , определенный в DDS. h, равен \_ флагу тома DDSCAPS2.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-228">The DDS\_FLAGS\_VOLUME flag, which is defined in Dds.h, is equal to the DDSCAPS2\_VOLUME flag.</span></span>

> [!Note]  
> <span data-ttu-id="c7dc4-229">Хотя Direct3D 9 поддерживает частичные карты кубов, Direct3D 10, 10,1 и 11, необходимо определить все шесть граней карты Куба (то есть необходимо установить DDS \_ кубической карты \_ аллфацес).</span><span class="sxs-lookup"><span data-stu-id="c7dc4-229">Although Direct3D 9 supports partial cube-maps, Direct3D 10, 10.1, and 11 require that you define all six cube-map faces (that is, you must set DDS\_CUBEMAP\_ALLFACES).</span></span>

 

</dd> <dt>

<span data-ttu-id="c7dc4-230">**dwCaps3**</span><span class="sxs-lookup"><span data-stu-id="c7dc4-230">**dwCaps3**</span></span>
</dt> <dd>

<span data-ttu-id="c7dc4-231">Тип: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c7dc4-231">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="c7dc4-232">Не используется.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-232">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="c7dc4-233">**dwCaps4**</span><span class="sxs-lookup"><span data-stu-id="c7dc4-233">**dwCaps4**</span></span>
</dt> <dd>

<span data-ttu-id="c7dc4-234">Тип: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c7dc4-234">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="c7dc4-235">Не используется.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-235">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="c7dc4-236">**dwReserved2**</span><span class="sxs-lookup"><span data-stu-id="c7dc4-236">**dwReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="c7dc4-237">Тип: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c7dc4-237">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="c7dc4-238">Не используется.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-238">Unused.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7dc4-239">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c7dc4-239">Remarks</span></span>

<span data-ttu-id="c7dc4-240">Включите флаги в **dwFlags** для элементов структуры, содержащих допустимые данные.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-240">Include flags in **dwFlags** for the members of the structure that contain valid data.</span></span>

<span data-ttu-id="c7dc4-241">Используйте эту структуру в сочетании с [**\_ заголовком DDS \_ DXT10**](dds-header-dxt10.md) для хранения массива ресурсов в файле DDS.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-241">Use this structure in combination with a [**DDS\_HEADER\_DXT10**](dds-header-dxt10.md) to store a resource array in a DDS file.</span></span> <span data-ttu-id="c7dc4-242">Дополнительные сведения см. в разделе [массивы текстур](dx-graphics-dds-pguide.md).</span><span class="sxs-lookup"><span data-stu-id="c7dc4-242">For more information, see [texture arrays](dx-graphics-dds-pguide.md).</span></span>

<span data-ttu-id="c7dc4-243">**DDS \_ ЗАГОЛОВОК** идентичен структуре DIRECTDRAW DDSURFACEDESC2 без зависимостей DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="c7dc4-243">**DDS\_HEADER** is identical to the DirectDraw DDSURFACEDESC2 structure without DirectDraw dependencies.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7dc4-244">Требования</span><span class="sxs-lookup"><span data-stu-id="c7dc4-244">Requirements</span></span>



| <span data-ttu-id="c7dc4-245">Требование</span><span class="sxs-lookup"><span data-stu-id="c7dc4-245">Requirement</span></span> | <span data-ttu-id="c7dc4-246">Значение</span><span class="sxs-lookup"><span data-stu-id="c7dc4-246">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c7dc4-247">Header</span><span class="sxs-lookup"><span data-stu-id="c7dc4-247">Header</span></span><br/> | <dl> <span data-ttu-id="c7dc4-248"><dt>DDS. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7dc4-248"><dt>Dds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7dc4-249">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7dc4-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7dc4-250">Справочник по DDS</span><span class="sxs-lookup"><span data-stu-id="c7dc4-250">Reference for DDS</span></span>](dx-graphics-dds-reference.md)
</dt> </dl>

 

