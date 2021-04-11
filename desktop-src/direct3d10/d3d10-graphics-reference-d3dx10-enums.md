---
description: 'В этом разделе содержатся сведения о следующих перечислимых типах и флагах, используемых с D3DX.:'
ms.assetid: 8836f350-9edd-4521-b7a3-3aa827394c57
title: Перечисления D3DX (графика Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a34ae9c1b275376343ecab321ab9e7762c59fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262695"
---
# <a name="d3dx-enumerations-direct3d-10-graphics"></a><span data-ttu-id="f6424-103">Перечисления D3DX (графика Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="f6424-103">D3DX Enumerations (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="f6424-104">В этом разделе содержатся сведения о следующих перечислимых типах и флагах, используемых с D3DX.:</span><span class="sxs-lookup"><span data-stu-id="f6424-104">This section contains information about the following enumerated types and flags used with D3DX.:</span></span>



| <span data-ttu-id="f6424-105">Перечисление</span><span class="sxs-lookup"><span data-stu-id="f6424-105">Enumeration</span></span>                                                       | <span data-ttu-id="f6424-106">Описание</span><span class="sxs-lookup"><span data-stu-id="f6424-106">Description</span></span>                                                                                                                                                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f6424-107">**\_Флаг канала \_ D3DX10**</span><span class="sxs-lookup"><span data-stu-id="f6424-107">**D3DX10\_CHANNEL\_FLAG**</span></span>](d3dx10-channel-flag.md)              | <span data-ttu-id="f6424-108">Эти флаги используются функциями, которые работают с одним или несколькими каналами в текстуре.</span><span class="sxs-lookup"><span data-stu-id="f6424-108">These flags are used by functions which operate on one or more channels in a texture.</span></span>                                                                                                  |
| [<span data-ttu-id="f6424-109">**\_Оптимизация ЦП \_ D3DX**</span><span class="sxs-lookup"><span data-stu-id="f6424-109">**D3DX\_CPU\_OPTIMIZATION**</span></span>](d3dx-cpu-optimization.md)          | <span data-ttu-id="f6424-110">Указывает, что набор инструкций D3DX в настоящее время оптимизирован для.</span><span class="sxs-lookup"><span data-stu-id="f6424-110">Specifies the instruction set D3DX is currently optimized for.</span></span>                                                                                                                         |
| [<span data-ttu-id="f6424-111">**D3DX10 \_ Err**</span><span class="sxs-lookup"><span data-stu-id="f6424-111">**D3DX10\_ERR**</span></span>](d3dx10-err.md)                                 | <span data-ttu-id="f6424-112">Ошибки представлены отрицательными значениями и не могут быть объединены.</span><span class="sxs-lookup"><span data-stu-id="f6424-112">Errors are represented by negative values and cannot be combined.</span></span>                                                                                                                      |
| [<span data-ttu-id="f6424-113">**\_Флаг фильтра \_ D3DX10**</span><span class="sxs-lookup"><span data-stu-id="f6424-113">**D3DX10\_FILTER\_FLAG**</span></span>](d3dx10-filter-flag.md)                | <span data-ttu-id="f6424-114">Флаги фильтрации текстур.</span><span class="sxs-lookup"><span data-stu-id="f6424-114">Texture filtering flags.</span></span>                                                                                                                                                               |
| [<span data-ttu-id="f6424-115">**\_ \_ Формат файла изображения \_ D3DX10**</span><span class="sxs-lookup"><span data-stu-id="f6424-115">**D3DX10\_IMAGE\_FILE\_FORMAT**</span></span>](d3dx10-image-file-format.md)   | <span data-ttu-id="f6424-116">Описывает поддерживаемые форматы файлов изображений.</span><span class="sxs-lookup"><span data-stu-id="f6424-116">Describes the supported image file formats.</span></span>                                                                                                                                            |
| [<span data-ttu-id="f6424-117">**\_Сетка D3DX10**</span><span class="sxs-lookup"><span data-stu-id="f6424-117">**D3DX10\_MESH**</span></span>](d3dx10-mesh.md)                               | <span data-ttu-id="f6424-118">Флаги, используемые для указания параметров создания сетки.</span><span class="sxs-lookup"><span data-stu-id="f6424-118">Flags used to specify creation options for a mesh.</span></span>                                                                                                                                     |
| [<span data-ttu-id="f6424-119">**\_ \_ Флаги удаления сетки D3DX10 \_**</span><span class="sxs-lookup"><span data-stu-id="f6424-119">**D3DX10\_MESH\_DISCARD\_FLAGS**</span></span>](d3dx10-mesh-discard-flags.md) | <span data-ttu-id="f6424-120">Указывает, какие части данных сетки следует отбросить от устройства.</span><span class="sxs-lookup"><span data-stu-id="f6424-120">Specifies which pieces of mesh data to discard from the device.</span></span> <span data-ttu-id="f6424-121">Используется с [**ID3DX10Mesh::D**](id3dx10mesh-discard.md).</span><span class="sxs-lookup"><span data-stu-id="f6424-121">Used with [**ID3DX10Mesh::Discard**](id3dx10mesh-discard.md).</span></span>                                                         |
| [<span data-ttu-id="f6424-122">**D3DX10 \_ мешопт**</span><span class="sxs-lookup"><span data-stu-id="f6424-122">**D3DX10\_MESHOPT**</span></span>](d3dx10-meshopt.md)                         | <span data-ttu-id="f6424-123">Указывает тип оптимизации сетки для выполнения.</span><span class="sxs-lookup"><span data-stu-id="f6424-123">Specifies the type of mesh optimization to be performed.</span></span>                                                                                                                               |
| [<span data-ttu-id="f6424-124">**\_Флаг НОРМАЛМАП \_ D3DX10**</span><span class="sxs-lookup"><span data-stu-id="f6424-124">**D3DX10\_NORMALMAP\_FLAG**</span></span>](d3dx10-normalmap-flag.md)          | <span data-ttu-id="f6424-125">Эти флаги используются для управления тем, как [**D3DX10ComputeNormalMap**](d3dx10computenormalmap.md) создает нормальные карты.</span><span class="sxs-lookup"><span data-stu-id="f6424-125">These flags are used to control how [**D3DX10ComputeNormalMap**](d3dx10computenormalmap.md) generates normal maps.</span></span> <span data-ttu-id="f6424-126">Любое число этих флагов может быть или в любом сочетании.</span><span class="sxs-lookup"><span data-stu-id="f6424-126">Any number of these flags may be OR'd together in any combination.</span></span> |
| [<span data-ttu-id="f6424-127">**D3DX10 \_ Сохранить \_ \_ флаг текстуры**</span><span class="sxs-lookup"><span data-stu-id="f6424-127">**D3DX10\_SAVE\_TEXTURE\_FLAG**</span></span>](d3dx10-save-texture-flag.md)   | <span data-ttu-id="f6424-128">Параметры сохранения текстуры.</span><span class="sxs-lookup"><span data-stu-id="f6424-128">Texture save options.</span></span>                                                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="f6424-129">См. также</span><span class="sxs-lookup"><span data-stu-id="f6424-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6424-130">Справочник по D3DX</span><span class="sxs-lookup"><span data-stu-id="f6424-130">D3DX Reference</span></span>](d3d10-graphics-reference-d3dx10.md)
</dt> </dl>

 

 



