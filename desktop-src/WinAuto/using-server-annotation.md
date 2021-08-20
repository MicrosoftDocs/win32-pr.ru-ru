---
title: Использование заметок сервера
description: В этом разделе содержатся сведения об использовании заметок сервера для указания объекта обратного вызова.
ms.assetid: eeeebddc-2752-4d8f-b4fa-38ce156acc08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65b2955d49431b502c8587484208321bc1ab1bc0c8201fabf466b60b68f548a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118823908"
---
# <a name="using-server-annotation"></a>Использование заметок сервера

В этом разделе содержатся сведения об использовании заметок сервера для указания объекта обратного вызова.

**Переопределение свойства, определяющего объект обратного вызова**

1.  Получите указатель на интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) для элемента, доступного для добавления в заметки.
2.  Вызовите метод [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для доступного элемента, чтобы получить указатель интерфейса [**иакЦидентити**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) .
3.  Вызовите метод [**иакЦидентити:: жетидентитистринг ()**](/windows/desktop/api/Oleacc/nf-oleacc-iaccidentity-getidentitystring) в указателе интерфейса [**иакЦидентити**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) , чтобы получить строку, которая однозначно определяет доступный элемент, для которого необходимо добавить заметки.
4.  Для создания объекта [**иаккпропсервицес**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) используйте [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) или [**кокреатеинстанцеекс**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) .
5.  Создайте объект модели COM, реализующий [**иаккпропсервер**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver).
6.  Вызовите [**иаккпропсервицес:: сетпропсервер**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver), передав строку идентификатора, GUID, указывающий переопределяемое свойство, и указатель на объект обратного вызова [**иаккпропсервер**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver) .
7.  Освободить указатели интерфейса и свободную память.

Когда клиент запрашивает свойство доступного элемента, объект обратного вызова будет вызван и вернет значение клиенту.

Как и при указании значения, разработчики сервера могут также использовать метод [**иаккпропсервицес:: компосехвндидентитистринг**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-composehwndidentitystring) для получения строки идентификатора. также можно использовать метод [**иаккпропсервицес:: сесвндпропсервер**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropserver) и указать параметры *HWND*, *идобжект* или *идчилд* вместо строки удостоверения.

При использовании [**сетпропсервер**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver) или [**сесвндпропсервер**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropserver) для объекта-контейнера разработчики сервера могут дополнительно указать, что переопределяемые сведения также должны применяться ко всем дочерним элементам этого контейнера.

Серверы могут явно очищать заметку в любое время с помощью [**иаккпропсервицес:: клеарпропс**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearprops). Обычно это не требуется, так как Служба заметок будет автоматически очищать и выпустить сведения о заметках, когда доступ к элементу с аннотацией исчезает.

Ниже приведен список свойств, которые можно закомментировать с помощью этой процедуры.

## <a name="properties-supported-when-specifying-a-callback"></a>Свойства, поддерживаемые при указании обратного вызова

При указании обратного вызова можно добавлять заметки к следующим свойствам. В настоящее время эти свойства нельзя напрямую закомментировать, указав значение.



| Свойство                      | Тип                                                             |
|-------------------------------|------------------------------------------------------------------|
| \_имя счетов \_ PropID             | VT \_ BSTR                                                         |
| \_Описание счетов \_ PropID      | VT \_ BSTR                                                         |
| \_роль PropID ACC \_             | VT \_ I4                                                           |
| \_состояние счетов \_ PropID            | VT \_ I4                                                           |
| \_ \_ Справка по PropID             | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ кэйбоардшорткут | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ DEFAULTACTION    | VT \_ BSTR                                                         |
| PROPID \_ ACC — \_ VALUEMAP         | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ ролемап          | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ статемап         | VT \_ BSTR                                                         |
| \_фокус на счет PropID \_            | \_Диспетчер VT<br/> VT \_ I4<br/>                        |
| \_Выбор счетов \_ PropID        | \_Диспетчер VT<br/> VT \_ I4<br/> VT \_ Unknown<br/> |
| \_ \_ родительский счет PropID           | \_Диспетчер VT                                                     |
| \_счет за \_ PropID \_          | \_Диспетчер VT<br/> VT \_ I4<br/>                        |
| \_счет по \_ PropID \_        | \_Диспетчер VT<br/> VT \_ I4<br/>                        |
| \_левый счет для \_ навигации \_ по PropID        | \_Диспетчер VT<br/> VT \_ I4<br/>                        |
| \_правый счет \_ навигации по PropID \_       | \_Диспетчер VT<br/> VT \_ I4<br/>                        |
| Переход по \_ сумме PropID \_ \_ назад        | \_Диспетчер VT<br/> VT \_ I4<br/>                        |
| \_ \_ Следующая навигационная панель \_        | \_Диспетчер VT<br/> VT \_ I4<br/>                        |
| \_FIRSTCHILD по сумме PropID \_ \_  | \_Диспетчер VT<br/> VT \_ I4<br/>                        |
| \_LASTCHILD по сумме PropID \_ \_   | \_Диспетчер VT<br/> VT \_ I4<br/>                        |



 

 

