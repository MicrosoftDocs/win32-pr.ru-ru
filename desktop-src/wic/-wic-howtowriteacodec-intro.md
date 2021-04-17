---
description: Компонент Windows Imaging Component (WIC) — это расширяемая платформа для создания цифровых образов в операционных системах Windows Vista и Windows 7.
ms.assetid: ffcd5239-ae2d-436f-9402-8c10a79256c3
title: Введение (написание WIC-Enabled кодека)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776bf9f2c0cb5df8b45ce04d55f20d40d05a12a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712040"
---
# <a name="introduction-how-to-write-a-wic-enabled-codec"></a>Введение (написание WIC-Enabled кодека)

Компонент Windows Imaging Component (WIC) — это расширяемая платформа для создания цифровых образов в операционных системах Windows Vista и Windows 7. Компонент WIC также доступен в Windows XP и Windows Server 2003 либо в составе Microsoft .NET Framework 3,0, либо в виде отдельного компонента, который можно распространять повторно. Любое приложение, использующее WIC, может получать доступ, отображать, обрабатывать и печатать изображения в любом формате изображения, предоставляющем кодек с поддержкой WIC, используя единый набор последовательных интерфейсов, устраняющих необходимость специального знания определенных форматов.

Проводник Windows Vista, фотоальбом Windows Vista, фотоальбом Live Photo Viewer и средство просмотра фотографий Windows 7 основаны на WIC. После установки кодеков с поддержкой WIC в системе Windows Vista или Windows 7 операционная система предоставляет тот же уровень поддержки для соответствующего формата изображений, что и для стандартных форматов изображений, поставляемых с платформой. Так как вы пишете кодек для собственного формата изображений, вы можете обеспечить единообразное качество в любом месте, где используется формат изображения, и получить преимущества полной поддержки платформы.

## <a name="related-topics"></a>См. также

<dl> <dt>

**Зрения**
</dt> <dt>

[Написание WIC-Enabled КОДЕка](-wic-howtowriteacodec.md)
</dt> <dt>

[Принцип работы компонента Windows Imaging](-wic-howwicworks.md)
</dt> <dt>

Написание WIC-Enabled КОДЕка
</dt> <dt>

[Общие сведения о компоненте создания образов Windows](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



