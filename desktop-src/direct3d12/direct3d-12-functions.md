---
title: Основные функции (графика Direct3D 12)
description: Следующие функции объявляются в d3d12. h.
ms.assetid: C0F9A52C-483D-40B2-9E1F-CB92ADDC2856
ms.localizationpriority: low
ms.topic: article
ms.date: 11/27/2018
ms.openlocfilehash: 99ec8516634a0a59262df9862e03732c9d6d579a
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/12/2019
ms.locfileid: "105700783"
---
# <a name="core-functions"></a><span data-ttu-id="50c98-103">Базовые функции</span><span class="sxs-lookup"><span data-stu-id="50c98-103">Core functions</span></span>

<span data-ttu-id="50c98-104">Следующие функции объявляются в d3d12. h.</span><span class="sxs-lookup"><span data-stu-id="50c98-104">The following functions are declared in d3d12.h.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="50c98-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="50c98-105">In this section</span></span>

| <span data-ttu-id="50c98-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="50c98-106">Topic</span></span> | <span data-ttu-id="50c98-107">Описание</span><span class="sxs-lookup"><span data-stu-id="50c98-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="50c98-108">**D3D12CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="50c98-108">**D3D12CreateDevice**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) | <span data-ttu-id="50c98-109">Создает устройство, представляющее адаптер дисплея.</span><span class="sxs-lookup"><span data-stu-id="50c98-109">Creates a device that represents the display adapter.</span></span> |
| [<span data-ttu-id="50c98-110">**D3D12CreateRootSignatureDeserializer**</span><span class="sxs-lookup"><span data-stu-id="50c98-110">**D3D12CreateRootSignatureDeserializer**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) | <span data-ttu-id="50c98-111">Десериализует корневую подпись, чтобы можно было определить Определение макета ([**D3D12 \_ корневая \_ сигнатура \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)).</span><span class="sxs-lookup"><span data-stu-id="50c98-111">Deserializes a root signature so you can determine the layout definition ([**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)).</span></span> |
| [<span data-ttu-id="50c98-112">**D3D12CreateVersionedRootSignatureDeserializer**</span><span class="sxs-lookup"><span data-stu-id="50c98-112">**D3D12CreateVersionedRootSignatureDeserializer**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12createversionedrootsignaturedeserializer) | <span data-ttu-id="50c98-113">Создает интерфейс, который может возвращать десериализованную структуру данных через [**жетунконвертедрутсигнатуредеск**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc).</span><span class="sxs-lookup"><span data-stu-id="50c98-113">Generates an interface that can return the deserialized data structure, via [**GetUnconvertedRootSignatureDesc**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc).</span></span> |
| [<span data-ttu-id="50c98-114">**D3D12EnableExperimentalFeatures**</span><span class="sxs-lookup"><span data-stu-id="50c98-114">**D3D12EnableExperimentalFeatures**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12enableexperimentalfeatures) | <span data-ttu-id="50c98-115">Включает список экспериментальных функций.</span><span class="sxs-lookup"><span data-stu-id="50c98-115">Enables a list of experimental features.</span></span> |
| [<span data-ttu-id="50c98-116">**D3D12GetDebugInterface**</span><span class="sxs-lookup"><span data-stu-id="50c98-116">**D3D12GetDebugInterface**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12getdebuginterface) | <span data-ttu-id="50c98-117">Возвращает интерфейс отладки.</span><span class="sxs-lookup"><span data-stu-id="50c98-117">Gets a debug interface.</span></span> |
| [<span data-ttu-id="50c98-118">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="50c98-118">**D3D12SerializeRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature) | <span data-ttu-id="50c98-119">Сериализует корневую подпись версии 1,0, которую можно передать в [**ID3D12Device:: креатерутсигнатуре**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span><span class="sxs-lookup"><span data-stu-id="50c98-119">Serializes a root signature version 1.0 that can be passed to [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span></span> |
| [<span data-ttu-id="50c98-120">**D3D12SerializeVersionedRootSignature**</span><span class="sxs-lookup"><span data-stu-id="50c98-120">**D3D12SerializeVersionedRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature) | <span data-ttu-id="50c98-121">Сериализует корневую подпись любой версии, которую можно передать в [**ID3D12Device:: креатерутсигнатуре**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span><span class="sxs-lookup"><span data-stu-id="50c98-121">Serializes a root signature of any version that can be passed to [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span></span> |

## <a name="related-topics"></a><span data-ttu-id="50c98-122">См. также</span><span class="sxs-lookup"><span data-stu-id="50c98-122">Related topics</span></span>

* [<span data-ttu-id="50c98-123">Справочник по коду</span><span class="sxs-lookup"><span data-stu-id="50c98-123">Core reference</span></span>](direct3d-12-core-reference.md)
* [<span data-ttu-id="50c98-124">Справочник по Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="50c98-124">Direct3D 12 reference</span></span>](direct3d-12-reference.md)






