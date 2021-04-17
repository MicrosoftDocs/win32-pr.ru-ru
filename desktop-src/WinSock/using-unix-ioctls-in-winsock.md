---
description: Команда СИОКГИФКОНФ, предоставляемая большинством реализаций UNIX, поддерживается в виде функций Всаиоктл и Вспиоктл с помощью команды SIO \_ Get \_ Interface \_ List. Эта команда возвращает список настроенных интерфейсов и их параметров.
ms.assetid: c5028dae-052a-444c-837c-cd8d6d901b6c
title: Использование ioctl через UNIX в Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0b52c311ea8c5f67dc374503f00c3ca16c5d053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693162"
---
# <a name="using-unix-ioctls-in-winsock"></a>Использование ioctl через UNIX в Winsock

Команда **сиокгифконф** , предоставляемая большинством реализаций UNIX, поддерживается в виде функций [**всаиоктл**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) и [**вспиоктл**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) с помощью команды **SIO \_ Get \_ Interface \_ List**. Эта команда возвращает список настроенных интерфейсов и их параметров.

> [!Note]  
> Эта команда является обязательной для поставщиков служб TCP/IP, совместимых с Windows Sockets 2.

 

Параметр *лпваутбуффер* указывает на буфер, в котором [**всаиоктл**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) и [**вспиоктл**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) хранят сведения об интерфейсах. Количество интерфейсов (число структур, возвращаемых в *лпваутбуффер*) можно определить на основе фактической длины выходного буфера, возвращаемого в *лпкббитесретурнед*.

 

 
