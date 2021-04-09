---
title: Функции восстановления и перезапуска приложений
description: Восстановление и перезапуск приложений определяет следующие функции.
ms.assetid: 17de24d1-32fe-4b2d-a224-3730af73c892
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f9f5fb41f2ef694b4d99044a8756ff0bb66c3f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134270"
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



 

 

 