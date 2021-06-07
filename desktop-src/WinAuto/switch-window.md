---
title: Переключить окно (Справочник по элементу пользовательского интерфейса MSAA)
description: Окно переключения отображается каждый раз, когда пользователь нажимает клавиши ALT + TAB для переключения на другое приложение. Окно переключения содержит значок для каждого выполняемого в данный момент приложения.
ms.assetid: 77b32eb1-7722-410b-b141-ac09fc7fdffb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa12b5fa3bfb9e6207ddaff4133b030e6c233c3
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443985"
---
# <a name="switch-window-msaa-ui-element-reference"></a>Переключить окно (Справочник по элементу пользовательского интерфейса MSAA)

Окно переключения отображается каждый раз, когда пользователь нажимает клавиши ALT + TAB для переключения на другое приложение. Окно переключения содержит значок для каждого выполняемого в данный момент приложения.

Имя класса Window для окна переключения — " \# 32771".

## <a name="iaccessible-methods"></a>Методы IAccessible

Окно Switch поддерживает следующие методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Метод                                                                    | Комментарии                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**аккдодефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Сам объект окна Switch не имеет свойства **DefaultAction** . Метод [**аккдодефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) для каждого элемента в окне Switch активирует указанный элемент. |
| [**акчиттест**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                   |
| [**акклокатион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                   |
| [**аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                   |
| [**аккселект**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                   |



 

## <a name="iaccessible-properties"></a>Свойства IAccessible

Окно Switch поддерживает следующие свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



|      Свойство                                                                          |      Описание                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**получить \_ аккчилдкаунт**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | Свойство **ChildCount** равно нулю.                                                                                                                                                                                           |
| [**получить \_ аккдефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | Сам объект окна Switch не имеет свойства **DefaultAction** . Свойство **DefaultAction** для каждого элемента в окне Switch имеет значение Switch.                                                                     |
| [**получить \_ аккфокус**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 | Родительский объект окна переключения не может получать фокус; фокус может получать только отдельные дочерние элементы.                                                                                                                          |
| [**получить \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | Сам объект окна Switch не имеет свойства **Name** . Свойство **Name** для каждого значка приложения в окне коммутатора совпадает с отображаемым именем приложения.                                         |
| [**получить \_ аккроле**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | Сам объект окна Switch имеет свойство **Role** "Window \[ 32771 \] ". Кроме того, каждый значок приложения в окне Switch имеет роль  свойства роли [**\_ System \_ ListItem**](object-roles.md). |
| [**получить \_ аккстате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | Сам объект окна Switch не поддерживает свойство **State** . Значение **состояния** элементов представления списка — это [**\_ \_ фокус системы состояния**](object-state-constants.md).                     |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Интерфейс IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




