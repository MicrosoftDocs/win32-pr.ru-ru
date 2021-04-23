---
title: Объект перешифрования DRM
description: Объект перешифрования DRM
ms.assetid: 50c041b3-6621-4618-843f-6ef9b8e741ab
keywords:
- Windows Media Format SDK, объекты перешифрования DRM
- Расширенный системный формат (ASF), объекты перешифрования DRM
- ASF (Расширенный системный формат), объекты перешифрования DRM
- объекты, объекты перешифрования DRM
- Объекты перешифрования DRM
- Windows Media Format SDK, объекты перешифрования
- Расширенные системные форматы (ASF), объекты шифрования
- ASF (Расширенный системный формат), объекты перешифрования
- объекты, объекты перешифрования
- объекты перешифрования
- Управление цифровыми правами (DRM), объекты-отшифрования
- DRM (Управление цифровыми правами), объекты-отшифрования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d46213dd7ebfbe48ff22039c201dbff3aab462f5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104133503"
---
# <a name="drm-transcryptor-object"></a><span data-ttu-id="d4e04-115">Объект перешифрования DRM</span><span class="sxs-lookup"><span data-stu-id="d4e04-115">DRM Transcryptor Object</span></span>

<span data-ttu-id="d4e04-116">Объект-Отправитель DRM преобразует файлы ASF, защищенные с помощью DRM, в потоки данных, готовые к отправке на сетевые устройства, использующие Windows Media DRM 10 для сетевых устройств.</span><span class="sxs-lookup"><span data-stu-id="d4e04-116">The DRM transcryptor object converts DRM-protected ASF files into data streams ready to be sent to network devices that use Windows Media DRM 10 for Network Devices.</span></span>

<span data-ttu-id="d4e04-117">Объект перешифрования DRM создается функцией [**вмкреатедрмтранскриптор**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor) , которая устанавливает указатель на интерфейс [**ивмдрмтранскриптор**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor) .</span><span class="sxs-lookup"><span data-stu-id="d4e04-117">The DRM transcryptor object is created by the [**WMCreateDRMTranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor) function, which sets a pointer to the [**IWMDRMTranscryptor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor) interface.</span></span> <span data-ttu-id="d4e04-118">**IUnknown** и **ивмдрмтранскриптор** — это единственные интерфейсы, поддерживаемые этим объектом.</span><span class="sxs-lookup"><span data-stu-id="d4e04-118">**IUnknown** and **IWMDRMTranscryptor** are the only interfaces supported by this object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4e04-119">См. также</span><span class="sxs-lookup"><span data-stu-id="d4e04-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4e04-120">**Объекты**</span><span class="sxs-lookup"><span data-stu-id="d4e04-120">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




