---
description: Общие записи реестра
ms.assetid: 6a140c7f-df8c-4a8e-9e4d-dbb38901e14f
title: Общие записи реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d7c3514adcc0aeaaf9adadd2b71dfdffcd8d408
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702529"
---
# <a name="general-registry-entries"></a><span data-ttu-id="ae5ee-103">Общие записи реестра</span><span class="sxs-lookup"><span data-stu-id="ae5ee-103">General Registry Entries</span></span>


<span data-ttu-id="ae5ee-104">Следующие записи реестра должны быть сделаны отдельно для декодера и кодировщика:</span><span class="sxs-lookup"><span data-stu-id="ae5ee-104">The following registry entries must be made separately for both the decoder and the encoder:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Encoder/Decoder CLSID}
         Author = Author's Name
         Description = Your Codec Description
         DeviceManufacturer = Manufacturer's Name
         DeviceModels = Device,Device
         FriendlyName = Codec Friendly Name
         Date = mm-dd-yyyy
         Vendor = {GUID_Vendor}
         ContainerFormat = {GUID_ContainerFormat}
         Version = Major.Minor.Build.Number
         SpecVersion = Major.Minor.Build.Number
         MimeTypes = Your Mime Type
         SupportAnimation = 0|1
         SupportChromakey = 0|1
         SupportLossless = 0|1
         SupportMultiframe = 0|1
         Formats
            {Supported PixelFormat GUID 1}
            {Supported PixelFormat GUID ...}
            {Supported PixelFormat GUID N}
         ArbitrationPriority  = 0-10
```

<span data-ttu-id="ae5ee-105">Записи FriendlyName, Вендоргуид, Контаинерформат, Миметипес, FileExtensions и formats являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="ae5ee-105">The FriendlyName, VendorGUID, ContainerFormat, MimeTypes, FileExtensions, and Formats entries are required.</span></span> <span data-ttu-id="ae5ee-106">Все остальные являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="ae5ee-106">All of the others are optional.</span></span>

<span data-ttu-id="ae5ee-107">Обратите внимание, что записи Девицемануфактурер и DeviceModels относятся к необработанным кодекам и относятся к производителю камеры и моделям камеры, к которым применим кодек.</span><span class="sxs-lookup"><span data-stu-id="ae5ee-107">Note that the DeviceManufacturer and DeviceModels entries are specific to raw codecs and refer to the camera manufacturer and camera models that the codec is applicable to.</span></span> <span data-ttu-id="ae5ee-108">Версия спецификации — это версия спецификации формата изображения, которая соответствует кодеку.</span><span class="sxs-lookup"><span data-stu-id="ae5ee-108">The spec version is the version of the image format specification with which the codec complies.</span></span> <span data-ttu-id="ae5ee-109">В записи formats указываются форматы пикселей, поддерживаемые кодеком.</span><span class="sxs-lookup"><span data-stu-id="ae5ee-109">The Formats entry specifies the pixel formats supported by the codec.</span></span> <span data-ttu-id="ae5ee-110">Кодек может поддерживать более одного формата пикселей.</span><span class="sxs-lookup"><span data-stu-id="ae5ee-110">A codec may support more than one pixel format.</span></span> <span data-ttu-id="ae5ee-111">В этом случае вы вводите несколько ключей в \_ \_ форматах корневого CLSID класса hKey \\ \\ (CLSID/кодировщик) \\ .</span><span class="sxs-lookup"><span data-stu-id="ae5ee-111">In that case, you would enter multiple keys under HKEY\_CLASSES\_ROOT\\CLSID\\{Encoder/Decoder CLSID}\\Formats.</span></span>

## <a name="arbitrationpriority"></a><span data-ttu-id="ae5ee-112">арбитратионприорити</span><span class="sxs-lookup"><span data-stu-id="ae5ee-112">ArbitrationPriority</span></span>

<span data-ttu-id="ae5ee-113">Начиная с Windows 8, Арбитратионприорити является новой записью реестра.</span><span class="sxs-lookup"><span data-stu-id="ae5ee-113">Starting in Windows 8, ArbitrationPriority is a new registry entry.</span></span> <span data-ttu-id="ae5ee-114">Допустимые значения: от 0 до 10.</span><span class="sxs-lookup"><span data-stu-id="ae5ee-114">Valid values are 0 through 10.</span></span> <span data-ttu-id="ae5ee-115">При наличии ключа Арбитратионприорити значение этого параметра указывает компоненту WIC определить приоритет связанного кодека для других кодеков с меньшим значением Арбитратионприорити.</span><span class="sxs-lookup"><span data-stu-id="ae5ee-115">When the ArbitrationPriority key is present, the value of this key will instruct WIC to prioritize the associated codec behind any other codecs with a lower ArbitrationPriority value.</span></span> <span data-ttu-id="ae5ee-116">Эта оценка происходит до того, как будет вызвана существующая арбитражка кодека WIC и обеспечивает приоритет для соответствующего кодека под любым конкурирующим кодеком, даже если он является как или более мощным.</span><span class="sxs-lookup"><span data-stu-id="ae5ee-116">This evaluation occurs before the existing WIC codec arbitration occurs, and ensures the associated codec is prioritized below any competing codec, even if it is as or more capable.</span></span> <span data-ttu-id="ae5ee-117">Любой кодек, не имеющий явного значения Арбитратионприорити, определенного в реестре, по умолчанию имеет приоритет 0.</span><span class="sxs-lookup"><span data-stu-id="ae5ee-117">Any codec that doesn’t have an explicit ArbitrationPriority value defined in the registry will default to Priority 0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae5ee-118">См. также</span><span class="sxs-lookup"><span data-stu-id="ae5ee-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ae5ee-119">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="ae5ee-119">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ae5ee-120">Установка и регистрация КОДЕка</span><span class="sxs-lookup"><span data-stu-id="ae5ee-120">CODEC Installation and Registration</span></span>](-wic-codecinstallandreg.md)
</dt> <dt>

[<span data-ttu-id="ae5ee-121">Записи реестра, относящиеся к кодировщику</span><span class="sxs-lookup"><span data-stu-id="ae5ee-121">Encoder-Specific Registry Entries</span></span>](-wic-encoderregentries.md)
</dt> <dt>

[<span data-ttu-id="ae5ee-122">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="ae5ee-122">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="ae5ee-123">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="ae5ee-123">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="ae5ee-124">**Принцип работы компонента Windows Imaging: обнаружение и арбитраж кодеков**</span><span class="sxs-lookup"><span data-stu-id="ae5ee-124">**How the Windows Imaging Component Works: Codec Discovery and Arbitration**</span></span>](-wic-howwicworks.md)
</dt> </dl>

 

 



