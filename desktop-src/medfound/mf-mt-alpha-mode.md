---
description: Указывает, является ли режим альфа для видеороликов цветового носителя предварительно умноженным или прямым.
ms.assetid: A263C3F7-357B-426D-B38C-533F9F6A1262
title: Атрибут MF_MT_ALPHA_MODE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06b81da14bc0a9e089a5af4815e5bf97359a9cb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080867"
---
# <a name="mf_mt_alpha_mode-attribute"></a><span data-ttu-id="6ae17-103">\_Атрибут « \_ альфа- \_ режим» MF MT</span><span class="sxs-lookup"><span data-stu-id="6ae17-103">MF\_MT\_ALPHA\_MODE attribute</span></span>

<span data-ttu-id="6ae17-104">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="6ae17-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6ae17-105">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="6ae17-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6ae17-106">Указывает, является ли режим альфа для видеороликов цветового носителя предварительно умноженным или прямым.</span><span class="sxs-lookup"><span data-stu-id="6ae17-106">Specifies whether the alpha mode for color media video types is premultiplied or straight.</span></span>

## <a name="data-type"></a><span data-ttu-id="6ae17-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6ae17-107">Data type</span></span>

<span data-ttu-id="6ae17-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="6ae17-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="6ae17-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6ae17-109">Remarks</span></span>

<span data-ttu-id="6ae17-110">Это значение можно привести к значению [**\_ \_ режима альфа-канала DXGI**](/windows/win32/api/dxgi1_2/ne-dxgi1_2-dxgi_alpha_mode) .</span><span class="sxs-lookup"><span data-stu-id="6ae17-110">This value can be cast to a [**DXGI\_ALPHA\_MODE**](/windows/win32/api/dxgi1_2/ne-dxgi1_2-dxgi_alpha_mode) value.</span></span> <span data-ttu-id="6ae17-111">Если этот атрибут отсутствует, для обеспечения обратной совместимости это значение является **\_ \_ режимом \_ "DXGI Alpha" непосредственно** для видеоформата, поддерживающего альфа-канал, например ARGB32, или **\_ режим альфа Alpha, \_ \_ игнорирующий** формат видео без альфа-канала, например RGB32.</span><span class="sxs-lookup"><span data-stu-id="6ae17-111">If this attribute isn’t present, for backward compatibility, the value is **DXGI\_ALPHA\_MODE\_STRAIGHT** for video format supporting alpha channel, such as ARGB32, or **DXGI\_ALPHA\_MODE\_IGNORE** for video format without alpha channel, such as RGB32.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ae17-112">Требования</span><span class="sxs-lookup"><span data-stu-id="6ae17-112">Requirements</span></span>



| <span data-ttu-id="6ae17-113">Требование</span><span class="sxs-lookup"><span data-stu-id="6ae17-113">Requirement</span></span> | <span data-ttu-id="6ae17-114">Значение</span><span class="sxs-lookup"><span data-stu-id="6ae17-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6ae17-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6ae17-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6ae17-116">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="6ae17-116">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6ae17-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6ae17-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6ae17-118">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="6ae17-118">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="6ae17-119">Header</span><span class="sxs-lookup"><span data-stu-id="6ae17-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ae17-120"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ae17-120"><dt>Mfapi.h</dt></span></span> </dl> |



 

 
