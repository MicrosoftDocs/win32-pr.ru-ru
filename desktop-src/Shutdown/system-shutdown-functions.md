---
description: При завершении работы системы используются следующие функции.
ms.assetid: 6a08a769-1acf-49eb-ba95-beaf56a374bf
title: Функции завершения работы системы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b1304a2333d817be7cbb51ee599f37cda8b3e185f56cfc5959f1646e9ab639
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664344"
---
# <a name="system-shutdown-functions"></a>Функции завершения работы системы

При завершении работы системы используются следующие функции.



| Функция                                                         | Описание                                                                                                                         |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**абортсистемшутдовн**](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna)               | Останавливает запущенное завершение работы системы.                                                                                    |
| [**екситвиндовс**](/windows/desktop/api/Winuser/nf-winuser-exitwindows)                               | Выполнит выход интерактивного пользователя.                                                                                                      |
| [**Функцию**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)                           | Выполнит выход интерактивного пользователя, завершит работу системы или завершит работу и перезапустит систему.                                        |
| [**инитиатешутдовн**](/windows/desktop/api/Winreg/nf-winreg-initiateshutdowna)                     | Инициирует завершение работы и перезагрузку указанного компьютера и перезапускает все приложения, зарегистрированные для перезапуска.    |
| [**инитиатесистемшутдовн**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna)         | Инициирует завершение работы и необязательное перезагрузку указанного компьютера.                                                                |
| [**инитиатесистемшутдовнекс**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa)     | Инициирует завершение работы и необязательное перезагрузку указанного компьютера и при необходимости записывает причину завершения работы.            |
| [**локкворкстатион**](/windows/desktop/api/Winuser/nf-winuser-lockworkstation)                       | Блокирует отображение рабочей станции.                                                                                                    |
| [**шутдовнблоккреасонкреате**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate)   | Указывает, что система не может быть выключена, и задает строку причины, которая будет отображаться пользователю при инициировании выключения системы. |
| [**шутдовнблоккреасондестрой**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasondestroy) | Указывает, что система может завершить работу и освободить строку причины.                                                             |
| [**шутдовнблоккреасонкуери**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasonquery)     | Извлекает строку причины, заданную функцией [**шутдовнблоккреасонкреате**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) .                     |



 

 

 



