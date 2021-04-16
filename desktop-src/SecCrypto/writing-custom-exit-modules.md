---
description: Пользовательские модули выхода должны реализовывать интерфейс Ицертексит, который вызывается ядром сервера.
ms.assetid: 509e7945-b656-4c4c-b5eb-45fbe80377c7
title: Написание пользовательских модулей выхода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81798996059e878ef11dbcdf290298094d0849cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664228"
---
# <a name="writing-custom-exit-modules"></a>Написание пользовательских модулей выхода

Пользовательские модули выхода должны реализовывать интерфейс [**ицертексит**](/windows/desktop/api/Certexit/nn-certexit-icertexit) , который вызывается ядром сервера. Метод [**ицертексит:: Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) вызывается ядром сервера при загрузке модуля Exit. Он позволяет модулю Exit выполнять инициализацию и возвращать значение, которое информирует серверный механизм о том, для каких событий требуется уведомление. Метод [**ицертексит::-Description**](/windows/desktop/api/Certexit/nf-certexit-icertexit-getdescription) должен возвращать строку описания, когда подсистема сервера запрашивает его. Метод [**ицертексит:: notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify) вызывается ядром сервера для уведомления модуля выхода о том, что произошло событие.

Модули выхода могут вызывать интерфейс [**ицертсерверексит**](/windows/desktop/api/Certif/nn-certif-icertserverexit) , который поддерживает многие из тех же методов, что и интерфейс [**ицертсерверполици**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) , за исключением методов [**сетцертификатикстенсион**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) и [**сетцертификатепроперти**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) .

Сведения об удалении существующего модуля Exit и установке нового см. в разделе о настройке модуля выхода в справке.

 

 



