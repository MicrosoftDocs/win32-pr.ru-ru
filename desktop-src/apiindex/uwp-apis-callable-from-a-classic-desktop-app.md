---
description: общее правило заключается в том, что классическое приложение может вызывать API среда выполнения Windows (WinRT). Однако некоторые API, включая API пользовательского интерфейса XAML, занимают у вызывающего приложения удостоверение пакета.
ms.assetid: F3808C28-72DE-49B5-A389-EB085EFC02CC
title: API-интерфейсы WinRT, вызываемые из классического приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3bbfb2316a6fd4dd8d35d0744acc4ad301dba7f42aee36ee865d67bb2fff805
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130306"
---
# <a name="winrt-apis-callable-from-a-desktop-app"></a>API-интерфейсы WinRT, вызываемые из классического приложения

большинство [api среда выполнения Windows (WinRT)](/uwp/api/) могут использоваться приложениями для настольных систем (.net и native C++). Однако некоторые классы WinRT предназначены для и поддерживаются только в приложениях UWP. Сюда входят [CoreDispatcher](/uwp/api/Windows.UI.Core.CoreDispatcher), [CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow), [аппликатионвиев](/uwp/api/windows.ui.viewmanagement.applicationview)и некоторые связанные классы. Другие классы WinRT работают в классических приложениях, за исключением определенных элементов.

Дополнительные сведения см. в статье [API среды выполнения Windows не поддерживаются в классических приложениях](/windows/apps/desktop/modernize/desktop-to-uwp-supported-api). Когда это возможно, в этой статье предлагаются альтернативные API для обеспечения функциональности, которую предоставляют неподдерживаемые API.
