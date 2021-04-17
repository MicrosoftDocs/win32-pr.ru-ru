---
description: Сроки
ms.assetid: 6cc36034-224c-4126-873b-0cfeceec9781
title: Сроки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10d1f802f12df6ca3469b8283bd4fe8b27e22412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684638"
---
# <a name="timeline"></a>Сроки

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

Объект временной шкалы управляет всеми объектами в проекте редактирования видео. Чтобы создать этот объект, вызовите **CoCreateInstance**. Идентификатор класса — CLSID \_ амтимелине.

Для чтения™ файлов Windows Media приложение должно предоставить сертификат программного обеспечения, который также называется ключом. Зарегистрируйте приложение в качестве поставщика ключей через интерфейс **IObjectWithSite** временной шкалы. Дополнительные сведения см. [в разделе Разблокировка пакета SDK Windows Media Format](unlocking-the-windows-media-format-sdk.md).

Объект временной шкалы предоставляет следующие интерфейсы:

-   [**иамсетеррорлог**](iamseterrorlog.md)
-   [**иамтимелине**](iamtimeline.md)
-   **IObjectWithSite**
-   **IPersistStream**

## <a name="related-topics"></a>См. также

<dl> <dt>

[Модель временной шкалы](the-timeline-model.md)
</dt> <dt>

[Создание временной шкалы](constructing-a-timeline.md)
</dt> </dl>

 

 



