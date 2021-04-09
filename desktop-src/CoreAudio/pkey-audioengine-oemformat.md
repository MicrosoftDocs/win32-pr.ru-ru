---
description: Свойство PKEY \_ аудиоенгине \_ оемформат задает формат по умолчанию для устройства, используемого для отрисовки или записи потока. Значения заполняются поставщиком вычислительной техники в INF-файле.
ms.assetid: 3a199ecf-642c-491c-a565-f0083783d180
title: PKEY_AudioEngine_OEMFormat (Ммдевицеапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be7ed65ae8a7bd717992b13dc7b5517a5725b241
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142418"
---
# <a name="pkey_audioengine_oemformat"></a><span data-ttu-id="e61b2-104">PKEY \_ аудиоенгине \_ оемформат</span><span class="sxs-lookup"><span data-stu-id="e61b2-104">PKEY\_AudioEngine\_OEMFormat</span></span>

<span data-ttu-id="e61b2-105">Свойство PKEY \_ аудиоенгине \_ оемформат задает формат по умолчанию для устройства, используемого для отрисовки или записи потока.</span><span class="sxs-lookup"><span data-stu-id="e61b2-105">The PKEY\_AudioEngine\_OEMFormat property specifies the default format of the device that is used for rendering or capturing a stream.</span></span> <span data-ttu-id="e61b2-106">Значения заполняются поставщиком вычислительной техники в INF-файле.</span><span class="sxs-lookup"><span data-stu-id="e61b2-106">The values are populated by the OEM in an .inf file.</span></span>

<span data-ttu-id="e61b2-107">Элементу **VT** структуры **пропвариант** задано значение VT \_ BLOB.</span><span class="sxs-lookup"><span data-stu-id="e61b2-107">The **vt** member of the **PROPVARIANT** structure is set to VT\_BLOB.</span></span>

<span data-ttu-id="e61b2-108">Членом **большого двоичного объекта** структуры **пропвариант** является структура типа **BLOB** , содержащая два члена.</span><span class="sxs-lookup"><span data-stu-id="e61b2-108">The **blob** member of the **PROPVARIANT** structure is a structure of type **BLOB** that contains two members.</span></span> <span data-ttu-id="e61b2-109">Member **BLOB. кбсизе** — это **DWORD** , указывающий число байтов в описании формата.</span><span class="sxs-lookup"><span data-stu-id="e61b2-109">Member **blob.cbSize** is a **DWORD** that specifies the number of bytes in the format description.</span></span> <span data-ttu-id="e61b2-110">Member **BLOB. пблобдата** указывает на структуру **вавеформатекс** , содержащую описание формата.</span><span class="sxs-lookup"><span data-stu-id="e61b2-110">Member **blob.pBlobData** points to a **WAVEFORMATEX** structure that contains the format description.</span></span> <span data-ttu-id="e61b2-111">Дополнительные сведения о большом двоичном объекте см. в документации по Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="e61b2-111">For more information about BLOB, see the Windows SDK documentation.</span></span> <span data-ttu-id="e61b2-112">Дополнительные сведения о **вавеформатекс** см. в документации по Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="e61b2-112">For more information about **WAVEFORMATEX**, see the Windows DDK documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="e61b2-113">Требования</span><span class="sxs-lookup"><span data-stu-id="e61b2-113">Requirements</span></span>



| <span data-ttu-id="e61b2-114">Требование</span><span class="sxs-lookup"><span data-stu-id="e61b2-114">Requirement</span></span> | <span data-ttu-id="e61b2-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e61b2-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e61b2-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e61b2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e61b2-117">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e61b2-117">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e61b2-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e61b2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e61b2-119">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e61b2-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e61b2-120">Header</span><span class="sxs-lookup"><span data-stu-id="e61b2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e61b2-121"><dt>Ммдевицеапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="e61b2-121"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e61b2-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e61b2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e61b2-123">**Свойства конечной точки аудио**</span><span class="sxs-lookup"><span data-stu-id="e61b2-123">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="e61b2-124">Основные свойства звука</span><span class="sxs-lookup"><span data-stu-id="e61b2-124">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




