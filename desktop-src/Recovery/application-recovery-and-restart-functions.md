---
title: Функции восстановления и перезапуска приложений
description: Восстановление и перезапуск приложений определяет следующие функции.
ms.assetid: 17de24d1-32fe-4b2d-a224-3730af73c892
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df0a2139a24c3e69ae328533d6bf8b1baeee2043bc82b9f8d50f4272a16e2f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024624"
---
# <a name="application-recovery-and-restart-functions"></a>Функции восстановления и перезапуска приложений

Восстановление и перезапуск приложений определяет следующие функции:



| Функция                                                                               | Описание                                                                                |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**аппликатионрековерифинишед**](/windows/win32/api/winbase/nf-winbase-applicationrecoveryfinished)                     | Указывает, что вызывающее приложение завершило восстановление данных.                    |
| [**аппликатионрековеринпрогресс**](/windows/win32/api/winbase/nf-winbase-applicationrecoveryinprogress)                 | Указывает, что вызывающее приложение продолжает восстанавливать данные.                      |
| [**жетаппликатионрековерикаллбакк**](/windows/win32/api/winbase/nf-winbase-getapplicationrecoverycallback)               | Возвращает указатель на подпрограммы обратного вызова восстановления, зарегистрированную для указанного процесса. |
| [**жетаппликатионрестартсеттингс**](/windows/win32/api/winbase/nf-winbase-getapplicationrestartsettings)                 | Извлекает сведения о перезапуске, зарегистрированные для указанного процесса.                    |
| [**регистераппликатионрековерикаллбакк**](/windows/win32/api/winbase/nf-winbase-registerapplicationrecoverycallback)     | Регистрирует активный экземпляр приложения для восстановления.                              |
| [**регистераппликатионрестарт**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart)                       | Регистрирует активный экземпляр приложения для перезапуска.                               |
| [**унрегистераппликатионрековерикаллбакк**](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrecoverycallback) | Удаляет активный экземпляр приложения из списка восстановления.                      |
| [**унрегистераппликатионрестарт**](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrestart)                   | Удаляет активный экземпляр приложения из списка перезапуска.                       |



 

 

 