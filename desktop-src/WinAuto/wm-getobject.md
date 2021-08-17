---
title: Сообщение WM_GETOBJECT (Winuser. h)
description: Посылается как Microsoft Active Accessibility, так и Microsoft UI Automation для получения сведений о доступном объекте, который содержится в серверном приложении.
ms.assetid: 59350aa1-1697-4110-b9a6-f30ee56c4cff
keywords:
- WM_GETOBJECT сообщения Windows специальные возможности
topic_type:
- apiref
api_name:
- WM_GETOBJECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2767a689b87c2e293cb481647c61a29ad40167992e637802d1c0be63d18fc74e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744740"
---
# <a name="wm_getobject-message"></a>\_Сообщение WM GetObject

Посылается как Microsoft Active Accessibility, так и Microsoft UI Automation для получения сведений о доступном объекте, который содержится в серверном приложении.

Приложения никогда не отправляют это сообщение напрямую. Microsoft Active Accessibility отправляет это сообщение в ответ на вызовы [**акцессиблеобжектфромпоинт**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), [**акцессиблеобжектфромевент**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)или [**акцессиблеобжектфромвиндов**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow). Однако серверные приложения обработают это сообщение. Модель автоматизации пользовательского интерфейса отправляет это сообщение в ответ на вызовы [**иуиаутоматион:: елементфромхандле**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**елементфромпоинт**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)и [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), а при обработке событий, для которых зарегистрирован клиент.


```C++
dwFlags = (WPARAM)(DWORD) wParam;
dwObjId = (LPARAM)(DWORD) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*dwFlags* 
</dt> <dd>

Предоставляет дополнительные сведения о сообщении и используется только системой. Серверы передают *dwFlags* в качестве параметра *wParam* в вызове [**функции lresultfromobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) при обработке сообщения.

</dd> <dt>

*двобжид* 
</dt> <dd>

Идентификатор объекта. Это значение является одной из констант [идентификатора объекта](object-identifiers.md) или идентификатором пользовательского объекта. Серверное приложение должно проверить это значение, чтобы определить тип запрашиваемой информации. перед сравнением этого значения со \_ значениями OBJID сервер должен привести его к типу **DWORD**. в противном случае в 64-разрядном Windows расширение имени объекта *lParam* может помешать сравнению.

-   Если *двобжид* является одним из значений OBJID \_ , таких как [**OBJID \_ Client**](object-identifiers.md), то запрос предназначен для объекта Microsoft Active Accessibility, который реализует [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).
-   Если *двобжид* равен **уиарутобжектид**, то запрос предназначен для поставщика автоматизации пользовательского интерфейса. Если сервер реализует автоматизацию пользовательского интерфейса, он должен возвращать поставщик с помощью функции [**уиаретурнравелементпровидер**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .
-   Если *двобжид* — [**OBJID \_ нативеом**](object-identifiers.md), то запрос предназначен для базовой объектной модели элемента управления. Если элемент управления поддерживает этот запрос, он должен вернуть соответствующий COM-интерфейс, вызвав функцию [**функции lresultfromobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .
-   если *двобжид* — [**OBJID \_ куерикласснамеидкс**](object-identifiers.md), то запрос предназначен для того, чтобы элемент управления определял себя как стандартный Windows элемент управления или общий элемент управления, реализованный общей библиотекой элементов управления (ComCtrl.dll).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если окну или элементу управления не нужно отвечать на это сообщение, оно должно передать сообщение функции [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ; в противном случае окно или элемент управления должны возвращать значение, соответствующее запросу, заданному параметром *двобжид*:

-   Если окно или элемент управления реализует автоматизацию пользовательского интерфейса, окно или элемент управления должны возвращать значение, полученное при вызове функции [**уиаретурнравелементпровидер**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .
-   Если *двобжид* — [**OBJID \_ нативеом**](object-identifiers.md) , а окно предоставляет собственную объектную модель, то Windows должна вернуть значение, полученное при вызове функции [**функции lresultfromobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .
-   Если *двобжид* — [**OBJID \_ Client**](object-identifiers.md) , а окно реализует [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), окно должно вернуть значение, полученное при вызове функции [**функции lresultfromobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .

## <a name="remarks"></a>Remarks

Когда клиент вызывает [**акцессиблеобжектфромвиндов**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) или любую другую функцию **акцессиблеобжектфром**_X_ , которая получает интерфейс к объекту, Microsoft Active Accessibility отправляет сообщение **WM \_ GetObject** в соответствующую процедуру окна в соответствующем серверном приложении. При обработке **WM \_ GetObject** серверные приложения вызывают [**функции lresultfromobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) и используют возвращаемое значение этой функции в качестве возвращаемого значения для сообщения. Microsoft Active Accessibility, в сочетании с библиотекой COM, выполняет соответствующий маршалирование и передает указатель интерфейса с сервера обратно клиенту.

Серверы не отвечают на **WM \_ GetObject** перед полной инициализацией объекта или после его начала. Когда приложение создает новое окно, система отправляет [**\_ объект события \_ CREATE**](event-constants.md) для уведомления клиентов перед отправкой сообщения о [ \_ создании WM](../winmsg/wm-create.md) в процедуру окна приложения. Так как многие приложения используют приложение WM \_ Create для запуска процесса инициализации, серверы не реагируют на сообщение **WM \_ GetObject** до тех пор, пока не завершится обработка сообщения **WM \_ CREATE** .

Сервер использует **WM \_ GetObject** для выполнения следующих задач:

-   [Создание новых объектов со специальными возможностями](create-new-accessible-objects.md)
-   [Повторное использование существующих указателей на объекты](reuse-existing-pointers-to-objects.md)
-   [Создание новых интерфейсов для одного и того же объекта](create-new-interfaces-to-the-same-object.md)

Для клиентов это означает, что они могут получить разные указатели интерфейса для одного и того же элемента пользовательского интерфейса в зависимости от действия сервера. Чтобы определить, указывают ли два указателя интерфейса на один и тот же элемент пользовательского интерфейса, клиенты сравнивают свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) объекта. Сравнение указателей не работает.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Распространяемые компоненты<br/>          | Active Accessibility 1,3 Windows NT 4,0 с пакетом обновления SP6 и более поздней версии и Windows 95<br/>              |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Как работать с WM \_ GetObject](how-to-handle-wm-getobject.md)
</dt> <dt>

[Как \_ работает WM GetObject](how-wm-getobject-works.md)
</dt> <dt>

[**Функции lresultfromobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)
</dt> </dl>

 

