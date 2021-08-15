---
description: Функции целостности изображений управляют набором сертификатов в файле образа.
ms.assetid: db77b8af-3c36-4e01-88e0-4c44ef8504ff
title: Функции целостности изображений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47a2311ccfc59fb228a8f71c380205dc754452ba4a9d0a7e1dcb3c9edcd92a14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957103"
---
# <a name="image-integrity-functions"></a>Функции целостности изображений

Функции целостности изображений управляют набором сертификатов в файле образа. Предоставляются подпрограммы для добавления, удаления и запроса сертификатов. Кроме того, существует функция, позволяющая получить поток байтов файла изображения, необходимый для вычисления дайджеста сообщения файла изображения. Это необходимо для создания сертификатов подписи.

Каждый сертификат в файле имеет индекс, который может изменяться при удалении сертификатов. Новые сертификаты всегда будут добавляться в конец списка существующих сертификатов. То есть им будут назначены индексы, превышающие индекс, который используется в настоящий момент. Как правило, приложение не должно рассчитывать, что у данного сертификата тот же индекс, что и при последнем обращении.

-   [**дижестфунктион**](/windows/desktop/api/Imagehlp/nc-imagehlp-digest_function)
-   [**имажеаддцертификате**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageaddcertificate)
-   [**имажеенумератецертификатес**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageenumeratecertificates)
-   [**имажежетцертификатедата**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificatedata)
-   [**имажежетцертификатехеадер**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificateheader)
-   [**имажежетдижестстреам**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetdigeststream)
-   [**имажеремовецертификате**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageremovecertificate)

 

 



