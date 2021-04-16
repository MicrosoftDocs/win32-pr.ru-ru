---
title: Руководство обзор ADSI с Visual Basic
description: Active Directory является базой данных специального назначения \ 8212; Это не замена реестра.
ms.assetid: 899799e3-5ab9-4d19-883a-5bc9f20d2bad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607d9da26d1c96d7cb6f83a799c7633404e5bb4
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104557430"
---
# <a name="tutorial-overview-adsi-with-visual-basic"></a>Обзор учебника: ADSI с Visual Basic

> [!Note]  
> Следующая документация является частью описания расширенного сценария для Visual Basic разработчиков. Общие сведения о Active Directory см. в документации по [ИТ-специалистам на сайте TechNet](/previous-versions/windows/it-pro/windows-2000-server/cc977985(v=technet.10)). Более подробные сведения о разработке Active Directory см. в разделе [домен Active Directory Services](/windows/desktop/AD/active-directory-domain-services). Дополнительные сведения об интерфейсах служб Active Directory см. в разделе "родительский раздел" этой статьи: [интерфейсы служб Active Directory](active-directory-service-interfaces-adsi.md), а также родственный раздел: [о Active Directory интерфейсах службы](about-adsi.md).

 

Active Directory является базой данных специального назначения — это не замена реестра. Каталог предназначен для выполнения большого количества операций чтения и поиска и значительно меньшего количества изменений и обновлений. Active Directory данные являются иерархическими, реплицируемыми и расширяемыми. Так как он реплицируется, вы не хотите хранить динамические данные, например стоимость корпоративных акций или производительность ЦП. Если данные зависят от компьютера, храните их в реестре. Типичными примерами данных, хранящихся в каталоге, являются данные очереди печати, контактные данные пользователя и данные конфигурации сети или компьютера. База данных Active Directory состоит из объектов и атрибутов. Определения объектов и атрибутов хранятся в схеме Active Directory.

Возможно, вас интересует, какие объекты в данный момент хранятся в Active Directory. Active Directory содержит три секции. Они также называются контекстами именования: домен, схема и конфигурация. Раздел домена содержит пользователей, группы, контакты, компьютеры, подразделения и многие другие типы объектов. Поскольку Active Directory является расширяемой, можно также добавить собственные классы и атрибуты. Секция схемы содержит классы и определения атрибутов. Раздел конфигурации включает данные конфигурации для служб, секций и сайтов.

На следующем снимке экрана показан Active Directory раздел домена.

![раздел домена Active Directory](images/adadsi1.png)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Доступ к Active Directory с помощью Visual Basic](accessing-active-directory-using-visual-basic.md)
</dt> <dt>

[Сценарий: Корпорация Fabrikam](scenario--the-fabrikam-corporation.md)
</dt> <dt>

[Дополнительные разделы](advanced-topics.md)
</dt> </dl>

 

 