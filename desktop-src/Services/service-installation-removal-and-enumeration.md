---
description: Программа настройки использует функцию CreateService для установки новой службы в базе данных SCM.
ms.assetid: 554b9983-4e49-4b11-b420-a4754123d854
title: Установка, удаление и перечисление служб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1069bba094205efd3257063a89c74326b2806455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809443"
---
# <a name="service-installation-removal-and-enumeration"></a>Установка, удаление и перечисление служб

Программа настройки использует функцию [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) для установки новой службы в базе данных SCM. Эта функция задает имя службы и предоставляет сведения о конфигурации, которые хранятся в базе данных. Описание сведений, хранящихся в базе данных для каждой службы, см. в разделе [Database of Installed Services](database-of-installed-services.md). Пример кода см. [в разделе Установка службы](installing-a-service.md).

Программа настройки использует функцию [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) для удаления установленной службы из базы данных. Дополнительные сведения см. [в разделе Удаление службы](deleting-a-service.md).

Чтобы получить имя службы, вызовите функцию [**жетсервицекэйнаме**](/windows/desktop/api/Winsvc/nf-winsvc-getservicekeynamea) . Отображаемое имя службы, используемое в приложении панели управления "службы", можно получить, вызвав функцию [**жетсервицедисплайнаме**](/windows/desktop/api/Winsvc/nf-winsvc-getservicedisplaynamea) .

Программа настройки службы может использовать функцию [**енумсервицесстатусекс**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) для перечисления всех служб и их состояний. Кроме того, с помощью функции [**енумдепендентсервицес**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) можно перечислить, какие службы зависят от указанного объекта службы.

 

 



