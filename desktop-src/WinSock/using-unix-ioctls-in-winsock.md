---
description: команда сиокгифконф, предоставляемая большинством реализаций UNIX, поддерживается в форме функций всаиоктл и вспиоктл с помощью команды SIO \_ GET \_ INTERFACE \_ LIST. Эта команда возвращает список настроенных интерфейсов и их параметров.
ms.assetid: c5028dae-052a-444c-837c-cd8d6d901b6c
title: использование UNIX ioctl в Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da517adb6480a1bd20100a3d9a6d0896f544c1b541ce547a0f76e5c88aa24210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118558866"
---
# <a name="using-unix-ioctls-in-winsock"></a>использование UNIX ioctl в Winsock

команда **сиокгифконф** , предоставляемая большинством реализаций UNIX, поддерживается в форме функций [**всаиоктл**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) и [**вспиоктл**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) с помощью команды **SIO \_ GET \_ INTERFACE \_ LIST**. Эта команда возвращает список настроенных интерфейсов и их параметров.

> [!Note]  
> поддержка этой команды обязательна для поставщиков служб TCP/IP, соответствующих сокетам Windows 2.

 

Параметр *лпваутбуффер* указывает на буфер, в котором [**всаиоктл**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) и [**вспиоктл**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) хранят сведения об интерфейсах. Количество интерфейсов (число структур, возвращаемых в *лпваутбуффер*) можно определить на основе фактической длины выходного буфера, возвращаемого в *лпкббитесретурнед*.

 

 
