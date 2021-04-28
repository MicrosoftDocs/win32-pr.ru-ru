---
description: Начало работы с графикой DirectX
ms.assetid: 49E0D0C2-E6EC-4849-A44F-36FDEFBB9838
title: Начало работы с графикой DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c5e8cca9f0cea4c1c5e484ba330c7c108cad40
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117592"
---
# <a name="getting-started-with-directx-graphics"></a>Начало работы с графикой DirectX

Microsoft DirectX Graphics предоставляет набор интерфейсов API, которые можно использовать для создания игр и других высокопроизводительных мультимедийных приложений. DirectX Graphics поддерживает высокопроизводительные высокопроизводительные и трехмерные графики.

Для трехмерной графики используйте API Microsoft Direct3D 11. Даже при наличии аппаратного обеспечения Microsoft Direct3D 9-Level или Microsoft Direct3D 10, вы можете использовать API Direct3D 11 и ориентироваться на устройство [уровня "](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x" или "Feature" 10 \_ x. Сведения о разработке трехмерной графики с помощью DirectX см. в статье [Создание трехмерной графики с помощью DirectX](/previous-versions/windows/apps/hh465137(v=win.10)
).

Для двухмерной графики и текста используйте Direct2D и [DirectWrite](./directwrite/direct-write-portal.md) , а не Windows интерфейс графических устройств (GDI).

Чтобы создать точечные рисунки, заполненные Direct3D 11 или Direct2D, используйте [DirectComposition](./directcomp/directcomposition-portal.md).

Дополнительные сведения о создании приложения для Магазина Windows, использующего DirectX, см. в статье [Создание первого приложения для Магазина Windows с помощью DirectX](/previous-versions/windows/apps/br229580(v=win.10)
). Вы можете использовать класс [**Windows. UI:: XAML:: Controls:: SwapChainPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainPanel?view=winrt-19041) для создания высокопроизводительных приложений DirectX с наложением ПОЛЬЗОВАТЕЛЬСКОГО интерфейса XAML. Дополнительные сведения о сочетании XAML и DirectX в приложении Windows см. в разделе [взаимодействие DirectX и XAML](/previous-versions/windows/apps/hh825871(v=win.10)).

Дополнительные сведения о создании видеодрайверов для Windows 8 см. в разделе [Путеводитель по модели видеодрайверов Windows (WDDM)](/windows-hardware/drivers/display/roadmap-for-developing-drivers-for-the-windows-vista-display-driver-mo).

Если вам нужна документация по предыдущим версиям DirectX, см. раздел [Классическая графика DirectX](/windows/desktop/classic-directx-graphics).


 

 
