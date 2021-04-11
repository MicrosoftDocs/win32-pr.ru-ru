---
title: Синхронизация вызовов
description: Синхронизация вызовов
ms.assetid: e74407ef-f500-4d13-aef4-ca6bb37d5858
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec9254aceaaa8a6fa26d56d4a86987cc955b90dc
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070687"
---
# <a name="call-synchronization"></a>Синхронизация вызовов

Приложения COM должны уметь правильно работать с вводом данных при обработке одного или нескольких вызовов из COM или операционной системы. COM обеспечивает синхронизацию вызовов только для однопотоковых апартаментов. Многопоточные подразделения (содержащие свободные потоки) не получают вызовы при выполнении вызовов (в одном потоке). Многопоточные подразделения не могут выполнять входные синхронизированные вызовы. Асинхронные вызовы преобразуются в синхронные вызовы в многопоточных апартаментах. Фильтр сообщений не вызывается ни для одного потока в многопоточном апартаменте. Дополнительные сведения о проблемах с потоками см. в разделе [процессы, потоки и подразделения](processes--threads--and-apartments.md).

Вызовы COM между процессами делятся на три категории следующим образом:

<dl> <dt>

<span id="Synchronous_calls"></span><span id="synchronous_calls"></span><span id="SYNCHRONOUS_CALLS"></span>*Синхронные вызовы*
</dt> <dd>

Большая часть взаимодействия, выполняемого в модели COM, является синхронной. При выполнении синхронных вызовов вызывающий объект ждет ответа перед продолжением и сможет принимать входящие сообщения в ожидании. COM входит в модальный цикл для ожидания ответа, получения и отправки других сообщений управляемым способом.

</dd> <dt>

<span id="Asynchronous_notifications"></span><span id="asynchronous_notifications"></span><span id="ASYNCHRONOUS_NOTIFICATIONS"></span>*Асинхронные уведомления*
</dt> <dd>

При отправке асинхронных уведомлений вызывающий объект не ждет ответа. COM использует события на основе [**сообщений**](/windows/win32/api/winuser/nf-winuser-postmessagea) или высокого уровня для отправки асинхронных уведомлений в зависимости от платформы. COM определяет пять асинхронных методов [**иадвисесинк**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink):

-   [**ондатачанже**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange)
-   [**онвиевчанже**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onviewchange)
-   [**Onrename**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onrename)
-   [**OnSave**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onsave)
-   [**OnClose**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onclose)

> [!Note]  
> Хотя COM обрабатывает асинхронный вызов, синхронные вызовы не могут быть выполнены. Например, реализация [**ондатачанже**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange) приложения-контейнера не может содержать вызов [**Иперсистстораже:: Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststorage-save). Эти вызовы являются единственными асинхронными вызовами, поддерживаемыми COM. В настоящее время невозможно создать настраиваемый интерфейс, который является асинхронным.

 

</dd> <dt>

<span id="Input-synchronized_calls"></span><span id="input-synchronized_calls"></span><span id="INPUT-SYNCHRONIZED_CALLS"></span>*Синхронные вызовы входных данных*
</dt> <dd>

При выполнении вызовов, синхронизированных с входом, объект, вызываемый, должен завершить вызов до получения элемента управления. Это гарантирует, что управление фокусом работает правильно и данные, введенные пользователем, обрабатываются соответствующим образом. Эти вызовы делаются COM через функцию [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) без входа в модальный цикл. При обработке синхронизированного вызова объект не должен вызывать ни одну функцию или метод (включая синхронные методы), которые могут привести к управлению. Следующие методы являются синхронизированными входными данными

-   [**Иолевиндов::/Window**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-getwindow)
-   [**Метода IOleInPlaceActiveObject:: OnFrameWindowActivate**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-onframewindowactivate)
-   [**Метода IOleInPlaceActiveObject:: OnDocWindowActivate**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-ondocwindowactivate)
-   [**Метода IOleInPlaceActiveObject:: ResizeBorder**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-resizeborder)
-   [**Иолеинплацеуивиндов:: награница**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-getborder)
-   [**Иолеинплацеуивиндов:: Рекуестбордерспаце**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-requestborderspace)
-   [**Иолеинплацеуивиндов:: Сетбордерспаце**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-setborderspace)
-   [**Иолеинплацефраме:: Сетмену**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setmenu)
-   [**Иолеинплацефраме:: Сетстатустекст**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setstatustext)
-   [**Иолеинплацеобжект:: Сетобжектректс**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceobject-setobjectrects)

</dd> </dl>

Чтобы избежать проблем, которые могут возникнуть при асинхронной обработке сообщений, большинство вызовов COM-методов являются синхронными. При синхронном обмене не требуется специальный код для отправки и обработки входящих сообщений. Когда приложение выполняет синхронный вызов метода, COM входит в модальный цикл ожидания, который обрабатывает необходимые ответы и отправляет входящие сообщения приложениям, которые способны их обрабатывать.

COM управляет вызовами методов путем присвоения идентификатора, называемого *идентификатором логического потока*. Новый назначается, когда пользователь выбирает команду меню или когда приложение инициирует новую операцию COM. Последующие вызовы, связанные с первоначальным вызовом COM, присваиваются тому же ИДЕНТИФИКАТОРу логического потока, что и начальный вызов.

 

 