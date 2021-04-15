---
description: Если приложение запрашивает уступающую блокировку, все файлы, для которых он запрашивает блокировки, должны быть открыты для перекрывающихся (асинхронных) входных и выходных данных с помощью функции CreateFile с \_ \_ флагом File Flag OVERLAPPED.
ms.assetid: 1595c03e-9f6d-456c-8164-fafba06bbd79
title: Операции оппортунистической блокировки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefd9b292747e89f5ebafd94cb8aa0e38833e8cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545543"
---
# <a name="opportunistic-lock-operations"></a>Операции оппортунистической блокировки

Если приложение запрашивает уступающую блокировку, все файлы, для которых он запрашивает блокировки, должны быть открыты для перекрывающихся (асинхронных) входных и выходных данных с помощью функции [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) с флагом **File \_ Flag \_ OVERLAPPED** . После открытия файлов для работы с перекрытием можно использовать функцию [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) с одним из следующих управляющих кодов для работы с этими файлами уступающей блокировкой:

<dl>

[**\_ \_ \_ Ожидание закрытия фсктл опбатч ACK \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending)  
[**ФСКТЛ \_ OPLOCK \_ break \_ ACK \_ No \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2)  
[**ФСКТЛ \_ OPLOCK \_ break, \_ подтверждение**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_acknowledge)  
[**\_ \_ уведомление о разрыве фсктл OPLOCK \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_notify)  
[**\_ \_ Пакетная блокировка запроса фсктл \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_batch_oplock)  
[**ФСКТЛ \_ запрос \_ фильтрации \_ оппортунистической блокировки**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)  
[**\_ \_ нежесткая блокировка запроса фсктл**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock)  
[**\_Запрос фсктл \_ уровень жесткой блокировки \_ \_ 1**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1)  
[**\_Запрос фсктл \_ уровень жесткой блокировки \_ \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2)  
</dl>

 

 
