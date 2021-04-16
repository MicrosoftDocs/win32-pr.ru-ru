---
description: Сведения о пользователе — это буфер, который может быть передан из одного конца соединения в другое. Эти сведения относятся к стандарту ISDN Q. 931. Ознакомьтесь с документацией поставщиков услуг по значению и использованию этих данных.
ms.assetid: 7040ab51-184e-4ffc-9333-b82ae5a5a7f3
title: Сведения о пользователе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d4539db192b9c24b5d71dfb60a2129e66b6658b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546298"
---
# <a name="user-user-information"></a>Сведения о пользователе

Сведения о пользователе — это буфер, который может быть передан из одного конца соединения в другое. Эти сведения относятся к стандарту ISDN Q. 931. Ознакомьтесь с документацией поставщика услуг по значению и использованию этих данных.

Не все поставщики служб поддерживают использование этих сведений.

* * TAPI 2. x: * *[**линежеткаллинфо**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **двкаллдатасизе** и **двкаллдатаоффсет** члены [**линекаллинфо**](/windows/win32/api/tapi/ns-tapi-linecallinfo), [**линесендусерусеринфо**](/windows/win32/api/tapi/nf-tapi-linesenduseruserinfo)

* * TAPI 3. x: * *[**иткаллинфо:: жеткаллинфобуффер**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer), вызванный с элементом **ЦИБ \_ усерусеринфо** в [**Каллинфо \_ buffer**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer), [**иткаллинфо:: релеасеусерусеринфо**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-releaseuseruserinfo)

 

 
