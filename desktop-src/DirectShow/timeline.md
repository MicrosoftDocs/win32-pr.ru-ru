---
description: Сроки
ms.assetid: 6cc36034-224c-4126-873b-0cfeceec9781
title: Сроки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d85809aed689d63ccdfc0b1dee1b5b792cafc9d7d0267d27e33bd7b6c1bea6cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651257"
---
# <a name="timeline"></a>Сроки

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

Объект временной шкалы управляет всеми объектами в проекте редактирования видео. Чтобы создать этот объект, вызовите **CoCreateInstance**. Идентификатор класса — CLSID \_ амтимелине.

для чтения Windows файлов мультимедиа™, приложение должно предоставить сертификат программного обеспечения, также называемый ключом. Зарегистрируйте приложение в качестве поставщика ключей через интерфейс **IObjectWithSite** временной шкалы. дополнительные сведения см. [в разделе разблокировка пакета SDK для Windows Media Format](unlocking-the-windows-media-format-sdk.md).

Объект временной шкалы предоставляет следующие интерфейсы:

-   [**иамсетеррорлог**](iamseterrorlog.md)
-   [**иамтимелине**](iamtimeline.md)
-   **IObjectWithSite**
-   **IPersistStream**

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Модель временной шкалы](the-timeline-model.md)
</dt> <dt>

[Создание временной шкалы](constructing-a-timeline.md)
</dt> </dl>

 

 



