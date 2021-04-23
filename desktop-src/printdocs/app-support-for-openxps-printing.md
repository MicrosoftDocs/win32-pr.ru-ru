---
description: Опенкспс — это формат спецификаций формата Open XML для документов, который основан на стандарте Европейской спецификации Association (ECMA) для европейских коробок.
ms.assetid: 52FB5B3F-BEBF-4851-8BE9-5DC7AE535313
title: Поддержка приложений для печати Опенкспс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914d8c365209ea3486bedd5e0352e63a8e31086f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702203"
---
# <a name="app-support-for-openxps-printing"></a><span data-ttu-id="16dac-103">Поддержка приложений для печати Опенкспс</span><span class="sxs-lookup"><span data-stu-id="16dac-103">App Support for OpenXPS Printing</span></span>

<span data-ttu-id="16dac-104">Опенкспс — это формат спецификаций формата Open XML для документов, который основан на стандарте Европейской спецификации ассоциации компьютерных производителей (ECMA).</span><span class="sxs-lookup"><span data-stu-id="16dac-104">OpenXPS is the Open XML Paper Specification format for documents, and it’s based on the European Computer Manufacturers Association (ECMA) standard specification.</span></span>

<span data-ttu-id="16dac-105">Windows 8 обеспечивает полную поддержку Опенкспс печати с помощью модели драйвера печати V4, параллельно с постоянной поддержкой формата Microsoft XPS.</span><span class="sxs-lookup"><span data-stu-id="16dac-105">Windows 8 provides full support for OpenXPS printing via the v4 print driver model, side-by-side with continued support for the Microsoft XPS format.</span></span> <span data-ttu-id="16dac-106">В этом разделе рассматривается часть этой поддержки, относящаяся к разработчикам приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="16dac-106">And this topic focuses on the portion of this support that is relevant to Windows application developers.</span></span> <span data-ttu-id="16dac-107">Сведения о требованиях к драйверу для поддержки Опенкспс см. в статье [Поддержка драйверов для опенкспс](/windows-hardware/drivers/print/printer-driver-overview).</span><span class="sxs-lookup"><span data-stu-id="16dac-107">For information about driver requirements for OpenXPS support, see [Driver Support for OpenXPS](/windows-hardware/drivers/print/printer-driver-overview).</span></span>

## <a name="sending-xps-data-to-the-print-system"></a><span data-ttu-id="16dac-108">Отправка данных XPS в систему печати</span><span class="sxs-lookup"><span data-stu-id="16dac-108">Sending XPS data to the Print System</span></span>

<span data-ttu-id="16dac-109">Рекомендуется использовать [**ипринтдокументпаккажетаржет**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) для отправки всех заданий печати XPS в систему печати.</span><span class="sxs-lookup"><span data-stu-id="16dac-109">We recommend that you use [**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) for sending all XPS print jobs to the print system.</span></span> <span data-ttu-id="16dac-110">**Ипринтдокументпаккажетаржет** принимает объектную модель XPS (OM) без сериализации и помогает повысить общую производительность.</span><span class="sxs-lookup"><span data-stu-id="16dac-110">**IPrintDocumentPackageTarget** accepts the XPS object model (OM) without serialization, and that helps to improve the overall performance.</span></span>

<span data-ttu-id="16dac-111">Ниже приведен краткий обзор интерфейса **ипринтдокументпаккажетаржет** .</span><span class="sxs-lookup"><span data-stu-id="16dac-111">Here's a brief summary of the **IPrintDocumentPackageTarget** interface:</span></span>

-   <span data-ttu-id="16dac-112">Этот интерфейс поддерживает печать из специализированных решений, а также настольных приложений.</span><span class="sxs-lookup"><span data-stu-id="16dac-112">This interface supports printing from tailored solutions as well as desktop applications.</span></span>

-   <span data-ttu-id="16dac-113">Для настольных приложений это можно использовать вместо [**StartXpsPrintJob1**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob1).</span><span class="sxs-lookup"><span data-stu-id="16dac-113">For desktops apps, this can be used in place of [**StartXpsPrintJob1**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob1).</span></span>

-   <span data-ttu-id="16dac-114">Доступно в Windows 7 с пакетом обновления 1 (SP1), обновлением платформы и Windows 8.</span><span class="sxs-lookup"><span data-stu-id="16dac-114">Available on Windows 7 with Service Pack 1 (SP1) + Platform Update, and Windows 8.</span></span>

-   <span data-ttu-id="16dac-115">Включите *документтаржет. h* в проекты, чтобы использовать эти API.</span><span class="sxs-lookup"><span data-stu-id="16dac-115">Include *DocumentTarget.h* in projects to use these APIs.</span></span>

<span data-ttu-id="16dac-116">Приложения, использующие документы Опенкспс, должны отметить, что тип MIME для Опенкспс выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="16dac-116">Applications that consume OpenXPS documents should note that the MIME type for OpenXPS is as follows:</span></span>

<dl> <span data-ttu-id="16dac-117">\\oxps приложения</span><span class="sxs-lookup"><span data-stu-id="16dac-117">application\\oxps</span></span>  
</dl>

## <a name="sending-openxps-data-to-the-xps-print-api"></a><span data-ttu-id="16dac-118">Отправка данных Опенкспс в API печати XPS</span><span class="sxs-lookup"><span data-stu-id="16dac-118">Sending OpenXPS data to the XPS Print API</span></span>

<span data-ttu-id="16dac-119">В отношении Опенкспс, OM XPS принимает как МСКСПС, так и Опенкспс, и предоставляет методы для преобразования и сериализации в любой формат.</span><span class="sxs-lookup"><span data-stu-id="16dac-119">Specific to OpenXPS, XPS OM accepts both MSXPS and OpenXPS, and provides methods for conversion and serialization to either format.</span></span> <span data-ttu-id="16dac-120">Это позволяет разработчикам приложений независимо от целевого драйвера, если они нужны.</span><span class="sxs-lookup"><span data-stu-id="16dac-120">This allows application developers to be agnostic of the target driver, if they want.</span></span> <span data-ttu-id="16dac-121">Это также означает, что разработчики приложений всегда могут отправлять задания печати в виде модели XPS в StartXpsPrintJob1 или Идокументпаккажетаржет, зная, что система печати будет работать с любым необходимым преобразованием.</span><span class="sxs-lookup"><span data-stu-id="16dac-121">This also means that app developers can always submit print jobs as XPS OM to either StartXpsPrintJob1 or IDocumentPackageTarget, knowing that the print system will handle any necessary conversion.</span></span>

<span data-ttu-id="16dac-122">Конечно, предотвращение преобразования между форматами XPS повысит производительность сквозной работы.</span><span class="sxs-lookup"><span data-stu-id="16dac-122">Of course, preventing conversion between XPS formats will improve end-to-end performance.</span></span> <span data-ttu-id="16dac-123">В приложении разработчик может проверить следующий раздел реестра, чтобы определить предпочтительный формат XPS для целевого драйвера печати:</span><span class="sxs-lookup"><span data-stu-id="16dac-123">From the application, the developer can check the following registry key to determine the preferred XPS format of the targeted print driver:</span></span>

``` syntax
HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Print\Printers\[PrintDriverName]\PrintDriverData\XpsFormat
```

<span data-ttu-id="16dac-124">После определения предпочтительного формата XPS приложение может предоставлять объекты OM XPS, для которых не требуется преобразование.</span><span class="sxs-lookup"><span data-stu-id="16dac-124">Once the preferred XPS format has been determined, the application can provide XPS OM objects that will not require conversion.</span></span> <span data-ttu-id="16dac-125">В частности, это использование Фото HD в МСКСПС и ЖПЕГКСР в Опенкспс.</span><span class="sxs-lookup"><span data-stu-id="16dac-125">Of particular note is the use of HD Photo in MSXPS and JPEGXR in OpenXPS.</span></span> <span data-ttu-id="16dac-126">Преобразование из ЖПЕГКСР в HD Photo относительно просто, поскольку основное различие в этом преобразовании заключается в том, что Фото HD игнорирует 4 управляющие биты, необходимые ЖПЕГКСР.</span><span class="sxs-lookup"><span data-stu-id="16dac-126">Converting from JPEGXR to HD Photo is relatively lightweight since the primary difference in this conversion is that HD Photo ignores 4 control bits that JPEGXR requires.</span></span> <span data-ttu-id="16dac-127">Однако преобразование из Photo HD в ЖПЕГКСР требует повторной кодирования всего образа для создания необходимых управляющих битов.</span><span class="sxs-lookup"><span data-stu-id="16dac-127">However, converting from HD Photo to JPEGXR requires the entire image to be re-encoded in order to generate the required control bits.</span></span> <span data-ttu-id="16dac-128">Таким образом, предоставление образов ЖПЕГКСР для изображений с высоким разрешением обеспечит совместимость с Опенкспс и сокращает стоимость преобразования образа для МСКСПС.</span><span class="sxs-lookup"><span data-stu-id="16dac-128">Thus, providing JPEGXR images for high-resolution images will ensure compatibility with OpenXPS and minimize the conversion cost of the image for MSXPS.</span></span>

<span data-ttu-id="16dac-129">Заголовок *кспсобжектмодел \_ 1. h* определяет дополнительные API и объекты для опенкспс.</span><span class="sxs-lookup"><span data-stu-id="16dac-129">The *Xpsobjectmodel\_1.h* header defines the additional APIs and objects for OpenXPS.</span></span> <span data-ttu-id="16dac-130">И интерфейс IXpsOMObjectFactory1 предоставляет дополнительные методы для преобразования изображений.</span><span class="sxs-lookup"><span data-stu-id="16dac-130">And the IXpsOMObjectFactory1 interface provides additional methods for image conversion.</span></span> <span data-ttu-id="16dac-131">Ниже приведен синтаксис.</span><span class="sxs-lookup"><span data-stu-id="16dac-131">Here's the syntax:</span></span>


```C++
IXpsOMObjectFactory1->ConvertHDPhotoToJpegXR(IXpsOMImageResource *imageResource);

IXpsOMObjectFactory1->ConvertJpegXRToHDPhoto(IXpsOMImageResource *imageResource);
```



<span data-ttu-id="16dac-132">Windows 8 предоставляет следующие новые и обновленные перечисления.</span><span class="sxs-lookup"><span data-stu-id="16dac-132">Windows 8 provides the following new and updated enumerations.</span></span>

<span data-ttu-id="16dac-133">Новое перечисление:</span><span class="sxs-lookup"><span data-stu-id="16dac-133">New enumeration:</span></span>

<dl>

[<span data-ttu-id="16dac-134">**\_тип документа \_ XPS**</span><span class="sxs-lookup"><span data-stu-id="16dac-134">**XPS\_DOCUMENT\_TYPE**</span></span>](/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type)  
</dl>

<span data-ttu-id="16dac-135">Обновленное перечисление</span><span class="sxs-lookup"><span data-stu-id="16dac-135">Updated enumeration</span></span>

<dl>

[<span data-ttu-id="16dac-136">**\_тип образа \_ XPS**</span><span class="sxs-lookup"><span data-stu-id="16dac-136">**XPS\_IMAGE\_TYPE**</span></span>](/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type)  
</dl>

<span data-ttu-id="16dac-137">Новые методы GetDocumentType позволяют приложению определить формат XPS документов.</span><span class="sxs-lookup"><span data-stu-id="16dac-137">The new GetDocumentType methods allow an application to determine the XPS format of documents.</span></span> <span data-ttu-id="16dac-138">Они доступны в [**IXpsOMObjectFactory1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsomobjectfactory1), [**IXpsOMPackage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompackage1)и [**IXpsOMPage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompage1).</span><span class="sxs-lookup"><span data-stu-id="16dac-138">These are available in [**IXpsOMObjectFactory1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsomobjectfactory1), [**IXpsOMPackage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompackage1), and [**IXpsOMPage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompage1).</span></span> <span data-ttu-id="16dac-139">Ниже приведен список методов.</span><span class="sxs-lookup"><span data-stu-id="16dac-139">Here's a list of the methods.</span></span>

<dl>

[<span data-ttu-id="16dac-140">**IXpsOMObjectFactory1:: Жетдокументтипефромфиле**</span><span class="sxs-lookup"><span data-stu-id="16dac-140">**IXpsOMObjectFactory1::GetDocumentTypeFromFile**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromfile)  
[<span data-ttu-id="16dac-141">**IXpsOMObjectFactory1:: Жетдокументтипефромстреам**</span><span class="sxs-lookup"><span data-stu-id="16dac-141">**IXpsOMObjectFactory1::GetDocumentTypeFromStream**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromstream)  
[<span data-ttu-id="16dac-142">**IXpsOMPackage1:: GetDocumentType**</span><span class="sxs-lookup"><span data-stu-id="16dac-142">**IXpsOMPackage1::GetDocumentType**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompackage1-getdocumenttype)  
[<span data-ttu-id="16dac-143">**IXpsOMPage1:: GetDocumentType**</span><span class="sxs-lookup"><span data-stu-id="16dac-143">**IXpsOMPage1::GetDocumentType**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompage1-getdocumenttype)  
</dl>

<span data-ttu-id="16dac-144">Windows 8 предоставляет следующие новые коды ошибок для поддержки Опенкспс:</span><span class="sxs-lookup"><span data-stu-id="16dac-144">Windows 8 provides the following new error codes in support of OpenXPS:</span></span>

<dl> <span data-ttu-id="16dac-145">\_несоответствие \_ \_ пространства имен XPS E.</span><span class="sxs-lookup"><span data-stu-id="16dac-145">XPS\_E\_MISMATCHED\_NAMESPACE.</span></span> <dl> <span data-ttu-id="16dac-146">Эта ошибка возвращается, если имеется несовпадающее пространство имен.</span><span class="sxs-lookup"><span data-stu-id="16dac-146">This error is returned, if there is a mismatched namespace.</span></span>  
</dl> </dd> XPS\_E\_ABSOLUTE\_REFERENCE. <dl> <span data-ttu-id="16dac-147">Эта ошибка возвращается, если МСКСПС использует абсолютные URI во внутренних ссылках или пытается использовать внутренние ссылки для сериализации в потоке.</span><span class="sxs-lookup"><span data-stu-id="16dac-147">This error is returned if MSXPS uses absolute URIs in internal references, or attempts to use internal references to serialize in the stream.</span></span> <span data-ttu-id="16dac-148">Это обусловлено тем, что модель XPS OM создает относительные URI.</span><span class="sxs-lookup"><span data-stu-id="16dac-148">That is because XPS OM generates relative URIs.</span></span> <span data-ttu-id="16dac-149">Хотя МСКСПС поддерживает как относительные, так и абсолютные URI, Опенкспс требует относительных URI.</span><span class="sxs-lookup"><span data-stu-id="16dac-149">And although MSXPS supports both relative and absolute URIs, OpenXPS requires relative URIs.</span></span>  
</dl> </dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="16dac-150">См. также</span><span class="sxs-lookup"><span data-stu-id="16dac-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16dac-151">Поддержка драйверов для Опенкспс</span><span class="sxs-lookup"><span data-stu-id="16dac-151">Driver Support for OpenXPS</span></span>](/windows-hardware/drivers/print/printer-driver-overview)
</dt> <dt>

[<span data-ttu-id="16dac-152">**ипринтдокументпаккажетаржет**</span><span class="sxs-lookup"><span data-stu-id="16dac-152">**IPrintDocumentPackageTarget**</span></span>](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)
</dt> <dt>

[<span data-ttu-id="16dac-153">**IXpsOMObjectFactory1:: Жетдокументтипефромфиле**</span><span class="sxs-lookup"><span data-stu-id="16dac-153">**IXpsOMObjectFactory1::GetDocumentTypeFromFile**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromfile)
</dt> <dt>

[<span data-ttu-id="16dac-154">**IXpsOMObjectFactory1:: Жетдокументтипефромстреам**</span><span class="sxs-lookup"><span data-stu-id="16dac-154">**IXpsOMObjectFactory1::GetDocumentTypeFromStream**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromstream)
</dt> <dt>

[<span data-ttu-id="16dac-155">**IXpsOMPackage1:: GetDocumentType**</span><span class="sxs-lookup"><span data-stu-id="16dac-155">**IXpsOMPackage1::GetDocumentType**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompackage1-getdocumenttype)
</dt> <dt>

[<span data-ttu-id="16dac-156">**IXpsOMPage1:: GetDocumentType**</span><span class="sxs-lookup"><span data-stu-id="16dac-156">**IXpsOMPage1::GetDocumentType**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompage1-getdocumenttype)
</dt> <dt>

[<span data-ttu-id="16dac-157">**\_тип документа \_ XPS**</span><span class="sxs-lookup"><span data-stu-id="16dac-157">**XPS\_DOCUMENT\_TYPE**</span></span>](/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type)
</dt> <dt>

[<span data-ttu-id="16dac-158">**\_тип образа \_ XPS**</span><span class="sxs-lookup"><span data-stu-id="16dac-158">**XPS\_IMAGE\_TYPE**</span></span>](/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type)
</dt> </dl>

 

 
