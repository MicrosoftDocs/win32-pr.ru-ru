---
description: Начало работы с графикой DirectX
ms.assetid: 49E0D0C2-E6EC-4849-A44F-36FDEFBB9838
title: Начало работы с графикой DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32e0bc8a3485091ec8b8fa53c8245a3a4916e11af96493d4895585061f2b080f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830574"
---
# <a name="getting-started-with-directx-graphics"></a>Начало работы с графикой DirectX

Microsoft DirectX Graphics предоставляет набор интерфейсов API, которые можно использовать для создания игр и других высокопроизводительных мультимедийных приложений. DirectX Graphics поддерживает высокопроизводительные высокопроизводительные и трехмерные графики.

Для трехмерной графики используйте API Microsoft Direct3D 11. Даже при наличии аппаратного обеспечения Microsoft Direct3D 9-Level или Microsoft Direct3D 10, вы можете использовать API Direct3D 11 и ориентироваться на устройство [уровня "](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x" или "Feature" 10 \_ x. Сведения о разработке трехмерной графики с помощью DirectX см. в статье [Создание трехмерной графики с помощью DirectX](/previous-versions/windows/apps/hh465137(v=win.10)
).

для двухмерной графики и текста используйте Direct2D и [DirectWrite](./directwrite/direct-write-portal.md) , а не Windows интерфейс графических устройств (GDI).

Чтобы создать точечные рисунки, заполненные Direct3D 11 или Direct2D, используйте [DirectComposition](./directcomp/directcomposition-portal.md).

дополнительные сведения о создании приложения для магазина Windows, использующего directx, см. в статье [создание первого приложения для магазина Windows с помощью directx](/previous-versions/windows/apps/br229580(v=win.10)
). Можно использовать [**Windows. Класс UI:: XAML:: Controls:: SwapChainPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainPanel?view=winrt-19041) для создания высокопроизводительных приложений DirectX с наложением пользовательского интерфейса XAML. дополнительные сведения о сочетании XAML и DirectX в Windows приложении см. в разделе [взаимодействие DirectX и xaml](/previous-versions/windows/apps/hh825871(v=win.10)).

сведения о том, как создать видеодрайвер для Windows 8, см. в разделе [путеводитель по модели Windowsного драйвера (WDDM)](/windows-hardware/drivers/display/roadmap-for-developing-drivers-for-the-windows-vista-display-driver-mo).

Если вам нужна документация по предыдущим версиям DirectX, см. раздел [Классическая графика DirectX](/windows/desktop/classic-directx-graphics).


 

 
