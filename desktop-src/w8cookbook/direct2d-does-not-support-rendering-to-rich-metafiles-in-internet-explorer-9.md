---
title: Direct2D не поддерживает отрисовку в насыщенных метафайлах в Internet Explorer 9
description: Direct2D не поддерживает отрисовку в насыщенных метафайлах в Internet Explorer 9
ms.assetid: D106FBD6-F05E-41A6-B8F8-569EB9810E2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28f51ae6d098c08c0a18656aae2adf3d79d68652
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314827"
---
# <a name="direct2d-does-not-support-rendering-to-rich-metafiles-in-internet-explorer-9"></a>Direct2D не поддерживает отрисовку в насыщенных метафайлах в Internet Explorer 9

## <a name="platforms"></a>Платформы

**Клиенты** — Windows Vista, Windows 7, Windows 8  
**Серверы** — windows Server 2008, windows Server 2008 R2, windows Server 2012  




## <a name="description"></a>Описание

Благодаря внутренним изменениям отрисовки в Internet Explorer 9 интерфейсы API [ихтмлелементрендер::D равтодк](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85)) и [ивиевобжект::D RAW](/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw) теперь создают метафайл, содержащий один точечный рисунок, представляющий веб-содержимое, а не расширенный метафайл, содержащий сведения о тексте и векторе. Это изменение было вызвано переходом с рендеринга GDI на аппаратное ускорение Direct2D (D2D).

Это изменение влияет на приложения, использующие эти API, и использует текстовые или векторные сведения в метафайле.

## <a name="manifestation"></a>Проявление

В зависимости от приложения, на которое влияет это изменение, пользователи могут столкнуться с поврежденным или неправильным поведением в своих приложениях.

## <a name="mitigation"></a>Меры по снижению риска

Приложения, для которых требуется извлечь текстовые данные из веб-документа (без сведений о размещении), могут использовать свойство [InnerText](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85)) для извлечения текста.

Приложения, использующие Ивиевобжект::D RAW, могут использовать [функцию \_ ивиевобжектдрав \_ DMLT9 \_ с \_ ](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85)) ключом управления функциями GDI для возврата к отрисовке GDI, если режим документа:

-   Меньше или равно 8
-   ФКК разрешает этому узлу использовать GDI
-   И в API передается метафайл DC

## <a name="resources"></a>Ресурсы

-   [Ихтмлелементрендер::D Равтодк](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85))
-   [Ивиевобжект::D RAW](/windows/win32/api/oleidl/nf-oleidl-iviewobject-draw)
-   [Свойство Ихтмлелемент:: innerText](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85))
-   [Элементы управления функциями Интернета (I. Н](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85))

 

 