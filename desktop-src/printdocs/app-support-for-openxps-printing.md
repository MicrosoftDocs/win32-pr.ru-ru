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
# <a name="app-support-for-openxps-printing"></a>Поддержка приложений для печати Опенкспс

Опенкспс — это формат спецификаций формата Open XML для документов, который основан на стандарте Европейской спецификации ассоциации компьютерных производителей (ECMA).

Windows 8 обеспечивает полную поддержку Опенкспс печати с помощью модели драйвера печати V4, параллельно с постоянной поддержкой формата Microsoft XPS. В этом разделе рассматривается часть этой поддержки, относящаяся к разработчикам приложений Windows. Сведения о требованиях к драйверу для поддержки Опенкспс см. в статье [Поддержка драйверов для опенкспс](/windows-hardware/drivers/print/printer-driver-overview).

## <a name="sending-xps-data-to-the-print-system"></a>Отправка данных XPS в систему печати

Рекомендуется использовать [**ипринтдокументпаккажетаржет**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) для отправки всех заданий печати XPS в систему печати. **Ипринтдокументпаккажетаржет** принимает объектную модель XPS (OM) без сериализации и помогает повысить общую производительность.

Ниже приведен краткий обзор интерфейса **ипринтдокументпаккажетаржет** .

-   Этот интерфейс поддерживает печать из специализированных решений, а также настольных приложений.

-   Для настольных приложений это можно использовать вместо [**StartXpsPrintJob1**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob1).

-   Доступно в Windows 7 с пакетом обновления 1 (SP1), обновлением платформы и Windows 8.

-   Включите *документтаржет. h* в проекты, чтобы использовать эти API.

Приложения, использующие документы Опенкспс, должны отметить, что тип MIME для Опенкспс выглядит следующим образом:

<dl> \\oxps приложения  
</dl>

## <a name="sending-openxps-data-to-the-xps-print-api"></a>Отправка данных Опенкспс в API печати XPS

В отношении Опенкспс, OM XPS принимает как МСКСПС, так и Опенкспс, и предоставляет методы для преобразования и сериализации в любой формат. Это позволяет разработчикам приложений независимо от целевого драйвера, если они нужны. Это также означает, что разработчики приложений всегда могут отправлять задания печати в виде модели XPS в StartXpsPrintJob1 или Идокументпаккажетаржет, зная, что система печати будет работать с любым необходимым преобразованием.

Конечно, предотвращение преобразования между форматами XPS повысит производительность сквозной работы. В приложении разработчик может проверить следующий раздел реестра, чтобы определить предпочтительный формат XPS для целевого драйвера печати:

``` syntax
HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Print\Printers\[PrintDriverName]\PrintDriverData\XpsFormat
```

После определения предпочтительного формата XPS приложение может предоставлять объекты OM XPS, для которых не требуется преобразование. В частности, это использование Фото HD в МСКСПС и ЖПЕГКСР в Опенкспс. Преобразование из ЖПЕГКСР в HD Photo относительно просто, поскольку основное различие в этом преобразовании заключается в том, что Фото HD игнорирует 4 управляющие биты, необходимые ЖПЕГКСР. Однако преобразование из Photo HD в ЖПЕГКСР требует повторной кодирования всего образа для создания необходимых управляющих битов. Таким образом, предоставление образов ЖПЕГКСР для изображений с высоким разрешением обеспечит совместимость с Опенкспс и сокращает стоимость преобразования образа для МСКСПС.

Заголовок *кспсобжектмодел \_ 1. h* определяет дополнительные API и объекты для опенкспс. И интерфейс IXpsOMObjectFactory1 предоставляет дополнительные методы для преобразования изображений. Ниже приведен синтаксис.


```C++
IXpsOMObjectFactory1->ConvertHDPhotoToJpegXR(IXpsOMImageResource *imageResource);

IXpsOMObjectFactory1->ConvertJpegXRToHDPhoto(IXpsOMImageResource *imageResource);
```



Windows 8 предоставляет следующие новые и обновленные перечисления.

Новое перечисление:

<dl>

[**\_тип документа \_ XPS**](/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type)  
</dl>

Обновленное перечисление

<dl>

[**\_тип образа \_ XPS**](/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type)  
</dl>

Новые методы GetDocumentType позволяют приложению определить формат XPS документов. Они доступны в [**IXpsOMObjectFactory1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsomobjectfactory1), [**IXpsOMPackage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompackage1)и [**IXpsOMPage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompage1). Ниже приведен список методов.

<dl>

[**IXpsOMObjectFactory1:: Жетдокументтипефромфиле**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromfile)  
[**IXpsOMObjectFactory1:: Жетдокументтипефромстреам**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromstream)  
[**IXpsOMPackage1:: GetDocumentType**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompackage1-getdocumenttype)  
[**IXpsOMPage1:: GetDocumentType**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompage1-getdocumenttype)  
</dl>

Windows 8 предоставляет следующие новые коды ошибок для поддержки Опенкспс:

<dl> \_несоответствие \_ \_ пространства имен XPS E. <dl> Эта ошибка возвращается, если имеется несовпадающее пространство имен.  
</dl> </dd> XPS\_E\_ABSOLUTE\_REFERENCE. <dl> Эта ошибка возвращается, если МСКСПС использует абсолютные URI во внутренних ссылках или пытается использовать внутренние ссылки для сериализации в потоке. Это обусловлено тем, что модель XPS OM создает относительные URI. Хотя МСКСПС поддерживает как относительные, так и абсолютные URI, Опенкспс требует относительных URI.  
</dl> </dd> </dl>

## <a name="related-topics"></a>См. также

<dl> <dt>

[Поддержка драйверов для Опенкспс](/windows-hardware/drivers/print/printer-driver-overview)
</dt> <dt>

[**ипринтдокументпаккажетаржет**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)
</dt> <dt>

[**IXpsOMObjectFactory1:: Жетдокументтипефромфиле**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromfile)
</dt> <dt>

[**IXpsOMObjectFactory1:: Жетдокументтипефромстреам**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromstream)
</dt> <dt>

[**IXpsOMPackage1:: GetDocumentType**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompackage1-getdocumenttype)
</dt> <dt>

[**IXpsOMPage1:: GetDocumentType**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompage1-getdocumenttype)
</dt> <dt>

[**\_тип документа \_ XPS**](/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type)
</dt> <dt>

[**\_тип образа \_ XPS**](/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type)
</dt> </dl>

 

 
