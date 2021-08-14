---
description: Завершение работы подключения SChannel
ms.assetid: 7081ba1f-df3c-41b4-96da-24d44e74d714
title: Завершение работы подключения SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb700c8ac896d0e64b82b25371ea67cc343d8297c95445ca4126c5718d8024a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918063"
---
# <a name="shutting-down-an-schannel-connection"></a>Завершение работы подключения SChannel

Если клиент или сервер завершил работу с подключением, он должен завершить работу. Другая сторона, в свою очередь, должна распознать завершение работы и удалить подключение.

**Завершение работы подключения SChannel**

1.  Вызовите функцию [**аппликонтролтокен**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken) , указав \_ токен управления для завершения работы SChannel.
2.  После получения значения, \_ возвращаемого в секунду E \_ ОК из [**аппликонтролтокен**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken), вызовите функцию [**InitializeSecurityContext (Schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) (клиенты) или [**AcceptSecurityContext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) (Servers), передав пустые буферы.
3.  Продолжайте, как если бы приложение создавало новое подключение до тех пор, пока функция не вернет значение в секундах с \_ \_ \_ истечением времени или в секунду \_ \_ , чтобы указать, что подключение завершено.
4.  Отправка конечных данных удаленной стороне (если таковые имеются).
5.  Вызовите [**делетесекуритиконтекст**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) , чтобы освободить ресурсы, удерживаемые соединением.

## <a name="recognizing-a-shutdown"></a>Распознавание завершения работы

Функция [**декриптмессаже (Schannel)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) возвращает значение секунд \_ с \_ \_ истекшим сроком действия в контексте, когда отправитель сообщения отключил соединение. После получения этого возвращаемого значения выполните процедуру завершения подключения SChannel ранее в этом разделе.

 

 
