---
title: SendMessage, сообщение и связанные функции
description: В этом разделе приводятся рекомендации по пересылке сообщений с помощью SendMessage, сообщений и связанных функций с сенсорными сообщениями.
ms.assetid: 9fba2013-17a3-499c-80dc-627e89c0edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1274327b53630058779bc3913ce4466394c4c4fa37ba78528d122b8d68e376e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118435302"
---
# <a name="sendmessage-postmessage-and-related-functions"></a>SendMessage, сообщение и связанные функции

В этом разделе приводятся рекомендации по пересылке сообщений с помощью [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [сообщений](/windows/win32/api/winuser/nf-winuser-postmessagea)и связанных функций с сенсорными сообщениями.

Если сенсорное сообщение пересылается с помощью [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [сообщения](/windows/win32/api/winuser/nf-winuser-postmessagea)или другой связанной функции, то маркер сенсорного ввода закрывается. Если вы получили сведения, содержащиеся на ссылке сенсорного ввода с помощью вызова [**жеттаучинпутинфо**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo), эти данные останутся действительными до тех пор, пока не освободится память.

Приложение, получающее сенсорные сообщения, пересылаемые через один из этих механизмов, владеет сенсорным приемом ввода, который он получает в сообщении *lParam* и отвечает за его закрытие. Если вы не закроете дескриптор с вызовом [**клосетаучинпусандле**](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle), передайте сообщение в [дефвиндовпрок](/windows/win32/api/winuser/nf-winuser-defwindowproca)или перешлите сообщение с помощью [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [сообщения](/windows/win32/api/winuser/nf-winuser-postmessagea)или связанной функции, произойдет утечка памяти.

> [!Note]  
> При переадресации сообщений сенсорного ввода действуют обычные правила изоляции прав пользовательского интерфейса (UIPI).

 

## <a name="functions-related-to-sendmessage-and-postmessage"></a>Функции, относящиеся к SendMessage и почте

Следующие функции, которые могут повлиять на состояние сенсорного ввода.

-   [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage)
-   [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)
-   сенднотифимессаже
-   сендмессажекаллбакк
-   Функции sendmessagetimeout
-   постсреадмессаже

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Функции](mtfunctions.md)
</dt> <dt>

[дефвиндовпрок](/windows/win32/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

 