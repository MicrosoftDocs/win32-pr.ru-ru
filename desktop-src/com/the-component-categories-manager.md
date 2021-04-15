---
title: Диспетчер категорий компонентов
description: Диспетчер категорий компонентов
ms.assetid: bd43ef98-2299-4c8a-9f35-bf9aceb074ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fdf301e1b344bbc2403fd656dd90447ccffc357
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486772"
---
# <a name="the-component-categories-manager"></a>Диспетчер категорий компонентов

Чтобы упростить обработку категорий компонентов и обеспечить согласованность реестра, система предоставляет диспетчер категорий компонентов, COM-объект с идентификатором CLSID \_ СТДКОМПОНЕНТКАТЕГОРИЕСМГР CLSID. Этот COM-объект предоставляет следующие интерфейсы:

-   [**икатинформатион**](/windows/desktop/api/ComCat/nn-comcat-icatinformation)
-   [**икатрегистер**](/windows/desktop/api/ComCat/nn-comcat-icatregister)

[**Икатинформатион**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) предоставляет методы для получения сведений о категориях, реализованных или необходимых определенным классом, и предоставляет сведения о категориях, зарегистрированных на данном компьютере.

[**Икатрегистер**](/windows/desktop/api/ComCat/nn-comcat-icatregister) предоставляет методы для регистрации и отмены регистрации сведений о категориях компонентов в реестре. К ним относятся понятные для человека имена категорий и категории, реализованные или необходимые для данного компонента или класса.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Связывание значков с категорией](associating-icons-with-a-category.md)
</dt> <dt>

[Категоризация по возможностям компонентов](categorizing-by-component-capabilities.md)
</dt> <dt>

[Категоризация по возможностям контейнеров](categorizing-by-container-capabilities.md)
</dt> <dt>

[Классы и ассоциации по умолчанию](default-classes-and-associations.md)
</dt> <dt>

[Определение категорий компонентов](defining-component-categories.md)
</dt> </dl>

 

 




