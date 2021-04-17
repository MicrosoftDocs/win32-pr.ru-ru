---
description: 'При работе с енклавес, которые используются для создания доверенных сред выполнения, используются следующие функции:'
ms.assetid: DF6CDEE1-CAAA-429C-9939-DDC844302027
title: Доверенные функции выполнения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4b1bd2411d0448346f0a8afcca870c26b4a61ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673341"
---
# <a name="trusted-execution-functions"></a>Доверенные функции выполнения

При работе с енклавес, которые используются для создания доверенных сред выполнения, используются следующие функции:

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                               | Описание                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**калленклаве**](/windows/desktop/api/Enclaveapi/nf-enclaveapi-callenclave)<br/>                                       | Вызывает функцию в анклава. <br/>                                                                                                                                                                                |
| [**креатинклаве**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave)<br/>                                   | Создает новый неинициализированный анклава. Анклава — это изолированная область кода и данных в адресном пространстве для приложения. Только код, который выполняется в анклава, может обращаться к данным в одном анклава.<br/> |
| [**делетинклаве**](/windows/desktop/api/Enclaveapi/nf-enclaveapi-deleteenclave)<br/>                                   | Удаляет указанный анклава.<br/>                                                                                                                                                                                      |
| [**енклавежетаттестатионрепорт**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport)<br/>       | Возвращает отчет аттестации анклава, который описывает текущий анклава и подписывается центром, отвечающим за тип анклава. <br/>                                                              |
| [**енклавежетенклавеинформатион**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetenclaveinformation)<br/>     | Возвращает сведения о текущем выполняемом анклава.<br/>                                                                                                                                                             |
| [**енклавесеалдата**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavesealdata)<br/>                               | Создает зашифрованный большой двоичный объект (BLOB) из данных уненциптед.<br/>                                                                                                                                             |
| [**енклавеунсеалдата**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclaveunsealdata)<br/>                           | Расшифровывает зашифрованный большой двоичный объект (BLOB).<br/>                                                                                                                                                                   |
| [**енклавеверифяттестатионрепорт**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclaveverifyattestationreport)<br/> | Проверяет отчет аттестации, созданный в текущей системе. <br/>                                                                                                                                           |
| [**инитиализинклаве**](/windows/desktop/api/enclaveapi/nf-enclaveapi-initializeenclave)<br/>                           | Инициализирует анклава, созданный и загруженный с данными.<br/>                                                                                                                                                       |
| [**исенклаветипесуппортед**](/windows/desktop/api/enclaveapi/nf-enclaveapi-isenclavetypesupported)<br/>                 | Возвращает значение, определяющее, поддерживается ли указанный тип анклава.<br/>                                                                                                                                                       |
| [**лоаденклаведата**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata)<br/>                               | Загружает данные в неинициализированную анклава, созданную путем вызова [**креатинклаве**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave).<br/>                                                                                                        |
| [**лоаденклавеимаже**](/windows/desktop/api/Enclaveapi/nf-enclaveapi-loadenclaveimagew)<br/>                             | Загружает изображение и все его импорты в анклава.<br/>                                                                                                                                                              |
| [**терминатинклаве**](/windows/desktop/api/Enclaveapi/nf-enclaveapi-terminateenclave)<br/>                             | Завершает выполнение потоков, выполняющихся в анклава.<br/>                                                                                                                                               |



 

 

 




