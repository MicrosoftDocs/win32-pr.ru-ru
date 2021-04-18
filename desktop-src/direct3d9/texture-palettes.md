---
description: Direct3D 9 поддерживает текстуры с палитрой, используя набор из 256 палитр записей, связанных с объектом IDirect3DDevice9.
ms.assetid: dea4b4bc-7eba-40fa-9c2c-0851fe7e231b
title: Палитры текстур (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a0fbb1c5d6766b879b898145ec2385a41d94b8e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105701111"
---
# <a name="texture-palettes-direct3d-9"></a><span data-ttu-id="846d8-103">Палитры текстур (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="846d8-103">Texture Palettes (Direct3D 9)</span></span>

<span data-ttu-id="846d8-104">Direct3D 9 поддерживает текстуры с палитрой, используя набор из 256 палитр записей, связанных с объектом [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="846d8-104">Direct3D 9 supports paletted textures through a set of 256 entry palettes associated with the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) object.</span></span> <span data-ttu-id="846d8-105">Палитра становится текущей путем вызова метода [**IDirect3DDevice9:: сеткурренттекстурепалетте**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="846d8-105">A palette is made current by calling the [**IDirect3DDevice9::SetCurrentTexturePalette**](/windows/desktop/api) method.</span></span> <span data-ttu-id="846d8-106">Текущая палитра используется для преобразования всех текстур с палитрой для всех активных стадий текстуры.</span><span class="sxs-lookup"><span data-stu-id="846d8-106">The current palette is used for translating all paletted textures for all active texture stages.</span></span> <span data-ttu-id="846d8-107">[**IDirect3DDevice9:: сетпалеттинтриес**](/windows/desktop/api) обновляет все записи 256 палитры.</span><span class="sxs-lookup"><span data-stu-id="846d8-107">[**IDirect3DDevice9::SetPaletteEntries**](/windows/desktop/api) updates all of a palette's 256 entries.</span></span> <span data-ttu-id="846d8-108">Каждая запись является структурой [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) формата D3DFMT \_ A8R8G8B8.</span><span class="sxs-lookup"><span data-stu-id="846d8-108">Each entry is a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure of the format D3DFMT\_A8R8G8B8.</span></span> <span data-ttu-id="846d8-109">Все записи по умолчанию имеют значение 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="846d8-109">All entries default to 0xFFFFFFFF.</span></span>

<span data-ttu-id="846d8-110">Палитры [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) содержат альфа-канал.</span><span class="sxs-lookup"><span data-stu-id="846d8-110">The [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) palettes contain an alpha channel.</span></span> <span data-ttu-id="846d8-111">Этот альфа-канал можно использовать \_ , если установлен флаг возможности устройства D3DPTEXTURECAPS алфапалетте, указывающий, что устройство поддерживает альфа-версию из палитры.</span><span class="sxs-lookup"><span data-stu-id="846d8-111">This alpha channel can be used when the D3DPTEXTURECAPS\_ALPHAPALETTE device capability flag is set, indicating that the device supports alpha from the palette.</span></span> <span data-ttu-id="846d8-112">Альфа-канал палитры используется, если формат текстуры не имеет альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="846d8-112">The palette alpha channel is used when the texture format does not have an alpha channel.</span></span> <span data-ttu-id="846d8-113">Если устройство не поддерживает альфа-канал из палитры, а формат текстуры не имеет альфа-канала, для Alpha используется значение 0xFF.</span><span class="sxs-lookup"><span data-stu-id="846d8-113">If the device does not support alpha from the palette and the texture format does not have an alpha channel, then a value of 0xFF is used for alpha.</span></span>

<span data-ttu-id="846d8-114">Существует максимум 65 536 (0x0000FFFF) палитр.</span><span class="sxs-lookup"><span data-stu-id="846d8-114">There is a maximum of 65,536 (0x0000FFFF) palettes.</span></span> <span data-ttu-id="846d8-115">Так как ресурсы памяти, связанные с набором палитр, пропорциональны максимальному значению палитры, на которое ссылается приложение, используйте смежные цифры палитры, начинающиеся с нуля.</span><span class="sxs-lookup"><span data-stu-id="846d8-115">Because memory resources associated with the set of palettes are proportional to the maximum palette number that an application references, use contiguous palette numbers starting at zero.</span></span>

## <a name="related-topics"></a><span data-ttu-id="846d8-116">См. также</span><span class="sxs-lookup"><span data-stu-id="846d8-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="846d8-117">Основные понятия текстурирования</span><span class="sxs-lookup"><span data-stu-id="846d8-117">Basic Texturing Concepts</span></span>](basic-texturing-concepts.md)
</dt> </dl>

 

 
