---
description: Общее правило заключается в том, что классическое приложение может вызывать API среда выполнения Windows (WinRT). Однако некоторые API, включая API пользовательского интерфейса XAML, занимают у вызывающего приложения удостоверение пакета.
ms.assetid: F3808C28-72DE-49B5-A389-EB085EFC02CC
title: Интерфейсы API WinRT, вызываемые из классического приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36f99cca14c066f372ad7fd417e04137a62ae628
ms.sourcegitcommit: 133954d5dbcd5b2b3b50c8efd16cd101278fc1db
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108172486"
---
# <a name="winrt-apis-callable-from-a-desktop-app"></a>Интерфейсы API WinRT, вызываемые из классического приложения

Большинство [api среда выполнения Windows (WinRT)](/uwp/api/) могут использоваться приложениями для настольных систем (.NET и Native C++). Однако некоторые классы WinRT предназначены для и поддерживаются только в приложениях UWP. Сюда входят [CoreDispatcher](/uwp/api/Windows.UI.Core.CoreDispatcher), [CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow), [аппликатионвиев](/uwp/api/windows.ui.viewmanagement.applicationview)и некоторые связанные классы. Другие классы WinRT работают в настольных приложениях, за исключением конкретных членов.

Дополнительные сведения см. [в статье среда выполнения Windows интерфейсы API, не поддерживаемые в классических приложениях](/windows/apps/desktop/modernize/desktop-to-uwp-supported-api). Когда это возможно, в этой статье предлагаются альтернативные API-интерфейсы для достижения тех же функций, что и неподдерживаемые API.
