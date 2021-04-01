---
description: Интерфейс Иинсталлатионресулт определяет следующие свойства.
ms.assetid: bd6cd5ae-2e43-4ac3-8ce7-ac80b7fc5cb8
title: Свойства Иинсталлатионресулт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78783b6758ab30d6a77c07cd71111486f3a7343e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072806"
---
# <a name="iinstallationresult-properties"></a>Свойства Иинсталлатионресулт

Интерфейс [**иинсталлатионресулт**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationresult) определяет следующие свойства.



| Свойство                                                     | Описание                                                                                                                            |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Состав**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_hresult)               | Возвращает **значение HRESULT** исключения (при его наличии), которое возникает во время установки.                                                 |
| [**RebootRequired**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_rebootrequired) | Возвращает логическое значение, указывающее, требуется ли перезагрузка компьютера для завершения установки или удаления обновления. |
| [**ResultCode**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_resultcode)         | Возвращает значение [**оператионресулткоде**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) , указывающее результат операции над обновлением.               |



 

 

 



