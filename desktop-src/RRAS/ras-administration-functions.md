---
title: Функции администрирования RAS
description: В этой документации описываются функции RRAS, которые используются для разработки программного обеспечения для администрирования подключений удаленного доступа RAS.
ms.assetid: 27cf63e2-9dd3-4bc1-98af-e93055d89492
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec2013305f1e37cdc90a1e331c93813520ff20aaafc6b32ffd2471f1f2cb7074
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036284"
---
# <a name="ras-administration-functions"></a>Функции администрирования RAS

В этой документации описываются функции RRAS, которые используются для разработки программного обеспечения для администрирования подключений удаленного доступа RAS. К этим функциям относятся:

-   [**мпрадминконнектионклеарстатс**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionclearstats)
-   [**мпрадминконнектионенум**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum)
-   [**мпрадминконнектионенумекс**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenumex)
-   [**мпрадминконнектионжетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfo)
-   [**мпрадминконнектионжетинфоекс**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfoex)
-   [**мпрадминконнектионремовекуарантине**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionremovequarantine)
-   [**мпрадминпортклеарстатс**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)
-   [**мпрадминпортдисконнект**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect)
-   [**мпрадминпортенум**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum)
-   [**мпрадминпортжетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo)
-   [**мпрадминпортресет**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportreset)

Дополнительные функции используются как для администрирования службы удаленного доступа, так и для администрирования маршрутизатора. Следующие функции описаны в справочнике по [функциям администрирования маршрутизатора](router-administration-functions.md) :

-   [**мпрадминбуфферфри**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree)
-   [**мпрадминжетеррорстринг**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring)
-   [**мпрадминиссервицеруннинг**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning)
-   [**мпрадминсерверконнект**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect)
-   [**мпрадминсервердисконнект**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverdisconnect)

Для реализации библиотеки DLL администрирования RAS используйте функции, описанные в следующем разделе:

-   [Функции DLL администратора RAS](ras-admin-dll-functions.md)

Для управления пользователями сервера RAS используйте функции, описанные в следующем разделе:

-   [Функции администрирования пользователей RAS](ras-user-administration-functions.md)

 

 




